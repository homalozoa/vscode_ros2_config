# Visual Studio Code ROS 2 Work Space Configuration

## What is it

This is a VS Code plugin that is easy to configure the ROS 2 development environment.

## How to use it

1. Copy the `.vscode` (maybe a hidden file) in the environment to the workspace of `ROS 2`, that is, you can run the directory of `colcon` directly.

   The directory structure is as follows, among which some folders under `.vscode` are not in this warehouse, like `build`, `install`, and `log` are folders generated during compilation, while `src_0` and `src_1` refer to Your code folder.

   |--.vscode
   |--build
   |--install
   |--log
   |--src_0
   |--src_1

2. Modify the path in `c_cpp_properties.json` in the `.vscode` directory, if `ROS 2` is compiled according to the source code and specified to the `/opt/ros2/galactic` directory, the path is `/opt/ros2/galactic /include/**`, at the same time, it is necessary to ensure that all paths related to `/opt/` are consistent with the path.
3. If you use a different C/C++ version, such as C11, C++ 17, you need to modify `cStandard` in `c_cpp_properties.json` to `C11`, and `cppStandard` to `C++17`.
4. Batch replace the `Python` version to the `Python` version on the device, the file is `settings.json`, find `python3.` in it, and then modify the following number to your own version. Generally speaking, Ubuntu 18.04 is Python3.6 , Ubuntu 20.04 is Python 3.8, I am using Arch Linux, which corresponds to Python 3.9.
5. Open VS Code in the root directory of the workspace and run `code .`.
6. At this time, the recommended plugins will pop up, just allow it.
7. It is recommended to install the following plugins at the same time to facilitate development. 
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
8. After completing the installation, when you develop ROS 2 related projects, you can quickly view various variable function definition declarations, etc., which are the same as other IDE functions, so I won't go into details.

## Reference

[vscode_ros2_workspace](https://github.com/athackst/vscode_ros2_workspace)
