db/01/mysql
***********

 mysql简介 
=================
TODO





终端客户端常用命令
================

先安装 *mysql-client*

show databases;
  显示所有数据库

show tables;
  显示当前数据库的所有表

describe *table*
  显示 *table* 的表结构

select User from mysql.user
  获取用户列表

  .. note:: 

    内置有 *mysql* 数据库， 存储各种信息

show global variables like 'port'
  获取mysql server所用端口

  .. note:: global variables 存储有全局变量


创建数据库
===============

创建数据库时, 指定 ``character set`` 和 ``collate``.
一般``character set`` 设置为 ``utf-8``, 
``collate`` 设置为 ``utf8_unicode_ci``.

.. code-block:: sql

  CREATE DATABASE tutorial 
    CHARACTER SET utf8 COLLATE utf8_unicode_ci;

:ref:`stackoverflow` https://stackoverflow.com/questions/10929836/utf8-bin-vs-utf-unicode-ci
:ref:`mysql` https://dev.mysql.com/doc/refman/5.7/en/create-database.html

.. note:: ``**_ci`` 表示 *case-insensitive*, ``**_cs`` 表示 *case-sensitive*.


创建表
============
