# &lt;CardTable&gt;

Component to render a table inside a Card

## Attributes

* **`rows:`** Required. Array of table rows
  * **`key:`** Required. String representing row key
  * **`value:`** Required. String representing row value

Examples:

JSX
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

JSON
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

{
  "elementName": "Card",
  "children": [
    {
      "elementName": "CardTable",
      "attributes": {
        "rows": rows,
      }
    }
  ]
}
```
