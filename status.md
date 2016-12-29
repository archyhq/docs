# &lt;Status&gt;

Status badge

## Attributes

**iconName **\(optional\)** **string

name of an icon from [font awesome icon library](https://fontawesome.io/icons/)

**color** \(optional\) string

Hexadecimal RGB color for an icon. Default \#000000

**label** \(optional\) string

Text inside a badge

### Example

JSX
```js
<Card>
  <Status
    label="Closed"
    iconName="close"
    color="#fafafa"
  />
</Card>
```

JSON
```js

{
  "elementName": "Card",
  "children": [
    {
      "elementName": "Status",
      "attributes": {
        "label": "Closed",
        "iconName": "close",
        "color": "#fafafa",
      }
    }
  ]
}
```
