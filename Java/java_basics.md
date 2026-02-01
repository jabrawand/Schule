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
- [Java Strings](#java-strings)
- [Java Booleans](#java-booleans)
- [Java Type Casting](#java-type-casting)
- [Java Operators](#java-operators)
- [Java Math](#java-math)
- [Java If...Else](#java-ifelse)
- [Java Switch](#java-switch)
- [Java While Loop](#java-while-loop)
- [Java For Loop](#java-for-loop)
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


---
# Java Strings

---
# Java Booleans

---
# Java Type Casting


---
# Java Operators

---
# Java Math

---
# Java If...Else

---
# Java Switch

---
# Java While Loop

---
# Java For Loop

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