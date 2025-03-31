```

```

## 安装WSL

```
wsl -- install
```

## 查看可以安装的linux系统

```
wsl --list --online
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
wsl --export Ubuntu ubuntu.tar
```

## 导入系统

```
wsl -- import Ubuntu2 D:\WSL C:\Users\Administrator\ubuntu.tar
```

## 卸载系统

```
wsl --unregister
```

