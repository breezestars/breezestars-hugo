+++
draft = false
date = "2016-08-03T03:20:40+08:00"
title = "CORD OFTest"
tags = [ "OFDPA" ]
categories = [ "CORD" ]
+++

# 目標

建置出一個OFTest的環境來測試Switch支援OpenFlow的程度
<!--more-->

# 環境

- Server or VM with three nics


# 補充wiki上少的package

```
sudo apt-get install python python-pip python-dev python-lxml libffi-dev libssl-dev -y
sudo pip install cryptography
sudo pip install ncclient
sudo pip install scapy pycrypto
sudo apt-get install python-ecdsa git
```


# 參考

[ONOS wiki:Hardware Conformance OpenFlow Test](https://wiki.onosproject.org/display/ONOS/Hardware+Conformance+OpenFlow+Test)
