# Notes for Read 08 - Collections

## Collections
[Microsoft Docs - Collections]()

Collections are similar to *arrays* in that they store groups of data.  
Unlike arrays *Collections* do not have to be a fixed size.  They can grow and shrink as needed.

There are several different types of collections

+ Dictionaries - Can place objects in a key/value pair
+ Lists - Can search using *index* numbers
+ Queue - FIFO (First In Last Out)
+ Stack - LIFO (Last In First Out)

```
List<Starship> federationShips = List<Starship>();
```

```
Dictionary<Cruisers> imperialClass = new Dictionary <string, Cruisers>();
```

You can use *LINQ* (Language Integrated Query) to set filters on searching through *Collections*

## Enumerations
[Microsoft Docs - Enumeration Types](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/enum)

Is a value type that is set by a series of constants.  
```
enum SuperMarioTwoChar
{
    Mario,
    Luigi,
    Toad,
    Princess Peach
}
```
Can add more functionality by an *extension* method

You can get the number of the values.
```
(int)Luigi //will equal 2
```







[&lt;--&#91;BACK&#93;](/README.md)