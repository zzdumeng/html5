mysql
***********

 mysql简介 
=================






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

