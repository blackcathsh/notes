[TOC]

# project

设置此工程的名称（版本、描述、主页URL、编程语言等）信息。

```cmake
project(<PROJECT-NAME> [<language-name>...])
project(<PROJECT-NAME>
    [VERSION <major>[.<minor>[.<patch>[.<tweak>]]]]
    [DESCRIPTION <project-description-string>]
    [HOMEPAGE_URL <url-string>]
    [LANGUAGES <language-name>...]
)
```

每次使用此命令设置工程的名字时，将会设置以下变量的值：

- PROJECT_NAME
- PROJECT_SOURCE_DIR，\<PROJECT-NAME\>_SOURCE_DIR
- PROJECT_BINARY_DIR，\<PROJECT-NAME\>_BINARY_DIR

如果是在顶层CMakeLists.txt文件里调用此命令，还会设置以下变量的值：

- CMAKE_PROJECT_NAME

project命令支持四个可选的选项，不同的选项会有不同的影响。

## 选项

### VERSION

使用此选项设置工程的版本，同时设置以下变量的值：

- PROJECT_VERSION，\<PROJECT-NAME\>_VERSION
- PROJECT_VERSION_MAJOR，\<PROJECT-NAME\>_VERSION_MAJOR
- PROJECT_VERSION_MINOR，\<PROJECT-NAME\>_VERSION_MONIR
- PROJECT_VERSION_PATCH，\<PROJECT-NAME\>_VERSION_PATCH
- PROJECT_VERSION_TWEAK，\<PROJECT-NAME\>_VERSION_TWEAK

如果在顶层CMakeLists.txt中调用此命令，还会设置以下变量的值：

- CMAKE_PROJECT_VERSION

> 想要使用VERSION选项，需要保证策略CMP0048为NEW。在3.10版本前需手动设置，3.10后无需手动设置策略CMP0048

### DESCRIPTION

### HOMEPAGE_URL

### LANGUAGES

# 用法

在顶层CMakeLists.txt中的开头（但要在cmake_minimum_required命令后面）必须直接调用此命令。

## 示例

```cmake
# 指定工程名为HelloWorld
project(HelloWorld)
```

```cmake
# 指定工程名为HelloWorld，版本为1.0.0
# 指定cmake的最小版本为3.10
cmake_minimum_required(3.10)
project(HelloWorld VERSION 3.10)
```

