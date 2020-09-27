[TOC]

# target_include_directories

向一个目标中添加头文件路径。

```cmake
target_include_directories(<target> [SYSTEM] [BEFORE]
    <INTERFACE|PUBLIC|PRIVATE> [item ...]
    [<INTERFACE|PUBLIC|PRIVATE> [item ...] ...]
)
```

target必须是使用add_executable()或add_library()命令创建的，而不能是一个目标别名。

指定的目录一般是追加的方式进行添加，但如果指定了BEFORE，后面指定的目录将添加在原有目录的前面。

INTERFACE、PUBLIC、PRIVATE指定了后面参数的范围：

- PRIVATE、PUBLIC的项目将会在目标的INCLUDE_DIRECTORIES属性
- PUBLIC、INTERFACE的项目将会在目标的INTERFACE_INCLUDE_DIRECTORIES属性

## 示例

```cmake
#使用add_executable()创建一个目标
add_executable(test "a.c" "b.c")
#将相对目录../my_math加入到目标的头文件目录列表中
target_include_directories(test PUBLIC "../my_math")
#将绝对路径/usr/local/ffmpeg/include追加到目标的头文件目录列表中
target_include_directories(test PUBLIC "/usr/local/ffmpeg/include")
#将绝对路径/usr/local/boost加到目标的头文件目录列表的开头
target_include_directories(test BRFORE PUBLIC "/usr/local/boost")
```

