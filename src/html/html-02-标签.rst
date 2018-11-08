HTML 标签
************

HTML5 包含145个标签, 可以按照不同的方式来分类.


按照功能分类
============

主根节点
---------

- html

文档元信息
-----------

- link 
- meta 
- style 
- title 

区域根节点
---------

- body

内容分割节点
-------------

- address
- article
- aside
- footer
- header
- h1~h6
- hgroup
- mian
- nav
- section

文本内容
----------

创建块级文本, 描述文档的内容和结构,
对于可用性(Accessibility) 和 SEO 有重要意义.

- blockquote
- dd 
- dir 
- div
- dl 
- dt 
- figcaption
- figure 
- hr 
- li
- main 
- o 
- p
- pre 
- ul 

内联语义化文本
--------------

- a 
- abbr 
- b 
- bdi 
- bdo 
- br 
- cite 
- code 
- data 
- dfn
- em 
- i 
- kbd 
- mark 
- q 
- rb 
- rp 
- rt
- rtc 
- ruby 
- s 
- samp 
- small 
- span 
- strong 
- sub 
- sup 
- time 
- tt 
- u
- var 
- wbr 

TODO:

非替换元素和替换元素
==================

按照元素的替换性, 可以分为非替换元素和替换元素.

替换元素是指标签本身不包含内容(空元素), 它指定的内容由其属性
来决定, 在浏览器渲染的时候被替换.
常见的替换元素包括 :code:`img`, :code:`input`, :code:`hr`, 等.

.. note:: 

  由于替换元素的特性, 无法为其添加 :code:`::before` 和 :code:`::after`
  伪元素, 因为这两者是在标签的内容的前后来添加.

