data persistence
********************


pre note 
============

commucation model **C/S**

The **Client/Server** model is that the data is not 
saved on the 


And in the web world, the **C/S** became the **B/S** 
(Browser/Server), as the browser acts as the *client*.





cookie
==========

cookie de 问题

- cookie的内容随request每次发送到服务器，将增加payload的大小
- cookie的容量较小，约为4kb，不能存储较大的对象
- 存储为字符串，不易操作


query cookie
---------------

.. code-block:: js

  document.cookie
  // it's a string

add cookie
------------

If the browser quit, then cookie will be removed if
not set the *expires* or *max-age*

.. code-block:: js

  document.cookie = 'name=username'
  var d = new Date()
  d.setDate(d.getDate() + 3)
  document.cookie = 'remain=true; expires=' + d.getUTCString()

If a cookie kv pair has set both *expires* and *max-age*,
then its lifetime will be decided by *max-age*.

set cookie
-------------

If the key already exists in the cookie, then
it will be override if set again.



remove cookie
---------------

Set the cookie item to null, and set the *expires* to 
a passed time, or set *max-age* to a negative value.

.. code-block:: js

  document.cookie = 'remain=; max-age=-1'




Security issue
--------------------

Cookie in other domain can be accessed by insert an 
iframe in a page and use :code:`iframe.contentDocument.cookie`
This method can only get non http cookie.
If a cookie item is ``http-only``, then it can not accessed
by this method.

And if the source site set the privacy policy `frame-ancestors 'none'`,
the frame will not be displayed in other domain.





localStorage
====================




sessionStorage
====================

The life cycle of a session is the same as 
the browser page.
If the page is closed, the data will be cleared.

The *sessionCookie*, i.e, cookie item not set of 
*expires* or *max-age*, will be cleared after the browser
closed.

Cookie 的一个会话指的是整个浏览器的持续时间，而 sessionStorage
的会话指的是一个页面（浏览器的一个tab）的生存周期。

一个页面对话在浏览器页面打开时会持续存在，而且当页面刷新以及
页面恢复（浏览器的后退和前进按钮， 或者通过historyAPI）
sessionStorage 的数据可以在浏览器页面的

usage scenario
--------------------

- 在一个页面会话的持续期间，在不同的跳转页面之间传递数据

**conclusion**

LocalStorage 和 SessionStorage 都是一个Storage对象，它们的不同就是生存周期不同，
一般容量大小为5MB。

规范中可以存储多种数据类型，但是目前的浏览器实现中仍然存储为字符串，
可以使用:code:`JSON.parse` 来解析为js对象。



