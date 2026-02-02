# Java Chaet Sheet

---
## Content 
- [Java Chaet Sheet](#java-chaet-sheet)
  - [Content](#content)
- [The main() Method](#the-main-method)
  - [System.out.println()](#systemoutprintln)
- [Statements](#statements)
- [Java println() / print()](#java-println--print)
  - [The println() method](#the-println-method)
  - [The print() method](#the-print-method)
  - [Print Text](#print-text)
  - [Print Numbers](#print-numbers)
- [Java Comments](#java-comments)
- [Java Variables](#java-variables)
  - [Declaring Variables](#declaring-variables)
  - [Print Variables](#print-variables)
  - [Mixing Text and Numbers](#mixing-text-and-numbers)
- [Java Identifiers](#java-identifiers)
- [Java Data Types](#java-data-types)
  - [Primitive Data Types](#primitive-data-types)
- [Java Strings](#java-strings)
  - [length()](#length)
  - [toUpperCase() / toLowerCase()](#touppercase--tolowercase)
  - [indexOf()](#indexof)
  - [charAt()](#charat)
  - [equals()](#equals)
- [trim()](#trim)
  - [Strings - Special Characters](#strings---special-characters)
    - [Example](#example)
    - [Example](#example-1)
  - [String Concatenation](#string-concatenation)
  - [Concatenation in Sentences](#concatenation-in-sentences)
    - [The concat() Method](#the-concat-method)
- [Java Type Casting](#java-type-casting)
- [Java Operators](#java-operators)
  - [Arithmetic Operators](#arithmetic-operators)
    - [Incrementing and Decrementing](#incrementing-and-decrementing)
  - [Assignment Operators](#assignment-operators)
  - [Comparison Operators](#comparison-operators)
  - [Logical Operators](#logical-operators)
  - [Java Operator Precendence](#java-operator-precendence)
- [Java Math](#java-math)
  - [Math.max(x,y)](#mathmaxxy)
  - [Math.min(_x,y_)](#mathminxy)
  - [Math.sqrt(_x_)](#mathsqrtx)
  - [Math.abs(_x_)](#mathabsx)
  - [Math.pow(_x, y_)](#mathpowx-y)
  - [Rounding Methods](#rounding-methods)
  - [Random Numbers](#random-numbers)
    - [Example](#example-2)
- [Java If...Else](#java-ifelse)
  - [The if Statement](#the-if-statement)
  - [The else Statement](#the-else-statement)
  - [The else if Statement](#the-else-if-statement)
  - [Nested if](#nested-if)
- [Java Ternary Operator](#java-ternary-operator)
  - [Nested Ternary Operator](#nested-ternary-operator)
- [Java Logical Operators in Condition](#java-logical-operators-in-condition)
  - [AND (\&\&)](#and-)
  - [OR (||)](#or-)
  - [NOT (!)](#not-)
- [Java Switch](#java-switch)
- [Java Loops](#java-loops)
  - [The While Loop](#the-while-loop)
  - [The Do-While Loop](#the-do-while-loop)
  - [The For Loop](#the-for-loop)
    - [Nested Loop](#nested-loop)
- [Java Break/Continue](#java-breakcontinue)
- [Java Arrays](#java-arrays)
  - [Declare Arrays](#declare-arrays)
  - [Access Elements](#access-elements)
  - [Change an Element](#change-an-element)
  - [Array Length](#array-length)
  - [The new Keyword](#the-new-keyword)
  - [Java Arrays Loop](#java-arrays-loop)
  - [Calculate the Sum of Elements](#calculate-the-sum-of-elements)
  - [Loop with For-Each](#loop-with-for-each)

Every line of code that runs in Java must be inside a `class`. The class name should always start with an uppercase first letter. 

> [!NOTE] 
> Java is case-sensitive. `MyClass` and `myclass` would be treated as two completely different names.
> 

The name of the Java file **must match** the class name. So if the class is called `Main`, the file must be saved as `Main.java`. This is because Java uses the class name to find and run the code. If the names don't match, Java will give an error and the program will not run.

---
# The main() Method
The `main()` method is required in every Java program. It is where the program starts running:

```java
public static void main(String[] args)
```

Any code placed inside the `main()` method will be executed.

---
## System.out.println()
Inside the `main()` method, we can use the `println()` method to print a line of text to the screen:
```java
public static void main(String[] args) {
  System.out.println("Hello World");
}
```

> [!NOTE] 
> The curly braces `{}` mark the beginning and the end of a block of code.
> `System.out.println()` may look long, but it as a single command that means: **"Send this text to the screen."**
> What each part means
> - `System` is a built-in Java class.
> - `out` is a member of `System`, short for "output".
> - `println()` is a method, short for "print line".
> 
> Finally, each Java statement must end with a semicolon (;).

---
# Statements
A computer program is a list of "instructions" to be "executed" by a computer.

In a programming language, these programming instructions are called statements.

**Example of a Statemene**

```java
System.out.println("Java is fun!");
```

> [!NOTE]
> Every statement have to end with a semicolon `;`.

---
# Java println() / print()
You can add as many `print()` or `println()` methods as you want

## The println() method
This method will add a new line for each output.

**Example**
```java
System.out.println("Hello World!");
System.out.println("How are you today?");
System.out.println("I'm fine.");
```

Prints:
*Hello World!*
*How are you today?*
*I'm fine.*

---
## The print() method
This method is similar to `println()`. The only difference is that it does **not** insert a new line at the end.

**Example**
```java
System.out.print("Hello World! ");
System.out.print("I will print on the same line.");
```
Prints:
*Hello World! I will print on the same line.*

---
## Print Text
Text must be wrapped inside double quotations marks "".

```java
System.out.println("This sentence will work!");
```

---
## Print Numbers
You can also use the println() method to print numbers. However, unlike text, we don't put numbers inside double quotes:

**Example**
```java
System.out.println(3);
System.out.println(358);
System.out.println(50000);
```

It's also possible to perform mathematical calculations inside the `println()` method

**Example**
```java
System.out.println(3 + 3); //Output: 6
```

```java
System.out.println(2 * 5); //Output: 10
```

---
# Java Comments

**Example**
```java
// single line comment

/* multi line comments
are generally used to describe a method
or make document within the code. */
```

---
# Java Variables
In Java, there are different types of variables

- `String` - stores text
- `int` - stores integers
- `float` - stores floating point numbers
- `char` - stores single characters
- `boolean` - stores values with two states: true or false

---
## Declaring Variables

**Syntax**
```java
type variableName = value;
```

**Example**
```java
int myNum = 5;
float myFloatNum = 5.99f;
char myLetter = 'D';
boolean myBool = true;
String myText = "Hello";
```
or 
```java
int myNum; // declears the variable
myNum = 15; // assign the value
```

> [!NOTE]
> If you assign a new value to an existing variable, it will overwrite the previous value

```java
int myNum = 15;
myNum = 20;  // myNum is now 20
System.out.println(myNum);
```

You can also assign the same value to multiple variables

**Example**
```java
int x, y, z;
x = y = z = 50;
System.out.println(x + y + z); // Output: 150
```

or more than one variable to the same type

**Example**
```java
int x = 5, y = 6, z = 50;
System.out.println(x + y + z); // Output: 61
```

> [!NOTE]
> Declaring many variables in one line is shorter, but writing one variable per line can somethimes make the code easier to read.


---
## Print Variables
You can combine text and a variable by using the `+` character

```java
String name = "John";
System.out.println("Hello " + name);
```
or
```java
String firstName = "John ";
String lastName = "Doe";
String fullName = firstName + lastName;
System.out.println(fullName);
```

> [!NOTE]
> In Java the `+` symbol has two meanings:
> - For `String`, it joins them together -> concatination.
> - For numbers, it adds values together.

**Example**
```java
int x = 5;
int y = 6;
System.out.println(x + y); // Output: 11
```

---
## Mixing Text and Numbers
Without parenteses, Java will treat the numbers as text after the first `String`.

**Example**
```java
int x = 5;
int y = 6;

System.out.println("The sum is " + x + y);   // Output: The sum is 56
System.out.println("The sum is " + (x + y)); // Output: The sum is 11
```

---
# Java Identifiers
All Java variables must be identified with unique names.

> [!NOTE]
> It is recommended to use descriptive names in order to create understandable and maintainable code.

**Example**
```java
// Good
int minutesPerHour = 60;

// OK, but not so easy to understand what min actually is
int min = 60;
```

The general rules for naming variables are:

- Names can contain letters, digits, underscores, and dollar signs
- Names should start with a lowercase letter, and cannot contain whitespace
- Names can also begin with $ and _
- Names are case-sensitive ("myVar" and "myvar" are different variables)
- Reserved words like Java keywords cannot be used as names
  
---
# Java Data Types
A variable in Java must be a specified data type.

Data types are divided into two groups:

- Primitive data types - includes `byte`, `short`, `int`, `long`, `float`, `double`, `boolean` and `char`
- Non-primitive data types - such as `String`, `Arrays` and `Classes` 

## Primitive Data Types

A primitive data type specifies the type of a variable and the kind of values it can hold.

There are eight primitive data types in Java:

|Data Type|Description|
|---|---|
|`byte`|Stores whole numbers from -128 to 127|
|`short`|Stores whole numbers from -32,768 to 32,767|
|`int`|Stores whole numbers from -2,147,483,648 to 2,147,483,647|
|`long`|Stores whole numbers from -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807|
|`float`|Stores fractional numbers. Sufficient for storing 6 to 7 decimal digits|
|`double`|Stores fractional numbers. Sufficient for storing 15 to 16 decimal digits|
|`boolean`|Stores true or false values|
|`char`|Stores a single character/letter or ASCII values|

> [!NOTE]
> Once a variable is declared with a type, it cannot change to another later in the program.
>
> If you really need to change between types, you must use [type casting](#java-type-casting) or conversion methods (for example, turning an int into a double).

---
# Java Strings
A `String` variable contains a **collection of characters** surrounded by double quotes ("").

A String in Java is actually an **object**, which means it contains methods that can perform certain operations on strings.

---
## length()
You can find the **length** of a string with the `length()` method.

**Example**
```java
String txt = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
System.out.println("The length of the txt string is: " + txt.length());
// Output: The length of the txt string is: 26
```

---
##  toUpperCase() / toLowerCase()
The `toUpperCase()` method converts a string to **upper case** letters.
The `toLowerCase()` method converts a string to **lower case** letters.

**Example**
```java
String txt = "Hello World";
System.out.println(txt.toUpperCase());   // Output: "HELLO WORLD"
System.out.println(txt.toLowerCase());   // Output: "hello world"
```

---
## indexOf()
The `indexOf()` method returns the **index** (the position) of the first occurrence of a specified text in a string (including whitespace).

**Example**
```java
String txt = "Please locate where 'locate' occurs!";
System.out.println(txt.indexOf("locate")); // Output: 7
```

> [!NOTE]
>
> Java counts positions from zero.  
> 0 is the first position in a string, 1 is the second, 2 is the third ...

---
## charAt()
You can use the `charAt()` method to access a character at a **specific position** in a string.

**Example**
```java
String txt = "Hello";
System.out.println(txt.charAt(0));  // H
System.out.println(txt.charAt(4));  // o
```

---
## equals()
To **compare** two strings, you can use the `equals()` method.

**Example**
```java
String txt1 = "Hello";
String txt2 = "Hello";

String txt3 = "Greetings";
String txt4 = "Great things";

System.out.println(txt1.equals(txt2));  // Output: true
System.out.println(txt3.equals(txt4));  // Output: false
```

---
# trim()
The `trim()` method removes **whitespace** from the beginning and the end of a string.

**Example**
```java
String txt = "   Hello World   ";
System.out.println("Before: [" + txt + "]");
System.out.println("After:  [" + txt.trim() + "]");
// Output: Before: [   Hello World   ]
// Output: After: [Hello World]
```

---
## Strings - Special Characters

Because strings must be written within quotes, Java will misunderstand this string, and generate an error:

```java
String txt = "We are the so-called "Vikings" from the north.";
// Output: error: ';' expected
```

The solution to avoid this problem, is to use the **backslash escape character**.

The backslash (`\`) escape character turns special characters into string characters:

|Escape character|Result|Description|
|---|---|---|
|\'|'|Single quote|
|\"|"|Double quote|
|\\|\|Backslash|

The sequence `\"`  inserts a double quote in a string:

```java
String txt = "We are the so-called \"Vikings\" from the north.";
```

The sequence `\'`  inserts a single quote in a string:

### Example

```java
String txt = "It\'s alright.";
```

The sequence `\\`  inserts a single backslash in a string:

### Example

```java
String txt = "The character \\ is called backslash.";
```

Other common escape sequences that are valid in Java are:

| Code | Result          |
| ---- | --------------- |
| \n   | New Line        |
| \t   | Tab             |
| \b   | Backspace       |
| \r   | Carriage Return |
| \f   | Form Feed       |


> [!NOTE] 
> Most of these escape codes are rarely used in modern programming. The most common ones are `\n` (new line), `\"` (double quote), and `\\` (backslash).

---
## String Concatenation

The `+` operator can be used between strings to combine them. This is called **concatenation**:

```java
String firstName = "John";
String lastName = "Doe";
System.out.println(firstName + " " + lastName);
```

> [!NOTE]
> Note that there is added an empty `String` (" ") to create a space between firstName and lastName on print.

---

## Concatenation in Sentences

You can use string concatenation to build sentences with both text and variables:

 **Example**

```java
String name = "John";
int age = 25;
System.out.println("My name is " + name + " and I am " + age + " years old.");
// Output: My name is John and I am 25 years old.
```

---

### The concat() Method

You can also use the `concat()` method to concatenate strings:

 **Example**

```java
String firstName = "John ";
String lastName = "Doe";
System.out.println(firstName.concat(lastName));
```

You can also join more than two strings by chaining `concat()` calls:

 **Example**

```java
String a = "Java ";
String b = "is ";
String c = "fun!";
String result = a.concat(b).concat(c);
System.out.println(result);
// Output: Java is fun!
```


> [!NOTE]
> While you can use `concat()` to join multiple strings, most developers prefer the `+` operator because it is shorter and easier to read.


---
# Java Type Casting


---
# Java Operators
Operators are used to perform operations on variables and values.

Java divides the operators into the following groups:

- [Arithmetic operators](#arithmetic-operators)
- [Assignment operators](#assignment-operators)
- [Comparison operators](#comparison-operators)
- [Logical operators](#logical-operators)
- Bitwise operators

---
## Arithmetic Operators
Arithmetic operators are used to perform common mathematical operations.


| Opperator | Name           | Description                            | Example |
| --------- | -------------- | -------------------------------------- | ------- |
| +         | Addition       | Adds together two values               | x + y   |
| -         | Subtraction    | Subtracts one value from another       | x - y   |
| *         | Multiplikation | Multiplies two values                  | x * y   |
| /         | Division       | Divides one value by another           | x / y   |
| %         | Modulus        | Returns the division remainder         | x % y   |
| ++        | Increment      | Increases the value of a variable by 1 | ++x     |
| --        | Decrement      | Decreases the value of a variable by 1 | --x     |

**Example**
```java
int x = 10;
int y = 3;

System.out.println(x + y); // 13
System.out.println(x - y); // 7
System.out.println(x * y); // 30
System.out.println(x / y); // 3
System.out.println(x % y); // 1

int z = 5;
++z;
System.out.println(z); // 6
--z;
System.out.println(z); // 5
```

> [!NOTE]
> When dividing two integers in Java, the result will also be an integer. For example, `10 / 3`gives `3`. If you want a decimal result, use `double`values, like `10.0 / 3`.

**Example**
```java
int a = 10;
int b = 3;
System.out.println(a / b);   // Output: 3

double c = 10.0d;
double d = 3.0d;
System.out.println(c / d);   // Output: 3.333...
```

---
### Incrementing and Decrementing
Incrementing and decrementing are very common in programming, especially when working with counters, loops, and arrays.

The `++` operator increases a value by 1, while the `--` operator decreases a value by 1

**Example Increment**
```java
int x = 5;

++x; // Increment x by 1
System.out.println(x); // 6
```

**Example Decrement**
```java
int x = 5;

--x; // Decrement x by 1
System.out.println(x); // 4
```

---
## Assignment Operators
Assignment operators are used to assign values to variables.

```java
int x = 10;
```

A list of all assignment operators:

| Operator | Example | Same As    |
| -------- | ------- | ---------- |
| =        | x = 5   | x = 5      |
| +=       | x += 3  | x = x + 3  |
| -=       | x -= 3  | x = x - 3  |
| *=       | x *= 3  | x = x * 3  |
| /=       | x /= 3  | x = x / 3  |
| %=       | x %= 3  | x = x % 3  |
| &=       | x &= 3  | x = x & 3  |
| \|=      | x \|= 3 | x = x \| 3 |
| ^=       | x ^= 3  | x = x ^ 3  |
| >>=      | x >>= 3 | x = x >> 3 |
| <<=      | x <<= 3 | x = x << 3 |

> [!NOTE]
> Most assignment operators are just shorter ways of writing code. For example, `x += 5` is the same as `x = x + 5`, but shorter and often easier to read.
> 

---
## Comparison Operators
Comparison operators are used to compare two values (or variables). 

The return value of a comparison is either `true` or `false`.

**Example**
```java
int age = 18;

System.out.println(age >= 18); // Output: true
System.out.println(age < 18);  // Output: false
```

A list of all comparison operators:

| Operator | Name                     | Example |
| -------- | ------------------------ | ------- |
| ==       | Equal to                 | x == y  |
| !=       | Not equal                | x != y  |
| >        | Greater than             | x > y   |
| <        | Less than                | x < y   |
| >=       | Greater than or equal to | x >= y  |
| <=       | Less than or equal to    | x <= y  |


---
## Logical Operators
Logical operators are used to determine the logic between variables or values, by combining multiple conditions.

As with comparison operators, you can also test for `true`or `false` values with logical operators.

| Operator | Name        | Description                                             | Example            |
| -------- | ----------- | ------------------------------------------------------- | ------------------ |
| &&       | Logical and | Returns true if both statements are true                | x < 5 &&  x < 10   |
| \|       | Logical or  | Returns true if one of the statements is true           | x < 5 \| x < 4     |
| !        | Logical not | Reverse the result, returns false if the result is true | !(x < 5 && x < 10) |

**Example**
```java
boolean isLoggedIn = true;
boolean isAdmin = false;

System.out.println("Regular user: " + (isLoggedIn && !isAdmin)); // Output: Regular user: true
System.out.println("Has access: " + (isLoggedIn || isAdmin)); // Output: Has access: true
System.out.println("Not logged in: " + (!isLoggedIn)); // Output: false
```

---
## Java Operator Precendence
When a calculation contains more than one operator, Java follows **order of operations** rules to decide which part to calculate first.

Common operators, from highest to lowest priority:

- **Parentheses**:`()`
- **Multiplication, Division, Modulus**: `*`, `/`, `%` 
- **Multiplication, Division, Modulus**: `+`, `-` 
- **Comparison**: `>`, `<`, `>=`, `<=`
- **Equality**: `==`, `!=`
- **Logical AND**: `&&` 
- **Logical OR**: `||`
- **Assignment**: `=` 

**Example**
```java
int result1 = 2 + 3 * 4;     // 2 + 12 = 14
int result2 = (2 + 3) * 4;   // 5 * 4 = 20

System.out.println(result1);
System.out.println(result2);
```

> [!NOTE]
> Always use parentheses `( )` if you want to make sure the calculation is done in the order you expect. It also makes your code easier to read.

---
# Java Math
The Java Math class has many methods that allows you to perform mathematical tasks on numbers.

---
## Math.max(x,y)
The `Math.max(x,y)` method can be used to find the highest value of _x_ and _y_:

```java
Math.max(5, 10);
// Output: 10
```

---

## Math.min(_x,y_)

The `Math.min(x,y)` method can be used to find the lowest value of _x_ and _y_:

**Example**

```java
Math.min(5, 10);
// Output: 5
```

---

## Math.sqrt(_x_)

The `Math.sqrt(x)` method returns the square root of _x_:

**Example**

```java
Math.sqrt(64);
// Output: 8.0
```

---

## Math.abs(_x_)

The `Math.abs(x)` method returns the absolute (positive) value of _x_:

**Example**

```java
Math.abs(-4.7);
// Output: 4.7
```

---

## Math.pow(_x, y_)

The `Math.pow(x,y)` method returns the value of _x_ raised to the power of _y_:

**Example**

```java
Math.pow(2, 8);  // 256.0
```

> [!NOTE]
> 
>`Math.pow(2, 8)` means `2` multiplied by itself 8 times:  
2 * 2 * 2 * 2 * 2 * 2 * 2 * 2 = 256
>
>The `Math.pow()` method always returns a `double`, even if the result is a whole number. For example, `Math.pow(2, 8)` returns `256.0` (not `256`).

---

## Rounding Methods

Java has several methods for rounding numbers:

- `Math.round(x)` - rounds to the nearest integer
- `Math.ceil(x)` - rounds up (returns the smallest integer greater than or equal to x)
- `Math.floor(x)` - rounds down (returns the largest integer less than or equal to x)

**Example**

```java
Math.round(4.6);  // 5
Math.ceil(4.1);   // 5.0
Math.floor(4.9);  // 4.0
```

---

## Random Numbers

`Math.random()` returns a random number between 0.0 (inclusive), and 1.0 (exclusive):

**Example**

```java
Math.random();
```

To get more control over the random number, for example, if you only want a random number between 0 and 100, you can use the following formula:

### Example

```java
int randomNum = (int)(Math.random() * 101);  // 0 to 100
```


> [!NOTE]
> `Math.random()` returns a `double`. To get an integer, you need to cast it with `(int)`.


---
# Java If...Else
Conditions and if statements let you control the flow of your program - deciding which code runs, and which code is skipped.

Most often, conditions are created using comparison operators:

Less than: `a < b`
Less than or equal to: `a <= b`
Greater than: `a > b`
Greater than or equal to: `a >= b`
Equal to: `a == b`
Not equal to: `a != b`

Java has the following conditional statements:

- [`if`](#the-if-statement): to specify a block of code to be executed, if a specified condition is `true`
- [`else`](#the-else-statement): to specify a block of code to be executed, if the same condition is `false`
- [`else if`](#the-else-if-statement): to specify a new condition to test, if the first condition is `false`
- [`switch`](#java-switch): to specify many alternative blocks of code to be executed

---
## The if Statement
The `if` statement specifies a block of code to be executed if a condition is `true`.

**Syntax**
```java
if (condition) {
  // block of code to be executed if the condition is true
}
```

**Example**
```java
if (20 > 18) {
  System.out.println("20 is greater than 18");
}
```

or compare variables

```java
int x = 20;
int y = 18;
if (x > y) {
  System.out.println("x is greater than y");
}
```

Comparison is also often used to check if two values are equal, using the `==` operator:

```java
int x = 20;
int y = 20;
if (x == y) {
  System.out.println("x is equal to y");
}
```

You can also test boolean variables directly in an `if` statement:

```java
boolean isLightOn = true;

if (isLightOn) {
  System.out.println("The light is on.");
}
```

> [!NOTE]
> Writing `if (isLightOn)` is the same as writing `if (isLightOn == true)`, but shorter and easier to read.

---
## The else Statement
The `else` statement lets you run a block of code when the condition in the `if` statement is `false`.

**Syntax**
```java
if (condition) {
  // block of code to be executed if the condition is true
} else {
  // block of code to be executed if the condition is false
}
```

**Example**
```java
boolean isRaining = false;

if (isRaining) {
  System.out.println("Bring an umbrella!");
} else {
  System.out.println("No rain today, no need for an umbrella!");
} 
// Output: No rain today, no need for an umbrella!
```

> [!NOTE] 
> - `else` does not have a condition - it runs when the `if` condition is `false`.
> - Do not put a semicolon right after `if (condition)`. That would end the statement early and make `else` behave unexpectedly.

---
## The else if Statement
Use the `else if` statement to specify a new condition if the first condition is `false`.

**Syntax**
```java
if (condition1) {
  // block of code to be executed if condition1 is true
} else if (condition2) {
  // block of code to be executed if the condition1 is false and condition2 is true
} else {
  // block of code to be executed if the condition1 is false and condition2 is false
}
```

**Example**
```java
int weather = 2; // 1 = raining, 2 = sunny, 3 = cloudy

if (weather == 1) {
  System.out.println("Bring an umbrella.");
} else if (weather == 2) {
  System.out.println("Wear sunglasses.");
} else {
  System.out.println("Just go outside normally.");
}
// Output: "Wear sunglasses."
 
```

---
## Nested if
You can also place an `if` statement inside another `if`.

**Syntax**
```java
if (condition1) {
  // code to run if condition1 is true
  if (condition2) {
    // code to run if both condition1 and condition2 are true
  }
}
```

**Example**
```java
int x = 15;
int y = 25;

if (x > 10) {
  System.out.println("x is greater than 10");
  
  // Nested if 
  if (y > 20) {
    System.out.println("y is also greater than 20");
  }
}
// Output: x is greater than 10
// Output: y is also greater than 20
```

**Vote Example**
```java
int age = 20;
boolean isCitizen = true;

if (age >= 18) {
  System.out.println("Old enough to vote.");
  
  if (isCitizen) {
    System.out.println("And you are a citizen, so you can vote!");
  } else {
    System.out.println("But you must be a citizen to vote.");
  }
} else {
  System.out.println("Not old enough to vote.");
}
// Output: Old enough to vote.
// Output: And you are a citizen, so you can vote!
```

> [!NOTE] 
> - You can nest as many `if` statements as you want, but avoid making the code too deep - it can become hard to read.
>- Nested `if` is often used together with `else` and `else if` for more complex decision making.

---
# Java Ternary Operator
There is also a short-hand [if else](#java-ifelse), which is known as the **ternary operator** because it consists of three operands.

**Syntax**
```java
variable = (condition) ? expressionTrue :  expressionFalse;
```

**Example**
Instead of writing:
```java
int time = 20;
if (time < 18) {
  System.out.println("Good day.");
} else {
  System.out.println("Good evening.");
}
```
You can write:
```java
int time = 20;
String result = (time < 18) ? "Good day." : "Good evening.";
System.out.println(result);
```

or you can use it directly inside the `pringln()`

```java
int time = 20;
System.out.println((time < 18) ? "Good day." : "Good evening.");
```

---
## Nested Ternary Operator
You can nest ternary operators to handle more than two possible outcomes, but this can make your code harder to read:

**Example**
```java
int time = 22;
String message = (time < 12) ? "Good morning."
               : (time < 18) ? "Good afternoon."
               : "Good evening.";
System.out.println(message);
```

> [!NOTE] 
> Use the ternary operator for short, simple choices. For longer or more complex logic, the regular `if...else` is easier to read.

---
# Java Logical Operators in Condition
You can combine or reverse conditions using [logical operators](#logical-operators). These work together with `if`, `else`, and `else if` to build more complex decisions.

- `&&` (AND) - all conditions must be true
- `||` (OR) - at least one condition must be true
- `!` (NOT) - reverses a condition (true = false, false = true)
  
---
## AND (&&)
Use AND (`&&`) when **both** conditions must be true.

**Example**
```java
int a = 200;
int b = 33;
int c = 500;

if (a > b && c > a) {
  System.out.println("Both conditions are true");
}
```

---
## OR (||)
Use OR (`||`) when **at least one** of the conditions can be true.$

**Example**
```java
int a = 200;
int b = 33;
int c = 500;

if (a > b || a > c) {
  System.out.println("At least one condition is true");
}
```

---
## NOT (!)
Use NOT (`!`) to **reverse** a condition.

**Example**
```java
int a = 33;
int b = 200;

if (!(a > b)) {
  System.out.println("a is NOT greater than b");
}
```
---
**Login Example**
```java
boolean isLoggedIn = true;
boolean isAdmin = false;
int securityLevel = 3; // 1 = highest

if (isLoggedIn && (isAdmin || securityLevel <= 2)) {
  System.out.println("Access granted");
} else {
  System.out.println("Access denied");
}

// Try changing securityLevel to test different outcomes:
//
// securityLevel 1 = Access granted
// securityLevel 2 = Access granted
// securityLevel 3 = Access denied
// securityLevel 4 = Access denied
//
// If isAdmin = true, access is granted.
```

---
# Java Switch
Instead of writing **many** `if..else` statements, you can use the `switch` statement.

**Syntax**
```java
switch(expression) {
  case x:
    // code block
    break;
  case y:
    // code block
    break;
  default:
    // code block
}
```

This is how it works:

- The `switch` expression is evaluated once.
- The result is compared with each `case` value.
- If there is a match, the matching block of code runs.
- The `break` statement stops the switch after the matching case has run.
- The `default` statement runs if there is no match.

**Example**
```java
int day = 4;
switch (day) {
  case 1:
    System.out.println("Monday");
    break;
  case 2:
    System.out.println("Tuesday");
    break;
  case 3:
    System.out.println("Wednesday");
    break;
  case 4:
    System.out.println("Thursday");
    break;
  case 5:
    System.out.println("Friday");
    break;
  case 6:
    System.out.println("Saturday");
    break;
  case 7:
    System.out.println("Sunday");
    break;
}
// Outputs "Thursday" (day 4)
```

**Example with default**
```java
int day = 4;
switch (day) {
  case 6:
    System.out.println("Today is Saturday");
    break;
  case 7:
    System.out.println("Today is Sunday");
    break;
  default:
    System.out.println("Looking forward to the Weekend");
}
// Outputs "Looking forward to the Weekend"
 
```

> [!NOTE]
> Note that if the `default` statement is used as the last statement in a switch block, it does not need a break.

---
# Java Loops
Loops can execute a block of code as long as a specified condition is true.

Loops are handy because they save time, reduce errors, and they make code more readable.

---
## The While Loop
The `while` loop repeats a block of code as long as the specified condition is **true**:

**Syntax**
```java
while (condition) {
  // code block to be executed
}
```

**Example**
```java
int i = 0;
while (i < 5) {
  System.out.println(i);
  i++;
}
```

> [!NOTE]
> Do not forget to increase the variable used in the condition (`i++`), otherwise the loop will never end!
>
> The letter `i` a **counter** variable and a common choice in simple loops because it's short, traditional, and stands for 'index' or 'iterator'.

You can also use the `while` Loop to count down.

**Example**
```java
int countdown = 3;

while (countdown > 0) {
  System.out.println(countdown);
  countdown--;
}

System.out.println("Happy New Year!!");
```

> [!NOTE]
> If the condition is `false` at the beginning, the code inside the loop will never run.

**Example**
```java
int i = 10;

while (i < 5) {
  System.out.println("This will never be printed");
  i++;
}
```

---
## The Do-While Loop
The `do-while` loop is a variant of the `while` loop. This loop will execute the code block **once**, before checking if the condition is **true**. Then it will repeat the loop as long as the condition is **true**.

**Syntax**
```java
do {
  // code block to be executed
}
while (condition);
```

> [!NOTE] 
> The semicolon `;` after the `while` is required!

**Example**
```java
int i = 0;do {
  System.out.println(i);
  i++;
}
while (i < 5);
```

> [!NOTE] 
> Do not forget to increase the variable used in the condition (`i++`), otherwise the loop will never end!

**Example False Condition**
```java
int i = 10;

do {
  System.out.println("i is " + i);
  i++;
} while (i < 5);
```

> [!NOTE] 
> A `do/while` loop always runs at least once, even if the condition is false at the start. This is the key difference from a `while` loop, which would skip the code block completely in the same situation.
>
> This behavior makes `do/while` useful when you want something to happen at least once, such as showing a message or asking the user for input.

---
## The For Loop
When you know exactly how many times you want to loop through a block of code, use the `for` loop.

**Syntax**
```java
for (statement 1; statement 2; statement 3) {
  // code block to be executed
}
```
- **Statement 1** is executed (one time) before the execution of the code block.
- **Statement 2** defines the condition for executing the code block.
- **Statement 3** is executing (every time) after the code block has been executed.
  
---
**Example Print Numbers**
For example print the numbers 0 to 4.

```java
for (int i = 0; i < 5; i++) {  
  System.out.println(i);
}
```
- **Statement 1** sets a variable before the loop starts.
- **Statement 2** defines the condition for the loop to run: `i < 5`. If the condition is true, the loop will run again; if it is false, the loop ends.
- **Statement 3** increases a value each time the code block has run: `i++`.

---
**Example Print Even Numbers**
This example prints even values between 0 and 10

```java
for (int i = 0; i <= 10; i = i + 2) {  
  System.out.println(i);
}
// Output: 0 2 4 6 8 10
```
or combined with `if`
```java
for (int i = 0; i <= 10; i++) {  
  if (i % 2 == 0){
    System.out.println(i);
  }
}
// Output: 0 2 4 6 8 10
```
---
**Example Sum of Numbers**

```java
int sum = 0;
for (int i = 1; i <= 5; i++) {  
  sum = sum + i;
}
System.out.println("Sum is " + sum);
// Output: Sum is 15
```
---
**Example Reverse Output**

```java
for (int i = 5; i > 0; i--) {  
  System.out.println(i);
}
```
---
**Example False Condition**
If the condition is `false` right from the start, the code inside the loop will be skipped.

```java
for (int i = 10; i < 5; i++) {
  System.out.println("This will never be printed");
}
```
---
### Nested Loop
It is also possible to place a loop inside another loop.
The "inner loop" will be executed one time for each iteration of the "outer loop"

```java
// Outer loop
for (int i = 1; i <= 2; i++) {
  System.out.println("Outer: " + i); // Executes 2 times
  
  // Inner loop
  for (int j = 1; j <= 3; j++) {
    System.out.println(" Inner: " + j); // Executes 6 times (2 * 3)
  }
} 
```
**Multiplication Table Example**
```java
for (int i = 1; i <= 3; i++) {  
  for (int j = 1; j <= 3; j++) {
    System.out.print(i * j + " ");  
  }  System.out.println();
}
```
Output:
```
1 2 3
2 4 6
3 6 9
```
---
# Java Break/Continue

---
# Java Arrays
Arrays are used to store multiple values in a single variable, instead of declaring separate variables for each value.

**Syntax**
```java
Datatype[] identifier = {value1, value2, value3};
```
---
## Declare Arrays
To declare an array, define the variable type with **square brackets** `[]`

```java
String[] cars;
```

To insert values to it, you can place the values in a comma-separated list, inside **curly braces** `{}`.

```java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
```
Create an array of `int`
```java
int[] myNum = {10, 20, 30, 40};
```

---
## Access Elements
You can access an array element by referring to the index number.

**Example**
```java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
System.out.println(cars[0]);
// Output: Volvo
```
> [!NOTE] 
> Array indexes start with 0: [0] is the first element. [1] is the second element, etc.

---
## Change an Element
To change the value of a specific element, refer to the index number.

```java
cars[0] = "Opel";
```

**Example**
```java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
cars[0] = "Opel";
System.out.println(cars[0]);
// Output: Opel
```

---
## Array Length
To find out how many elements an array has, use the `length` property.

**Example**
```java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
System.out.println(cars.length);
// Output: 4
```

---
## The new Keyword
You can also create an array by specifying its size with `new`. This makes an empty array with space for a fixed number of elements, which you can fill later.

**Example**
```java
String[] cars = new String[4]; // size is 4

cars[0] = "Volvo";
cars[1] = "BMW";
cars[2] = "Ford";
cars[3] = "Mazda";

System.out.println(cars[0]); // Output: Volvo
```
If you already know the values, you don't need to use the `new`. Both ways create the same array.

**Example**
```java
// With new
String[] cars = new String[] {"Volvo", "BMW", "Ford", "Mazda"};

// Shortcut (most common)
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
```

> [!NOTE] 
> You cannot write `new String[4] {"Volvo", "BMW", "Ford", "Mazda"}`.
> In Java when using `new`, you either:
> - Use `new String[4]` to create an empty array with 4 slots, and then fill them later
> - Or use `new String[] {"Volvo", "BMW", "Ford", "Mazda"}` (without specifying the number of elements) to create the array and assign values at the same time

---
## Java Arrays Loop
You can loop through the array elements with the `for` loop, and use the `length` property to specify how many times the loop should run.

**Example**
```java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};

for (int i = 0; i < cars.length; i++) {
  System.out.println(cars[i]);
}
// Output: Volvo BMW Ford Mazda
```

A similar example with numbers

```java
int[] numbers = {10, 20, 30, 40};

for (int i = 0; i < numbers.length; i++) {
  System.out.println(numbers[i]);
}
```
---
## Calculate the Sum of Elements

**Example**
```java
int[] numbers = {1, 5, 10, 25};
int sum = 0;

// Loop through the array and add each element to sum
for (int i = 0; i < numbers.length; i++) {
  sum += numbers[i];
}

System.out.println("The sum is: " + sum);
// Output: The sum is: 41
```
## Loop with For-Each
There is also a **for-each** loop, which is used exclusively to loop through elements in an array (or other data structures)

**Syntax**
```java
for (type variable : arrayname) {
  // code block to be executed
}
```
The colon (`:`) is read as "in". So you can read the loop as: *"for each variable in array"*.

**Example**
```java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};

for (String car : cars) {
  System.out.println(car);
}
```

> [!NOTE]
> The for-each loop only gives you the values, not their positions (index) in the array.
>
> If you need both, a regular `for` loop is the right choice.

**Example**
```java
String[] seats = {"Jenny", "Liam", "Angie", "Bo"};

for (int i = 0; i < seats.length; i++) {
  System.out.println("Seat number " + i + " is taken by " + seats[i]);
}
```