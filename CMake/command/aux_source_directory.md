[TOC]

# aux_source_directory

在指定的目录中搜索所有的源文件。

```cmake
aux_source_directory(<dir> <variable>)
```

搜索指定目录的所有的源文件，并将结果列表存到指定的变量中。

## 示例

```cmake
# 在当前目录下搜索所有源文件，并将结果列表存到变量SOURCE_FILE_LIST中
aux_source_directory(. SOURCR_FILE_LIST)
```

