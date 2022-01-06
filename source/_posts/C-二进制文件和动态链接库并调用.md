---
title: Hello World
date: 2022-01-05 21:40:58
categories:
	- 随笔
tags:
	- C++
---

<p><img src="/assets/blogImg/bridge.jpg" width="500"></p>

记得第一次遇见yilia，那种如获至宝的心情。
时隔多年，博客重新上线，谢谢作者！

<!-- more -->

### Cpp 二进制文件和动态链接库并调用

**编译生成动态库文件**

``` bash
  g++ -fPIC -share -o libxxx.so xxx.cpp
  // -fPIC 作用于编译阶段, -share 表示共享的，用于实现程序的动态链接功能，和前一个参数往往搭配使用
```

**调用生成的库文件**

``` bash
  g++ -o main main.cpp ./libxxx.so
  // 头文件和库文件以及源文件在同一目录下
```

**.so库文件在/usr/lib下，.h头文件在/usr/include**

``` bash
  g++ main.cpp -o main -lmyTest
  // 默认动态库路径和头文件路径
```

**.so库文件.h头文件在指定目录下**

``` bash
  g++ main.cpp -I -L -lmyTest -o main 
  // -I (头文件所在目录) -L (库文件所在目录) -l (库名)
```

