+++
draft = false
date = "2016-07-19T03:20:09+08:00"
title = "EdgeCore 4600 Install"
categories = [ "Switch" ]
tags = [ "EdgeCore", "4600" ]
+++

# 目標

在EdgeCore 4600上安裝Cumulus
<!--more-->

# 環境

- EdgeCore 4600


# Get into ONIE


Reboot and interup autoboot, enter "run onie_rescue" to get in ONIE.


# Download ONIE-installer-xxxxx.bin

```
install_url tftp://<tftp IP address>/onie-installer-xxxxx.bin
```

然後就會自己跑完安裝了...
剛裝完的時候會因為沒有安裝License所以有部分service啟動fail

登入的預設

Username: cumulus

Password: CumulusLinux!


透過下方指令安裝license

```
cumulus@switch:~$ sudo cl-license -i
<paste file>
^+d
```

# 參考

[Cumulus Quick Start](https://docs.cumulusnetworks.com/display/CL22/Quick+Start+Guide)
