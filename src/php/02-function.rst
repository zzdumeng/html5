php-02-function
*******************

函数都是全局的，可以在函数内部定义函数

.. code-block:: php

  function a() {
    function b(){
    }
  }
  a(); // call a first
  b(); // now we can call b

anoymous function 匿名函数
=========================

可以定义匿名函数赋给变量

在函数内部可以定义匿名函数只供此函数使用。
此时，匿名函数实际上是一个Closure闭包。
所以可以使用 ``use`` 来inherit上下文中的变量
