# 文件拖拽

## VMware

1.虚拟机->设置->CD/DVD(SATA)->该虚拟盘下的master.iso      +CD/DVD2(SATA)->该虚拟盘下的linux.iso

2.虚拟机->安装tools->将磁盘里的压缩文件解压到桌面->到目标文件运行  sudo ./vmware-install.pl

3.输入命令： sudo apt-get autoremove open-vm-tools
                       sudo apt-get install open-vm-tools-desktop
