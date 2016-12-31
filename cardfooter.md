# &lt;CardFooter&gt;

Component to display a footer of a Card. It's similar to a Card header, useful to display a footnote.

## Attributes

* **`footnote:`** Required. String representing the footnote text

* **`labels:`** Required. List of labels

  * **`color:`** Required. String representing text of the label
  * **`name:`** Required. String the label color in Hexadecimal RGB

## Examples

JSX
```js
const labels = [{
  name: 'bug',
  color: 'FF6347',
},{
  name: 'feature',
  color: '1E90FF',
}]

<Card>
  <CardFooter labels={labels} footnote="Foot note"/>
</Card>
```

JSON
```js

const labels = [{
  name: 'bug',
  color: 'FF6347',
},{
  name: 'feature',
  color: '1E90FF',
}]

{
  "elementName": "Card",
  "children": [
    {
      "elementName": "CardFooter",
      "attributes": {
        "labels": labels,
        "footnote": "Foot note",
      }
    }
  ]
}
```
