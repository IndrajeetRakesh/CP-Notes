# Java Input and Output

## 1. What is Input and Output?

**Input** means taking data from the user.

**Output** means displaying data to the user.

```text
Input  →  Program  →  Output
```

Example:

```text
User enters: 10
Program calculates: 10 × 2
Output: 20
```

---

# 2. Output in Java

Java uses `System.out` to display output.

## `System.out.println()`

Prints the value and moves the cursor to the next line.

```java
System.out.println("Hello");
System.out.println("World");
```

Output:

```text
Hello
World
```

### Important

```java
System.out.println("Hello");
System.out.println("World");
```

is different from:

```java
System.out.print("Hello");
System.out.print("World");
```

---

## `System.out.print()`

Prints the value but **does not move to the next line**.

```java
System.out.print("Hello ");
System.out.print("World");
```

Output:

```text
Hello World
```

---

## `System.out.println()` vs `System.out.print()`

| Method      | New Line? | Example                     |
| ----------- | --------- | --------------------------- |
| `println()` | Yes       | `System.out.println("Hi");` |
| `print()`   | No        | `System.out.print("Hi");`   |

---

## 3. Printing Variables

Variables can be directly printed.

```java
int age = 18;

System.out.println(age);
```

Output:

```text
18
```

Example:

```java
int a = 10;
int b = 20;

System.out.println(a);
System.out.println(b);
```

Output:

```text
10
20
```

---

## 4. Printing Text and Variables Together

Use `+` to join text and variables.

```java
int age = 18;

System.out.println("Age = " + age);
```

Output:

```text
Age = 18
```

Example:

```java
String name = "Siddhant";
int age = 18;

System.out.println("Name: " + name);
System.out.println("Age: " + age);
```

Output:

```text
Name: Siddhant
Age: 18
```

---

# 5. String Concatenation

When `+` is used with a String, it joins values together.

```java
System.out.println("Hello " + "World");
```

Output:

```text
Hello World
```

Variables can also be joined:

```java
String name = "Siddhant";
int age = 18;

System.out.println(name + " is " + age + " years old.");
```

Output:

```text
Siddhant is 18 years old.
```

---

# 6. Important `+` Rule

The position of the String matters.

### Example 1

```java
System.out.println(10 + 20);
```

Output:

```text
30
```

Both are numbers, so Java performs addition.

### Example 2

```java
System.out.println("10" + 20);
```

Output:

```text
1020
```

Because `"10"` is a String, `+` performs concatenation.

### Example 3

```java
System.out.println(10 + 20 + "30");
```

Output:

```text
3030
```

Java works from **left to right**:

```text
10 + 20 = 30
30 + "30" = "3030"
```

### Example 4

```java
System.out.println("10" + 20 + 30);
```

Output:

```text
102030
```

Because once Java encounters a String, the following `+` operations become concatenation.

---

# 7. Taking Input from User

Java commonly uses the `Scanner` class to take input.

First import Scanner:

```java
import java.util.Scanner;
```

Then create a Scanner object:

```java
Scanner sc = new Scanner(System.in);
```

Complete example:

```java
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        int age = sc.nextInt();

        System.out.println("Age = " + age);
    }
}
```

Input:

```text
18
```

Output:

```text
Age = 18
```

---

# 8. Understanding Scanner

```java
Scanner sc = new Scanner(System.in);
```

### `Scanner`

A Java class used to take input.

### `sc`

Variable name/reference used to access Scanner methods.

You can name it something else:

```java
Scanner input = new Scanner(System.in);
```

### `new Scanner(System.in)`

Creates a Scanner object that reads input from the keyboard.

### `System.in`

Represents the standard input stream, usually the keyboard.

---

# 9. Taking Integer Input

Use:

```java
nextInt()
```

Example:

```java
Scanner sc = new Scanner(System.in);

int number = sc.nextInt();

System.out.println(number);
```

Input:

```text
25
```

Output:

```text
25
```

---

# 10. Taking Decimal Input

Use:

```java
nextDouble()
```

Example:

```java
Scanner sc = new Scanner(System.in);

double marks = sc.nextDouble();

System.out.println(marks);
```

Input:

```text
87.5
```

Output:

```text
87.5
```

---

# 11. Taking String Input

There are two commonly used methods.

## `next()`

Reads **one word**.

```java
String name = sc.next();
```

Input:

```text
Siddhant
```

Output:

```text
Siddhant
```

If input is:

```text
Siddhant Dubey
```

`next()` reads only:

```text
Siddhant
```

---

## `nextLine()`

Reads the **complete line**, including spaces.

```java
String name = sc.nextLine();
```

Input:

```text
Siddhant Dubey
```

Output:

```text
Siddhant Dubey
```

---

# 12. `next()` vs `nextLine()`

| Method       | Reads         |
| ------------ | ------------- |
| `next()`     | One word      |
| `nextLine()` | Complete line |

Example:

```java
String firstName = sc.next();
String fullName = sc.nextLine();
```

`next()`:

```text
Siddhant
```

`nextLine()`:

```text
Siddhant Dubey
```

---

# 13. Taking Character Input

Scanner does not have a direct `nextChar()` method.

Use:

```java
char ch = sc.next().charAt(0);
```

Example:

```java
Scanner sc = new Scanner(System.in);

char ch = sc.next().charAt(0);

System.out.println(ch);
```

Input:

```text
A
```

Output:

```text
A
```

### Understanding it

```java
sc.next()
```

gets a String.

```java
.charAt(0)
```

gets the character at index `0`.

Example:

```text
"Hello"
 01234
```

```java
"Hello".charAt(0)
```

gives:

```text
H
```

---

# 14. Taking Boolean Input

Use:

```java
nextBoolean()
```

Example:

```java
boolean isStudent = sc.nextBoolean();

System.out.println(isStudent);
```

Input:

```text
true
```

Output:

```text
true
```

Valid boolean values:

```text
true
false
```

---

# 15. Scanner Input Methods

| Method             | Data Type | Example       |
| ------------------ | --------- | ------------- |
| `nextInt()`        | `int`     | `25`          |
| `nextLong()`       | `long`    | `100000L`     |
| `nextFloat()`      | `float`   | `12.5f`       |
| `nextDouble()`     | `double`  | `12.5`        |
| `next()`           | `String`  | `Hello`       |
| `nextLine()`       | `String`  | `Hello World` |
| `nextBoolean()`    | `boolean` | `true`        |
| `next().charAt(0)` | `char`    | `A`           |

---

# 16. Taking Multiple Inputs

You can take multiple values using the same Scanner.

```java
Scanner sc = new Scanner(System.in);

int a = sc.nextInt();
int b = sc.nextInt();

System.out.println(a + b);
```

Input:

```text
10 20
```

Output:

```text
30
```

The inputs can also be on separate lines:

```text
10
20
```

Both work with `nextInt()`.

---

# 17. Taking Multiple Different Data Types

```java
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        String name = sc.next();
        int age = sc.nextInt();
        double marks = sc.nextDouble();

        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
        System.out.println("Marks: " + marks);
    }
}
```

Input:

```text
Siddhant
18
87.5
```

Output:

```text
Name: Siddhant
Age: 18
Marks: 87.5
```

---

# 18. Important Problem: `nextInt()` + `nextLine()`

This is a very common beginner problem.

Example:

```java
int age = sc.nextInt();
String name = sc.nextLine();
```

If you enter:

```text
18
Siddhant Dubey
```

`nextLine()` may read the leftover newline after `18`.

### Solution

Use an extra `nextLine()`:

```java
int age = sc.nextInt();
sc.nextLine();

String name = sc.nextLine();
```

Now:

```text
Input:
18
Siddhant Dubey
```

works correctly.

### Remember

```text
nextInt()
nextDouble()
next()
```

do not consume the line-ending newline in the same way `nextLine()` does.

When switching from a token-based method to `nextLine()`, often use:

```java
sc.nextLine();
```

once to consume the remaining newline.

---

# 19. Taking Input and Performing Calculation

Input:

```java
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        int a = sc.nextInt();
        int b = sc.nextInt();

        int sum = a + b;

        System.out.println("Sum = " + sum);
    }
}
```

Input:

```text
10 20
```

Output:

```text
Sum = 30
```

---

# 20. Taking Three Numbers

```java
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        int a = sc.nextInt();
        int b = sc.nextInt();
        int c = sc.nextInt();

        int sum = a + b + c;

        System.out.println("Sum = " + sum);
    }
}
```

Input:

```text
10 20 30
```

Output:

```text
Sum = 60
```

---

# 21. Input Without Prompt

In competitive programming, usually do not print messages asking for input.

Prefer:

```java
int a = sc.nextInt();
int b = sc.nextInt();

System.out.println(a + b);
```

Instead of:

```java
System.out.println("Enter first number:");
int a = sc.nextInt();

System.out.println("Enter second number:");
int b = sc.nextInt();
```

### Why?

Online judges expect exact output.

Extra text like:

```text
Enter first number:
```

can cause a **Wrong Answer**.

---

# 22. Output Formatting

## New Line

Use:

```java
System.out.println("Hello");
```

or:

```java
System.out.print("Hello\n");
```

`\n` means new line.

Example:

```java
System.out.print("Hello\nWorld");
```

Output:

```text
Hello
World
```

---

## Tab

Use:

```text
\t
```

Example:

```java
System.out.println("Name\tAge");
```

Output:

```text
Name    Age
```

---

## Escape Characters

| Escape | Meaning      |
| ------ | ------------ |
| `\n`   | New line     |
| `\t`   | Tab          |
| `\"`   | Double quote |
| `\\`   | Backslash    |

Example:

```java
System.out.println("Hello\nWorld");
```

Output:

```text
Hello
World
```

Example:

```java
System.out.println("\"Java\"");
```

Output:

```text
"Java"
```

---

# 23. Closing Scanner

You can close Scanner when you are finished:

```java
sc.close();
```

Example:

```java
Scanner sc = new Scanner(System.in);

int n = sc.nextInt();

System.out.println(n);

sc.close();
```

For beginner programs and competitive programming, you will often see Scanner left open without affecting the solution.

---

# 24. Complete Input-Output Template

```java
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        // Input
        int a = sc.nextInt();
        int b = sc.nextInt();

        // Processing
        int sum = a + b;

        // Output
        System.out.println(sum);

        sc.close();
    }
}
```

Basic structure:

```text
Input
  ↓
Processing
  ↓
Output
```

---

# 25. Common Mistakes

## Mistake 1: Forgetting Scanner import

Wrong:

```java
Scanner sc = new Scanner(System.in);
```

Correct:

```java
import java.util.Scanner;
```

---

## Mistake 2: Using `nextInt()` for decimal input

Wrong:

```java
int marks = sc.nextInt();
```

for:

```text
87.5
```

Correct:

```java
double marks = sc.nextDouble();
```

---

## Mistake 3: Expecting `next()` to read spaces

```java
String name = sc.next();
```

Input:

```text
Siddhant Dubey
```

Only:

```text
Siddhant
```

is read.

Use:

```java
String name = sc.nextLine();
```

for the complete line.

---

## Mistake 4: Confusing `print()` and `println()`

```java
System.out.print("A");
System.out.print("B");
```

Output:

```text
AB
```

But:

```java
System.out.println("A");
System.out.println("B");
```

Output:

```text
A
B
```

---

## Mistake 5: Forgetting semicolon

Wrong:

```java
System.out.println("Hello")
```

Correct:

```java
System.out.println("Hello");
```

---

# 26. Quick Revision

```text
OUTPUT
System.out.print()
    → prints without moving to next line

System.out.println()
    → prints and moves to next line
```

```text
INPUT
nextInt()
    → int

nextLong()
    → long

nextFloat()
    → float

nextDouble()
    → double

next()
    → one word

nextLine()
    → complete line

nextBoolean()
    → true / false

next().charAt(0)
    → char
```

---

# 27. Most Important Syntax

## Scanner Setup

```java
import java.util.Scanner;

Scanner sc = new Scanner(System.in);
```

## Integer

```java
int n = sc.nextInt();
```

## Decimal

```java
double n = sc.nextDouble();
```

## One Word

```java
String word = sc.next();
```

## Complete Line

```java
String line = sc.nextLine();
```

## Character

```java
char ch = sc.next().charAt(0);
```

## Boolean

```java
boolean value = sc.nextBoolean();
```

## Output

```java
System.out.println(value);
```


---

# 28. Exam / Interview Important Points

* `System.out.println()` prints and moves to the next line.
* `System.out.print()` prints without moving to the next line.
* `Scanner` is commonly used for keyboard input.
* `System.in` represents standard input.
* `nextInt()` reads an integer.
* `nextDouble()` reads a decimal number.
* `next()` reads one word.
* `nextLine()` reads the complete line.
* Java does not have a `nextChar()` method.
* Use `sc.next().charAt(0)` to read a character.
* `+` performs addition when both operands are numeric.
* `+` performs String concatenation when a String is involved.
* Java evaluates expressions from left to right.
* Be careful when mixing `nextInt()` and `nextLine()`.
* In competitive programming, avoid unnecessary prompt text in the output.
* Always match the required output format exactly.
