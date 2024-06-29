1. U盘做2个ext4分区，sda1，sda5
2. 浏览器停止自动更新，U盘插入N1或虚拟机openwrt环境，用ssl远程登入写入软链接
    `lsblk`               #确认以上2个分区
    ```python
    ln -s /etc/rc.local /mnt/sda5/rc.local
    ln -s /etc/init.d/done  /mnt/sda5/done
    ```
3. 京东云app~智能加速服务：挂载sda1分区
4. 开启webdav，修改sda5文件
   地址:56589或56590
   
   修改文件**rc.local**，增加/usr/sbin/dropbear`
   修改文件**done**，14-16行取消#
5. SSL远程进入，刷uboot不死，注意的是不同uboot未必都能刷进，以下是线上安装的uboot
 
   ```java
   curl -o u-boot.mbn http://oss-hk4.oss-cn-hongkong.aliyuncs.com/tmp/u-boot.mbn
   dd if=/root/u-boot.mbn of=/dev/mmcblk0p13
   dd if=/root/u-boot.mbn of=/dev/mmcblk0p14
   ```
6.   网线lan口直连电脑，并且电脑设为同一ip段
      关机-按着reset键-然后开机直至看到蓝灯，进入192.168.68.1后刷机等变绿灯

[插件安装：](https://op.dllkids.xyz/packages/)
[参考文章：](https://post.smzdm.com/p/a96dez8p/)
   


