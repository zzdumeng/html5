文档结构
**********

HTML和XML的区别:

HTML标签可以包含不闭合的标签,例如  :code:`img`, :code:`br`, :code:`hr`


基本结构:

.. code-block:: html

  <DOCTYPE html>
  <html>
    <head>
    <--! head content -->
    </head>
    <body>
    </body>
  </html>

Doctype 文档类型
==================

.. code-block:: html

  <Doctype >

HTML文档中, :code:`doctype` 必须在所有文档的顶部声明.
它的唯一作用是阻止浏览器在渲染文档时切换到 *quirks mode*,
确保浏览器能够遵循相关的规范.

在web的前期, 网页一般写为两种版本: Netscape Navigator 版 和
Microsoft IE版.
W3C标准出来之后, 为了兼容以前的写法, 浏览器引入了两种模式以区分标准
兼容站点和老式传统站点.

现在浏览器中布局引擎有三种模式: *quirks* 模式, *准标准模式*, *全标准
模式*. 
在 *quirks* 模式下, 布局引擎会模拟Navigator4 和 IE5 下的非标准
行为.
在全标准模式下, 布局引擎的行为完全符合HTML和CSS规范描述的行为.
在准标准模式下, 仅有少数的quirks被实现.

.. figure:: _static/html/quirks_mode.png

   *firefox->view page info* to view the render mode.

HTML5 规范推荐使用 :code:`<DOCTYPE html>` 来确保浏览器使用
全标准模式.



html 标签
==========

.. code-block:: html

  <html lang="en">
  </html>

:code:`html` 标签创建文档的根元素.
*lang* 属性为全局属性, 可以给任意节点添加,当添加到根节点时,
浏览器可以根据其值来提供额外的功能, 例如, 翻译插件可以自动翻译.

在设置样式时, 可以通过给:code:`HTML`标签添加类名来改变整个页面的样式.


head 标签
============

包含 :code:`meta`, :code:`title`, 
:code:`link`, :code:`style`, :code:`script`
等标签.

meta
--------

:code:`meta` 可以提供给浏览器一些元信息.
可以用于浏览器如何渲染,以及搜索引擎的信息提取.

常见的元信息:

charset
  编码方式::

  <meta charset="utf-8">

keywords
  网页内容的关键字::

  <meta name="keywords" content="kw1, kw2">

description
  网页简要描述::

  <meta name="description" content="a simple description of the page ">

title
---------

页面的标题, 显示在浏览器的tab栏上.

link
-------

:code:`link` 引入外部资源, i.e. 样式表, icon, 字体, 等等.

**note**

可以通过设置媒体属性来根据情况加载不同的样式表::

  <link href="desktop.css" rel="stylesheet" media="screen and (min-width: 600px)">
  <link href="highres.css" rel="stylesheet" media="screen and (min-resolution: 300dpi)">

style
------

样式表标签.
当有多个 :code:`link` 和 :code:`style` 标签的时候, 样式按照
引入的顺序渲染文档.

:code:`style` 标签同样有 *media* 属性以适应不同的媒体类型::

  <style media="all and (max-width: 500px)">
    p {
      color: blue;
      background-color: yellow;
    }
  </style> 

HTML5 默认类型为 *text/css*.

script
--------

引入脚本.

.. code-block:: html

  <script src="" type="text/javascript"> </script>

HTML5 默认类型为 *text/javascript*.
如果设置 :code:`type="module"`, 则可以直接使用es6的module, 
利用 :code:`export` 和 :code:`import` 来组织代码.

body
=====

**TODO**



