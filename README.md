# Get Started with C# for Beginners

Welcome to .NET Interactive and your first C# notebook. C# is an programming language that you can use to make many different types of programs including websites, games, and mobile applications. Let's explore some of the basics of using C# in this notebook and write your first .NET code!

## C# Syntax Basics

C# allows you to insert as much space as you would like between commands that you write. You can use tabs or spaces to format your C# code to make it easier for us humans to read. Complete lines of code, or **statements**, need to end with a semicolon so that the C# **compiler** knows that we have completed giving it an instruction.

A **compiler** turns our C# statements into a file that a computer can execute.

Let's write our first line of C# code, a simple "hello world" statement in C#:

```csharp
Console.riteLine("Hello, world!");
```

Let's review what happened there. **Console.WriteLine** is an instruction that tells C# to write the contents of the parenthesis **( )**. We include some text, referred to as a **string** enclosed in double-quotes that we would like C# to write for us.

## Introducing Variables

We can instruct C# to store values in memory using **variables**. A variable can store a value that we **assign** to it using the `=` operator.

Let's define a variable of type `string` called `aFriend` and store the name "Bill".

```csharp
string ariend = "Bill";
Console.WriteLine(aFriend);
```

You can also re-assign different values to a variable, like so:

```csharp
aFriend  "Maira";
Console.WriteLine(aFriend);
```

## Work with strings

The data type used above is called a `string`. It's used for textual data.

You can also combine strings. In this case, we'll use `+` to combine two strings:

```csharp
Console.riteLine("Hello " + aFriend);
```

When working with strings, you can also use [String Interpolation](https://docs.microsoft.com/dotnet/csharp/language-reference/tokens/interpolated) to combine values into a string:

```csharp
Console.WriteLine($"Hello {aFriend}");
```

You're not limited to a single variable between the curly braces when using String Interpolation:

```csharp
string firstFriend = "Maria";
string secondFriend = "Sage";
Console.WriteLine($"My friends are {firstFriend} and {secondFriend}");
```

As you explore more with strings, you'll find that strings are more than a collection of letters. You can find the length of a string using `Length`. `Length` is a property of a string and it returns the number of characters in that string:

```csharp
Console.WriteLine($"The name {firstFriend} has {firstFriend.Length} letters.");
Console.WriteLine($"The name {secondFriend} has {secondFriend.Length} letters.");
```

## Do more with strings

You've been using a _method_, `Console.WriteLine`, to print messages. A method is a block of code that implements some action. It has a name, so you can access it.

Suppose your strings have leading or trailing spaces that you don't want to display. You want to **trim** the spaces from the strings. The `Trim` method and related methods `TrimStart` and `TrimEnd` do that work. You can just use those methods to remove leading and trailing spaces.

```csharp
string greeting = " Hello World! ";
Console.WriteLine($"[{greeting}]");

string trimmedGreeting = greeting.TrimStart();
Console.WriteLine($"[{trimmedGreeting}]");

trimmedGreeting = greeting.TrimEnd();
Console.WriteLine($"[{trimmedGreeting}]");

trimmedGreeting = greeting.Trim();
Console.WriteLine($"[{trimmedGreeting}]");
```

There are other methods available to work with a string. For example, you've probably used a search and replace command in an editor or word processor before. The `Replace` method does something similar in a string. It searches for a substring and replaces it with different text. The `Replace` method takes two parameters. These are the strings between the parentheses. The first string is the text to search for. The second string is the text to replace it with:

```csharp
string sayHello = "Hello World!";
Console.WriteLine(sayHello);
sayHello = sayHello.Replace("Hello", "Greetings");
Console.WriteLine(sayHello);
```

Two other useful methods make a string ALL CAPS or all lower case:

```csharp
Console.WriteLine(sayHello.ToUpper());
Console.WriteLine(sayHello.ToLower());
```

## Search strings

The other part of a search and replace operation is to find text in a string. You can use the `Contains` method for searching. It tells you if a string contains a substring inside it:

```csharp
string songLyrics = "You say goodbye, and I say hello";
Console.WriteLine(songLyrics.Contains("goodbye"));
Console.WriteLine(songLyrics.Contains("greetings"));
```

## Comments

You can write comments by using the two forward-slash characters to indicate everything after them is a comment.

```csharp
// This is a comment
```

The below script needs to be able to find the current output cell; this is an easy method to get it.

You can create comments that span multiple lines by using slash asterisk fencing like the following:

```csharp
/\*
This is a multi-line comment

and this is still commented out
\*/
```

## Built-In Variable Types

Variables can be declared of various **types** and then interacted with. The simplest types in C# are called [Built-In Types](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types)

We define variables using in-memory storage for a type by preceeding the name of the variable we would like to create with the type of the variable we are creating.

```csharp
int i = 10;
double j = 5.5d;
char c = 'C';

c
```

### The var keyword

Sometimes, its a little cumbersome to declare a variable, assign a value, and have to specify the type before it. C# has built-in type inference and you can use the var keyword to force the compiler to detect the actual type being created and set the variable to the type of the value being assigned.

```csharp
var i = 10;
var someReallyLongVariableName = 9;
var foo = "Something";
display(someReallyLongVariableName);

var c = 'C';
c
```

You can ONLY use the var keyword when creating and assigning the variable in one statement.

### Real Literals

We can declare double, float, and decimal types with simple numeric notation, but we need to force the literal numbers we assign to be the correct type to match the variable type expected.

To do this, we add a d, f, or m suffix to a number being assigned. Try changing the suffix on the number in the next block and see what types it assigns.

```csharp
var myNumber = 4f;
myNumber.GetType()
```

## Type Casting

We can convert a variable between different types in several ways:

1. Assign to a variable of a different type
1. Convert between types by placing the destination type in parenthesis

```csharp
int valueA = 10;
decimal valueB = valueA; // Implicit conversion

display(valueB);

decimal valueC = 10;
//int valueD = valueC; // This errors out because int cannot be implicitly converted to by a decimal
int valueD = (int)valueC; // Explicitly convert valueC to int with the (int) modifier

display(valueD);
```

## Operators

Now that we have some basic types and can create variables, it would sure be nice to have them interact with each other. [Operators](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/operators/) can be used to interact with our variables.

Let's start by declaring two variables, apples and oranges and interact with them using different operators. Try changing some of the values and tinkering with the operators in the following code snippets.

```csharp
var apples = 100m; // Decimal value
var oranges = 30m; // Decimal value
```

Basic arithmetic operators and assignment are available:

````csharp
display(apples + oranges);

```csharp
display(apples - oranges);

```csharp
display(apples \* oranges);

```csharp
display(apples += 10);

display(apples -= 10);

display(apples \*= 10);

display(apples /= 3m);
````

C# makes the inequality operators available as well, and a test for equality using ==

````csharp
display(apples > oranges)

```csharp
display(apples >= oranges)

```csharp
display(apples < oranges)

```csharp
display(apples <= oranges)

```csharp
display(apples == oranges)

```csharp
display(apples != oranges)
````

## Loops and Conditionals

Common to every programming language are the concepts of loops or repeated execution of the same block of code and conditional execution of code. These features are typically manifest as the following statements:

- for
- while
- do
- if
- switch or case

### Conditionals

There are two statement-level conditional interactions in C#: if and switch...case statements. If statements can be combined with any number of else if statements and a single else statement to route code flow and interactions across branches of code. [(Link to official docs)](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/if-else)

Let's take a look at a simple if statement.

```csharp
var seconds = DateTime.Now.Second;
display("Current seconds: " + seconds);

// A simple test, are the number of seconds a multiple of 2?
if ( seconds % 2 == 0 ) {

    // Do this thing when seconds are even
    display("seconds are even");

}
```

The if statement starts with the if keyword and continues with a test in parenthesis. Next, the code to be executed if the test evaluates to true is contained within curly braces { }. The use of braces is optional, as long as the code to be executed is a single line.

```csharp
var seconds = DateTime.Now.Second;
display("Current seconds: " + seconds);

// One line if statement
if (seconds % 2 == 0) display("Seconds are even");

if (seconds % 2 == 1)
display("Seconds are odd");

    display("This will always execute, even though it LOOKS LIKE its in the if statement");
```

Great, if the condition is met we can execute some code. What if we need some more complex branching and potentially apply secondary tests and code if those tests return false? We can start using the else and else if syntax to add these additional branches of code to be executed.

Let's look a more complex branching scenario:

```csharp
var seconds = DateTime.Now.Second;
display("Current seconds: " + seconds);

if (seconds % 2 == 0) {
display("Seconds are even");
} else if (seconds % 3 == 0) {
display("Seconds are a multiple of 3");
} else if (seconds % 5 == 0) {
display("Seconds are a multiple of 5");
} else {
display("Seconds are neither even nor a multiple of 3");
}

if (seconds % 2 == 0) display("Seconds are even");
else if (seconds % 3 == 0) display("Seconds are a multiple of 3");
else if (seconds % 5 == 0) display("Seconds are a multiple of 5");
else display("Seconds are neither even nor a multiple of 3");
```

Testing for one condition is fine... but what if we have a compound scenario where we need to test for multiple factors before we determine which branch to take?

You can chain together conditional tests using the logical OR | and the logical AND & operators.

```csharp
var seconds = DateTime.Now.Second;
// seconds = 7;
display("Current seconds: " + seconds);

// Test for BOTH multiple of 2 AND a multiple of 3
if (seconds % 2 == 0 & seconds % 3 == 0) {
display("Seconds are even AND a multiple of 3");
} else if (seconds % 2 == 0) {
display("Seconds are even");
} else if (seconds % 3 == 0) {
display("Seconds are a multiple of 3");

// Test for seconds to be a multiple of 5 OR a multiple of 7
} else if (seconds % 5 == 0 | seconds % 7 == 0) {
display("Seconds are a multiple of 5 OR 7");
} else {
display("Seconds are neither even nor a multiple of 3");
}
```

There is another scenario that you will see many developers use to prioritize the compound boolean test inside an if statement, and that is using the 'short circuit' operators && and ||. They're referred to as a 'short circuit' operators because they evaluate the first condition on the left and if necessary evaluate the condition on the right side of the operator.

The && operator is called the **Conditional Logical AND** operator or referred to as **AndAlso** in Visual Basic. This operator behaves as follows:

1. Evaluate the left-side of the operator
1. IF the left-side evaluates to false, return false and stop processing
1. ELSE return the result of evaluating the right-side of the operator

Here's an example:

```csharp
var seconds = DateTime.Now.Second;
display("Current seconds: " + seconds);

bool MultipleOfThree() {
display("MultipleOfThree was called");
return seconds % 3 == 0;
}

if (seconds % 2 == 0 && MultipleOfThree()) {
display("Seconds are even and a multiple of three");
}

if (seconds != null && seconds % 2 == 1) {
display("Seconds are odd");
}
```

In this scenario, if the number of seconds are even then the MultipleOfThree method is executed. If the number of seconds is even and a multiple of three, then it is reported as such. We can also observe that when the number of seconds is even, the MultipleOfThree method is executed because it is reported in the output.

The || operator is called the **Conditional Logical OR operator** or referred to as the **OrElse** operator by the Visual Basic language. This operator behaves like the following:

1. Evaluate the left-side of the operator
1. IF the left-side evaluates to true, return true and stop processing
1. ELSE return the result of evaluating the right-side of the operator

Here's an example:

```csharp
var seconds = DateTime.Now.Second;
// seconds = 6;
display("Current seconds: " + seconds);

bool MultipleOfThree() {
display("MultipleOfThree was called");
return seconds % 3 == 0;
}

if (seconds % 2 == 0 || MultipleOfThree()) {
display("Seconds are even or a multiple of three");
}
```

### Switch Statements

Sometimes we have a LOT of conditions and branches that we want to evaluate and potentially traverse in our code. The [switch statement](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/switch) allows you to configure using the switch, case, break, and default statements the various branches you could potentially step down.

Use switch (test expression) to perform your test. Then use a series of case (result): statements to provide the various branching code paths to potentially execute. You can allow processing to 'fall out' of one statement into the next, and even provide a default branch at the end to ensure a branch is executed if none of the cases are matched.

Let's look at a real example:

```csharp
var dayOfTheWeek = DateTime.Now.DayOfWeek;
// dayOfTheWeek = DayOfWeek.Friday;

switch (dayOfTheWeek) {
case DayOfWeek.Monday:
display("Does somebody have a case of the Mondays?");
break;
case DayOfWeek.Tuesday:
display("It's TACO TUESDAY at the cafe!");
break;
case DayOfWeek.Wednesday:
display("Middle of the work-week... almost done!");
break;
case DayOfWeek.Thursday:
display("Friday is ALMOST HERE!!");
break;
case DayOfWeek.Friday:
display("The weekend starts.... NOW!");
break;
case DayOfWeek.Saturday:
display("Relaxing... no school, no work...");
break;
case DayOfWeek.Sunday:
display("School and work tomorrow? Better have some fun NOW!");
break;
default:
display("I don't care what day of the week it is... we're on HOLIDAY!");
break;
}
```

We can add additional tests for case statements using a when clause as well:

```csharp
var dayOfTheWeek = DateTime.Now.DayOfWeek;
var hourOfDay = DateTime.Now.Hour;

/_ Extra conditions to test with _/
dayOfTheWeek = DayOfWeek.Monday;
hourOfDay = 17;
/\* \*/

switch (dayOfTheWeek) {
case DayOfWeek.Monday:
case DayOfWeek.Tuesday:
case DayOfWeek.Wednesday:
case DayOfWeek.Thursday:
case DayOfWeek.Friday when hourOfDay < 16:
display("Work work work...");
break;
case DayOfWeek.Friday when hourOfDay >= 16:
display("The weekend starts.... NOW!");
break;
case DayOfWeek.Saturday:
case DayOfWeek.Sunday:
display("Relaxing... no school, no work...");
break;
}
```

### For Loops

[For loops](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/for) are a looping statement that allow you to repeat a block of code depending on a counter expression. The for statement takes the general form:

`for (Initializer; Condition; Iterator) { CODE TO EXECUTE }`

The Initializer typically initializes a counter variable to be worked with.

The Condition is a test to be executed at the beginning of each attempt to execute the code block. If the Condition evaluates to true then the code block will be executed.

The optional Iterator code executes after each loop and typically increments the initialized variable , stepping towards the end value.

Typical use for the for statement looks similar to the following, where 5 is an arbitrary number to stop counting at.

```
for (var i=0; i<5; i++) {

}
```

In practice it works like this:

```csharp
for (var counter=0; counter<5; counter++) {
display("Counting " + counter);
}
```

Loops can even count backwards! This is because the iterator expression at the end of the for statement can execute any code. Let's try it with the -= operator:

```csharp
for (var counter=5; counter>0; counter-= 3) {
display("Counting " + counter);
}
```

### Break Statement in For loops

If you need to exit a loop and continue processing, you can execute the break statement.

In the following loop, it is configured to run forever with the counter value starting at 1 and continuing as long as the counter > 0. The break statement will be triggered once the counter crosses 10.

```csharp
for (var counter=1; counter>0; counter++) {
display("Counting " + counter);

if (counter > 10) break;

}
```

### For-Each Loops

We haven't covered collections yet, but you can run a for loop across all of the items in the collection (like an array) and interact with each of those items directly. The [foreach statement](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/foreach-in) will run the contents of the loop and pass into your varaible each element in the collection, one at a time.

Let's look at an example:

```csharp
var arrNames = new string[] { "Fritz", "Scott", "Maria", "Jayme", "Maira", "James"};

foreach (var name in arrNames) {
display(name);
}
```

The `foreach` statement is functionally the same as the following for loop with an iterator:

```csharp
for (var nameCounter = 0; nameCounter < arrNames.Length; nameCounter++) {
display(arrNames[nameCounter]);
}
```

### While and Do Loops

`while` and `do` loops have almost identical structure and perform the same task. You provide a test condition over which the contents of the loop should continue to be executed. The [while loop](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/while) executes the test FIRST before the loop statements, and the [do loop](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/do) executes the test AFTER the statements.

Consider the examples of each statement below. The each start with a counter value of 6. Only the do loop executes and the while loop does not execute as the test fails immediately.

````csharp
var counter = 6;

while (counter < 5) {
counter++;
display(counter);
}

```csharp
var counter = 6;

do {
counter++;
display(counter);
} while (counter < 5);
````

## Summary

There is so much more to cover about C# and interacting with the .NET frameworks. You can learn more through our [Get Started with .NET series](https://dotnet.microsoft.com/learn)
