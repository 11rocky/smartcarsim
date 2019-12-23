# SCS 智能车仿真平台(CMake版)

修改自[Github项目](https://github.com/Sciroccogti/smartcarsim.git)

以全国大学生智能车竞赛为背景，依照智能车竞赛规则建立仿真模型，旨在为广大参与智能车竞赛的参赛选手提供一个仿真智能车机械，验证软件控制算法的平台。

该平台以刚体模型库 OpenDE 和图形库 OpenGL 为基础，
描述并绘制智能车以及赛道的机械模型，仿真智能车行进的
物理过程。


## 版本信息
修改了编译过程，采用CMake进行构建  

## 目录结构及说明
SCS-1.0.1	根目录  
├── scs			SCS 目录  
│   ├── include			SCS 头文件目录  
│   ├── src			SCS 源文件目录  
│   └── CMakeLists.txt			CMake文件  
├── demo			样例目录  
│   └── main.cpp	样例文件  
├── doc			文档目录  
│   ├── SCS-1.0.1.pdf		使用手册及编程接口  
│   └── src			文档源代码目录  
├── tracks    赛道文件目录  
├── LICENSE  
├── README.md		本文件  
└── CMakeLists.txt			CMake文件  

## 使用方法(Ubuntu)
1. 安装编译工具和库   
    + sudo apt install freeglut3-dev  
    + sudo apt install build-essential  
    + sudo apt install cmake    

2. 安装 OpenDE  
    + 下载 OpenDE http://sourceforge.net/p/opende/  
    + 解压并从终端进入该目录  
    + 运行 ./configure --enable-double-precision --disable-demos  
    + 运行 make  
    + 运行 sudo make install  

3. 编译工程  
    + 进入工程所在目录  
    + mkdir build  
    + cd build  
    + cmake ..  
    + make  
    + make install  

4. 运行
    + 编译结束后，进入工程根目录下的bin文件夹  
    + ./demo  