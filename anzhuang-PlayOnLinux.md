
## 安装PlayOnLinux
[教程链接](http://blog.csdn.net/lainegates/article/details/41011499)
```
一、安装wine，playonlinux需要wine支持。

sudo add-apt-repository ppa:ubuntu-wine/ppa  

sudo apt-get update  

sudo apt-get install wine1.7 winetricks

二、安装playonlinux

sudo apt-get update  

sudo apt-get install curl  

sudo apt-get install p7zip-full  

sudo apt-get install winbind  

sudo apt-get install playonlinux

安装完后直接在终PlayOnLinux打开即可！
```










### CrossOver问题　缺少32位的libgphoto2_port.so.10运行库
[安装运行库](https://www.codeweavers.com/support/wiki/Diag)
```
32 位 Debian 或 Ubuntu：sudo apt-get install libgphoto2-6
 64 位 Debian 或 Ubuntu：sudo apt-get install libgphoto2-6:i386
 32/64 位 Fedora：dnf install libgphoto2.i686
 32/64 位 Mandriva：urpmi libgphoto2
 32 位 SUSE：zypper install libgphoto2-6
 64 位 SUSE：zypper install libgphoto2-6-32bit
 32 位 Arch：pacman -Syu libgphoto2
```
