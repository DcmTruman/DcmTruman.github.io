---
title: cm_毕设开题答辩
tags: 
  - slides
  - 路由器
  - 漏洞挖掘
categories:
  - 答辩ppt
date: 2019-12-24
layout: slides
slide:
  theme: white
---

# 路由器前后端漏洞挖掘方法技术研究

#### The research on network routers' front and back-end vulnerability detection

答辩人 ： 2016信息安全 邓楚盟

指导教师 ： 范文庆

---

## 研究背景及现状

--

- [Felix Linder, a member of the hacker organization Phenoelit, attacked Cisco routers with routing & tunneling protocol in 2001](https://www.blackhat.com/presentations/bh-europe-01/fx/bh-europe-01-fx.pdf) ——路由隧道协议劫持
- [In 2005, Michael Lynn, a security researcher, presented a
vulnerability concerned handling of IPv6 packets at the Black Hat conference [2], informally
known as “Cisco gate”.](http://securityvulns.ru/files/lynn-cisco.pdf) ——实现任意代码执行
- [At the 2008 DEFCON Conference, security expert Alex Pilosov and Tony Kapela demonstrated an attack on BGP ,the core Internet routing protocol, which created a big stir among the industry and academia.](https://www.freebuf.com/articles/network/75305.html) —— BGP协议劫持

--

- 针对嵌入式设备的黑客攻击陆续进入人们视野

--

- 以思科路由器为例，截止2011年12月31号，共发现1056个漏洞。
- [各品牌路由器的各类型漏洞也逐渐被发现](http://routerpwn.com/)，而许多用户并没有更新路由器固件和硬件的意识。
- 路由器DNS劫持事件（[中东、北非](https://www.freebuf.com/column/201405.html)、[2013年LinkedIn遭遇DNS劫持](https://www.freebuf.com/news/10693.html)、[2013年54DNS劫持](https://guanjia.qq.com/news/n1/201305/17_173.html)）、路由器CSRF事件（[巴西](https://www.freebuf.com/news/60099.html))、[D-Link路由器后门](http://www.zoomeye.org/lab/dlink)等各种因路由器不安全产生损失的事件，在世界各地层出不穷。
- 《2013年我国互联网网络安全态势综述》中指出，设计通信网络设备的漏洞数量较2012年，增长1.5倍

--

- 路由器漏洞目前主要有四个方向，密码破解漏洞、web漏洞、后门漏洞和溢出漏洞
- 对于路由器的漏洞挖掘，常见手段有静态代码审计、动态跟踪分析、二进制自动化漏洞审计、定制审计攻击、模糊测试等。
- 路由器型号版本各异，黑盒挖掘的相关论文大多基于fuzz，白盒的审计也是很需要经验积累

---

## 我要做什么？

- 路由器的漏洞挖掘偏，本身需要大量经验，而总结性质的参考论文就非常少（[A Framework for DiscoveringRouter Protocols Vulnerabilities Based on Fuzzing](http://itiis.org/journals/tiis/digital-library/manuscript/file/20353/14.TIIS-RP-2012-Dec-0966.R1.pdf))
- 本次毕设，通过研究相关的技巧和工具，归纳总结一套路由器漏洞挖掘的流程框架。
- 主要针对的是路由器前端和后端服务器的漏洞，更偏向web，并尝试用渗透的思想去做路由器漏洞挖掘。

---

## 预期结果

- 根据总结的流程图，合理地按步骤进行漏洞挖掘，通过这套方法验证以前的部分漏洞可以被挖掘。
- 发现新的路由器漏洞，进一步证明流程方法的可行性。

---

## 研究意义

- 这个项目本质还是偏工程的项目的，至于意义，一言以蔽之，“为了挖洞”，或者说，为了锻炼自己漏洞挖掘的能力。
- “经验之谈”不够科学和清晰的展示挖掘思路，而且大多需要人与人之间的传授。如果能集百家之长，总结一套可行和清晰的方法，可以减少初学者的踩坑次数，降低一定的门槛，进一步提高大家对路由器安全的重视。

---

## 初步规划

- 12月—1月中旬 ： 学习web漏洞相关技巧工具和搭建路由器所需环境。
- 1月中旬~2月初 ：复现前人漏洞挖掘过程，总结记录个人思路。
- 2月初~3月初 ： 开始自己进行漏洞挖掘。
- 3月初~毕设答辩 ： 总结过程中相关的挖洞流程框架，并再次验证方法的可行性。

---

# THANKS

