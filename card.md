# &lt;Card&gt;

Card is the cornerstone of the current Archy Views version.

![](/assets/CardDemo.png)

## Attributes

**linkTo **object\|string \(default: undefined\)

A link to an Archy address or external Web URI. When defined, Archy will redirect user to the specified link when user touches/clicks on the Card.

_Example_:

JSX
```js
// link to an archy address
const link = {
  address: "@developer/namespace/command",
  args: {
    id: item.id,
  },
}

<Card linkTo={link}>...</Card>
```

JSON
```js
// or an URI to external web resource
const link = "https://github.com/archyhq/archy"

{
  "elementName": "Card",
  "attributes": {
    "linkTo": link
  }
}
```

**timestamp** string \(default: undefined\)

A timestamp in UTC format, telling Archy when the content of the Card was updated last time. This information is used in Notification System

**fullWidth** boolean \(default: false\)

Converts a Card into the full width representation mode.

**children** array
Possible children components:

[Action](action.md), [CardHeader](cardheader.md), [CardBodyText](cardbodytext.md), [CardFooter](cardfooter.md), [CardAttachments](cardattachments.md),[CardTable](cardtable.md), [CardImage](cardimage.md), [CardChart](cardchart.md), [CardCounter](cardcounter.md), [Status](status.md), [Media](media.md), [Separator](separator.md)


## Examples

JSX

```js
<Card
  linkTo={item.url}
  fullWidth={true}
  timestamp={item.updatedAt}>
    <CardHeader title={item.title} />
</Card>
```

JSON

```js
{
  "elementName": "Card",
  "attributes": {
    "linkTo": item.url,
    "fullWidth": true,
    "timestamp": item.updatedAt
  },
  "children": [
    {
      "elementName": "Card",
      "attributes": {
        "title": item.title
      }
    }
  ]
}
```
