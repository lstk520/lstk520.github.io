---
title: Git打Tag的命令
date: 2017-02-21 13:55:46
tags: git
---
1.打开Git命令行；
2.切换到你要打tag的分支上去，并输入如下示例语句：git tag -a V0.5 -m"描述信息：V0.5版本"；
3.输入命令行：git push origin V0.5 ，此处的"V0.5"与上面语句中的"V0.5"要一致，否则是无效的；
4.打开gitlab查看tag信息，点开就能看到你打的tag信息了！
