# &lt;Action&gt;

An action inside a Card

## Attributes

* **`label:`** Required. String representing action text.

* **`type:`** Required. String representing button type. Type can be 'primary' otherwise its default

## Examples

JSX
```js
<Card>
  <Action label="close" type="primary" />
</Card>
```

JSON
```js

{
  "elementName": "Card",
  "children": [
    {
      "elementName": "Action",
      "attributes": {
        "label": "close",
        "type": "primary",
      }
    }
  ]
}
```
