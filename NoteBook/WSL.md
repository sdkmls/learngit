## WSL打开步骤

```
1.wsl -d Ubuntu-22.04 #启动特定的ubuntu系统
2.su - user1          #启动用户
```

## 安装WSL

```
wsl -- install
```

## 查看可以安装的linux系统

```
wsl --list --online
```

## 下载linux系统以ubuntu24.04为例

```
wsl --install Ubuntu-24.04
```

## 查看已经下载的系统

```
wsl --list -v
```

## 启动系统

```
wsl -d Ubuntu
```

## 离开系统

```
exit
```

## 备份系统

```
wsl --export Ubuntu-20.04  D:\WSL\20.04\ubuntu2004.tar
```

## 导入系统

```
wsl -- import Ubuntu2 D:\WSL C:\Users\Administrator\ubuntu.tar
```

## 卸载系统

```
wsl --unregister

```

## 转换ubuntu安装路径

```
https://blog.csdn.net/muxuen/article/details/142714487
```

## WSL实现图形桌面

### 第一种方法

```
#启动xrdp（在wsl中）
sudo /etc/init.d/xrdp start

#Windows中
1.win+R  打开搜索框
2.mstsc
3.地址输入localhost:3390

#实现图形化显示
python examples/viewer.py --scene \root\app\git\habitat-sim\habitat_test_scenes\versioned_data\habitat_test_scenes\skokloster-castle.glb
```

### 第二种方法

```
1.打开ipconfig  查看WLAN的IPV4地址
2.sudo nano ~/.bashrc #添加新的IP
3.source ~/.bashrc
4.打开Xlaunch  
3.startxfce4      #wsl上启动窗口

```

## GUI应用

```
nautilus          #文件资源管理器
```

