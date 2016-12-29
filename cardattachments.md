# &lt;CardAttachments&gt;

A list of attachments inside a Card

## Attributes

**attachments** Array&lt;Object&gt; \(default: []\)

Button text

## Examples

JSX
```js
const attachments = [{
  img: 'https://avatars1.githubusercontent.com/u/3182655?v=3&s=460',
  text: 'EOdOW',
}]
<Card>
  <CardAttachments attachments={attachments}/>
</Card>
```

JSON
```js
const attachments = [{
  img: 'https://avatars1.githubusercontent.com/u/3182655?v=3&s=460',
  text: 'EOdOW',
}]

{
  "elementName": "Card",
  "children": [
    {
      "elementName": "CardAttachments",
      "attributes": {
        "attachments": attachments,
      }
    }
  ]
}
```
