[TOC]

# INTERFACE_LINK_LIBRARIES

库的公共链接库要求列表。

此属性包含传递链接依赖项的列表。

当使用target_link_libraries()命令将目标链接到另一个目标时，列出的库（以及递归其链接接口库）也将提供给另一个目标。