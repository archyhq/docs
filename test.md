



# Archy Brain: Results schema

The schema defines the following properties:

## `Separator` (Separator)

## `Media` (Media)

## `Counter` (Counter)

## `CardHeader` (CardHeader)

## `CardFooter` (CardFooter)

## `Card` (Card)

---

# Sub Schemas

The schema defines the following additional types:

## `uri` (string)

## `updatedAt` (undefined)

## `title` (boolean,integer,null,number,string)

## `timestamp` (undefined)

## `subtitle` (boolean,integer,null,number,string)

## `result` (array)

## `linkTo` (undefined)

## `labels` (array)

## `imageUrl` (string)

## `id` (boolean,integer,null,number,string)

## `footnote` (boolean,integer,null,number,string)

## `createdAt` (undefined)

## `counter` (boolean,integer,null,number,string)

## `component` (undefined)

This property must be one of the following types:

* `Card`
* `CardFooter`
* `CardHeader`
* `Counter`
* `Media`
* `Separator`

## `Separator` (object)

Properties of the `Separator` object:

### `elementName` (, enum, required)

This element must be one of the following enum values:

* `Separator`

### `children` (null, required)

### `attributes` (object, required)

Properties of the `attributes` object:

## `Media` (object)

Properties of the `Media` object:

### `elementName` (, enum, required)

This element must be one of the following enum values:

* `Media`

### `children` (null, required)

### `attributes` (object, required)

Properties of the `attributes` object:

#### `title` (title)

#### `imageUrl` (imageUrl)

## `Counter` (object)

Properties of the `Counter` object:

### `elementName` (, enum, required)

This element must be one of the following enum values:

* `CardCounter`

### `children` (null, required)

### `attributes` (object, required)

Properties of the `attributes` object:

#### `counter` (counter)

## `CardHeader` (object)

Properties of the `CardHeader` object:

### `elementName` (, enum, required)

This element must be one of the following enum values:

* `CardHeader`

### `children` (null, required)

### `attributes` (object, required)

Properties of the `attributes` object:

#### `title` (title)

#### `subtitle` (subtitle)

## `CardFooter` (object)

Properties of the `CardFooter` object:

### `elementName` (, enum, required)

This element must be one of the following enum values:

* `CardFooter`

### `children` (null, required)

### `attributes` (object, required)

Properties of the `attributes` object:

#### `labels` (labels)

#### `footnote` (footnote)

## `Card` (object)

Properties of the `Card` object:

### `elementName` (, enum, required)

This element must be one of the following enum values:

* `Card`

### `children` (array, required)

The elements of the array must match *at least one* of the following properties:

### (Separator)

### `attributes` (object, required)

Properties of the `attributes` object:

#### `uri` (uri)

#### `updatedAt` (updatedAt)

#### `timestamp` (timestamp)

#### `linkTo` (linkTo)

#### `id` (id)

#### `createdAt` (createdAt)
