### 安装CrossOver教程
[安装CrossOver](https://zhuanlan.zhihu.com/p/27549700)
```
1.检查软件包的依赖：

sudo apt-get clean
sudo apt-get -f install
2.由于系统是64位，在此添加对32位库的支持

sudo dpkg --add-architecture i386  
sudo apt-get update  
sudo apt-get install lib32z1 lib32ncurses5
3.下载三个crossover必要文件：（需要按顺序安装）
```
[三个包的链接](https://pan.baidu.com/share/init?surl=kVwX8W3)
密码: gn99
```
sudo dpkg -i crossover-15_15.0.3-1_all.deb
sudo dpkg -i crossover-15_15.0.3-1_all-free.deb
sudo dpkg -i deepin-crossover-helper_1.0deepin0_all.deb

```
### 安装ＱＱ
```
sudo dpkg -i apps.com.qq.im_8.1.17255deepin11_i386.deb
接下来打开crossover

运行QQ，如果字体是乱码：

原版那个ttf是SJIS内码，没有很多简体中文的汉字，是乱码的真正起因。
下载一个字体到crossover的fonts文件夹，替换原有的ume-ui-gothic.ttf
在这里我下载的是宋体（simsun.ttf）
步骤是（不放心的话可以先把ume-ui-gothic.ttf复制到别处）：
cp simsun.ttf /opt/cxoffice/share/wine/fonts
cp ume-ui-gothic.ttf ~/下载
rm ume-ui-gothic.ttf

```
### 当你退了QQ，然后再次登录同一个账号的时候，发现占用（登录失败）
```
我们可以使用命令来结束进程，但是每次都输入一串命令太烦人了
所以，创建一个脚本，每次需要使用，执行它就好了
步骤：
sudo gedit /usr/bin/killqq       （路径放你喜欢的就好，方便自己调用就行）
接下来吧下面这串内容复制进去：
ps aux|grep -v grep|grep wine|cut -c 9-15|xargs kill   
ps aux|grep -v grep|grep QQ|cut -c 9-15|xargs kill   
ps aux|grep -v grep|grep qq|cut -c 9-15|xargs kill   
pkill  plugplay.exe  
pkill  explorer.exe  
pkill  services.exe
cd  /usr/bin              （进入目录）
sudo chmod 777 killqq      (赋予权限)
killqq      （执行）
再次登录---成功！

以后每次下了QQ想要再次登录（不重启的情况下），执行killqq就好。。
```
