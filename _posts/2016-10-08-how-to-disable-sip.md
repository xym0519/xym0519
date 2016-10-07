---
layout: post
title: "How to disable SIP (System Integrity Protection)"
categories: tech
---

### What is SIP
SIP 技术主要是用来限制 root 用户的权限, 以提升系统的健壮性。   
可配置项如下: 

    Apple Internal
    Kext Signing
    Filesystem Protections
    Debugging Restrictions
    DTrace Restrictions
    NVRAM Protections

### How to disable
1. Reboot into RecoveryHD mode <a href='/tech/2016/10/07/how-to-enter-osx-recoveryhd-mode/' target='blank'>[Forward]</a>
1. Open terminal
1. csrutil disable

### References
1. <a href='http://havee.me/mac/2015-10/system-integrity-protection-on-el-capitan.html' target='blank'>El Capitan 中 SIP 介绍</a>
1. <a href='http://www.jianshu.com/p/0572336a0771' target='blank'>如何关闭OSX 10.11 SIP (System Integrity Protection)</a>
