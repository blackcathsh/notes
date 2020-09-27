[TOC]

# INTERFACE_LINK_DIRECTORIES

库的公共链接目录要求列表。

目标可以填充此属性以发布根据目标的标头编译所需的链接目录。

当使用target_link_libraries()指定目标依赖项时，CMake 将从所有目标依赖项读取此属性，以确定使用者的生成属性。