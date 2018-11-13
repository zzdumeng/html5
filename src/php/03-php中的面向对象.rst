面向对象
*****************

php支持常见的面向对象概念, 

- 修饰符 ``public``, ``protected``, ``private``, ``static``, ``const``, ``final``
- 构造函数 ``__construct`` 和 析构函数 ``__destruct``
- 使用 ``parent`` 来调用父类的方法
- 不支持方法重载overload
- 不支持多重继承, 一个类只能有一个父类

.. note:: 

  不要显示的调用析构函数 ``$var->__destruct``, 使用 ``unset($var)`` 来减少对象的引用,
  让php来进行自动的GC.
