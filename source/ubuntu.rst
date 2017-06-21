=================
Ubuntu 源使用帮助
=================

地址
====

https://mirror.nyist.edu.cn/ubuntu/

说明
====

Ubuntu 软件源

收录架构
========

AMD64 (x86_64), Intel x86

收录版本
========

所有 Ubuntu 当前支持的版本，包括开发版，具体版本见 https://wiki.ubuntu.com/Releases

对于 Ubuntu 不再支持的版本，请参考 :doc:`ubuntu-old-releases`

使用说明
========


手动更改配置文件
----------------

.. warning::
    操作前请做好相应备份

一般情况下，将 :file:`/etc/apt/sources.list` 文件中 Ubuntu 默认的源地址 ``http://archive.ubuntu.com/``
替换为 ``http://mirror.nyist.edu.cn`` 即可。

可以使用如下命令：

::

  sudo sed -i 's/archive.ubuntu.com/mirror.nyist.edu.cn/g' /etc/apt/sources.list

当然也可以直接编辑 :file:`/etc/apt/sources.list` 文件（需要使用 sudo）。以下是 Ubuntu 16.04 参考配置内容：

::

    # 默认注释了源码仓库，如有需要可自行取消注释
    deb https://mirror.nyist.edu.cn/ubuntu/ xenial main restricted universe multiverse
    # deb-src https://mirror.nyist.edu.cn/ubuntu/ xenial main restricted universe multiverse
    deb https://mirror.nyist.edu.cn/ubuntu/ xenial-updates main restricted universe multiverse
    # deb-src https://mirror.nyist.edu.cn/ubuntu/ xenial-updates main restricted universe multiverse
    deb https://mirror.nyist.edu.cn/ubuntu/ xenial-backports main restricted universe multiverse
    # deb-src https://mirror.nyist.edu.cn/ubuntu/ xenial-backports main restricted universe multiverse
    deb https://mirror.nyist.edu.cn/ubuntu/ xenial-security main restricted universe multiverse
    # deb-src https://mirror.nyist.edu.cn/ubuntu/ xenial-security main restricted universe multiverse

    # 预发布软件源，不建议启用
    # deb https://mirror.nyist.edu.cn/ubuntu/ xenial-proposed main restricted universe multiverse
    # deb-src https://mirror.nyist.edu.cn/ubuntu/ xenial-proposed main restricted universe multiverse

更改完 :file:`sources.list` 文件后请运行 ``sudo apt-get update`` 更新索引以生效。

.. tip::
    使用 HTTPS 可以有效避免国内运营商的缓存劫持。


镜像下载
--------

如果需要下载 Ubuntu 的 ISO 镜像以便安装，请参考 :doc:`ubuntu-releases`

相关链接
========

:官方主页: https://www.ubuntu.com/
:文档: https://help.ubuntu.com/
:Wiki: https://wiki.ubuntu.com/
:邮件列表: https://community.ubuntu.com/contribute/support/mailinglists/
:提问: https://askubuntu.com/
:论坛: https://ubuntuforums.org/
:中文论坛: https://forum.ubuntu.org.cn/
