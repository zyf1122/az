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
