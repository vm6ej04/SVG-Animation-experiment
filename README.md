SVG-Animation-experiment
========================
Attempts log
-------------------------------------------

3/Nov/2014
------------------------------------------- 
-Tried in-line SVG, trying to animate, noticed the CSS needs vendor prefix to work in Chrome.
 
-Rotate with offset origin(transform-origin), noticed that It doesn't work with FireFox... fix(Using SVG as img or CSS background does the trick). Saw some Stackoverflow article with similar problem? 

http://stackoverflow.com/questions/18938331/transform-origin-for-css-animation-on-svg-working-in-chrome-not-ff

However use SVG as img works for my purpose for now, won't look into it more at this stage.

-Notice that the anti-alias rendering in FireFox isn't that great. Saw some white bits along the viewbox edge. Adjusted the SVG width/height to whole number, didn't help.
