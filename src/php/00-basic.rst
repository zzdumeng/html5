php-00-basic
*************

``echo`` and ``print``

echo and print are **not** really function, 
they are language struct.
No need to use bracket  


data types
=====================


string
--------------

创建字符串， 使用单引号 ``'`` 和双引号 ``"`` 都可以，
双引号会

还可以使用

array 数组
-----------------

数组其实是一个有序map, 由键值对组成。

- 索引数组 IndexedArray
- 关联数组 

如果没有指定键名，那么将使用已经使用过的数字索引的最大值+1

.. code-block:: php

  $arr = array(2, 3, "fox");
  $arr2 = array("key" => "value", 10);
  $arr3 = ["a" => 32, 7 => 8, 9] // 使用 $arr3[8]来获取9



basic operation
=======================

To check the type of a variable, use ``is_[type]`` function

.. code-block:: php

    $a = 'sttring';
    is_string($a);


super global variables
============================

