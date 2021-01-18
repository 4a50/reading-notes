# Notes for Read 06 - OOP Principles

##

[Microsoft Docs - Inheritance](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/inheritance)

Inheritance is one of the 3 Fundamentals of OOP.
+ **Inheritance**
+ Encapsulation
+ Polymorphism


You start with a **base class**
```
class MushroomKingdomHero
    string HeroColor {get; set;}
    bool HasMushroom {get; set;}
    string Ability {get; set;}
    int Lives {get; set;}

    public void UseAbility(){} 
```
We make another class called "Princess Peach" that inherits from MushroomKingdomHero Class

```
class PrincessPeach : MushroomKingdomHero
    bool isKidnapped {get; set;}
```

So because **PrincessPeach** inherits from **MushroomKingdomHero** 

PrincessPeach has the following members:

+ `string HeroColor` **<--Inherited from MushroomKingdomHero**
+ `HasMushroom` **<--Inherited from MushroomKingdomHero**
+ `Ability` **<--Inherited from MushroomKingdomHero**
+ `Lives` **<--Inherited from MushroomKingdomHero**
+ `isKidnapped` ***<--Unique to PrincessPeach***
+  `public void UseAbility(){}` **<--Inherited from MushroomKingdomHero**
+  'public void Kidnapped(){} ***<--Unique to PrincessPeach***

We can still use another class to inherit from PrincessPeach.  Let's add Toad

```
class Toad : PrincessPeach
    bool hasAnnoyingScreechyVoice {get; set;}
```

Toad has the following members:

+ `string HeroColor` **<--Inherited from MushroomKingdomHero**
+ `HasMushroom` **<--Inherited from MushroomKingdomHero**
+ `Ability` **<--Inherited from MushroomKingdomHero**
+ `Lives` **<--Inherited from MushroomKingdomHero**
+ `isKidnapped`**<--Inherited from PrincessPeach**
+ `hasAnnoyingScreechyVoice` ***<--Unique to Toad*** 
+  `public void UseAbility(){}` **<--Inherited from MushroomKingdomHero**
+  'public void Kidnapped(){} ***<--Unique to PrincessPeach***

***Note*** Constructors and Cleanup items are **NOT** inherited

**Interfaces** are used to allow a class to use some of the members of a class that does not directly inherit from it.  
Or is not a "is a". 

You can *seal* a member of a class to prevent *inheriting* from it.

A *virtual* method allows an inherited class to *override* it.


## Abstract

[Microsoft Docs - Abstract](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/abstract-and-sealed-classes-and-class-members)

An **abstract** class is one that CANNOT be instantiated.  It's is meant to be a base for which to build off of, and not to be used alone.

if a member is abstract, the object that inherits it MUST implement it.
```
public abstract class BadGuy
{
    public virtual void AttackEnemy();
}
```

So we can't `BadGuy goomba = new BadGuy();` becuuse it is an Abstract.

```
public class Bowser : BadGuy
{
    public override void AttackEnemy()
    {
        
    }
    
}
In this way we can have *Bowser* inherit the members of BadGuy and override the method.

You can **sealed** a class or class member to prevent it from being inherited.

```
public class sealed MontyMole : BadGuy
{
    public override void AttackEnemy()
    {

    }
}
  
Nothing can inherit from MontyMole.

## Polymorphism

[Microsoft Docs - Polymorphism](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/polymorphism)

***Third Pillar*** of OOP

A *virtual* allows that property/method to be overridden to suit the inherited class's needs.
If it doesn't override it, then other derived classes from it can override if necessary.

The derived class may define *non-virtual* member to hide the *base * from subsequent derivations.

**NOTE** Fields **CANNOT** be virtual.  
Only 
+ Properties
+ Methods

*Inheritance* covered earlier.
*sealed* covered earlier.

## OOP Principles

[Microsoft Docs - OOP](https://docs.microsoft.com/en-us/dotnet/csharp/tutorials/intro-to-csharp/object-oriented-programming)

Most concepts already discussed above.  Only additional point to touch on.

+ You can use `: this (params)` in a constructor to call another constructor and add default params.

```
public NewClass(string stuff, int stuffNum) : this(name, stuffNum, 10){}

public NewClass(string stuff, int stuffNum, int moreStuff) {}
```

In addition to *public* and *private* there is also *protected*.
*protected* means that only classes derived from this class can use it.


[&lt;--&#91;BACK&#93;](/README.md)