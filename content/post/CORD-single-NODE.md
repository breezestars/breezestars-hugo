+++
date = "2016-08-01T03:20:29+08:00"
title = "CORD single NODE"
draft = false
categories = [ "CORD" ]
tags = [ "Ciab" ]
+++

# 目標

安裝CORD single node
<!--more-->


# 環境

- ubuntu server
- 64-bit server, with
  - 48GB+ RAM
  - 12+ CPU cores
  - 1TB+ disk
- Access to the Internet
- Ubuntu 14.04 LTS freshly installed
- Account used to SSH from build host has password-less sudo capability (e.g., like the ubuntu user)



# Download single node pod script

```
wget https://raw.githubusercontent.com/opencord/platform-install/master/scripts/single-node-pod.sh
```

最容易卡在config-virt : Wait for uvt-kvm image to be available 這塊

此時可先檢查是否已經有Ubuntu cloud images

沒有的話直接用

```
sudo uvt-simplestreams-libvirt sync release=trusty arch=amd64
```

或

```
uvt-simplestreams-libvirt sync \
    --source http://cloud-images.ubuntu.com/daily \
    release=trusty arch=amd64
```




把image 抓下來

等確認有image之後再把ansible中config-virt : Wait for uvt-kvm image to be available註解掉然後重新執行

# 參考
ONOS wiki

[gihyo.jp](http://gihyo.jp/admin/serial/01/ubuntu-recipe/0344)

[阿舍的隨手記記-Ubuntu 用 uvtool 快速建立 Ubuntu 虛擬機器](http://www.arthurtoday.com/2015/04/ubuntu-quickly-create-vms-with-uvtool.html)

[Linux system engineering and administration](http://linuxsysengineer.blogspot.tw/2014/10/installing-ubuntu-cloudimages-with.html)
