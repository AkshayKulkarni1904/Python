```markdown
# Day 1: Python Basics, Data Types, and Flow Control

## 1. Strings and Immutability
Strings in Python are immutable, meaning their data cannot be changed after creation. Modifying a string creates a new object in memory.

```python
s = "Akshay"
print(s)
print(s.capitalize())
print(s.upper())

```

**Output:**

```text
Akshay
Akshay
AKSHAY

```

---

## 2. Identifiers and Objects

* **Object:** A physical entity stored in memory (e.g., `100`, `"python"`, `4.55`).
* **Identifier:** The name given to an object (also known as a variable).

```python
x = 100  # x is an identifier and 100 is the object
y = "Python"
z = 4.55

print(y)
print(z)

```

**Output:**

```text
Python
4.55

```

### Rules for Declaring Identifiers

* Can use `a-z`, `A-Z`, numbers, and underscores (`_`).
* Must be meaningful.
* **Spaces are not allowed** (e.g., `first name = "python"` is invalid). Use `first_name = "python"`.
* **Cannot start with a number** (e.g., `1num = 100` is invalid). Numbers as a suffix are allowed (`num1 = 100`).
* **Do not use reserved keywords.** You can view Python keywords using the `keyword` library.

```python
import keyword

print(keyword.kwlist)
print("Total keywords:", len(keyword.kwlist))

```

**Output:**

```text
['False', 'None', 'True', 'and', 'as', 'assert', 'async', 'await', 'break', 'class', 'continue', 'def', 'del', 'elif', 'else', 'except', 'finally', 'for', 'from', 'global', 'if', 'import', 'in', 'is', 'lambda', 'nonlocal', 'not', 'or', 'pass', 'raise', 'return', 'try', 'while', 'with', 'yield']
Total keywords: 35

```

---

## 3. Variable Assignment & Reassignment

```python
# Reassigning variable values
site_name = "google.com"
print(site_name)

site_name = "youtube.com"
print(site_name)

# Assigning multiple values to multiple variables
a, b, c = 4, 3.5, 'hello'
print(a, b, c)

# Assigning the same value to multiple variables at once
x = y = "5"
print(x, y)

```

**Output:**

```text
google.com
youtube.com
4 3.5 hello
5 5

```

---

## 4. Collection Literals (Built-in Data Structures)

```python
fruit = ["apple", "mango", "orange"]       # List (Mutable, ordered)
numbers = ('1', '2', '3')                  # Tuple (Immutable, ordered)
alphabets = {'a': 'apple', 'b': 'ball'}    # Dictionary (Key-Value pairs)
vowels = {'a', 'e', 'i', 'o', 'u'}         # Set (Unordered, unique items)

print(fruit)
print(numbers)
print(alphabets)
print(vowels)

```

**Output:**

```text
['apple', 'mango', 'orange']
('1', '2', '3')
{'a': 'apple', 'b': 'ball'}
{'i', 'e', 'a', 'o', 'u'}

```

---

## 5. Python Type Conversion

### Implicit Type Conversion

Python automatically converts one data type to another to prevent data loss.

```python
int_number = 123
float_number = 1.23
new_number = int_number + float_number

print("value:", new_number)
print("Data Type:", type(new_number))

```

**Output:**

```text
value: 124.23
Data Type: <class 'float'>

```

### Explicit Type Conversion (Type Casting)

Manually converting data types using built-in functions like `int()`, `str()`, etc.

```python
num_string = '12'
num_integer = 23

# Converting string to integer
num_string = int(num_string)
num_sum = num_integer + num_string

print("sum:", num_sum)
print("Data Type of num_sum:", type(num_sum))

```

**Output:**

```text
sum: 35
Data Type of num_sum: <class 'int'>

```

---

## 6. Built-in Modules

### Random Module

```python
import random

print("Random range (10-20):", random.randrange(10, 20))

list1 = ['a', 'b', 'c', 'd', 'e']
print("Random choice from list:", random.choice(list1))

random.shuffle(list1)
print("Shuffled list:", list1)

print("Random float (0.0 to 1.0):", random.random())

```

**Output:** *(Note: Output values will vary due to randomness)*

```text
Random range (10-20): 14
Random choice from list: c
Shuffled list: ['d', 'b', 'a', 'e', 'c']
Random float (0.0 to 1.0): 0.648239102432

```

### Math Module

```python
import math

print("Pi:", math.pi)
print("Cos(Pi):", math.cos(math.pi))
print("Exp(10):", math.exp(10))
print("Log10(1000):", math.log10(1000))
print("Factorial of 7:", math.factorial(7))

```

**Output:**

```text
Pi: 3.141592653589793
Cos(Pi): -1.0
Exp(10): 22026.465794806718
Log10(1000): 3.0
Factorial of 7: 5040

```

---

## 7. Python Numeric Datatypes

Python supports integers, floating-point numbers, and complex numbers.

```python
num1 = 8
print(num1, 'is of type', type(num1))

num2 = 3.19
print(num2, 'is of type', type(num2))

num3 = 10 + 5j
print(num3, 'is of type', type(num3))

```

**Output:**

```text
8 is of type <class 'int'>
3.19 is of type <class 'float'>
(10+5j) is of type <class 'complex'>

```

---

## 8. Operators

### Arithmetic Operators

```python
a = 10
b = 4

print('Sum:', a + b)
print("Subtraction:", a - b)
print("Multiplication:", a * b)
print("Division:", a / b)
print("Floor Division:", a // b)
print("Modulo:", a % b)
print('Power:', a ** b)

```

**Output:**

```text
Sum: 14
Subtraction: 6
Multiplication: 40
Division: 2.5
Floor Division: 2
Modulo: 2
Power: 10000

```

### Assignment Operators

```python
a = 9
b = 6
a += b  # Equivalent to a = a + b
print("Sum of a + b =", a)

```

**Output:**

```text
Sum of a + b = 15

```

### Comparison Operators

```python
a = 5
b = 2

print('a == b ->', a == b)
print('a != b ->', a != b)
print('a > b  ->', a > b)
print('a < b  ->', a < b)
print('a >= b ->', a >= b)
print('a <= b ->', a <= b)

```

**Output:**

```text
a == b -> False
a != b -> True
a > b  -> True
a < b  -> False
a >= b -> True
a <= b -> False

```

---

## 9. Python Flow Control

### `if` Statement

```python
number = 5  # Example input
if number > 0:
    print(f'{number} is a positive number')
print("A statement outside the if condition")

```

**Output:**

```text
5 is a positive number
A statement outside the if condition

```

### `if...else` Statement

```python
number = -3  # Example input
if number > 0:
    print('Positive number')
else:
    print('Not a positive number')
print('This statement always executes')

```

**Output:**

```text
Not a positive number
This statement always executes

```

### `if...elif...else` Ladder

```python
number = -5

if number > 0:
    print('Positive number')
elif number < 0:
    print('Negative number')
else:
    print('Zero')

```

**Output:**

```text
Negative number

```

### Nested `if` Statement

```python
number = 5

if number >= 0:
    if number == 0:
        print('Number is 0')
    else:
        print('Number is positive')
else:
    print('Number is negative')

```

**Output:**

```text
Number is positive

```

### Ternary Operator

An elegant, one-line version of `if...else`.

```python
score = 40
result = 'pass' if score >= 50 else 'fail'
print(result)

```

**Output:**

```text
fail

```

### Logical Operators (Multiple Conditions)

```python
age = 28
salary = 6000

if age >= 30 and salary >= 5000:
    print('Eligible for the premium membership.')
else:
    print('Not eligible for the premium membership')

```

**Output:**

```text
Not eligible for the premium membership

```

```

```
