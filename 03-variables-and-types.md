# Declaring Variables 

The simplest way to declare a variable is with the `var` keyword

```csharp
public static void Main() 
{
  var i = 1;
  var f = 22.4;
  var c = 'h';
  var s = "hello world";
}
```

## The `var` keyword

The `var` keyword allows us to bind an identifier to a value. `var` is used to declare and instatiate a new value, and uses 'implicit typing' - i.e. it implicitly discerns the type of the variable based on what it is being instantiated with. Note that, once set, this variable can only be used to hold a value of the given type.

## Declaring a variable with explicit typing

The `var` keyword can be useful in certain scenarios, but it is generally better to be explicit about what type the variable will hold. With explicit typing, our program would look like this

```csharp
public static void Main() 
{
  int i = 1;
  float f = 22.4;
  char c = 'h';
  string s = "hello world";
}
```

`int`, `float` and `string` are the primitive data types we will concern ourselves with for now. 

## String concatenation

```csharp
string a = "Hello ";
string b = "World";
string concatenated = a + b;
Console.WriteLine(concatenated);
```

When we use the `+` operator with strings, it combines them into a single string.

## String interpolation

Sometimes we want to use the value of a variable within a string. The basic way to do this is with string concatenation and implicit casting (if its not a string, C# will turn it into a String as defined in it's toString() method that every Object must define).

```csharp
int x = 1;
int y = 2;
int sum = x + y;
Console.WriteLine("The sum of " + x + " and " + y + " is " + sum + "!");
```

This can be a bit cumbersome however, which is why we have the string interpolation syntax.


```csharp
int x = 1;
int y = 2;
int sum = x + y;
Console.WriteLine($"The sum of {x} and {y} is {sum}!");
```

With this syntax we can use a single string, prepended with a `$`, and within this string anything inside of a `{}` will be evaluated within the current scope.
