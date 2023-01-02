### Vmware安装Ubuntu
#### 软件安装
*1. open-vm-tool*  
`sudo apt install open-vm-tools-desktop`
#### 更换壁纸
![壁纸](picture/El%20Capitan.jpg)
#### 换阿里源
*1. 查看ubuntu版本*  
`lsb_release -a`
```sh
ding@linux:~$ lsb_release -a
No LSB modules are available.
Distributor ID:	Ubuntu
Description:	Ubuntu 16.04.7 LTS
Release:	16.04
Codename:	xenial
```
*2. 备份旧的源文件*  
[阿里源官方链接](https://developer.aliyun.com/mirror/ubuntu?spm=a2c6h.13651102.0.0.3e221b11aP6zt9)
```sh
sudo cp /etc/apt/sources.list /etc/apt/sources.list.bak
sudo gedit /etc/apt/sources.list
```
*3. 用以下内容替换全文件*  
```sh
deb https://mirrors.aliyun.com/ubuntu/ xenial main
deb-src https://mirrors.aliyun.com/ubuntu/ xenial main

deb https://mirrors.aliyun.com/ubuntu/ xenial-updates main
deb-src https://mirrors.aliyun.com/ubuntu/ xenial-updates main

deb https://mirrors.aliyun.com/ubuntu/ xenial universe
deb-src https://mirrors.aliyun.com/ubuntu/ xenial universe
deb https://mirrors.aliyun.com/ubuntu/ xenial-updates universe
deb-src https://mirrors.aliyun.com/ubuntu/ xenial-updates universe

deb https://mirrors.aliyun.com/ubuntu/ xenial-security main
deb-src https://mirrors.aliyun.com/ubuntu/ xenial-security main
deb https://mirrors.aliyun.com/ubuntu/ xenial-security universe
deb-src https://mirrors.aliyun.com/ubuntu/ xenial-security universe
```
*4. 更新*  
```sh
sudo apt update
sudo apt upgrade
```
#### 软件卸载
*1. LibreOffice*  
`sudo apt remove libreoffice-common`  
*2. Amazon*  
`sudo apt remove unity-webapps-common`  
*3. 自动卸载*  
`sudo apt-get autoremove`  
*4. 查看内核版本*  
`uname -a`  
```sh
ding@linux:~$ uname -a
Linux linux 4.15.0-112-generic #113~16.04.1-Ubuntu SMP Fri Jul 10 04:37:08 UTC 2020 x86_64 x86_64 x86_64 GNU/Linux
```