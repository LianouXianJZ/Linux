# Ubuntu19.04配置记录
   - **硬件**： 
                                 
     i3-8100，gtx1060，有核显，仅支持UEFI引导启动。
- **预配置环境** ：

   win10
- **配置前准备**：

   关闭快速启动，关闭安全模式，准备ubuntu19.04镜像,easy UEFI。

 


# 开始 










-  easy uefi选择镜像，创建新的引导,重启。（无问题）

- 安装界面，安装

      卡死在界面，解决方法，不进入安装界面，上下选择Install Ubuntu ,e进入编辑页面，删除quiet splash之后的---  输入$vt_handoff acpi_osi=linux nomodeset ,F10保存

- 分区完毕后，进入系统。

       卡死 解决方法 
      
       e编辑ubuntu高级设置，倒数第三行更改为 ro recovery nomodeset
      
       重新进入高级设置
      
       进入root Drop to root shell prompt 
      
       sudo chmod 666 /etc/modprobe.d/blacklist.conf
          
       echo "">>/etc/modprobe.d/blacklist.conf          
      
       echo "blacklist vga16fb">>/etc/modprobe.d/blacklist.conf
       
       echo "blacklist nouveau">>/etc/modprobe.d/blacklist.conf
      
       echo "blacklist rivafb">>/etc/modprobe.d/blacklist.conf
      
       echo "blacklist rivatv">>/etc/modprobe.d/blacklist.conf
      
       echo "blacklist nvidiafb">>/etc/modprobe.d/blacklist.conf
       
       sudo chmod 644 /etc/modprobe.d/blacklist.conf

       sudo update-initramfs -u

       sudo reboot -h now
     
     
     
- 进入终端

      $sudo add-apt-repository ppa:graphics-drivers/ppa
      $sudo apt-get update
      $ubuntu-drivers devices
      $sudo apt-get install nvidia-driver-
 # 额外记录

   + 安装过程中的问题大都来源于核显。

+ 主要参照博客

https://blog.csdn.net/qq_41199831/article/details/83860126 
