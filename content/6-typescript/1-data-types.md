---
title: 'Data types'
metaTitle: 'Typescript data types'
metaDescription: 'Typescript data types'
---

## Basic types

- string
- number
- boolean
- any
- array
- tuple
- object

```
// string
let id: string = "userId"

// number
let integer: number = 125

// boolean
let isPublish: boolean = true

// any
let x: any = "anything"

// array
let arrayofNumbers: number[] = [1, 2, 3, 4]

// tuple
let person: [number, string, boolean] = [1, "Brad", true]

// tuple array (array of tuples)
let employee: [number, string][] = [[1, "John"], [2, "Gil"]]

// object
let user: { id: number, name: string } = { id: 125, name: "John"}

```

## Union type

Unions are used to indicate to the compiler that the type can be of either type.
Here, pid can be either a `string` or a `number`.

```
let pid: string | number;
pid = "1321";
pid = 321;
```

## Enums

Enums are used to indicate to restrict the possible values of a given type.
The enum values default to numeric values starting with 0, but can be changed like below.

```
enum Direction {
	Up = "Up",
	Down = "Down",
	Left = "Left",
	Right = "Right",
}
```

They can the be accessed like this:

```
console.log(Direction.Up) // "Up"
```

## Type alias

Type aliasing is the creation of your own types, for example:

```
type User = {
	id: number,
	name: string
}
```

## Type Assertion

Type assertion is explicitly telling the compiler that we want to treat an entity as a specific type.

There are 2 syntaxes that we can use to assert a type.

```
let cid: any = 1;
let customerId = <number> cid; // 1st syntax
let alsoCusomterId = cid as number; // 2nd syntax
```

## Functions

You can specify which type a function's parameter and return value are:

```
function add(x: number, y: number): number {
	return x + y;
}
// You can also return nothing
function log(message: string | number): void {
	console.log(message);
}
```

Finish: https://www.youtube.com/watch?v=BCg4U1FzODs&t=2576s

## Difference between a Interface and Type

## Generics
