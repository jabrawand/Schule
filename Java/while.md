# While and Do While
## While Loop
The `while` loop repeats a block of code as long as the specified condition is **true**:

### Syntax
```java
while (condition) {
    // code block
}
```
---

In this code the loop will run as long as the variable `i` is less than 5:

```java
int i = 0;
while (i < 5) {
    System.out.println(i);
    i++
}
```

> [!NOTE]
> Do not forget to increase the variable used in the condition (`i++`), otherwise the loop will never end!

---
### Countdoun

```java
int countdown = 3;

while (countdown > 0) {
  System.out.println(countdown);
  countdown--;

System.out.println("Happy New Year!!");
}
```
---

### While Loop with false condition
If the condition is `false` at the beginning, the code inside the loop will never run:

```java
int i = 10;

while (i < 5) {
  System.out.println("This will never be printed");
  i++;
}
```
---
## Do While Loop

### Syntax

```java
do {
  // code block
}
while (condition);
```

> [!NOTE] 
> The semicolon `;` after the `while` is required!
> 
---

```java
int i = 0;do {
  System.out.println(i);
  i++;
}
while (i < 5);
```
---
### Do While with condition false

```java
int i = 0;do {
  System.out.println(i);
  i++;
}
while (i < 5);
```

> [!NOTE] 
> A `do/while` loop always runs at least once, even if the condition is false at the start. This is the key difference from a `while` loop, which would skip the code block completely in the same situation.
>
> This behavior makes `do/while` useful when you want something to happen at least once, such as showing a message or asking the user for input.