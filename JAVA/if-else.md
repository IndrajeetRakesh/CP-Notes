# Java If-Else

## 1. What is `if-else`?

`if-else` is used to make **decisions** in a program.

It allows Java to execute different code depending on whether a condition is `true` or `false`.

```text
Condition
    ↓
 true ──→ execute if block
    │
 false ─→ execute else block
```

Example:

```java
int age = 18;

if (age >= 18) {
    System.out.println("Adult");
} else {
    System.out.println("Not Adult");
}
```

Output:

```text
Adult
```

---

# 2. Basic `if`

Use `if` when you want to execute code **only when a condition is true**.

### Syntax

```java
if (condition) {
    // code
}
```

Example:

```java
int age = 20;

if (age >= 18) {
    System.out.println("Eligible");
}
```

Output:

```text
Eligible
```

If the condition is false, the code inside `if` is skipped.

---

# 3. Conditions

A condition usually produces either:

```text
true
```

or:

```text
false
```

Example:

```java
int age = 20;

age >= 18
```

Result:

```text
true
```

---

# 4. Relational Operators

Relational operators are commonly used in conditions.

| Operator | Meaning               | Example  |
| -------- | --------------------- | -------- |
| `>`      | Greater than          | `a > b`  |
| `<`      | Less than             | `a < b`  |
| `>=`     | Greater than or equal | `a >= b` |
| `<=`     | Less than or equal    | `a <= b` |
| `==`     | Equal to              | `a == b` |
| `!=`     | Not equal to          | `a != b` |

Example:

```java
int a = 10;
int b = 20;

System.out.println(a > b);
System.out.println(a < b);
System.out.println(a == b);
```

Output:

```text
false
true
false
```

---

# 5. `if-else`

Use `if-else` when there are **two possible paths**.

### Syntax

```java
if (condition) {
    // if condition is true
} else {
    // if condition is false
}
```

Example:

```java
int number = 7;

if (number % 2 == 0) {
    System.out.println("Even");
} else {
    System.out.println("Odd");
}
```

Output:

```text
Odd
```

---

# 6. `if-else` Flow

```text
             condition
                 |
          ┌──────┴──────┐
        true           false
          |               |
       if block       else block
          |               |
          └──────┬────────┘
                 ↓
              continue
```

Only **one** of the two blocks executes.

---

# 7. `if-else if-else`

Use this when there are **multiple conditions**.

### Syntax

```java
if (condition1) {

} else if (condition2) {

} else if (condition3) {

} else {

}
```

Example:

```java
int marks = 75;

if (marks >= 90) {
    System.out.println("A");
} else if (marks >= 80) {
    System.out.println("B");
} else if (marks >= 70) {
    System.out.println("C");
} else {
    System.out.println("D");
}
```

Output:

```text
C
```

---

# 8. How `else-if` Works

Java checks conditions **from top to bottom**.

Example:

```java
int marks = 85;

if (marks >= 90) {
    System.out.println("A");
} else if (marks >= 80) {
    System.out.println("B");
} else if (marks >= 70) {
    System.out.println("C");
} else {
    System.out.println("D");
}
```

Java checks:

```text
85 >= 90 → false
85 >= 80 → true
```

So it prints:

```text
B
```

Once a condition becomes true, the remaining `else-if` conditions are skipped.

---

# 9. Multiple `else-if`

You can have multiple `else-if` blocks.

```java
if (condition1) {

} else if (condition2) {

} else if (condition3) {

} else if (condition4) {

} else {

}
```

There can be:

```text
0 or more else-if blocks
```

But there can be only:

```text
1 else block
```

---

# 10. `else` is Optional

This is valid:

```java
if (age >= 18) {
    System.out.println("Adult");
}
```

`else` is not compulsory.

---

# 11. `else-if` Without `else`

This is also valid:

```java
if (marks >= 90) {
    System.out.println("A");
} else if (marks >= 80) {
    System.out.println("B");
}
```

If none of the conditions are true, nothing is printed.

---

# 12. Nested `if`

An `if` inside another `if` is called a **nested if**.

Example:

```java
int age = 20;
boolean hasID = true;

if (age >= 18) {

    if (hasID) {
        System.out.println("Allowed");
    }

}
```

Output:

```text
Allowed
```

Structure:

```text
if
└── if
```

---

# 13. Nested `if-else`

Example:

```java
int age = 20;
boolean hasID = true;

if (age >= 18) {

    if (hasID) {
        System.out.println("Allowed");
    } else {
        System.out.println("ID required");
    }

} else {
    System.out.println("Not eligible");
}
```

Output:

```text
Allowed
```

Logic:

```text
age >= 18?
    |
    ├── No → Not eligible
    |
    └── Yes
          |
          hasID?
          |
          ├── Yes → Allowed
          |
          └── No → ID required
```

---

# 14. Nested `if` Example

Check whether a number is positive and even.

```java
int n = 12;

if (n > 0) {

    if (n % 2 == 0) {
        System.out.println("Positive Even");
    }

}
```

Output:

```text
Positive Even
```

---

# 15. Nested `if` vs `else-if`

### Nested `if`

Used when one decision depends on another decision.

```java
if (condition1) {

    if (condition2) {

    }

}
```

### `else-if`

Used when choosing between multiple alternative conditions.

```java
if (condition1) {

} else if (condition2) {

} else {

}
```

---

# 16. Logical Operators

Logical operators combine multiple conditions.

| Operator | Name | Meaning                      |    |                                     |
| -------- | ---- | ---------------------------- | -- | ----------------------------------- |
| `&&`     | AND  | Both conditions must be true |    |                                     |
| `        |      | `                            | OR | At least one condition must be true |
| `!`      | NOT  | Reverses true/false          |    |                                     |

---

# 17. AND `&&`

Both conditions must be true.

```java
int age = 20;

if (age >= 18 && age <= 60) {
    System.out.println("Valid age");
}
```

Output:

```text
Valid age
```

Truth table:

| A     | B     | `A && B` |
| ----- | ----- | -------- |
| true  | true  | true     |
| true  | false | false    |
| false | true  | false    |
| false | false | false    |

---

# 18. OR `||`

At least one condition must be true.

```java
int day = 7;

if (day == 6 || day == 7) {
    System.out.println("Weekend");
}
```

Output:

```text
Weekend
```

Truth table:

| A | B | `A || B` |
|---|---|---|
| true | true | true |
| true | false | true |
| false | true | true |
| false | false | false |

---

# 19. NOT `!`

`!` reverses a boolean value.

```java
boolean raining = false;

if (!raining) {
    System.out.println("Go outside");
}
```

Output:

```text
Go outside
```

```text
!true  → false
!false → true
```

---

# 20. Combining Logical Operators

You can combine multiple conditions.

```java
int age = 25;
boolean hasID = true;

if (age >= 18 && hasID) {
    System.out.println("Allowed");
}
```

Output:

```text
Allowed
```

---

# 21. Using `if-else` with User Input

```java
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        int number = sc.nextInt();

        if (number > 0) {
            System.out.println("Positive");
        } else {
            System.out.println("Not Positive");
        }

    }
}
```

Input:

```text
10
```

Output:

```text
Positive
```

---

# 22. Positive, Negative or Zero

```java
int n = -5;

if (n > 0) {
    System.out.println("Positive");
} else if (n < 0) {
    System.out.println("Negative");
} else {
    System.out.println("Zero");
}
```

Output:

```text
Negative
```

---

# 23. Even or Odd

```java
int n = 24;

if (n % 2 == 0) {
    System.out.println("Even");
} else {
    System.out.println("Odd");
}
```

Output:

```text
Even
```

### Important

```text
n % 2 == 0
```

means the number is divisible by 2.

---

# 24. Check Divisibility

Check whether a number is divisible by 5.

```java
int n = 25;

if (n % 5 == 0) {
    System.out.println("Divisible by 5");
} else {
    System.out.println("Not divisible by 5");
}
```

Output:

```text
Divisible by 5
```

---

# 25. Find Greater of Two Numbers

```java
int a = 10;
int b = 20;

if (a > b) {
    System.out.println(a);
} else {
    System.out.println(b);
}
```

Output:

```text
20
```

---

# 26. Find Greater or Equal Numbers

If both numbers can be equal:

```java
int a = 20;
int b = 20;

if (a > b) {
    System.out.println("A is greater");
} else if (b > a) {
    System.out.println("B is greater");
} else {
    System.out.println("Both are equal");
}
```

Output:

```text
Both are equal
```

---

# 27. Find Greatest of Three Numbers

```java
int a = 10;
int b = 25;
int c = 15;

if (a >= b && a >= c) {
    System.out.println(a);
} else if (b >= a && b >= c) {
    System.out.println(b);
} else {
    System.out.println(c);
}
```

Output:

```text
25
```

---

# 28. Check Leap Year

A year is a leap year if:

```text
divisible by 400
OR
divisible by 4 AND not divisible by 100
```

Java:

```java
int year = 2024;

if (year % 400 == 0 || (year % 4 == 0 && year % 100 != 0)) {
    System.out.println("Leap Year");
} else {
    System.out.println("Not a Leap Year");
}
```

Output:

```text
Leap Year
```

---

# 29. Grade Calculator

```java
int marks = 85;

if (marks >= 90) {
    System.out.println("A");
} else if (marks >= 80) {
    System.out.println("B");
} else if (marks >= 70) {
    System.out.println("C");
} else if (marks >= 60) {
    System.out.println("D");
} else {
    System.out.println("F");
}
```

Output:

```text
B
```

---

# 30. Important Order in Conditions

Condition order matters.

Wrong approach:

```java
int marks = 95;

if (marks >= 50) {
    System.out.println("Pass");
} else if (marks >= 90) {
    System.out.println("Excellent");
}
```

Output:

```text
Pass
```

Why?

Because:

```text
95 >= 50
```

is already true.

Java never reaches the second condition.

Correct:

```java
if (marks >= 90) {
    System.out.println("Excellent");
} else if (marks >= 50) {
    System.out.println("Pass");
} else {
    System.out.println("Fail");
}
```

Output:

```text
Excellent
```

### Rule

For ranges, usually check the **more specific / higher condition first**.

---

# 31. Comparing Strings

Do **not** use `==` to compare String contents.

Avoid:

```java
if (name == "Siddhant") {
    System.out.println("Correct");
}
```

Use:

```java
if (name.equals("Siddhant")) {
    System.out.println("Correct");
}
```

Example:

```java
String name = "Siddhant";

if (name.equals("Siddhant")) {
    System.out.println("Matched");
}
```

Output:

```text
Matched
```

---

# 32. Case-Insensitive String Comparison

```java
String answer = "YES";

if (answer.equalsIgnoreCase("yes")) {
    System.out.println("Correct");
}
```

Output:

```text
Correct
```

Both can match:

```text
YES
Yes
yes
yEs
```

---

# 33. Boolean Conditions

A boolean variable can directly be used in an `if`.

```java
boolean isStudent = true;

if (isStudent) {
    System.out.println("Student");
}
```

Output:

```text
Student
```

You do not need:

```java
if (isStudent == true)
```

Although it works, this is cleaner:

```java
if (isStudent)
```

---

# 34. Checking `false`

Instead of:

```java
if (isStudent == false) {
    System.out.println("Not a student");
}
```

you can write:

```java
if (!isStudent) {
    System.out.println("Not a student");
}
```

---

# 35. `else` Belongs to the Nearest `if`

This is an important concept.

Example:

```java
if (a > 0) {

    if (b > 0) {
        System.out.println("Both positive");
    } else {
        System.out.println("B is not positive");
    }

}
```

The `else` belongs to:

```java
if (b > 0)
```

not:

```java
if (a > 0)
```

Use braces `{}` to make the logic clear.

---

# 36. Nested `if-else` Example

Check whether a number is positive/negative and then even/odd.

```java
int n = 10;

if (n > 0) {

    if (n % 2 == 0) {
        System.out.println("Positive Even");
    } else {
        System.out.println("Positive Odd");
    }

} else if (n < 0) {

    if (n % 2 == 0) {
        System.out.println("Negative Even");
    } else {
        System.out.println("Negative Odd");
    }

} else {

    System.out.println("Zero");

}
```

Output:

```text
Positive Even
```

---

# 37. Ternary Operator

For a simple `if-else`, Java also provides the ternary operator.

### Syntax

```java
condition ? valueIfTrue : valueIfFalse;
```

Example:

```java
int age = 20;

String result = age >= 18 ? "Adult" : "Minor";

System.out.println(result);
```

Output:

```text
Adult
```

Equivalent `if-else`:

```java
if (age >= 18) {
    result = "Adult";
} else {
    result = "Minor";
}
```

### Use ternary when:

The logic is simple.

### Use `if-else` when:

The logic is more complex or contains multiple statements.

---

# 38. `if-else` vs Ternary

| `if-else`                   | Ternary                     |
| --------------------------- | --------------------------- |
| Better for complex logic    | Better for simple decisions |
| Can contain many statements | Usually one expression      |
| Easier for beginners        | Shorter syntax              |

---

# 39. Empty `if` Block

Avoid unnecessary empty blocks.

Bad:

```java
if (age >= 18) {

} else {
    System.out.println("Minor");
}
```

Write meaningful logic instead.

---

# 40. Braces `{}`

Always using braces is recommended.

Prefer:

```java
if (age >= 18) {
    System.out.println("Adult");
}
```

Instead of:

```java
if (age >= 18)
    System.out.println("Adult");
```

Both can work, but braces make nested and larger programs safer and easier to read.

---

# 41. Common Mistakes

## Mistake 1: Using `=` instead of `==`

Wrong:

```java
if (a = 10)
```

Correct:

```java
if (a == 10)
```

```text
=   → assignment
==  → comparison
```

---

## Mistake 2: Forgetting parentheses

Wrong:

```java
if age > 18 {
}
```

Correct:

```java
if (age > 18) {
}
```

---

## Mistake 3: Wrong `else-if` order

Wrong:

```java
if (marks >= 50) {
    System.out.println("Pass");
} else if (marks >= 90) {
    System.out.println("A");
}
```

Correct:

```java
if (marks >= 90) {
    System.out.println("A");
} else if (marks >= 50) {
    System.out.println("Pass");
}
```

---

## Mistake 4: Using `==` for String content

Wrong:

```java
if (name == "Siddhant")
```

Correct:

```java
if (name.equals("Siddhant"))
```

---

## Mistake 5: Incorrect logical operator

For both conditions:

```java
&&
```

For either condition:

```java
||
```

Example:

```java
age >= 18 && age <= 60
```

means both must be true.

---

# 42. Quick Revision

```text
if
    → execute code when condition is true

if-else
    → choose between two paths

if-else if-else
    → choose between multiple paths

nested if
    → if inside another if

&&
    → AND
    → both conditions must be true

||
    → OR
    → at least one condition must be true

!
    → NOT
    → reverses boolean value

==
    → equal comparison

!=
    → not equal

>
    → greater than

<
    → less than

>=
    → greater than or equal

<=
    → less than or equal
```

---

# 43. Decision-Making Structure

```text
                    if
                     |
                 condition
                /         \
             true         false
              |             |
           execute      else / else-if
              |             |
              └──────┬──────┘
                     ↓
                  continue
```

---

# 44. If-Else Cheat Sheet

### Basic `if`

```java
if (condition) {
    // code
}
```

### `if-else`

```java
if (condition) {
    // true
} else {
    // false
}
```

### `if-else-if`

```java
if (condition1) {

} else if (condition2) {

} else {

}
```

### Nested `if`

```java
if (condition1) {

    if (condition2) {

    }

}
```

### AND

```java
if (condition1 && condition2) {
}
```

### OR

```java
if (condition1 || condition2) {
}
```

### NOT

```java
if (!condition) {
}
```

### Ternary

```java
result = condition ? value1 : value2;
```

---

# 45. Practice Questions

## Easy

### Q1. Positive or Negative

Take an integer and print:

```text
Positive
```

if it is greater than `0`, otherwise print:

```text
Negative
```

---

### Q2. Even or Odd

Take an integer and print whether it is:

```text
Even
```

or:

```text
Odd
```

---

### Q3. Eligible or Not

Take age as input.

Print:

```text
Eligible
```

if age is `18` or more, otherwise:

```text
Not Eligible
```

---

### Q4. Divisible by 5

Take an integer and check whether it is divisible by `5`.

---

### Q5. Greater of Two Numbers

Take two integers and print the greater number.

---

## Moderate

### Q6. Positive, Negative or Zero

Take an integer and print:

```text
Positive
Negative
Zero
```

---

### Q7. Greatest of Three Numbers

Take three integers and print the greatest number.

---

### Q8. Smallest of Three Numbers

Take three integers and print the smallest number.

---

### Q9. Grade Calculator

Take marks and print:

```text
90+  → A
80-89 → B
70-79 → C
60-69 → D
Below 60 → F
```

---

### Q10. Leap Year

Take a year and determine whether it is a leap year.

---

### Q11. Vowel or Consonant

Take a character and check whether it is a vowel or consonant.

Consider:

```text
a, e, i, o, u
```

and uppercase versions too.

---

### Q12. Divisible by Both

Take a number and check whether it is divisible by both `3` and `5`.

---

## Hard

### Q13. Greatest of Three Without `Math.max()`

Take three integers and find the greatest using only:

```text
if
else if
else
```

---

### Q14. Number Classification

Take an integer and print:

```text
Positive Even
Positive Odd
Negative Even
Negative Odd
Zero
```

Use nested `if-else`.

---

### Q15. Valid Triangle

Take three angles.

A triangle is valid if:

```text
angle1 + angle2 + angle3 == 180
```

and each angle is greater than `0`.

Print:

```text
Valid Triangle
```

or:

```text
Invalid Triangle
```

---

### Q16. Valid Triangle by Sides

Take three side lengths.

A triangle is possible only if:

```text
a + b > c
b + c > a
c + a > b
```

Print whether the triangle is valid.

---

### Q17. Triangle Type

Take three side lengths and determine whether the triangle is:

```text
Equilateral
Isosceles
Scalene
Invalid
```

---

### Q18. Electricity Bill

Take units consumed and calculate the bill using:

```text
0–100 units     → ₹5 per unit
101–200 units   → ₹7 per unit
201–300 units   → ₹10 per unit
Above 300       → ₹15 per unit
```

---

### Q19. Simple Calculator

Take:

```text
number1
number2
operator
```

For example:

```text
10 5 +
```

Perform:

```text
+
-
*
/
%
```

Use `if-else`.

---

### Q20. Login Check

Take:

```text
username
password
```

Check whether both match predefined values.

Print:

```text
Login Successful
```

or:

```text
Invalid Credentials
```

Use String comparison correctly.

---

# 46. Challenge Questions

### Challenge 1 — Second Largest

Take three different integers and print the second largest number.

---

### Challenge 2 — Date Validation

Take:

```text
day
month
year
```

Check whether the date is valid.

Consider different numbers of days in each month and leap years.

---

### Challenge 3 — Quadratic Equation

Take:

```text
a
b
c
```

For:

```text
ax² + bx + c = 0
```

Use the discriminant:

```text
D = b² - 4ac
```

Determine whether the equation has:

```text
Two real roots
One real root
No real roots
```

---

# 47. Final Revision Questions

Try solving these **without looking at the notes**.

1. What is the difference between `if` and `if-else`?
2. What is an `else-if` ladder?
3. What is nested `if`?
4. What is the difference between `&&` and `||`?
5. What does `!` do?
6. What is the difference between `=` and `==`?
7. Why should Strings generally be compared using `.equals()`?
8. What happens when multiple `else-if` conditions are true?
9. Which `else-if` condition executes?
10. Can an `if` exist without an `else`?
11. Can `else` exist without `if`?
12. How many `else` blocks can one `if-else` chain have?
13. How can you check whether a number is even?
14. How do you check whether a number is divisible by both `3` and `5`?
15. What is the ternary operator?
16. When should you prefer `if-else` over ternary?
17. Why does the order of `else-if` conditions matter?
18. What is the difference between nested `if` and `else-if`?
19. How do you check whether a character is a vowel?
20. How would you classify a number as positive/negative and even/odd?
