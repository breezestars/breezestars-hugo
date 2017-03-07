+++
title = "ubuntu repo"
draft = true
date = "2016-07-21T03:20:23+08:00"
categories = [ "Other" ]
tags = [ "APT", "repo" ]
+++

# 目標

把ubuntu repo換成NCTU repo
<!--more-->

# 環境

- ubuntu server/desktop


# Change repo

```
sudo sed -i 's/tw.archive.ubuntu.com/ubuntu.cs.nctu.edu.tw/g' /etc/apt/sources.list
```

# 參考

[凍仁的筆記](http://note.drx.tw/2012/01/mirror.html)
