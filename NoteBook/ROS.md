# 初始环境配置

打开终端

```
Crtl+Alt+T 
```

创建文件夹后面再创建一个子文件夹src

```
mkdir -p demo01_ws/src
```

创建ROS功能包

```
catkin_make
```

到达指定文件夹启动vscode

```
cd   demo01_ws
code .
```

在vscode中对src文件创建依赖文件

```
右键+Create Catkin Package  
命名包名
导入需要的依赖包
```

让Ctrl+shift+B可以编译

```
Ctrl+shift+B  弹出catkin_make:build  点击后面的小齿轮
在.vscode文件夹内出现一个tasks.json文件
```

修改tasks.json文件

```
{
// 有关 tasks.json 格式的文档，请参见
    // https://go.microsoft.com/fwlink/?LinkId=733558
    "version": "2.0.0",
    "tasks": [
        {
            "label": "catkin_make:debug", //代表提示的描述性信息
            "type": "shell",  //可以选择shell或者process,如果是shell代码是在shell里面运行一个命令，如果是process代表作为一个进程来运行
            "command": "catkin_make",//这个是我们需要运行的命令
            "args": [],//如果需要在命令后面加一些后缀，可以写在这里，比如-DCATKIN_WHITELIST_PACKAGES=“pac1;pac2”
            "group": {"kind":"build","isDefault":true},
            "presentation": {
                "reveal": "always"//可选always或者silence，代表是否输出信息
            },
            "problemMatcher": "$msCompile"
        }
    ]
}
```

运行C++文件需要配置hello下面的CMakeLists.txt文件

```
add_executable(hello.cpp src/hello.cpp)                              #前后文件名最好保持一致

# Specify libraries to link a library or executable target against
target_link_libraries(hello.cpp
  ${catkin_LIBRARIES}
)
```

在demo01_ws上运行

```
roscore
```

换个终端在demo01_ws上运行hello就是src文件下的文件

```
rosrun hello  hello.cpp
```

