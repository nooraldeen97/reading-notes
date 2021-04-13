**Charts:**Charts are far better for displaying data visually than tables and have the added benefit that no one <br>
is ever going to press-gang them into use as a layout tool.<br>

in order to draw a line chart first we need to create `<canvas>` element in our html page ,the `<canvas>`element <br>
has only two attributes, `width` and `height`, Next, we need to get the context and to instantiate the char for example :<br>

`var countries= document.getElementById("id").getContext("2d");`<br>
`new Chart(id).Pie(pieData, pieOptions);`<br>



You’ll notice that this time, we are going to supply some options to the chart.<br>

Next we need to create the data. This data is a little different to the line chart because the pie chart is <br>
simpler, we just need to supply a value and a color for each section:<br>
the same for pie the same for line and bar chart.<br>

by canvas element you can draw texts , drawing shapes the grid by (x,y) coordinate like drawing rectangle <br>
`clearRect(x, y, width, height)`, Drawing paths , Drawing a triangle , Lines ,Arcs ,Bezier and quadratic curves<br>
, and Path2D objects .