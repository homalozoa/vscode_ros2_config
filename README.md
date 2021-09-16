# Visual Studio Code ROS 2 Work Space Configuration

## 这是什么

这是一个便于配置ROS 2开发环境的VS Code插件. 

## 如何使用

1. 将环境里的`.vscode`(有可能是隐藏文件) 复制到`ROS 2`的工作空间, 即你可以直接运行`colcon`的目录. 

   目录结构如下：

   |--.vscode

2. 修改`.vscode`目录下的`c_cpp_properties.json`里的路径, 如果`ROS 2`是按照源码编译, 并且指定到`/opt/ros2/galactic`目录的话, 路径是`/opt/ros2/galactic/include/**`, 同时, 需要保证所有的`/opt/`相关的路径, 都与该路径保持一致. 
3. 批量替换`Python`版本到设备上的`Python`版本, 文件为`settings.json`, 在里面找到`python3.`, 然后修改后面的数字为自己的版本. 一般情况, Ubuntu 18.04是Python3.6, Ubuntu 20.04是Python 3.8, 我使用的是Arch Linux, 对应Python 3.9.
4. 在工作空间根目录打开VS Code, 即运行`code .`即可. 
5. 此时会弹出推荐安装的插件, 允许即可. 
6. 推荐同时安装如下插件, 以便于开发. 
   1. C/C++
   2. C++ Intellisense
   3. CMake
   4. CMake Integration
   5. CMake Tools
   6. Compare Folders
   7. Better C++ Syntax
   8. compareit
   9. XML Tools
   10. Python
7. 完成安装后, 再开发ROS 2相关的工程时, 可以快速查看各类变量函数定义声明等, 和其他IDE功能相同, 不赘述. 

## 参考自

[vscode_ros2_workspace](https://github.com/athackst/vscode_ros2_workspace)
