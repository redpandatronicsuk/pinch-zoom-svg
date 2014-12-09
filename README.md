pinch-zoom-svg
==============

Angular directive to enable pinch zooming on SVG elements, which uses proper viewport zooming, to keep SVGs looking sharp!

it is based on this gist: <a href="https://gist.github.com/ktknest/5276f368c92bc1ce4dda">https://gist.github.com/ktknest/5276f368c92bc1ce4dda</a>, but rather than mofifying the elements CSS transform properties, it operates on the SVGs viewport to achive smooth zooming.

For example, this demo shows that when using the pinch-zoom from the above mentioned gist, it does not zoom smoothly on SVGs (multi-touch screen required to work):
<p data-height="147" data-theme-id="0" data-slug-hash="JoGeZq" data-default-tab="result" data-user="dobe" class='codepen'>See the Pen <a href='http://codepen.io/dobe/pen/JoGeZq/'>JoGeZq</a> by Dominik Beste (<a href='http://codepen.io/dobe'>@dobe</a>) on <a href='http://codepen.io'>CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>
