[TOC]

# add_subdirectory

将子目录添加到构建中。

```cmake
add_subdirectory(source_dir [binary_dir] [EXCLUDE_FROM_ALL])
```

source_dir指定了子CMakeLists.txt和源代码文件的路径。

## 示例

```cmake
# 将子目录CMakeProject1添加到构建中
add_subdirectory("CMakeProject1")
```

