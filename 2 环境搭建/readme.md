# _环境搭建_

## 1. 开启FTP
```sh
sudo apt-get install vsftpd
sudo vim /etc/vsftpd.conf
local_enable=YES
write_enable=YES
sudo /etc/init.d/vsftpd restart
```

## 2. SSH
```sh
sudo apt-get install openssh-server
```

## 3. 交叉编译工具链
```sh
sudo mkdir /usr/local/arm
sudo cp gcc-linaro-4.9.4-2017.01-x86_64_arm-linux-gnueabihf.tar.xz /usr/local/arm/
sudo tar -vxf gcc-linaro-4.9.4-2017.01-x86_64_arm-linux-gnueabihf.tar.xz
# 打开配置文件
sudo vi /etc/profile
# 在最后一行添加
export PATH=$PATH:/usr/local/arm/gcc-linaro-4.9.4-2017.01-x86_64_arm-linux-gnueabihf/bin
sudo apt-get install lsb-core lib32stdc++6
```
查看版本号
```sh
arm-linux-gnueabihf-gcc -v
```

