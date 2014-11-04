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

-------------------------------------------

4/Nov/2014
-------------------------------------------
-Realised if I use SVG as background image, if I group them together with div, I can't really scale the whole thing together.

-another attempt with the solution found yesterday. Figured it out eventually. How it works is this. 
1.Translate the initial path so the desire pivot point is at the 0,0 coordinate.
2.Group the initial path, apply animation to this "g" tag
3.Group again, and apply the absolute position of this group.

Basically

<g (offset)>
	<g (animation)>
		<g (align pivot point)>
		</g>
	</g>
</g>

-Came across the "z-index" layering problem. Apparently Z-index has no effects on inline SVG. Whichever lines of code comes first, it stays at the bottom layer.

-Call it a day, done basic rotation animation and blinking. Planning to create rotating head, crinkle nose, subtle breathing