# &lt;CardImage&gt;

Image inside a Card

## Attributes

**uri** string \(default: undefined\)

A URI of an image to show inside a Card

**width** number \(default: undefined\)

Width of an image.

**height** number \(default: undefined\)

Height of an image.

## Examples

```js
<Card>
  <CardImage
    uri="https://archy.ai/images/demos/001@2x.png"
    width={300}
    height={300} />
</Card>
```

JSON
```js
{
  "elementName": "Card",
  "children": [
    {
      "elementName": "CardImage",
      "attributes": {
        "uri": "https://archy.ai/images/demos/001@2x.png",
        "width": 300,
        "height": 300,
      }
    }
  ]
}
```
