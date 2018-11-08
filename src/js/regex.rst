regex
***********

正则表达式

创建方式

语义表达式
	使用 :code:`/pattern/`来创建一个正则表达式

使用new创建一个正则对象
.. code-block:: js
	
	var re = new RegExp('\\w+', 'i')

两者的区别：

- 语义表达式语句被执行的时候，将被编译而成为一个常量。
- 使用``new``创建的是运行时对象，用于不确定的正则表达式，例如
  其pattern来自于用户的输入
- 对于需要转义的特殊字符，语义表达式只需用*\*进行转义，
  而使用RegExp对象则需要进行双重转义



元字符
=========


Quantifiers 量词
================

quantifier  meaning
{m}  only appear m times
{m,n}  appear at least m times and at most n times



Assertions 断言
================

+-----+-----+-----+
| x(?=y) | 只匹配以y结尾的x |
+-----+-----+-----+
| x(?!=y) | 不匹配以y结尾的x |
+-----+-----+-----+


常用的正则表达式
================

汉字
--------

.. code-block:: js

   var re = /\u4e00-\u9fa5/

邮箱
----------


notes
=========

需要转义的字符
--------

.. code-block:: js

  . \ + * ? [ ^ ] $ ( ) { } = ! < > | : -

