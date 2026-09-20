# Java Basics

## 1. What is Java?

Java is a high-level, object-oriented programming language.

Java is used for:

- Backend development
- Android development
- Web applications
- Desktop applications
- Large software systems
- DSA and competitive programming

---

## 2. First Java Program


```java 
import java.util.*;
public class Main {
    public static void main(String[] args) {
        System.out.println("Hello World");
    }
}
```
output: 
```java
    Hello World
```
---
---
#1
```java
import java.util.*;
```
Imports classes from Java's java.util package.

* means all available classes in that package.
Common example: Scanner, ArrayList, etc.
This allows us to use them without writing 

#2
```
public class Main {
    ```
- Creates a class named Main.
- public means the class can be accessed from anywhere.
- Main is the class name.
- { marks the beginning of the class.

#3
```
public static void main(String[] args) { 
    ```
- This is the main method.
- Java starts executing the program from the main() method.
- **public** → accessible to Java from outside the class.
- **static** → Java can run it without creating an object of Main.
- **void** → the method does not return a value.
- **main** → the special method name where program execution starts.
- **String[] args** → stores command-line arguments.
- **{** → marks the beginning of the main() method.
- **}**
- The first **}** closes the **main()** method.
- The second **}** closes the **Main** class.

---

# Java Data Types

## 1. What is a Data Type?

A data type tells Java:

- What type of value a variable can store
- How much memory is required
- What kind of operations can be performed on the value
```
Data Types
│
├── Primitive Data Types
│   ├── byte
│   ├── short
│   ├── int
│   ├── long
│   ├── float
│   ├── double
│   ├── char
│   └── boolean
│
└── Non-Primitive / Reference Data Types
    ├── String
    ├── Arrays
    ├── Classes
    ├── Objects
    └── Interfaces
    ```

3. Primitive Data Types

Java has 8 primitive data types.

|Data Type |	Size |	Range / Values |
|---|---|---|
|byte	|1 byte	|-128 to 127|
|short	|2 bytes|	-32,768 to 32,767|
|int	|4 bytes|	-2³¹ to 2³¹ - 1|
|long	|8 bytes|	-2⁶³ to 2⁶³ - 1|
|float	|4 bytes|	Approximately ±3.4 × 10³⁸|
|double	|8 bytes|	Approximately ±1.7 × 10³⁰⁸|
|char	|2 bytes|	0 to 65,535|
|boolean|	JVM-dependent|	true or false|

---
---
# Arithmetic Operators
|Operator| Meaning|
|---| ---|
|+ |	Addition|
|- |	Subtraction|
|* |	Multiplication|
|/ |	Division|
|% |	Remainder|

Example:
```
int a = 10;
int b = 3;

System.out.println(a + b);
System.out.println(a - b);
System.out.println(a * b);
System.out.println(a / b);
System.out.println(a % b);
```
Output:
```
13
7
30
3
1
```
## Integer Division

When both numbers are integers:
```
int a = 10;
int b = 3;

System.out.println(a / b);
```
Output:
```
3
```
The decimal part is removed.

### For decimal division:

```
double a = 10;
double b = 3;

System.out.println(a / b);
```
output:
```
3.3333333333333335
```
 ### Increment and Decrement
Increment
```
int x = 5;

x++;

System.out.println(x);
````
Output:
```
6
```
Same as:
x = x + 1;

Decrement
```
int x = 5;

x--;

System.out.println(x);
````
Output:
```
4
```
Same as:

x = x - 1;

# Practice Questions
### Easy
Q1 Print your name.
Q2 Create variables for your name, age and marks.
Q3 Add two numbers.
Q4 Find the remainder of two numbers.

