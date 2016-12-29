# &lt;CardTable&gt;

Component to render a table inside a Card

## Attributes

**rows** Array&lt;{ value: string; key: string }&gt;

Examples:

```js
const rows = [
  {
    key: "Users",
    value: "100",
  }, {
    key: "Admins",
    value: "2",
  },
]

<Card>
  <CardTable rows={rows} />
</Card>
```
