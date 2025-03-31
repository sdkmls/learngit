## 命令集合

```
pwd         #打印当前绝对路径
mkdir       #创建文件夹
ls          #查看当前目录文件夹  
cd ..       #退回上一个文件
mv * ./     #将本目录所有文件升为上一级
mv a.txt a1.txt #修改文件名
exit        #ubuntu退出root
rm test.py  #删除文件
sudo reboot #重启linux系统
```

## vi命令合集

```
vi test.txt              #创建test.txt文件
在vi里面填完信息后，使用Esc键，
:u --撤销上一次操作
:w --保存文件
:q --退出Vim编辑器


```

## nano

```
nano script.py    #创建一个python脚本
Ctrl O            #保存脚本
Ctrl X            #退出nano
```



# Ubuntu安装Docker

### 第 1 步：更新软件包并安装必要软件运行以下命令，更新软件包索引并安装添加 Docker 仓库所需的前置软件包：

```
sudo apt update
sudo apt install apt-transport-https curl
```

## 第 2 步：导入 Docker 官方 GPG 密钥

```
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
```

## 第 3 步：添加 Docker 官方仓库

将 Docker 的官方仓库添加到 Ubuntu 24.04 LTS 的软件源列表：

```
echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

## 第 4 步：更新软件包列表

刷新软件包列表，以便系统识别新添加的 Docker 仓库：

```
sudo apt update
```

## 第 5 步：安装 Docker

执行以下命令在 Ubuntu 24.04 LTS 上安装最新版本的 Docker，包括 Docker 引擎及其相关组件：

```
sudo apt install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

## 第 6 步：检查 Docker 服务状态

```
sudo systemctl is-active docker
```

