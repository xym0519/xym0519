---
layout: post
title: "Bitnami Redmine 升级记录"
categories: tech
---

### Backup
<pre>
1. 停止服务
./ctlscript.sh stop

2. 压缩打包
tar zcvf bak.tgz redmine
</pre>

---

### Restore
<pre>
1. 解压
tar xvf bak.tgz

2. 运行服务
./ctlscript.sh start
</pre>

---

### Upgrade
<pre>
1. 备份数据库
mysqldump -ubitnami -P3307 -p bitnami_redmine > bak.sql

2. 停止服务
./ctlscript.sh stop

3. 安装新版本redmine
./***.run

4. 启动mysql
./ctlscript.sh start mysql

5. 登录mysql
mysql -uroot -p

6. 删除数据库
drop database bitnami_redmine;

7. 创建数据库
create database bitnami_redmine;

8. 赋权
grant all privileges on bitnami_redmine.* to 'bn_redmine'@'localhost' identified by 'DATABASE_PASSWORD';

9. 恢复数据库
mysql -uroot -p bitnami_redmine < bak.sql

10. 编辑数据库连接文件
vim ./apps/redmine/htdocs/config/database.yml
修改username和password为8中设定的用户名密码

11. 迁移数据库
cd ./apps/redmine/htdocs
ruby bin/rake db:migrate RAILS_ENV=production

12. 迁移文件
cp -r oldpath/apps/redmine/htdocs/files .

13. 权限修改
chown -R user:group files

14. 刷新缓存和会话
ruby bin/rake tmp:cache:clear
ruby bin/rake tmp:sessions:clear

15. 重启服务
./ctlscript.sh restart
</pre>

---

### Questions
1. 在其他机器上恢复后, 执行ctlscript.sh start无反应  
创建对应的目录, 放到同样的路径下后执行成功  

2. 执行成功后, 登录时提示redmine Invalid form authenticity token错误  
清理cookie后解决  

3. mysql数据库root用户密码是什么  
和安装时设定的管理员密码相同  

---

### References
<a href='https://wiki.bitnami.com/Applications/BitNami_Redmine' target='blank'>Bitnami Redmine 官方 wiki</a>  
<a href='https://wiki.bitnami.com/Components/MySQL' target='blank'>Bitnami MySql 官方 wiki</a>  
