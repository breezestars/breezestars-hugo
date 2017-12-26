+++
draft = false
title = "用p4app建立一個基本的P4測試開發環境"
date = "2017-12-26T22:00:00+08:00"
categories = ["P4"]
tags = ["SDN","Docker"]
+++

> 複雜的事情簡單做，別複雜化了

主要介紹如何利用p4lang/p4app來作為一個簡單基本的測試環境

可以免去裝PI, P4C, ptf, p4-hlir, thrift, bmv2等Repo的繁雜過程

<!--more-->

# p4app
---
p4app是一個p4lang底下發展的專案，是一套已經包好的工具，可以用來build、run和測試P4 programs.

相信大家在想要接觸P4的同時，就已經裝一堆環境裝到很煩，被一堆環境問題困擾著，這時候就適合先用p4app起手練習

在我整個使用過程中，發現p4app雖然是設計成一整套包好的工具希望P4寫好就可以直接run，但是在關於mininet topo的一些部分還沒有辦法做到可以任意動態調整，所以提醒大家使用上自行徵酌。

# Environment
---
- [ ] OS
  - [X] Ubuntu 16.04 Server
  - [ ] Ubuntu 14.04 Server
  - [ ] CentOS 7.4
- [ ] Application
  - [X] Docker
  - [X] Git

```bash
sudo apt update && sudo apt install git curl -y
```

# Installation
---
## 1.先安裝Docker

```bash
sudo curl -sSL https://get.docker.io | bash
```

## 2.安裝p4app

```bash
git clone https://github.com/p4lang/p4app.git
cd p4app
```
你可以把 <kbd>p4app</kbd> 複製到任何一個$PATH資料夾裡，或者把p4app整個資料夾新增到$PATH

個人習慣是在/usr/local/bin裡用ln建立鏈結

## 3.執行Example

基本上就是希望大家可以最快習慣這個工具，所以就直接跑一個最基本Example來看看吧！

```bash
p4app run examples/simple_router.p4app
```
應該會出現下圖

![p4app example執行畫面](https://raw.githubusercontent.com/breezestars/breezestars-hugo/master/images/p4app-1.png "p4app example執行畫面")
![p4app example mininet畫面](https://raw.githubusercontent.com/breezestars/breezestars-hugo/master/images/p4app-2.png "p4app example mininet畫面")

在這個Example裡，網路拓墣是

> h1<->s1<->h2

我們直接在mininet terminal裡面直接輸入
```
h1 ping h2 -c 3
```
應該要可以看到上圖中一樣的結果

到目前為止應該就知道如何把Repo裡其他的example也run起來跑看看
其餘細節後續文章會繼續介紹





