# &lt;CardHeader&gt;

A header inside a Card

![](/assets/CardHeader.png)

## Attributes

* **`title:`** Required. String representing the title for a card, empty string by default.

* **`subtitle:`** Required. String representing the subtitle for a card, empty string by default.

* **`created:`** Required. Object containing information about who and when created this entity
  * **`by:`** Required. String representing owner of the entity.
  * **`when:`** Required. Timestamp in millisecond representing when entity was created.

## Examples

JSX
```js
const created = {
  by: 'Admin',
  when: 1483044914860,
}

<Card>
  <CardHeader created={created} title="Card title" subtitle="Card subtitle" />
</Card>
```

JSON
```js

const created = {
  by: 'Admin',
  when: 1483044914860,
}

{
  "elementName": "Card",
  "children": [
    {
      "elementName": "CardHeader",
      "attributes": {
        "title": "Card title",
        "subtitle": "Card subtitle",
        "created": created,
      }
    }
  ]
}
```
