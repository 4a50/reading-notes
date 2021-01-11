# Notes for Read 01 - Exception handling and Debugging

## Debugging for Absolute Beginners

[Debugging for Absolute Beginners](https://docs.microsoft.com/en-us/visualstudio/debugger/debugging-absolute-beginners?view=vs-2019)

Clarify the problem by asking the RIGHT questions:

+ What did you expect your code to do?
+ What happened instead?

Examine your assumptions:

+ Are you using the correct APi?
+ Are you using the API correctly?
+ Does your code contain typos?
+ Did you make a change to your code and assume it is unrelated to the problem you see?
+ Did you expect the **object** or **variable** to contain a certain *value*?
+ Fo you know the intent of the code?  That is, if it is not YOUR code, do you know what it is supposed to do?

Step through your code in debugging mode to find where the problem occured.

## Try and Catch Blocks

[Try and Catch Blocks](https://docs.microsoft.com/en-us/dotnet/standard/exceptions/how-to-use-the-try-catch-block-to-catch-exceptions)

Place any code statements that may throw an exception in a `try{}` block and place statement used to handle the exceptions or exceptions in one or more catch blocks.

```try{
  //Do something in here that may throw and exception
}
catch (FileNotFoundException e)
{
  Console.WriteLine("File not found: " + e);
}

catch (Exception e) {
  Console.WriteLine("It was another error." + e);
}
```

## Exception Handling

[Exception Handling Keywords](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/statement-keywords)

Keywords:

+ try-catch
+ try-finally
+ try-catch-finally
+ throw

## C# in a Nutshell (pg 158-166)

**try** block used to execute code that may throw an error
**catch** will execute if there is an error

+ There can be multiple **catch** blocks used.  Each can handle only one type of exception
+ You can set conditional catches using the **when** *keyword*.

**finally** will execute after the computer leave the **try** or **catch** blocks to execute cleanup code.

Can **throw** an excpetion manuall in code.

+ can also use it as an expression `public string Foo() => throw new Exception();`

Alternatives to **Exceptions**

ex. `int.tryParse`

## Therac-25

[Therac-25](https://en.wikipedia.org/wiki/Therac-25)

A computer-controlled radiation therapy machine produced by Atomic Energy of Canada Limited (AECL) in 1982.

**Problem**:  It has six documented accidents occured when intense radiation was delivered to a patient when it was not meant to. Three patients died due to the radiation exposure
**Cause**:  

+ Hardware interlocks were removed, which were previously in place on earlier models, and relied solely on software checks
+ Poor **software design** and **development practices**
+ The software was designed so that it was virtually impossible to test it in a clean automated way.
  + AECL did not have the software code independently reviewed and chose to rely on in-house code, including the operating system.
  + AECL did not consider the design of the software during its assessment of how the machine might produce the desired results and what failure modes existed, focusing purely on hardware and asserting that the software was free of bugs.
  + Machine operators were reassured by AECL personnel that overdoses were impossible, leading them to dismiss the Therac-25 as the potential cause of many incidents.[1]:428
  + AECL had never tested the Therac-25 with the combination of software and hardware until it was assembled at the hospital.

[Ariane-5](https://en.wikipedia.org/wiki/Ariane_5)

Notable problem:

+ First Test Flight:  Self-Destructed in 37-seconds
  + Due to a data conversion from a **64-bit floating point** to an **unsigned 16-bit** integer.  The floating point was to big to be handled by the unsigned 16-bit int, cause a OPERAND error.  This bug was also present in the previous version, and was carried over into the new version.

[&lt;--&#91;BACK&#93;](/README.md)
