# Notes for Read 12 - Chart.js, Canvas

## Chart.js API [Chart.js API](https://www.webdesignerdepot.com/2013/11/easily-create-stunning-animated-charts-with-chart-js/)

To use download [Chart.js](https://github.com/nnnick/Chart.js) and put Chart.min.js into your *working directory*

Place the appropriate tag in your HTML `<script src='Chart.min.js'></script>`

create a canvas element in **HTML** `<canvas id="buyers" width="600" height="400"></canvas>`

example of a *line chart* JS Code for reference:

```var buyers = document.getElementById('buyers').getContext('2d');
    new Chart(buyers).Line(buyerData);
    var buyerData = {
	labels : ["January","February","March","April","May","June"],
	datasets : [
		{
			fillColor : "rgba(172,194,132,0.4)",
			strokeColor : "#ACC26D",
			pointColor : "#fff",
			pointStrokeColor : "#9DB86D",
			data : [203,156,99,251,305,247]
		}
	]
}
```

## Chart.js Docs

[chart.js Documentation](https://www.chartjs.org/docs/latest/)

## Canvas API (API = Application Programming Interface)

[Basics](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Basic_usage)
[Drawing Shapes](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Basic_usage)

Grid is follows Quadrant II |x| and |y|  x = right, y = down.  **0, 0** top-left

the `<canvas>` tag only needs a width and height.  There are defaults.  it DOES need to be closed.
the methods and functions are access in JS

```tx.fillStyle = 'orange';
ctx.fillStyle = '#FFA500';
ctx.fillStyle = 'rgb(255, 165, 0)';
ctx.fillStyle = 'rgba(255, 165, 0, 1)';
```

Can take most color formats.
Many examples of rendering colors and styles:
*stroke* sets the style for shapes' outlines

+ fillStyle
+ strokeStyle
+ globalAlpha
+ lineWidths
+ lineCap
+ lineJoin
+ miterLimit - how far outside the connection point of lines
+ gradients
+ patterns

fill rules:
to determine if a point is inside or outside a path.

Drawing text:

+ fillText
+ strokeText
+ styling Text

[&lt;--&#91;BACK&#93;](README.md)