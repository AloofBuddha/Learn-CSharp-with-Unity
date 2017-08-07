We will write all of our Unity scripts in C# using MonoDevelop, Unity's built-in code editor. Before we get into using C# with Unity however, let's learn C# with basic Console Applications.

# Creating a new C# Project

* Open MonoDevelop

* File -> New -> Solution

* Choose 'Console Project'

* We give the Solution / Project a name

* create our first file 'HelloWorld.cs' with the following boiler plate code

* hit play to debug :)

# Boilerplate

I use the term 'boilerplate' to refer to everything we need to include in order to get any code to run. C# is a relatively sophisticated language, so unfortunately it asks for a lot of boilerplate upfront that won't make a lot of sense until a bit later. For now, we just include it by default.

```c#
using System;

namespace ConsoleApplication
{
    public class Program
    {
        public static void Main()
        {
            Console.WriteLine("Hello World!");
        }
    }
}
```

## `using` keyword

`using System;`

the `using` keyword is used to import code from other sources. In this case, we are importing code from the 'namespace' `System`, which is provided as part of the C# standard library, and is where we get access to the class `Console` which we use to perform I/O. Note the `;` at the end of this statement - it is a **statement**, and as such it is evaluated before the next line of code is run, as it *does something* (in this case, imports some code so it is available in the rest of the file). Without the semicolon at the end of this statement, the C# compiler will not let us compile our program.

## `namespace` keyword

The `namespace` keyword is used to defined a namespace, and it is the counterpart to the `using` statement. If we wanted to access this code from another file, we would write `using ConsoleApplication;` at the top of the file and then we would have access to our `Program` class. Note that there is no `;` following our namespace definition, as it is a 'control structure', not a statement. This means it doesn't 'do' anything on it's own, but it does define a unique scope, so we can avoid ambiguities.

## `class` keyword

Everything in C# is a `class`, and a class is defined as above. Much like the `namespace` keyword it is a control structure, and so it defines a unique scope but doesn't 'do anything', rather it's meaning is the structure we are creating, in this case a class definiton. Note that this class has the keyword `public` before it. This is the default, which means it is accessible from other files and is what we will be working with in general.

## `public static void Main()`

Every C# program needs a single class with a single method name 'Main' to know where the program 'starts'. `public` means this method is accesible to any instance of our class. `static` means it is a class method, as opposed to an instance method. We will explore that idea much later :) `void` is the return type for our function, in this case, we return nothing, so the type is 'void'. `()` defines the parameters our function takes, but in this case it takes none. Note once again this is a control structure, not a statement.

## Console.WriteLine("Hello World");

This is the 'real' code in our program. It is a statement (does something, ends in a semi-colon). What it does is use the `Console` class (which was imported from System), and calls the static method `WriteLine` on this class, passing the method the paramter "Hello World"

Altogether this results in a simple program that opens a new console window and prints "Hello World" to the console, then immediately ends. Not too fancy, but an important starting point to refer back to!

# Conclusion

When experimenting with C#, we can copy this file and replace only what we want to experiment with within the body of our `Main()` method.







