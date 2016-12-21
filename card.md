# Card



Card is the cornerstone of the current Archy Views version.

![](/assets/CardDemo.png)

## Attributes

**linkTo **object\|string \(default: undefined\)

A link to an Archy address or external Web URI. When defined, Archy will redirect user to the specified link when user touches/clicks on the Card.

_Example_:

```js
// link to an archy address
const link = {
  address: "@developer/namespace/command",
  args: {
    id: item.id,
  },
}

<Card linkTo={link}>...</Card>

// or an URI to external web resource
const uri = "https://github.com/archyhq/archy"

<Card linkTo={uri}>...</Card>
```

**timestamp **string \(default: undefined\)

A timestamp in UTC format, telling Archy when the content of the Card was updated last time. This information is used in Notification System

**fullWidth** boolean \(default: false\)

Converts a Card into the full width representation mode.

## Examples

```js
<Card
  linkTo={item.url}
  fullWidth={true}
  timestamp={item.updatedAt}>
    <CardHeader title={item.title} />
</Card>
```



