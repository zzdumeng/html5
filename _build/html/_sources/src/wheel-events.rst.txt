mouse wheel event
==========================


deprecated mouse wheel event
********************************

On Gecko-base browser(firefox), there is a 
**DOMMouseEvent** .
On other browsers, use **mousewheel** event

The **DOMMouseEvent** has a :code:`detail` property,
it's the count of number of scroll lines.

We can encapsulate a function to both support Gecko-based
browser and other browsers.

.. code:: js

  function addWheelListener(ele, fn) {
    function cb(e) {
      var eve = window.event || e
      var dir = eve.wheelDelta ? eve.wheelDelta : e.detail
      fn(dir)
    }
    ele.addWheelListener('mousewheel', cb)
    ele.addWheelListener('DOMMouseScroll', cb)
  }

standard wheel event
**************************
The above two event listener are both not deprecated,
and not in standard track.

The standard event is *wheel* event.
It has three properties:

- deltaX
- deltaY
- deltaZ
- deltaMode


