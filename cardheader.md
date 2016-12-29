# &lt;CardHeader&gt;

A header inside a Card

![](/assets/CardHeader.png)

## Attributes

**title **string \(default: ""\)

A title for a card.

**subtitle** string \(default: ""\)

A subtitle for a card

**created** Object \(default: {}\)

Information about who and when created this entity

## Examples

```js
const created = {
  by: 'Admin',
  when: 1483044914860,
}

<Card>
  <CardHeader created={created} title="Card title" subtitle="Card subtitle" />
</Card>
```
