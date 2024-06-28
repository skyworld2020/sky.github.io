1. U盘做2个分区，sda1，sda5
2. 浏览器停止自动更新，N1或虚拟机openwrt环境，用ssl远程登入写入软链接
    `lsblk`#确认分区
    `ln -s /etc/rc.local /mnt/sda5/rc.local
     ln -s /etc/init.d/done  /mnt/sda5/done`

3. 