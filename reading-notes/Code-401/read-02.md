# Notes for Read 01 - Exception handling and Debugging

## Unit Testing Best Practices 

[Unit Testing Best Practices](https://stackify.com/unit-testing-basics-best-practices/)

Unit Testing *IS*: It's a method that test somthing about a method *in isolation*

You can use a C# unit framework by starting a new projece and selecting ***Unit Test Project**

Example:

```[TestClass]
public class UnitTest1
{
    [TestMethod]
    public void TestMethod1()
    {
        var calculator = new Calculator();

        int result = calculator.Add(4, 3);

        Assert.AreEqual(7, result);
    }
}
```

*Taken from the example on the site listed above*

Best Practices

+ Arrange, Act, Assert
+ One Assert Per Test Method
+ Avoid Test Interdependence - Have the test stand alone.  Should not rely on other methods
+ Keep is Short, Sweet, and Visible
+ Add Them to the Build - If the tests fail, so does the build. <-- Helpful

## xUnit Documentation
[xUnit Documentation](https://xunit.net/)

xUnit.net is a free, open source, community-focused unit testing tool for the .NET Framework.

Automatically creates a test class template from the command line.

## Art of README
[Art of README](https://github.com/noffle/art-of-readme)

README is a one-stop shop look at what you have created.

You need to:

+ tell them what it is (with context)
+ show them what it looks like in action
+ show them how they use it
+ tell them any other relevant details

The README should only be as long as it needs to be.  Make seperate pages if required, but keep it to the point

No README means developers will need to delve into your code in order to understand it. <-- Most won't

> Your documentation is complete when someone can use your module without ever having to look at its code. This is very important. This makes it possible for you to separate your module's documented interface from its internal implementation (guts). This is good because it means that you are free to change the module's internals as long as the interface remains the same.
> Remember: the documentation, not the code, defines what a module does. -- Ken Williams

Key Elements

1. Name - self-explanatory names
2. One Liner - Module Purpose
3. Usage -Show an example of how it works
4. API - Detail the module's functions, and other details.  Also, include caveats
5. Installation - How to install and run the thing 
   + Could be as simple as **npm -i coolApp**
6. License - If other than the standard open licenses, move up the list to make it apparent to the reader.


**Care about people's time, don't waste it**

## README Best Practices

[Example Template](https://raw.githubusercontent.com/jehna/readme-best-practices/master/README-default.md)

[Local Copy of Template](./example-readme.md)

[&lt;--&#91;BACK&#93;](/README.md)