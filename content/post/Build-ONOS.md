+++
draft = false
date = "2016-07-11T03:10:32+08:00"
title = "Build ONOS"
categories = [ "ONOS" ]
tags = [ "Controller" ]
+++

這篇是準備給7/21 讀書會報告用的，同時自己做Note
<!--more-->

# 目標

在Control Node安裝ONOS Compile環境，從GitHub pull source code, compile並push到ONOS Nodes上

# 環境

- Build Machine
  - Ubuntu 14.04
  - Ansible 2.1.0.0
  - Java SE Runtime Environment 1.8.0_91
  - Apache karaf 3.0.5
  - Apache maven 3.3.9

- ONOS Node
  - Ubuntu 14.04
  - Java SE Runtime Environment 1.8.0_91


## Install Ansible on Build Machine

```
sudo apt-get install software-properties-common -y
sudo apt-add-repository ppa:ansible/ansible -y
sudo apt-get update
sudo apt-get install ansible -y
```


```
sudo apt-get install software-properties-common -y && sudo apt-add-repository ppa:ansible/ansible -y && sudo apt-get update && sudo apt-get install ansible -y
```


[Ansible script](https://github.com/breezestars/ONOS-Install)
