animation
====================

Prefer to use css animation  on mobile devices as 
it is more energy efficient than js timers.

- setInterval
- setTimeout
- requestAnimationFrame
- 

The animation created by :code:`requestAnimationFrame`
will not refresh if the animation is not visible on 
the page, or the browser tab is not current tab, or 
the browser is minimized.
It will only execute when the browser need to update
its screen, so it will perfectly fit the refresh rate of 
the browser.

As for the timer function, :code:`setInterval`, if 
the interval is set too short to create a smooth animation
effect, it will 

**note**

Prefer to change the :code:`transform` property of an 
element than the :code:`left/top/right/bottom` properties.

