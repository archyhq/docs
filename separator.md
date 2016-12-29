# &lt;Separator&gt;

An separator between components inside a Card

## Examples

JSX
```js
<Card>
  <CardHeader title="Header" />
  <Separator/>
  <Media title="Media" iconName="close"/>
</Card>
```

JSON
```js

{
  "elementName": "Card",
  "children": [
    {
      "elementName": "CardHeader",
      "attributes": {
        "title": "Header",
      },
    }, {
      "elementName": "Separator",
    }, {
      "elementName": "Media",
      "attributes": {
        "title": "Media",
        "iconName": "close",
      }
    }
  ]
}
```
