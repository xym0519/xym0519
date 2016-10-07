---
layout: post
title: "RVM installation instruction"
categories: [tech]
tags: [ruby]
---

### Official site
<a href='http://www.rvm.io/' target='blank'>http://www.rvm.io/</a>

### What is RVM
RVM is a command-line tool which allows you to easily install, manage, and work with multiple ruby environments from interpreters to sets of gems.




### Installation
Install

    curl -sSL https://get.rvm.io | bash -s stable

Run command or add to zshrc file

    source /Users/broche/.rvm/scripts/rvm

Check

    rvm -v

Install Ruby

    rvm install 2.2

Change default

    rvm use 2.2 --default

### Others

    rvm list 查看已安装ruby
    rvm list known 列出ruby可安装版本信息
    rvm remove 2.2.2 卸载一个已安装的ruby版本

### References
<a href='http://blog.csdn.net/archer_sc/article/details/52043305' target='blank'>mac下升级ruby环境版本</a>
