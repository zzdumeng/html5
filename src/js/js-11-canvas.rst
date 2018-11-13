js/11/canvas
**************

canvas 能做什么?

- 基本图形
- 文本, 图像, 视频

浏览器支持: IE9+, 现代浏览器

canvas 本身只有两个属性, ``width`` 和 ``height``, 
默认大小是300X150.
canvas可以通过css来设置样式, 但是如果css样式设置的宽高比和
它的属性设置的宽高比不同, 那么将会放缩以适应布局, 造成内容失真.

canvas作为HTML5添加的新标签, 和 *audio*, *video*, *picture* 等
标签一样是双标签, 作为替换元素, 支持的浏览器将忽略其中的内容,
只根据标签属性而创建要展示的对象. 不支持的浏览器就只展示其中的内容.

Basic Usage 基本使用
======================

.. code-block:: js

  var canvas = document.getElementId('canvas')
  var ctx = canvas.getContext('2d')


basic shape 基本图形
---------------------


对象样式
----------

一般
  - fillStyle
  - strokeStyle

线
  - lineWidth
  - lineCap
  - lineJoin

文本
  - font
  - textAlign
  - textBaseline
  - direction

阴影
  - shadowBlur
  - shadowColor
  - shadowOffsetX
  - shadowOffsetY

.. note:: 

  当使用 ``lineCap`` 的时候, 注意在 *stroke()* 之前不能使用 *closePath()*,
  否则就没有效果.
  因为 *closePath()* 将从当前点和起始点用一条直线连接起来, 实际上多了一条线

  .. code-block:: js

    ctx.lineCap = 'round'
    ctx.beginPath()
    ctx.moveTo(20,20)
    ctx.lineTo(200,200)
    // ctx.closePath()  // 如果调用closePath, 那么线仍然是方的 
    // ctx.lineJoin = 'round' // 设置lineJoin, 可以解决这个问题
    ctx.stroke()


canvas 图像和视频处理
====================

使用 ``context.drawImage`` 和 ``context.getImageData``, 
可以获取图像数据, 进而对图像进行处理.
``drawImage`` 方法也支持视频.

.. code-block:: js

  var image = new Image()
  image.onload = function() {

  }
  image.src = 'some.png'

  // video
  var video = document.createElement('video')
  video.addEventListener('canplay', function() {

  })
  video.src = 'some.mp4'

``context.getImageData`` 方法返回一个 ``ImageData`` 对象,


canvas 动画
==============