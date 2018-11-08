BrowserObjectModel(BOM)
************************

常用的window对象的属性：

console
	控制台对象

alert
	弹出对话框

confirm
	确认对话框

prompt


atob
	将base64编码过的字符串解码

btoa
	将字符串进行base64编码方案编码

localStorage

sessionStorage
	

geography related

innerHeight， innerWidth
	不包括书签栏，工具栏等的浏览器显示区域大小


location
=============

`Location` 接口定义了这些属性和方法

.. js:attribute:: location.href
	
	网址

.. js:attribute:: location.host
	
	主机名，包括端口


**methods**

.. js:method:: location.assign(url)
	
	:param string url: An url to direct to.

.. js:method:: location.replace(url)

	almost the same as :js:meth:`location.assign`, but
	does not save current url in browser history, so can not be restored by push *back* button.


	


navigator
==========
	
窗口操作
=============

窗口的创建
--------------

.. js:function:: window.open(url, windowName，windowFeature)


关闭窗口
---------

.. js:function:: win.close()

关闭窗口对象
只能关闭由js代码创建的窗口









