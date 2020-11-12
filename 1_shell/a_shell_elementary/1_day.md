# 一、基础
## 1 shell是一个命令行解析器, 我们是通过shell 和Linux 进行交互
## 2.hell 主要包含四个部分：
```
a. 系统内存的管理
b. 软件程序的管理
c. 硬件设备的管理
d. 文件系统的管理
```
## 3. liunx 中有多种shell , 默认使用的是 /bin/bash
```
cat /etc/shells  ==  /bin/bash -c 'cat /est/shells'
```
## 4. linux 中经常使用的目录
```
/bin linux 用户经常使用的命令
/sbin linux super 用户经常使用的命令
```
## 5. shell 脚本的编码要求
```
声明：#!/bin/bash  -->  说明这个script 是要使用 /bin/bash 来执行的
正文：必须是shell 解释器能解释的
    在shell 脚本中一切皆字符串
    在shell 中，空格通常用来切分变量，所提空格是不能随便输入的
```
## 6. 脚本的执行方法
```
a. bash / sh  +  script.sh
b. ./script.sh
d. source / .  + script.sh
```

# 二、变量的操作
## 1. 增、删、改、查
```
增（定义）变量名=变量值
删 unset 变量名
改 变量名=变量值
查 echo $变量名
    查看当前bash 下的所有变量: set
```
## 2. 特殊字符
```
readonly 用来修饰一个只读变量 （不可修改，不可删除）
export 讲一个变量提升为全局变量
           局部变量默认只在定义的bash 中起作用（类似于作用域）
如何在bash_b 中 访问 bash_a 中的变量
    1. bash_a 不能关闭
    2. 该变量为全局变量
```
## 3. 注意
```
1. 变量赋值是，值全部以字符串存在，无法进行运算
2. 赋值中如果有空格，需要用引号引起来
    单引号：不脱义
    双引号：脱义
3. 反引号：将程序执行的结果赋值给变量
    反引号等价于： ${}
4. ./ 和 source 相当于在当前 bash run script
   /bin/bash 和 bash 相当与要新打开一个bash run script
```
# 4. 特殊变量
```
$? 上一条命令的返回值，在bash 中，如果返回的值为 0 代表执行成功，
$# 参数的个数
$* 参数列表
$@ 参数列表
$0-n 第n个参数
    超过10以上，使用 ${n}
```

