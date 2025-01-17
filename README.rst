SQLAlchemy
==========

|PyPI| |Python| |Downloads|

.. |PyPI| image:: https://img.shields.io/pypi/v/sqlalchemy
    :target: https://pypi.org/project/sqlalchemy
    :alt: PyPI

.. |Python| image:: https://img.shields.io/pypi/pyversions/sqlalchemy
    :target: https://pypi.org/project/sqlalchemy
    :alt: PyPI - Python Version

.. |Downloads| image:: https://img.shields.io/pypi/dm/sqlalchemy
    :target: https://pypi.org/project/sqlalchemy
    :alt: PyPI - Downloads


The Python SQL Toolkit and Object Relational Mapper

Introduction
-------------

本仓库是基于 sqlalchemy commit `fb81f9c <https://github.com/vimiix/sqlalchemy/commit/fb81f9c8d914f9911925dd3f4e77d7fc374b267c>`_
基础上进行修改，主要新增两个特性：

1. 新增 py_opengauss 驱动支持（需安装 ``pip install py-opengauss==1.3.6``）
2. openGauss 数据库支持多主机连接，自动选主库

Usage
-------

这里单独演示 opengauss 数据库多主机连接方式用法：

1. 检查 py-opengauss 是否安装以及版本大于1.3.6 ::

    $ pip list | grep py-opengauss
    py-opengauss  1.3.6


2. 使用 sqlalchemy 创建连接 ::

    from sqlalchemy import create_engine
    # 初始化数据库连接:
    engine = create_engine('postgresql+pyopengauss://user:password@host1:port1,host2:port2/db')

Documentation
-------------

Latest documentation is at:

https://www.sqlalchemy.org/docs/

Installation / Requirements
---------------------------

Full documentation for installation is at
`Installation <https://www.sqlalchemy.org/docs/intro.html#installation>`_.

Getting Help / Development / Bug reporting
------------------------------------------

Please refer to the `SQLAlchemy Community Guide <https://www.sqlalchemy.org/support.html>`_.

Code of Conduct
---------------

Above all, SQLAlchemy places great emphasis on polite, thoughtful, and
constructive communication between users and developers.
Please see our current Code of Conduct at
`Code of Conduct <https://www.sqlalchemy.org/codeofconduct.html>`_.

License
-------

SQLAlchemy is distributed under the `MIT license
<https://www.opensource.org/licenses/mit-license.php>`_.

