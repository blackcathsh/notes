[TOC]

# target_link_directories

向一个目标中添加链接目录。

```cmake
target_link_directories(<target> [BEFORE]
    <INTERFACE|PUBLIC|PRIVATE> [item ...]
    [<INTERFACE|PUBLIC|PRIVATE> [item ...] ...]
)
```

target必须是使用add_executable()或add_library()命令创建的，而不能是一个目标别名。

指定的目录一般是追加的方式进行添加，但如果指定了BEFORE，后面指定的目录将添加在原有目录的前面。

INTERFACE、PUBLIC、PRIVATE指定了后面参数的范围：

- PRIVATE、PUBLIC的项目将会在目标的LINK_DIRECTORIES属性
- PUBLIC、INTERFACE的项目将会在目标的INTERFACE_LINK_DIRECTORIES属性

> 在有其他选择的情况下，不要使用此命令。例如：
>
> - 使用库的绝对路径来准确的指定库
> - 使用find_library()命令，来获取库的绝对路径

## 示例

```cmake
#使用add_executable()创建一个目标
add_executable(test "a.c" "b.c")
#将相对目录../my_math加入到目标的链接目录列表中
target_link_directories(test PUBLIC "../my_math")
#将绝对路径/usr/local/ffmpeg/lib追加到目标的链接目录列表中
target_link_directories(test PUBLIC "/usr/local/ffmpeg/lib")
#将绝对路径/usr/local/boost/lib加到目标的链接目录列表的开头
target_link_directories(test BRFORE PUBLIC "/usr/local/boost/lib")
```

