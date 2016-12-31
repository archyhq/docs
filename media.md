# &lt;Media&gt;

Renders a media object inside a Card

## Attributes

* **`iconName:`** Required. String representing the name of an icon from [font awesome icon library](https://fontawesome.io/icons/)

* **`color:`** Required. String representing the hexadecimal RGB color for an icon. Default \#000000

* **`title:`** Optional. String representing the title for the media object

* **`subtitle:`** Optional. String representing the subtitle for the media object

* **`imageUrl:`** Optional. String representing the image url

### Example

JSX
```js
<Card>
  <Media
    title="Media title"
    subtitle="Media subtitle"
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
      "elementName": "Media",
      "attributes": {
        "title": "Media title",
        "subtitle": "Media subtitle",
        "iconName": "close",
        "color": "#fafafa",
      }
    }
  ]
}
```
