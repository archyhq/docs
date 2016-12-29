# &lt;CardCharts&gt;

A list of attachments inside a Card

![](/assets/CardCharts.png)

## Attributes

**data** Array<Object>

Chart data for type 'lineChart' and 'histogramChart':

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
**points** Array&lt;{ x: number; y: number }&gt;

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Array of objects representing a single set of data points on the graph. Each object contains x (timestamp in ms) and y coordinates of a single point in a data set.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
**start** number

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Start timestamp in milliseconds for the data set

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
**end** number

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
End timestamp in milliseconds for the data set

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
**interval** number

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Interval between x points

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
**name** string

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Name for a single set of data points on the graph

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
**color** \(optional\) string

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Hexadecimal RGB color for the data points representation. Automatically generated if not provided.

Chart data for type 'barChart' and 'donutChart':

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
**name** string \(default: ''\)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Name for a single set of data points on the graph

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
**value** number \(default: null\)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Value for a single set of data points on the graph

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
**color** \(optional\) string

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Hexadecimal RGB color for the data points representation. Automatically generated if not provided.


**unit** string \(default: ""\)

Chart units

**type** string \(default: ""\)

Chart type, one of the following: lineChart, histogramChart, barChart, donutChart

**fullWidth** boolean \(default: false\)

Converts a Card into the full width representation mode.

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
