# Notes for Read 10 - Error Handling and Debugging

## Javascript and JQuery

### Chapter 10: “Error Handling & Debugging”

Execution contexts

+ Global context
+ Function context
+ Eval Context &lt;-- Text is executed like code in an internal function

Variable Scope

+ Global Scope **NOTE**: If you do not use *var* when declaring a variable, it will be global
+ Function Level Scope

Execution is in the form of a *stack*.  As functions call other functions, the other functions go on top of the stack and is executed first.

Hoisting - variables and functions are created in memory before they are executed.  You can assign variables or invoke functions before they have been declared.

**lexical scope** Parent variables can share their information with the children.  But children cannot share information with parent.

Error are objects that can be accessed and utilized

+ Error
+ SyntaxError
+ ReferenceError
+ TypeError
+ RangeError
+ URIError - URI not used correctly (Incorrectly *escaped* error)
+ EvalError - type() used incorrectly.

You can script in the console.  See *page 471*

**Breakpoint** you can stop code at certain spots to error check
*Executed in browser*

**Can also Step through code** - Using the sources tab in *Developer Options*

Add *conditional breakpoints*

Can set a *breakpoint* in js is the dev tools are open

```try:
do comething
catch:
do something if it fails
finally:
execute regardless of what the conditions are.
```

You can throw your own errors

`throw new Error('This is NOT working man!');`

Can test and throw for NaN:

```if (!NaN) {
  Good to go
}
else
{
  throw new Error('NaN detected!');
}
```

[&lt;--&#91;BACK&#93;](README.md)
