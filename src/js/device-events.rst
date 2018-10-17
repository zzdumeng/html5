device events
==================

- DeviceLightEvent
- DeviceOrientationEvent
- DeviceMotionEvent

shake detect
****************

Use the :code:`DeviceMotionEvent`.

If the device is in motion, and the two records
differ each other in a rather big value, we can 
think the user is shaking the device.


orientation detect
********************

Add event listener of :code:`orientationchange`


