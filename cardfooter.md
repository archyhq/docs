# &lt;CardFooter&gt;

Component to display a footer of a Card. It's similar to a Card header, useful to display a footnote.

## Attributes

**footnote** string \(default: ""\)

A string to display in a footnote.

**labels** Array&lt;{ color: string; name: string }&gt;

List of labels

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
