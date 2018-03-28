##挂载##
1. cat /proc/partitions
2. sudo mount -t vfat /dev/sdc ~/usb
3. sudo fdish -l /dev/sdc
4. sudo fdisk -l
5. sudo mount -t vfat /dev/sdc4 ~/usb
6. umount ~/usb

##ssh退出程序运行##
1. nohup ./a.out > out.txt 2>&1 &
2. tail -fn 10 out.txt