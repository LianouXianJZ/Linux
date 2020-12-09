# 命令记录
恢复默认的.bashrc文件

    cd /etc/skel
    cp .bashrc ~/  (覆盖了搞坏的文件）

修改host

    sudo gedit /etc/hosts

安装deb文件

    sudo dpkg -i linuxidc.deb

重启网络服务

    sudo service network-manager restart

查看显卡占用并结束某个进程

    nvidia-smi
    kill -9 pid_number

查找某个文件

    find / -name xxx.xx
    
hosts文件的修改

    sudo vim/etc/hosts
    
    解决某些人尽皆知的原因：https://www.ipaddress.com/
    
    ip+error网址
    
vim 编辑器
    
    :+wq 保存并退出 vim
    o 光标位置另起一行并插入

         
