---
layout: post
title: "Leanote部署记录"
categories: [tech]
tags: [mongodb, ubuntu, 树莓派, leanote]
---

倒腾了半天，终于把leanote又重新部署了一下。   
之前部署的leanote总是莫名其妙的问题，一会mongodb起不出来了，一会leanote访问不了了。这次痛下决心，好好整理了一下，接下来再观察观察，看看是否可以稳定运行了。大概总结下干了些啥：   
1. 把树莓派外挂硬盘的启动自动挂载加上了，这次应该不会莫名其妙的硬盘找不到了   
1. 重新安装了一下mongodb，参看[《MongoDB使用指南》](http://home.xuym.me:9000/blog/post/xym_0519_cn@163.com/MongoDB%E4%BD%BF%E7%94%A8%E6%8C%87%E5%8D%97)   
1. 重新部署了一下leanote，参看[《Leanote使用指南》](http://home.xuym.me:9000/blog/post/xym_0519_cn@163.com/Leanote%E4%BD%BF%E7%94%A8%E6%8C%87%E5%8D%97)   
1. 将mongodb和leanote的默认路径都调整到了外挂硬盘上，提高读取速度，也便于资料的整理   

好像也没干多少事情，不过终于把leanote用起来了，evernote不支持markdown，实在是有些郁闷，考虑年后evernote还继续续费么，哎，大象啥时候能发发飙，让我也不至于这么纠结。   

目前考虑evernote主要用作资料收集，大象在这方面做的还是比较完善的，leanote用来作为资料整理，毕竟还是觉得markdown写的方便，而且可以自建服务，资料还是放自己手里放心啊，第三方平台真是伤不起，最后jekyll就用来发发牢骚，感觉这样也挺好，各司其职。   

整理资料也套用三层构架，感觉自己的强迫症真是没治了，算了，不治也罢   
