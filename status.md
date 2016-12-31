# &lt;Status&gt;

Status badge

## Attributes

* **`iconName:`** Required. String representing the name of an icon from [font awesome icon library](https://fontawesome.io/icons/)

* **`color:`** Required. String representing the hexadecimal RGB color for an icon. Default \#000000

* **`label:`** Required. String representing the text inside a badge

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
