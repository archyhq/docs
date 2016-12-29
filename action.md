# &lt;Action&gt;

An action inside a Card

## Attributes

**label** string \(default: ""\)

Button text

**type** string \(default: ""\)

Type can be 'primary' otherwise its default

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
      "elementName": "Card",
      "attributes": {
        "label": "close",
        "type": "primary",
      }
    }
  ]
}
```
