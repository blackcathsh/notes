[TOC]

# target_link_libraries

指定链接目标时需要链接的库或者链接选项。

## 示例

```cmake
#创建一个目标
add_exectable(test "a.c" "b.c")
#指定链接pthread库
target_link_libraries(test pthread)
```

