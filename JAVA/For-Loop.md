# Java For Loop

## 1. What is a `for` Loop?

A `for` loop is used to **repeat a block of code multiple times**.

It is especially useful when we know:

* Where the loop should start
* Where the loop should stop
* How the loop variable should change

Example:

```java
for (int i = 1; i <= 5; i++) {
    System.out.println(i);
}
```

Output:

```text
1
2
3
4
5
```

---

# 2. Why Use a `for` Loop?

Without a loop:

```java
System.out.println(1);
System.out.println(2);
System.out.println(3);
System.out.println(4);
System.out.println(5);
```

With a loop:

```java
for (int i = 1; i <= 5; i++) {
    System.out.println(i);
}
```

The `for` loop makes repetitive code shorter and easier to manage.

---

# 3. Basic Syntax

```java
for (initialization; condition; update) {

    // code
}
```

Example:

```java
for (int i = 1; i <= 5; i++) {
    System.out.println(i);
}
```

The three parts are:

```text
initialization
       ↓
   condition
       ↓
      body
       ↓
     update
       ↓
   condition
       ↓
     repeat
```

---

# 4. Understanding the Three Parts

Consider:

```java
for (int i = 1; i <= 5; i++) {
    System.out.println(i);
}
```

### 1. Initialization

```java
int i = 1
```

Runs **once**, before the loop starts.

It sets the starting value.

---

### 2. Condition

```java
i <= 5
```

Checked before every iteration.

If `true`:

```text
run the loop
```

If `false`:

```text
stop the loop
```

---

### 3. Update

```java
i++
```

Runs after every iteration.

It changes the value of `i`.

---

# 5. Complete Execution

Code:

```java
for (int i = 1; i <= 5; i++) {
    System.out.println(i);
}
```

Execution:

```text
i = 1
1 <= 5 → true → print 1
i++ → 2

2 <= 5 → true → print 2
i++ → 3

3 <= 5 → true → print 3
i++ → 4

4 <= 5 → true → print 4
i++ → 5

5 <= 5 → true → print 5
i++ → 6

6 <= 5 → false → stop
```

---

# 6. Print Numbers from 1 to 10

```java
for (int i = 1; i <= 10; i++) {
    System.out.println(i);
}
```

Output:

```text
1
2
3
4
5
6
7
8
9
10
```

---

# 7. Print Numbers from 10 to 1

Use decrement:

```java
for (int i = 10; i >= 1; i--) {
    System.out.println(i);
}
```

Output:

```text
10
9
8
7
6
5
4
3
2
1
```

---

# 8. Print Even Numbers

```java
for (int i = 2; i <= 10; i += 2) {
    System.out.println(i);
}
```

Output:

```text
2
4
6
8
10
```

---

# 9. Print Odd Numbers

```java
for (int i = 1; i <= 10; i += 2) {
    System.out.println(i);
}
```

Output:

```text
1
3
5
7
9
```

---

# 10. Increment by 2

```java
for (int i = 2; i <= 20; i += 2) {
    System.out.println(i);
}
```

Output:

```text
2
4
6
8
10
12
14
16
18
20
```

`i += 2` means:

```java
i = i + 2;
```

---

# 11. Increment by Any Number

```java
for (int i = 1; i <= 20; i += 5) {
    System.out.println(i);
}
```

Output:

```text
1
6
11
16
```

---

# 12. Decrement by Any Number

```java
for (int i = 20; i >= 1; i -= 5) {
    System.out.println(i);
}
```

Output:

```text
20
15
10
5
```

---

# 13. `for` Loop with User Input

```java
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();

        for (int i = 1; i <= n; i++) {
            System.out.println(i);
        }
    }
}
```

Input:

```text
5
```

Output:

```text
1
2
3
4
5
```

---

# 14. Sum from 1 to N

```java
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();

        int sum = 0;

        for (int i = 1; i <= n; i++) {
            sum += i;
        }

        System.out.println(sum);
    }
}
```

Input:

```text
5
```

Output:

```text
15
```

Because:

```text
1 + 2 + 3 + 4 + 5 = 15
```

---

# 15. Sum of Even Numbers

```java
int n = 10;
int sum = 0;

for (int i = 2; i <= n; i += 2) {
    sum += i;
}

System.out.println(sum);
```

Output:

```text
30
```

Because:

```text
2 + 4 + 6 + 8 + 10 = 30
```

---

# 16. Sum of Odd Numbers

```java
int n = 10;
int sum = 0;

for (int i = 1; i <= n; i += 2) {
    sum += i;
}

System.out.println(sum);
```

Output:

```text
25
```

---

# 17. Multiplication Table

```java
int n = 5;

for (int i = 1; i <= 10; i++) {
    System.out.println(n + " x " + i + " = " + (n * i));
}
```

Output:

```text
5 x 1 = 5
5 x 2 = 10
5 x 3 = 15
5 x 4 = 20
5 x 5 = 25
5 x 6 = 30
5 x 7 = 35
5 x 8 = 40
5 x 9 = 45
5 x 10 = 50
```

---

# 18. Factorial Using `for`

```java
int n = 5;
long factorial = 1;

for (int i = 1; i <= n; i++) {
    factorial *= i;
}

System.out.println(factorial);
```

Output:

```text
120
```

---

# 19. `for` Loop with Multiple Variables

You can initialize more than one variable.

```java
for (int i = 1, j = 5; i <= 5; i++, j--) {
    System.out.println(i + " " + j);
}
```

Output:

```text
1 5
2 4
3 3
4 2
5 1
```

---

# 20. Multiple Conditions

A `for` loop can use logical conditions.

```java
for (int i = 1; i <= 10 && i != 7; i++) {
    System.out.println(i);
}
```

Output:

```text
1
2
3
4
5
6
```

The loop stops when:

```text
i != 7
```

becomes false.

---

# 21. Infinite `for` Loop

A `for` loop can also be infinite.

```java
for (;;) {
    System.out.println("Hello");
}
```

There is:

```text
no initialization
no condition
no update
```

So the loop continues forever unless stopped using `break` or the program is terminated.

---

# 22. Empty Parts of a `for` Loop

All three parts are optional.

For example:

```java
int i = 1;

for (; i <= 5; ) {
    System.out.println(i);
    i++;
}
```

This works, but it is usually clearer to use a normal `for` loop or a `while` loop.

---

# 23. `break`

`break` immediately stops the loop.

```java
for (int i = 1; i <= 10; i++) {

    if (i == 5) {
        break;
    }

    System.out.println(i);
}
```

Output:

```text
1
2
3
4
```

When `i == 5`, the loop stops.

---

# 24. `continue`

`continue` skips the current iteration and moves to the next iteration.

Example:

```java
for (int i = 1; i <= 5; i++) {

    if (i == 3) {
        continue;
    }

    System.out.println(i);
}
```

Output:

```text
1
2
4
5
```

`3` is skipped.

---

# 25. `break` vs `continue`

| `break`               | `continue`              |
| --------------------- | ----------------------- |
| Stops the entire loop | Skips current iteration |
| Loop ends             | Loop continues          |
| Used to exit          | Used to skip            |

---

# 26. Nested `for` Loop

A loop inside another loop is called a **nested loop**.

Example:

```java
for (int i = 1; i <= 3; i++) {

    for (int j = 1; j <= 3; j++) {
        System.out.println(i + " " + j);
    }
}
```

Output:

```text
1 1
1 2
1 3
2 1
2 2
2 3
3 1
3 2
3 3
```

The inner loop completes all its iterations for every iteration of the outer loop.

---

# 27. Nested Loop Execution

For:

```java
for (int i = 1; i <= 3; i++) {

    for (int j = 1; j <= 3; j++) {
        System.out.println(i + " " + j);
    }
}
```

Execution:

```text
i = 1
    j = 1
    j = 2
    j = 3

i = 2
    j = 1
    j = 2
    j = 3

i = 3
    j = 1
    j = 2
    j = 3
```

Total inner-loop executions:

```text
3 × 3 = 9
```

---

# 28. Nested Loop for Repetition

Example:

```java
for (int i = 1; i <= 3; i++) {

    for (int j = 1; j <= 5; j++) {
        System.out.print("* ");
    }

    System.out.println();
}
```

Output:

```text
* * * * *
* * * * *
* * * * *
```

This concept is very important for **pattern printing**.

---

# 29. `System.out.print()` vs `println()` in Loops

### `print()`

```java
for (int i = 1; i <= 5; i++) {
    System.out.print(i + " ");
}
```

Output:

```text
1 2 3 4 5
```

### `println()`

```java
for (int i = 1; i <= 5; i++) {
    System.out.println(i);
}
```

Output:

```text
1
2
3
4
5
```

---

# 30. Nested Loop for Rows and Columns

A useful way to understand nested loops:

```java
for (int row = 1; row <= 3; row++) {

    for (int col = 1; col <= 4; col++) {
        System.out.print("* ");
    }

    System.out.println();
}
```

Output:

```text
* * * *
* * * *
* * * *
```

Here:

```text
row → controls number of rows
col → controls number of columns
```

---

# 31. `for` Loop with `if`

Loops and conditions are commonly used together.

Example:

```java
for (int i = 1; i <= 10; i++) {

    if (i % 2 == 0) {
        System.out.println(i);
    }
}
```

Output:

```text
2
4
6
8
10
```

---

# 32. Find Numbers Divisible by 3

```java
for (int i = 1; i <= 20; i++) {

    if (i % 3 == 0) {
        System.out.println(i);
    }
}
```

Output:

```text
3
6
9
12
15
18
```

---

# 33. Count Numbers Matching a Condition

Count even numbers from `1` to `N`.

```java
int n = 10;
int count = 0;

for (int i = 1; i <= n; i++) {

    if (i % 2 == 0) {
        count++;
    }
}

System.out.println(count);
```

Output:

```text
5
```

---

# 34. Find Largest Number

Suppose we have:

```text
10 25 15 30 20
```

We can find the largest using a loop.

```java
int[] numbers = {10, 25, 15, 30, 20};

int largest = numbers[0];

for (int i = 1; i < numbers.length; i++) {

    if (numbers[i] > largest) {
        largest = numbers[i];
    }
}

System.out.println(largest);
```

Output:

```text
30
```

> Arrays will be covered in detail later.

---

# 35. For Loop vs While Loop

Both can perform repetition.

### `while`

```java
int i = 1;

while (i <= 5) {
    System.out.println(i);
    i++;
}
```

### `for`

```java
for (int i = 1; i <= 5; i++) {
    System.out.println(i);
}
```

Both produce:

```text
1
2
3
4
5
```

---

# 36. When to Use `for`

Use `for` when the loop has a clear counter or range.

Example:

```java
for (int i = 1; i <= 100; i++) {
}
```

Good for:

* Counting
* Ranges
* Repeating a fixed number of times
* Pattern printing
* Array traversal
* Nested loops

---

# 37. When to Use `while`

Use `while` when the number of iterations may not be known beforehand.

Example:

```java
while (n != 0) {
    n = sc.nextInt();
}
```

Good for:

* Sentinel-controlled input
* Repeating until a condition changes
* Digit processing
* Situations where the stopping condition is more important than the counter

---

# 38. `for` vs `while`

| `for`                                            | `while`                             |
| ------------------------------------------------ | ----------------------------------- |
| Good for known ranges                            | Good for condition-based repetition |
| Initialization, condition and update in one line | Usually written separately          |
| Common for counting                              | Common when iterations are unknown  |
| Excellent for patterns                           | Excellent for digit problems        |
| Excellent for arrays                             | Useful for input loops              |

---

# 39. Scope of Loop Variable

A variable declared inside a `for` loop normally exists only inside that loop.

```java
for (int i = 1; i <= 5; i++) {
    System.out.println(i);
}
```

You cannot normally use `i` here:

```java
System.out.println(i);
```

because `i` was declared inside the loop.

---

# 40. Declaring the Variable Outside

If you need the variable after the loop:

```java
int i;

for (i = 1; i <= 5; i++) {
    System.out.println(i);
}

System.out.println(i);
```

Output:

```text
1
2
3
4
5
6
```

After the loop:

```text
i = 6
```

---

# 41. Common Mistakes

## Mistake 1: Using `;` after the `for`

Wrong:

```java
for (int i = 1; i <= 5; i++);
{
    System.out.println(i);
}
```

The semicolon ends the loop.

Correct:

```java
for (int i = 1; i <= 5; i++) {
    System.out.println(i);
}
```

---

## Mistake 2: Wrong Condition

To print `1` to `10`:

```java
i <= 10
```

includes `10`.

```java
i < 10
```

stops at `9`.

---

## Mistake 3: Wrong Update Direction

Wrong:

```java
for (int i = 10; i >= 1; i++) {
}
```

`i` keeps increasing.

Correct:

```java
for (int i = 10; i >= 1; i--) {
}
```

---

## Mistake 4: Infinite Loop

Example:

```java
for (int i = 1; i <= 10; ) {
    System.out.println(i);
}
```

`i` never changes.

Correct:

```java
for (int i = 1; i <= 10; i++) {
    System.out.println(i);
}
```

---

## Mistake 5: Off-by-One Error

These are different:

```java
i < 10
```

and:

```java
i <= 10
```

Remember:

```text
<  → does not include 10
<= → includes 10
```

---

# 42. Important Operator Shortcuts

Instead of:

```java
i = i + 1;
```

use:

```java
i++;
```

Instead of:

```java
i = i - 1;
```

use:

```java
i--;
```

Instead of:

```java
i = i + 2;
```

use:

```java
i += 2;
```

Instead of:

```java
i = i - 2;
```

use:

```java
i -= 2;
```

---

# 43. Character Loop

You can also loop through characters.

```java
for (char ch = 'A'; ch <= 'Z'; ch++) {
    System.out.print(ch + " ");
}
```

Output:

```text
A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
```

Similarly:

```java
for (char ch = 'a'; ch <= 'z'; ch++) {
    System.out.print(ch + " ");
}
```

---

# 44. ASCII / Unicode Character Increment

Characters can be incremented.

```java
char ch = 'A';

ch++;

System.out.println(ch);
```

Output:

```text
B
```

This works because characters have numeric Unicode values.

---

# 45. Reverse Counting

```java
for (int i = 20; i >= 1; i -= 2) {
    System.out.println(i);
}
```

Output:

```text
20
18
16
14
12
10
8
6
4
2
```

---

# 46. Nested Loop with `break`

`break` inside the inner loop normally stops the **inner loop**.

```java
for (int i = 1; i <= 3; i++) {

    for (int j = 1; j <= 5; j++) {

        if (j == 3) {
            break;
        }

        System.out.println(i + " " + j);
    }
}
```

Output:

```text
1 1
1 2
2 1
2 2
3 1
3 2
```

---

# 47. Nested Loop with `continue`

```java
for (int i = 1; i <= 2; i++) {

    for (int j = 1; j <= 4; j++) {

        if (j == 2) {
            continue;
        }

        System.out.println(i + " " + j);
    }
}
```

Output:

```text
1 1
1 3
1 4
2 1
2 3
2 4
```

---

# 48. Multiple Initialization and Update

```java
for (int i = 1, j = 10; i <= 5; i++, j--) {
    System.out.println(i + " " + j);
}
```

Output:

```text
1 10
2 9
3 8
4 7
5 6
```

---

# 49. Important `for` Loop Pattern

Memorize this:

```java
for (int i = start; i <= end; i++) {

}
```

Example:

```java
for (int i = 1; i <= 10; i++) {

}
```

For reverse:

```java
for (int i = end; i >= start; i--) {

}
```

Example:

```java
for (int i = 10; i >= 1; i--) {

}
```

---

# 50. Pattern Printing Connection

Nested `for` loops are extremely important for patterns.

Example:

```java
for (int row = 1; row <= 3; row++) {

    for (int col = 1; col <= 5; col++) {
        System.out.print("* ");
    }

    System.out.println();
}
```

Output:

```text
* * * * *
* * * * *
* * * * *
```

The next topic, **Patterns**, will use this concept heavily.

---

# 51. Quick Revision

```text
for loop
    → repeat code

Syntax:
for (initialization; condition; update) {
    // code
}
```

Execution order:

```text
Initialization
      ↓
Condition
      ↓
Body
      ↓
Update
      ↓
Condition
      ↓
Repeat
```

Important:

```text
i++       → i = i + 1
i--       → i = i - 1
i += 2    → i = i + 2
i -= 2    → i = i - 2
```

---

# 52. Most Important Patterns

### Print 1 to N

```java
for (int i = 1; i <= n; i++) {
    System.out.println(i);
}
```

### Print N to 1

```java
for (int i = n; i >= 1; i--) {
    System.out.println(i);
}
```

### Print Even Numbers

```java
for (int i = 2; i <= n; i += 2) {
    System.out.println(i);
}
```

### Print Odd Numbers

```java
for (int i = 1; i <= n; i += 2) {
    System.out.println(i);
}
```

### Sum 1 to N

```java
int sum = 0;

for (int i = 1; i <= n; i++) {
    sum += i;
}
```

### Factorial

```java
long factorial = 1;

for (int i = 1; i <= n; i++) {
    factorial *= i;
}
```

### Nested Loop

```java
for (int i = 1; i <= rows; i++) {

    for (int j = 1; j <= columns; j++) {

    }
}
```

---

# 53. Practice Questions

## Easy

### Q1. Print 1 to N

Take `N` as input and print numbers from `1` to `N`.

---

### Q2. Print N to 1

Take `N` as input and print numbers from `N` to `1`.

---

### Q3. Print Even Numbers

Print all even numbers from `1` to `N`.

---

### Q4. Print Odd Numbers

Print all odd numbers from `1` to `N`.

---

### Q5. Print Multiples

Take a number and print its first 10 multiples.

---

### Q6. Sum from 1 to N

Take `N` and calculate:

```text
1 + 2 + 3 + ... + N
```

---

### Q7. Factorial

Take `N` and calculate `N!`.

---

### Q8. Multiplication Table

Take a number and print its table from `1` to `10`.

---

## Moderate

### Q9. Count Even Numbers

Count how many even numbers exist from `1` to `N`.

---

### Q10. Count Odd Numbers

Count how many odd numbers exist from `1` to `N`.

---

### Q11. Sum of Even Numbers

Find the sum of all even numbers from `1` to `N`.

---

### Q12. Sum of Odd Numbers

Find the sum of all odd numbers from `1` to `N`.

---

### Q13. Sum of Squares

Calculate:

```text
1² + 2² + 3² + ... + N²
```

Example:

```text
Input:
3

Output:
14
```

Because:

```text
1² + 2² + 3² = 14
```

---

### Q14. Count Numbers Divisible by 3

Count numbers between `1` and `N` that are divisible by `3`.

---

### Q15. Print Numbers in a Range

Take `start` and `end` as input and print all numbers between them.

Example:

```text
Input:
5 10

Output:
5
6
7
8
9
10
```

---

### Q16. Print Characters

Print all uppercase English letters:

```text
A B C ... Z
```

using a `for` loop.

---

## Hard

### Q17. Reverse a Number

Take an integer and print its reverse.

Example:

```text
Input:
583

Output:
385
```

---

### Q18. Palindrome Number

Check whether a number is a palindrome.

---

### Q19. Sum of Digits

Find the sum of all digits of a number.

Example:

```text
Input:
58321

Output:
19
```

---

### Q20. Count Digits

Count the number of digits in an integer.

---

### Q21. Largest Digit

Find the largest digit in a number.

Example:

```text
Input:
58321

Output:
8
```

---

### Q22. Smallest Digit

Find the smallest digit in a number.

---

### Q23. Product of Digits

Find the product of all digits.

Example:

```text
Input:
1234

Output:
24
```

---

### Q24. Count a Digit

Take a number and a digit and count how many times the digit occurs.

Example:

```text
Input:
1223342
2

Output:
3
```

---

### Q25. Prime Number

Check whether a number is prime.

Example:

```text
Input:
17

Output:
Prime
```

---

### Q26. Count Factors

Count the number of positive factors of a number.

Example:

```text
Input:
12

Output:
6
```

---

### Q27. Sum of Factors

Find the sum of all positive factors of a number.

Example:

```text
Input:
6

Output:
12
```

---

# 54. Nested Loop Practice

## Moderate

### Q28. Print a Rectangle

Take `rows` and `columns` and print:

```text
* * * *
* * * *
* * * *
```

---

### Q29. Print Number Grid

Print:

```text
1 2 3
1 2 3
1 2 3
```

using nested loops.

---

### Q30. Print Row Numbers

Print:

```text
1 1 1
2 2 2
3 3 3
```

using nested loops.

---

# 55. Challenge Questions

### Q31. GCD / HCF

Take two numbers and find their GCD using a loop.

Example:

```text
Input:
24 36

Output:
12
```

---

### Q32. LCM

Take two numbers and find their LCM.

Example:

```text
Input:
4 6

Output:
12
```

---

### Q33. Fibonacci Series

Print the first `N` Fibonacci numbers.

Example:

```text
Input:
7

Output:
0 1 1 2 3 5 8
```

---

### Q34. Armstrong Number

Check whether a three-digit number is an Armstrong number.

Example:

```text
153
```

Because:

```text
1³ + 5³ + 3³ = 153
```

---

### Q35. Perfect Number

Check whether a number is a perfect number.

Example:

```text
6
```

Because:

```text
1 + 2 + 3 = 6
```

---

### Q36. Strong Number

Check whether a number is a Strong number.

A number is Strong if the sum of factorials of its digits equals the number.

Example:

```text
145
```

Because:

```text
1! + 4! + 5!
= 1 + 24 + 120
= 145
```

---

# 56. Final Revision Questions

1. What is a `for` loop?
2. What are the three parts of a `for` loop?
3. Which part runs only once?
4. When is the condition checked?
5. When does the update happen?
6. What happens when the condition becomes false?
7. What is the difference between `i++` and `i += 2`?
8. How do you print numbers from `N` to `1`?
9. How do you print only even numbers?
10. How do you print only odd numbers?
11. What is an infinite `for` loop?
12. What does `break` do?
13. What does `continue` do?
14. What is a nested loop?
15. How many times does an inner loop execute in a nested loop?
16. What is the difference between `for` and `while`?
17. Why is `for` useful for pattern printing?
18. What happens if you put a semicolon immediately after `for(...)`?
19. What is an off-by-one error?
20. Can the initialization, condition, and update sections of a `for` loop be empty?
21. Can a `for` loop have multiple variables?
22. How do you calculate factorial using a `for` loop?
23. How do you calculate the sum from `1` to `N`?
24. How do you reverse a number using a loop?
25. How do you check whether a number is prime?
26. How do nested loops help in pattern printing?
27. What is the difference between `print()` and `println()` inside a loop?
28. What is the scope of a variable declared inside a `for` loop?

---

# 57. Final Cheat Sheet

```java
// 1 to N
for (int i = 1; i <= n; i++) {
    System.out.println(i);
}
```

```java
// N to 1
for (int i = n; i >= 1; i--) {
    System.out.println(i);
}
```

```java
// Even numbers
for (int i = 2; i <= n; i += 2) {
    System.out.println(i);
}
```

```java
// Odd numbers
for (int i = 1; i <= n; i += 2) {
    System.out.println(i);
}
```

```java
// Sum
int sum = 0;

for (int i = 1; i <= n; i++) {
    sum += i;
}
```

```java
// Factorial
long factorial = 1;

for (int i = 1; i <= n; i++) {
    factorial *= i;
}
```

```java
// Nested loop
for (int i = 1; i <= rows; i++) {

    for (int j = 1; j <= columns; j++) {

    }
}
```

```java
// break
for (int i = 1; i <= n; i++) {

    if (condition) {
        break;
    }
}
```

```java
// continue
for (int i = 1; i <= n; i++) {

    if (condition) {
        continue;
    }

}
```

### Core Structure

```text
for (start; condition; update)
        ↓
      repeat
```

```text
Initialization
      ↓
Condition
      ↓
Body
      ↓
Update
      ↓
Condition
      ↓
Repeat
```

**Next Topic: `06-Patterns.md`**
