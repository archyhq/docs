# &lt;CardBodyText&gt;

Text component

## Attributes

**text** string

plain text to render

## Example

JSX
```js
<Card>
  <CardHeader title="Text title" subtitle="Text subtitle" />
  <CardBodyText text="Some text for your card" />
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
        "title": "Card title",
        "subtitle": "Card subtitle",
      }
    },{
      "elementName": "CardBodyText",
      "attributes": {
        "text": "Some text for your card",
      }
    }
  ]
}
```
