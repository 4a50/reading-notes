# Notes for Read 09 - Refactoring

[Functional Programming Concepts](https://medium.com/the-renaissance-developer/concepts-of-functional-programming-in-javascript-6bc84220d2aa)
[Refactoring Javascript](https://dev.to/healeycodes/refactoring-javascript-for-performance-and-readability-with-examples-1hec)

## Pure Functions

### It returns the same result if given the same arguments (it is also referred as deterministic)


Not pure:

```let PI = 3.14;

const calculateArea = (radius) => radius * radius * PI;

calculateArea(10); // returns 314.0
```

It is *not pure* because it uses a global variable and is not self contained

### It does not cause any observable side effects

```let counter = 1;

function increaseCounter(value) {
  counter = value + 1;
}

increaseCounter(counter);
console.log(counter); // 2
```

It is *not pure* because it uses a *global* variable, so changing it would affect other parts of the program that would use it.

***Immutability*** is the way to go.

Don't iterate using the standard **for..loop**, use *Map*, *filter* or *reduce*

### pure functions + immutable data = referential transparency

### Refactoring for Readability

**hash function** used to map a given key to a location in the hash table

**Break up** large functions

[&lt;--&#91;BACK&#93;](/README.md)
