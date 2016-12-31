# &lt;CardCharts&gt;

Component which can display line, histogram, bar and donut charts.

## Attributes

* **`unit:`** Required. String representing the units of the chart.

* **`type:`** Required. String representing chart type. One of the following: lineChart, histogramChart, barChart, donutChart

* **`fullWidth:`** Optional. Boolean which converts a Card into the full width representation mode. False by default.

* **`data:`** Required. Array of data sets for the graph.

  Chart data for type 'lineChart' and 'histogramChart':

  * **`points:`** Required. Array of objects representing a single set of data points on the graph. Each object contains `x` (timestamp in ms) and `y` coordinates of a single point in a data set.

  * **`start:`** Required. Number representing start timestamp in milliseconds for the data set

  * **`end:`** Required. Number representing start timestamp in milliseconds for the data set

  * **`interval:`** Required. Number representing the distance between `x` points

  * **`name:`** Required. String representing the name for a single set of data points on the graph

  * **`color:`** Optional. String representing the hexadecimal RGB color for the data points representation. Automatically generated if not provided.

  Chart data for type 'barChart' and 'donutChart':

  * **`name:`** Required. String representing the name for a single set of data points on the graph

  * **`value:`** Required. Number representing the value for a single set of data points on the graph

  * **`color:`** Optional. String representing the hexadecimal RGB color for the data points representation. Automatically generated if not provided.

## Examples

JSX

```js
const data1 = [{
  points [{
    x: 1483044906860,
    y: 10,
  },{
    x: 1483044914860,
    y: 20,
  },{
    x: 1483044922860,
    y: 10,
  }],
  interval: 1,
  end: 2,
  start: 1,
  name: 'Line 1',
  color: 'dodgerblue',
}]

const data2 = [{
  name: 'Group 1',
  value: 1,
},{
  name: 'Group 2',
  value: 20,
},{
  name: 'Group 3',
  value: 70,
},{
  name: 'Group 4',
  value: 9,
}]

<Card>
  <CardCharts data={data1} unit="%" type="lineChart"/>
  <CardCharts data={data1} unit="%" type="histogramChart"/>
  <CardCharts data={data2} unit="%" type="barChart"/>
  <CardCharts data={data2} unit="%" type="donutChart"/>
</Card>
```


JSON
```js
const data1 = [{
  points [{
    x: 1483044906860,
    y: 10,
  },{
    x: 1483044914860,
    y: 20,
  },{
    x: 1483044922860,
    y: 10,
  }],
  interval: 1,
  end: 2,
  start: 1,
  name: 'Line 1',
  color: 'dodgerblue',
}]

const data2 = [{
  name: 'Group 1',
  value: 1,
},{
  name: 'Group 2',
  value: 20,
},{
  name: 'Group 3',
  value: 70,
},{
  name: 'Group 4',
  value: 9,
}]

{
  "elementName": "Card",
  "children": [
    {
      "elementName": "CardCharts",
      "attributes": {
        "data": data1,
        "unit": "%",
        "type": "lineChart",
      },
    },{
      "elementName": "CardCharts",
      "attributes": {
        "data": data1,
        "unit": "%",
        "type": "histogramChart",
      },
    },{
      "elementName": "CardCharts",
      "attributes": {
        "data": data2,
        "unit": "%",
        "type": "barChart",
      },
    },{
      "elementName": "CardCharts",
      "attributes": {
        "data": data2,
        "unit": "%",
        "type": "donutChart",
      },
    },
  ]
}
```
