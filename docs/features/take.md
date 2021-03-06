---
layout: default
title: Take
nav_order: 4
has_children: false
parent: Base Features
grand_parent: Features
---

# Take

The `Take` feature defined in the Specification behaves the same as `Take` in Linq, and it accepts an `int count` as a parameter.

`Take` is used to select a certain number of the results in a query, starting from the beginning. For example:

```csharp
int[] numbers = { 1, 3, 2, 5, 7, 4 };

IEnumerable<int> subsetOfNumbers = numbers.Take(3);
```

Here, `subsetOfNumbers` would contain `{ 1, 3, 2 }`.

Alternatively:

```csharp
int[] numbers = { 1, 3, 2, 5, 7, 4 };

IEnumerable<int> subsetOfNumbers = numbers.OrderBy(n => n).Take(3);
```

Here, `subsetOfNumbers` would contain `{ 1, 2, 3 }`.

`Take` is commonly used in combination with [Skip](skip.md) to implement [Paging](paging.md), but as the above demonstrates, `Take` can also be used on its own.
