#命令记录
恢复默认的.bashrc文件

 cd /etc/skel
cp .bashrc ~/  (覆盖了搞坏的文件）

修改host
sudo gedit /etc/hosts

安装deb文件
sudo dpkg -i linuxidc.deb

重启网络服务
sudo service network-manager restart
