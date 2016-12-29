# &lt;CardAttachments&gt;

A list of attachments inside a Card

## Attributes

**attachments** Array&lt;Object&gt; \(default: []\)

Button text

## Examples

```js
const attachments = [{
  img: 'https://archy.ai/images/logos/logo-github@2x.png',
  text: 'github',
}]

<Card>
  <CardAttachments attachments={attachments}/>
</Card>
```
