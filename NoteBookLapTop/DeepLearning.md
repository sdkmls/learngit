# 环境配置

## CUDA,cudnn,pytorch联合安装

1.在官网下载CUDA

2.在官网下载cudnn是CUDA的工具  

3.下载带有CUDA的Pytorch  版本要低于CUDA

### CUDA技巧

在windows命令行中查看GPU运行情况

```
nvidia-smi
```



### jupyter notebook路径配置

1.命令行输入：

```
jupyter notebook --generate-config  #下载配置环境
```

2.在jupyter_notebook_config中修改配置环境

按ctrl +F 输入：The directory to use  查找更改路径

3.找到    jupyter  notebook 文件位置查找属性删除

<img src="fig/jupyter notebook属性更改.png" alt="jupyter notebook属性更改" style="zoom:50%;" />

# ANACONDA技巧

### 环境配置

创建新的环境

```
conda create -n env-name  [list of package]
```

假设已有环境名为A，需要生成的环境名为B：

```
conda create -n B --clone A
```



# jupyter notebook 快捷键

```
esc    #进入命令模式
esc m  #转为markdown模式
esc y  #转为code模式
esc b  #向下加代码块
esc a  #向上加代码块
esc D D #进入命令模式，选中要删除的模块按两下DD
shift enter  #运行

```

# 学习社区

1.ShowMeAi

[ShowMeAI知识社区](https://www.showmeai.tech/)

2.GOAI
