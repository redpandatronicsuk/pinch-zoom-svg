pinch-zoom-svg
==============

Angular directive to enable pinch zooming on SVG elements, which uses proper viewport zooming, to keep SVGs looking sharp!

it is based on this gist: <a href="https://gist.github.com/ktknest/5276f368c92bc1ce4dda">https://gist.github.com/ktknest/5276f368c92bc1ce4dda</a>, but rather than mofifying the elements CSS transform properties, it operates on the SVGs viewport to achive smooth zooming.

For example, this demo shows that when using the pinch-zoom from the above mentioned gist, it does not zoom smoothly on SVGs (multi-touch screen required to work):
<p data-height="147" data-theme-id="0" data-slug-hash="JoGeZq" data-default-tab="result" data-user="dobe" class='codepen'>See the Pen <a href='http://codepen.io/dobe/pen/JoGeZq/'>JoGeZq</a></p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

Therefore we have modified the above code to work with SVGs specifically, to enable smooth pinch-zooming and we also modified the code to center the zoom to the point between the two fingers you are pinching with. The results can be seen here:
<p data-height="268" data-theme-id="0" data-slug-hash="wBMRWy" data-default-tab="result" data-user="dobe" class='codepen'>See the Pen <a href='http://codepen.io/dobe/pen/wBMRWy/'>wBMRWy</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

**Things to note:**
1.  Rather than having the SVG included as an <img>, we embeded as a SVG. I think it should also be possible though to use <embed> or <object>, I'll try out later...
2.  Everytinh within the <svg> tag is nested in a <g> tag with id="viewport". We need to have this so we can do the proper SVG zooming, without loosing sharpness.
3.  This is manily for demonstration purposes, when I get around to, I'll write something in d3, that loads any given SVG, inserts the <g id="viewport"> thing and attaches the pinh and drag listeners.
