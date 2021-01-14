# Notes for Read 04 - Objects and Classes

## Reference Chapter

> C# in a Nutshell - Chapter 3 (Creating Types in C#)

## Classes
[Microsoft Docs - Classes](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/classes)

A *class* is a *reference type*

It is a null until **EXPLICITLY** create an instance

`MyClass myclass = new Myclass();`

Declaring another object of the same type, assigning it the value of the first object.

`MyClass mc2 = myclass;`


### Class Inheritance

When you create a class, you can inherit from any other class 

Done by using *derivation*

If a Manager is ***Inheriting*** (Receiving all *members* of the base class except the *constructor*) from the class Employerr

```
public class Manager : Employee
{
    // Employee fields, properties, methods and events are inherited
    // New Manager fields, properties, methods and events go here...
}
```

## Constructors
[Microsoft Docs - Constructors](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/constructors)

### Constructor Syntax

```
public class Person
{
   private string last;
   private string first;

   public Person(string lastName, string firstName) //<--Shares the same name as the class
   {
      last = lastName;
      first = firstName;
   }

   // Remaining implementation of Person class.
}
```

### If a constructor can be implemented as a single statement, you can use an ***expression body*** definition. 

```
public class Location
{
   private string locationName;

   public Location(string name) => Name = name;

   public string Name
   {
      get => locationName;
      set => locationName = value;
   }
}
```


### Static Constructors

A class or struct can also have a static constructor, which initializes static members of the type.

```
public class Adult : Person
{
   private static int minimumAge;

   public Adult(string lastName, string firstName) : base(lastName, firstName)
   { }

   static Adult()
   {
      minimumAge = 18;
   }

   // Remaining implementation of Adult class.
}
```

Can use ***Expression bodies**

```
public class Child : Person
{
   private static int maximumAge;

   public Child(string lastName, string firstName) : base(lastName, firstName)
   { }

   static Child() => maximumAge = 18;

   // Remaining implementation of Child class.
}
```

## Properties
[Microsoft Docs - Properties](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/properties)

**get** returns the property value

**set** assigns a new value

**value** is the *keyword* used to define the value being assigned by the **set** accessors.

Backing fields cannot be directly set outside the **object**.  Protects the values to ensure **proper validation**

Property accessors often consist of single-line statements that just assign or return the result of an expression. 
You can implement these properties as expression-bodied members. 
Expression body definitions consist of the **=>** symbol followed by the expression to assign to or retrieve from the property.

```
public class Person
{
   private string _firstName;
   private string _lastName;

   public Person(string first, string last)
   {
      _firstName = first;
      _lastName = last;
   }

   public string Name => $"{_firstName} {_lastName}";
}
```

Auto Implemented Properties

When properties just assign or retrieve a value.

`{get; set;}`

## Stack and Heap
[CSharp Corner - Stack and Heap](https://www.c-sharpcorner.com/article/C-Sharp-heaping-vs-stacking-in-net-part-i/)

### Stack

Stack is more or less responsible for keeping track of what's executing in our code (or what's been "called").

Value types are stored in the Stack.

(FILO) -> First In Last Out.

### Heap

Heap is responsible for keeping track of our objects.

Reference Types are stored in the heap


## Garbage Collection Fundamentals
[Microsoft Docs -Garbage Collection Fundamentals](https://docs.microsoft.com/en-us/dotnet/standard/garbage-collection/fundamentals)

Some Memory Fundamentals

+ Each process has its own, separate virtual address space. All processes on the same computer share the same physical memory and the page file, if there is one.
+ Virtual memory can be in three states:
    + Free - The block of memory has no references to it and is available for allocation.
    + Reserved - The block of memory is available for your use and cannot be used for any other allocation request. However, you cannot store data to this memory block until it is committed.
    + Committed - The block of memory is assigned to physical storage.

Memory Allocation

+ When you initialize a new process, the runtime reserves a contiguous region of address space for the process. 
+ Called the **managed heap**

Memory Release

Memory release
+ The garbage collector's optimizing engine determines the best time to perform a collection based on the allocations being made. 
+ When the garbage collector performs a collection, it releases the memory for objects that are no longer being used by the application.

Garbage Collection

+ The system has low physical memory. This is detected by either the low memory notification from the OS or low memory as indicated by the host.
+ The memory that's used by allocated objects on the managed heap surpasses an acceptable threshold. This threshold is continuously adjusted as the process runs.
+ The GC.Collect method is called. In almost all cases, you don't have to call this method, because the garbage collector runs continuously. This method is primarily used for unique situations and testing.






[&lt;--&#91;BACK&#93;](/README.md)