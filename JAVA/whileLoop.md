# Java While Loop

## 1. What is a Loop?

A **loop** is used to execute the same block of code repeatedly.

Instead of writing:

```java
System.out.println(1);
System.out.println(2);
System.out.println(3);
System.out.println(4);
System.out.println(5);
```

we can use a loop:

```java
int i = 1;

while (i <= 5) {
    System.out.println(i);
    i++;
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

# 2. Why Use Loops?

Loops are useful when we need to repeat something many times.

Examples:

* Print numbers from `1` to `100`
* Print a message 10 times
* Find the sum of numbers
* Count digits of a number
* Reverse a number
* Check whether a number is palindrome
* Repeat an operation until a condition becomes false

---

# 3. Types of Loops in Java

Java mainly provides:

```text
1. while loop
2. for loop
3. do-while loop
```

In this file:

```text
while loop
```

is covered in detail.

---

# 4. What is a `while` Loop?

A `while` loop repeatedly executes a block of code **while a condition is true**.

### Syntax

```java
while (condition) {
    // code
}
```

Example:

```java
int i = 1;

while (i <= 5) {
    System.out.println(i);
    i++;
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

# 5. How `while` Loop Works

A while loop usually has three important parts:

```text
Initialization
      ↓
   Condition
      ↓
   Loop Body
      ↓
    Update
      ↓
   Condition
      ↓
    repeat
```

Example:

```java
int i = 1;          // Initialization

while (i <= 5) {    // Condition

    System.out.println(i);  // Body

    i++;            // Update
}
```

---

# 6. Initialization

Initialization gives the loop variable its starting value.

```java
int i = 1;
```

Here:

```text
i starts from 1
```

---

# 7. Condition

The condition decides whether the loop should continue.

```java
while (i <= 5)
```

As long as:

```text
i <= 5
```

is true, the loop continues.

When it becomes false, the loop stops.

---

# 8. Update

The update changes the loop variable.

```java
i++;
```

This means:

```java
i = i + 1;
```

Without an update, the loop may never stop.

---

# 9. Complete While Loop

```java
int i = 1;

while (i <= 5) {
    System.out.println(i);
    i++;
}
```

Execution:

```text
i = 1 → print 1 → i becomes 2
i = 2 → print 2 → i becomes 3
i = 3 → print 3 → i becomes 4
i = 4 → print 4 → i becomes 5
i = 5 → print 5 → i becomes 6
i = 6 → condition false → stop
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

# 10. Print Numbers from 1 to 10

```java
int i = 1;

while (i <= 10) {
    System.out.println(i);
    i++;
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

# 11. Print Numbers from 10 to 1

Use decrement:

```java
int i = 10;

while (i >= 1) {
    System.out.println(i);
    i--;
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

# 12. Increment

```java
i++;
```

is the same as:

```java
i = i + 1;
```

Example:

```java
int i = 1;

while (i <= 5) {
    System.out.println(i);
    i++;
}
```

---

# 13. Decrement

```java
i--;
```

is the same as:

```java
i = i - 1;
```

Example:

```java
int i = 5;

while (i >= 1) {
    System.out.println(i);
    i--;
}
```

---

# 14. Increment by More Than 1

You can increase by any value.

```java
int i = 2;

while (i <= 10) {
    System.out.println(i);
    i += 2;
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

`i += 2` means:

```java
i = i + 2;
```

---

# 15. Decrement by More Than 1

```java
int i = 10;

while (i >= 2) {
    System.out.println(i);
    i -= 2;
}
```

Output:

```text
10
8
6
4
2
```

---

# 16. Print Odd Numbers

```java
int i = 1;

while (i <= 10) {
    System.out.println(i);
    i += 2;
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

# 17. Print Even Numbers

```java
int i = 2;

while (i <= 10) {
    System.out.println(i);
    i += 2;
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

# 18. Print Multiples of a Number

Print multiples of `5` from `5` to `50`.

```java
int i = 5;

while (i <= 50) {
    System.out.println(i);
    i += 5;
}
```

Output:

```text
5
10
15
20
25
30
35
40
45
50
```

---

# 19. Taking the Limit as Input

```java
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();

        int i = 1;

        while (i <= n) {
            System.out.println(i);
            i++;
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

# 20. Sum of Numbers from 1 to N

To calculate:

```text
1 + 2 + 3 + ... + N
```

use a variable to store the sum.

```java
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();

        int i = 1;
        int sum = 0;

        while (i <= n) {
            sum = sum + i;
            i++;
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

# 21. Understanding `sum`

Initially:

```java
int sum = 0;
```

For `n = 5`:

```text
sum = 0

i = 1 → sum = 1
i = 2 → sum = 3
i = 3 → sum = 6
i = 4 → sum = 10
i = 5 → sum = 15
```

Final:

```text
sum = 15
```

---

# 22. Product of Numbers from 1 to N

The product:

```text
1 × 2 × 3 × ... × N
```

is called **factorial** when starting from `1`.

Example:

```text
5! = 1 × 2 × 3 × 4 × 5 = 120
```

Java:

```java
int n = 5;

int i = 1;
int product = 1;

while (i <= n) {
    product = product * i;
    i++;
}

System.out.println(product);
```

Output:

```text
120
```

---

# 23. Factorial

### Formula

```text
n! = n × (n-1) × (n-2) × ... × 1
```

Example:

```text
5! = 120
```

Code:

```java
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();

        int i = 1;
        long factorial = 1;

        while (i <= n) {
            factorial = factorial * i;
            i++;
        }

        System.out.println(factorial);
    }
}
```

---

# 24. Counting

A loop can be used to count something.

Example: count numbers from `1` to `10`.

```java
int i = 1;
int count = 0;

while (i <= 10) {
    count++;
    i++;
}

System.out.println(count);
```

Output:

```text
10
```

---

# 25. Count Even Numbers

Count even numbers from `1` to `10`.

```java
int i = 1;
int count = 0;

while (i <= 10) {

    if (i % 2 == 0) {
        count++;
    }

    i++;
}

System.out.println(count);
```

Output:

```text
5
```

---

# 26. Count Odd Numbers

```java
int i = 1;
int count = 0;

while (i <= 10) {

    if (i % 2 != 0) {
        count++;
    }

    i++;
}

System.out.println(count);
```

Output:

```text
5
```

---

# 27. Sum of Even Numbers

Find the sum of even numbers from `1` to `10`.

```java
int i = 1;
int sum = 0;

while (i <= 10) {

    if (i % 2 == 0) {
        sum = sum + i;
    }

    i++;
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

# 28. Sum of Odd Numbers

```java
int i = 1;
int sum = 0;

while (i <= 10) {

    if (i % 2 != 0) {
        sum = sum + i;
    }

    i++;
}

System.out.println(sum);
```

Output:

```text
25
```

---

# 29. Multiplication Table

Print the table of `5`.

```java
int n = 5;
int i = 1;

while (i <= 10) {
    System.out.println(n * i);
    i++;
}
```

Output:

```text
5
10
15
20
25
30
35
40
45
50
```

To print it in proper format:

```java
int n = 5;
int i = 1;

while (i <= 10) {
    System.out.println(n + " x " + i + " = " + (n * i));
    i++;
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

# 30. Digits of a Number

The `%` and `/` operators are very useful for working with digits.

For:

```text
583
```

Last digit:

```java
583 % 10
```

gives:

```text
3
```

Remove the last digit:

```java
583 / 10
```

gives:

```text
58
```

Integer division removes the decimal part.

---

# 31. Extract Digits Using `while`

```java
int n = 583;

while (n > 0) {

    int digit = n % 10;

    System.out.println(digit);

    n = n / 10;
}
```

Output:

```text
3
8
5
```

Digits are processed from **right to left**.

---

# 32. Count Digits

```java
int n = 58321;

int count = 0;

while (n > 0) {
    count++;
    n = n / 10;
}

System.out.println(count);
```

Output:

```text
5
```

---

# 33. Important Zero Case in Digit Problems

The simple code:

```java
while (n > 0)
```

does not execute even once when:

```text
n = 0
```

If the input can be `0`, handle it separately.

```java
int n = 0;

if (n == 0) {
    System.out.println(1);
} else {

    int count = 0;

    while (n > 0) {
        count++;
        n = n / 10;
    }

    System.out.println(count);
}
```

---

# 34. Sum of Digits

Example:

```text
583
```

Sum:

```text
5 + 8 + 3 = 16
```

Code:

```java
int n = 583;
int sum = 0;

while (n > 0) {

    int digit = n % 10;

    sum = sum + digit;

    n = n / 10;
}

System.out.println(sum);
```

Output:

```text
16
```

---

# 35. Reverse a Number

Example:

```text
583 → 385
```

Logic:

```text
digit = n % 10
reverse = reverse × 10 + digit
n = n / 10
```

Code:

```java
int n = 583;
int reverse = 0;

while (n > 0) {

    int digit = n % 10;

    reverse = reverse * 10 + digit;

    n = n / 10;
}

System.out.println(reverse);
```

Output:

```text
385
```

---

# 36. Reverse Number Step-by-Step

For:

```text
n = 583
```

```text
reverse = 0
```

### First iteration

```text
digit = 3
reverse = 0 × 10 + 3
reverse = 3
n = 58
```

### Second iteration

```text
digit = 8
reverse = 3 × 10 + 8
reverse = 38
n = 5
```

### Third iteration

```text
digit = 5
reverse = 38 × 10 + 5
reverse = 385
n = 0
```

Loop stops.

---

# 37. Palindrome Number

A number is a palindrome if it remains the same when reversed.

Examples:

```text
121 → 121  → Palindrome
1331 → 1331 → Palindrome
123 → 321   → Not Palindrome
```

Code:

```java
int n = 121;

int original = n;
int reverse = 0;

while (n > 0) {

    int digit = n % 10;

    reverse = reverse * 10 + digit;

    n = n / 10;
}

if (original == reverse) {
    System.out.println("Palindrome");
} else {
    System.out.println("Not Palindrome");
}
```

Output:

```text
Palindrome
```

---

# 38. Why Store the Original Number?

The loop changes `n`:

```java
n = n / 10;
```

Eventually:

```text
n = 0
```

So save the original value first:

```java
int original = n;
```

Then compare:

```java
if (original == reverse)
```

---

# 39. Find First Digit

For a positive number, repeatedly divide by `10` until only one digit remains.

```java
int n = 58321;

while (n >= 10) {
    n = n / 10;
}

System.out.println(n);
```

Output:

```text
5
```

---

# 40. Find Last Digit

Use `% 10`.

```java
int n = 58321;

int lastDigit = n % 10;

System.out.println(lastDigit);
```

Output:

```text
1
```

---

# 41. Sum Until a Condition

You can use a condition inside a loop.

Example:

```java
int i = 1;
int sum = 0;

while (i <= 10) {

    if (i % 2 == 0) {
        sum += i;
    }

    i++;
}

System.out.println(sum);
```

Output:

```text
30
```

---

# 42. `break`

`break` immediately stops the loop.

Example:

```java
int i = 1;

while (i <= 10) {

    if (i == 5) {
        break;
    }

    System.out.println(i);
    i++;
}
```

Output:

```text
1
2
3
4
```

When:

```text
i == 5
```

`break` stops the loop.

---

# 43. `continue`

`continue` skips the current iteration and moves to the next iteration.

Example:

```java
int i = 1;

while (i <= 5) {

    if (i == 3) {
        i++;
        continue;
    }

    System.out.println(i);
    i++;
}
```

Output:

```text
1
2
4
5
```

The value `3` is skipped.

### Important

With a `while` loop, make sure the loop variable is updated before `continue`, otherwise you can accidentally create an infinite loop.

---

# 44. `break` vs `continue`

| `break`               | `continue`              |
| --------------------- | ----------------------- |
| Stops the entire loop | Skips current iteration |
| Loop ends immediately | Loop continues          |
| Used to exit a loop   | Used to skip something  |

---

# 45. Infinite Loop

An infinite loop never stops.

Example:

```java
int i = 1;

while (i <= 5) {
    System.out.println(i);
}
```

This is an infinite loop because `i` never changes.

The condition always remains:

```text
1 <= 5
```

---

# 46. How to Avoid Infinite Loops

Make sure the condition can eventually become false.

Correct:

```java
int i = 1;

while (i <= 5) {
    System.out.println(i);
    i++;
}
```

Here:

```text
1 → 2 → 3 → 4 → 5 → 6
```

At `6`:

```text
6 <= 5
```

is false.

---

# 47. Common Infinite Loop Mistake

Wrong:

```java
int i = 10;

while (i >= 1) {
    System.out.println(i);
    i++;
}
```

`i` increases:

```text
10 → 11 → 12 → 13 → ...
```

So:

```text
i >= 1
```

never becomes false.

Correct:

```java
int i = 10;

while (i >= 1) {
    System.out.println(i);
    i--;
}
```

---

# 48. Nested `while` Loop

A loop inside another loop is called a **nested loop**.

Example:

```java
int i = 1;

while (i <= 3) {

    int j = 1;

    while (j <= 3) {
        System.out.println(i + " " + j);
        j++;
    }

    i++;
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

The inner loop completes all its iterations for each iteration of the outer loop.

---

# 49. Nested Loop Flow

```text
Outer loop
    |
    ├── Inner loop
    │      1
    │      2
    │      3
    │
    ├── Inner loop
    │      1
    │      2
    │      3
    │
    └── Inner loop
           1
           2
           3
```

---

# 50. While Loop with User-Controlled Input

A loop can continue until the user enters a specific value.

Example:

```java
Scanner sc = new Scanner(System.in);

int n = sc.nextInt();

while (n != 0) {

    System.out.println(n);

    n = sc.nextInt();
}
```

Input:

```text
5
8
3
0
```

Output:

```text
5
8
3
```

When `0` is entered, the loop stops.

---

# 51. Sentinel Value

A value used to stop a loop is called a **sentinel value**.

Example:

```text
0
```

can be a sentinel value.

```java
while (n != 0) {
    // work
}
```

The loop continues until:

```text
n == 0
```

---

# 52. Input Until Negative Number

```java
Scanner sc = new Scanner(System.in);

int n = sc.nextInt();

while (n >= 0) {

    System.out.println(n);

    n = sc.nextInt();
}
```

Input:

```text
5
10
20
-1
```

Output:

```text
5
10
20
```

---

# 53. While Loop Pattern

The general pattern is:

```java
initialization;

while (condition) {

    // work

    update;
}
```

Example:

```java
int i = 1;

while (i <= n) {

    // work

    i++;
}
```

### Remember

```text
Initialization → Condition → Work → Update → Condition → ...
```

---

# 54. Important Difference: `while` vs `if`

### `if`

Runs at most once.

```java
if (condition) {
    // code
}
```

### `while`

Can run multiple times.

```java
while (condition) {
    // code
}
```

Example:

```java
int i = 1;

if (i <= 5) {
    System.out.println(i);
}
```

Output:

```text
1
```

But:

```java
int i = 1;

while (i <= 5) {
    System.out.println(i);
    i++;
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

# 55. `while` Loop vs `for` Loop

Both can repeat code.

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

The `for` loop will be covered separately.

---

# 56. Common Mistakes

## Mistake 1: Forgetting Initialization

Wrong:

```java
while (i <= 5) {
    System.out.println(i);
}
```

Correct:

```java
int i = 1;

while (i <= 5) {
    System.out.println(i);
    i++;
}
```

---

## Mistake 2: Forgetting Update

Wrong:

```java
int i = 1;

while (i <= 5) {
    System.out.println(i);
}
```

This creates an infinite loop.

Correct:

```java
int i = 1;

while (i <= 5) {
    System.out.println(i);
    i++;
}
```

---

## Mistake 3: Wrong Direction

Wrong:

```java
int i = 10;

while (i >= 1) {
    System.out.println(i);
    i++;
}
```

Correct:

```java
int i = 10;

while (i >= 1) {
    System.out.println(i);
    i--;
}
```

---

## Mistake 4: Off-by-One Error

To print `1` to `10`:

```java
while (i <= 10)
```

not:

```java
while (i < 10)
```

Because:

```text
i <= 10 → includes 10
i < 10  → stops before 10
```

---

## Mistake 5: Changing the Number You Still Need

For digit problems:

```java
int original = n;
```

should usually be saved before changing `n`.

---

# 57. Quick Revision

```text
while loop
    → repeats code while condition is true

Initialization
    → starting value

Condition
    → decides whether loop continues

Body
    → code executed repeatedly

Update
    → changes loop variable
```

Basic syntax:

```java
int i = 1;

while (i <= n) {

    // code

    i++;
}
```

---

# 58. Most Important Patterns

### Print 1 to N

```java
int i = 1;

while (i <= n) {
    System.out.println(i);
    i++;
}
```

### Print N to 1

```java
int i = n;

while (i >= 1) {
    System.out.println(i);
    i--;
}
```

### Sum 1 to N

```java
int i = 1;
int sum = 0;

while (i <= n) {
    sum += i;
    i++;
}
```

### Count Digits

```java
int count = 0;

while (n > 0) {
    count++;
    n /= 10;
}
```

### Sum of Digits

```java
int sum = 0;

while (n > 0) {
    sum += n % 10;
    n /= 10;
}
```

### Reverse Number

```java
int reverse = 0;

while (n > 0) {
    int digit = n % 10;
    reverse = reverse * 10 + digit;
    n /= 10;
}
```

### Even/Odd

```java
if (n % 2 == 0) {
    // even
} else {
    // odd
}
```

---

# 59. Practice Questions

## Easy

### Q1. Print 1 to N

Take `N` as input and print all numbers from `1` to `N`.

Example:

```text
Input:
5

Output:
1
2
3
4
5
```

---

### Q2. Print N to 1

Example:

```text
Input:
5

Output:
5
4
3
2
1
```

---

### Q3. Print Even Numbers

Print all even numbers from `1` to `N`.

---

### Q4. Print Odd Numbers

Print all odd numbers from `1` to `N`.

---

### Q5. Print Multiples

Take `N` and print its first 10 multiples.

Example:

```text
Input:
7

Output:
7
14
21
28
35
42
49
56
63
70
```

---

### Q6. Count from 1 to N

Print how many numbers exist from `1` to `N`.

---

## Moderate

### Q7. Sum from 1 to N

Example:

```text
Input:
10

Output:
55
```

---

### Q8. Sum of Even Numbers

Find the sum of all even numbers from `1` to `N`.

---

### Q9. Sum of Odd Numbers

Find the sum of all odd numbers from `1` to `N`.

---

### Q10. Factorial

Take `N` and calculate:

```text
N!
```

Example:

```text
Input:
5

Output:
120
```

---

### Q11. Multiplication Table

Take a number and print its multiplication table from `1` to `10`.

---

### Q12. Count Digits

Take an integer and count the number of digits.

Example:

```text
Input:
58321

Output:
5
```

---

### Q13. Sum of Digits

Example:

```text
Input:
583

Output:
16
```

---

### Q14. First and Last Digit

Take an integer and print its first and last digit.

Example:

```text
Input:
58321

Output:
First = 5
Last = 1
```

---

## Hard

### Q15. Reverse a Number

Example:

```text
Input:
583

Output:
385
```

---

### Q16. Palindrome Number

Check whether a number is a palindrome.

Example:

```text
Input:
121

Output:
Palindrome
```

---

### Q17. Count Even and Odd Digits

Example:

```text
Input:
58321

Output:
Even digits = 2
Odd digits = 3
```

---

### Q18. Sum of Even and Odd Digits

Example:

```text
Input:
58321

Output:
Even sum = 10
Odd sum = 9
```

---

### Q19. Largest Digit

Find the largest digit in a number.

Example:

```text
Input:
58321

Output:
8
```

---

### Q20. Smallest Digit

Find the smallest digit in a number.

Example:

```text
Input:
58321

Output:
1
```

---

### Q21. Product of Digits

Example:

```text
Input:
1234

Output:
24
```

Because:

```text
1 × 2 × 3 × 4 = 24
```

---

### Q22. Count a Particular Digit

Take a number and a digit. Count how many times that digit occurs.

Example:

```text
Input:
1223342
2

Output:
3
```

---

# 60. Challenge Questions

### Q23. Armstrong Number

Check whether a three-digit number is an Armstrong number.

Example:

```text
153
```

Because:

```text
1³ + 5³ + 3³ = 153
```

Output:

```text
Armstrong
```

---

### Q24. Perfect Number

Check whether a number is equal to the sum of its proper divisors.

Example:

```text
6
```

Because:

```text
1 + 2 + 3 = 6
```

Output:

```text
Perfect Number
```

---

### Q25. Prime Number

Take a number and determine whether it is prime.

A prime number has exactly two positive factors:

```text
1 and itself
```

Examples:

```text
2 → Prime
7 → Prime
10 → Not Prime
```

---

### Q26. Count Factors

Take a number and count how many positive factors it has.

Example:

```text
Input:
12

Output:
6
```

Factors:

```text
1, 2, 3, 4, 6, 12
```

---

### Q27. Sum of Factors

Take a number and calculate the sum of all its positive factors.

Example:

```text
Input:
6

Output:
12
```

Because:

```text
1 + 2 + 3 + 6 = 12
```

---

### Q28. GCD / HCF

Take two positive integers and find their GCD using a loop.

Example:

```text
Input:
24 36

Output:
12
```

---

### Q29. LCM

Take two positive integers and find their LCM.

Example:

```text
Input:
4 6

Output:
12
```

---

### Q30. Fibonacci Series

Print the first `N` Fibonacci numbers.

Example:

```text
Input:
7

Output:
0 1 1 2 3 5 8
```

---

# 61. Final Revision Questions

1. What is a loop?
2. Why are loops useful?
3. What is a `while` loop?
4. What are the three main parts of a typical while loop?
5. What is initialization?
6. What is the loop condition?
7. What is the loop update?
8. What happens if the condition is initially false?
9. What is an infinite loop?
10. How can you stop an infinite loop?
11. What is the difference between `i++` and `i--`?
12. What does `i += 2` mean?
13. How do you print even numbers using a while loop?
14. How do you print odd numbers using a while loop?
15. How do you calculate the sum from `1` to `N`?
16. How do you calculate factorial?
17. How do `% 10` and `/ 10` help with digits?
18. How do you count digits?
19. How do you find the sum of digits?
20. How do you reverse a number?
21. Why should you save the original number when checking a palindrome?
22. What does `break` do?
23. What does `continue` do?
24. What is the difference between `break` and `continue`?
25. What is a nested loop?
26. What is a sentinel value?
27. What is an off-by-one error?
28. What happens if you forget to update the loop variable?
29. What is the difference between `if` and `while`?
30. What is the basic structure of a while loop?

---

# 62. Key Formula / Logic Revision

```text
Last digit:
n % 10

Remove last digit:
n / 10

Count digits:
count++

Sum of digits:
sum += n % 10

Reverse:
reverse = reverse * 10 + n % 10

Even:
n % 2 == 0

Odd:
n % 2 != 0

Palindrome:
original == reverse

Factorial:
1 × 2 × 3 × ... × n
```

### Core While Loop

```java
int i = 1;

while (i <= n) {

    // work

    i++;
}
```

**Remember:**

```text
START
  ↓
Initialization
  ↓
Condition
  ↓
True?
  ├── No → Stop
  │
  └── Yes
       ↓
      Work
       ↓
      Update
       ↓
    Condition
       ↓
     Repeat
```
