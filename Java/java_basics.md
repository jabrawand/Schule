# Java Chaet Sheet
Every line of code that runs in Java must be inside a `class`. The class name should always start with an uppercase first letter. 

> [!NOTE] 
> Java is case-sensitive. `MyClass` and `myclass` would be treated as two completely different names.
> 

The name of the Java file **must match** the class name. So if the class is called `Main`, the file must be saved as `Main.java`. This is because Java uses the class name to find and run the code. If the names don't match, Java will give an error and the program will not run.

---
# The main Method
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

## Comments

**Example**
```java
// single line comment

/* multi line comments
are generally used to describe a method
or make document within the code. */
```

---

## Java Variables
In Java, there are different types of variables

- `String` - stores text
- `int` - stores integers
- `float` - stores floating point numbers
- `char` - stores single characters
- `boolean` - stores values with two states: true or false
  
### Declaring Variables

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

---

### Final Variables
This will declare the variable as "final" or "constant", which means unchangeable and read-only.

```java
final int myNum = 15;
myNum = 20;  // will generate an error: cannot assign a value to a final variable
```
