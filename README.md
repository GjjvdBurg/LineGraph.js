# Line graph for d3.js

This is an easy-to-use Javascript class to create a line graph in 
[d3.js](https://d3js.org/) (v5). It has support for zooming the graph and uses 
a mouse-over legend.  See 
[here](https://gertjanvandenburg.com/blog/thompson_sampling/) for an example 
of it being used.

It can be used as follows:

```javascript
var graph = new LineGraph("#selector", "/path/to/data.json");
graph.buildWhenReady(800, 400); // width, height
```

and expects the following JSON data format:

```json
{
  "meta": {
    "xlabel": "",
    "ylabel": "",
    "ymin": 0,
    "ymax": 10,
    "xmin": 0,
    "xmax": 100,
  },
  "data": {
    "X": [1 2, 3, 4, 5],
    "series": [
      {
        "name": "Y_1",
        "values": [0.1, 0.2, 0.3, 0.4, 0.5]
      },
      {
        "name": "Y_2",
        "values": [2, 1, 0, -1, -2]
      }
    ]
  }
}
```

Adding ``xmin, xmax, ymin``, and ``ymax`` is optional. The accompanying 
[graph.scss](/graph.scss) adds the necessary styling.

License: MIT. Created by [Gertjan van den Burg](https://gertjan.dev).
