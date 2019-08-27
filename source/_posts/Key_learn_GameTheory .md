---
title: Key_博弈学习笔记
tags: 
  - 博弈
  - 学习笔记
categories:
  - Key
  - 数学
  - 博弈
date: 2019-8-27
---

<!-- more -->

### 博弈

#### NIM博弈

$n$ 堆物品，每堆 $A_i$ 个，每次在同一堆取任意多，先手是否必胜。
$A_1 xor A_2 xor\cdots xorA_n\neq0$ 时，先手必胜。

---

#### Mex运算

$mex(S)$ 不属于集合 $S$ 的最小非负整数

---

#### SG函数

$y_1,y_2,y_3\cdots y_k$ 为 $x$ 的后继节点：$SG(x)=mex(\{SG(y_1),SG(y_2),SG(y_3),\cdots,SG(y_k)\})$

> 后继结点中有一个是必败节点，则该节点必胜
> 若都是必胜节点，则该节点必败
>
> *且当该节点为必胜节点时，下一步一定能走到一个值比其小的节点*

---

#### 有向图游戏的和

$G_1,G_2,\cdots,G_m$ 是 $m$ 个有向图游戏。定义有向图游戏 $G$ ，它的行动规则是任选某个有向图游戏 $G_i$ ，并在 $G_i$ 上行动一步.

$SG(G)=SG(G_1)xorSG(G_2)xor\cdots xorSG(G_m)$

---