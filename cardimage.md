# &lt;CardImage&gt;

Image inside a Card

## Attributes

* **`uri:`** Required. String representing image uri.
* **`width:`** Required. Number representing width of the image
* **`height:`** Required. Number representing height of the image

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
