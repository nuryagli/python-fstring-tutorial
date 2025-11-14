# What Is an f-string in Python?

In Python, an f-string allows you to place variables, calculations, and expressions directly and clearly inside a text.
You put an f in front of a string and write anything you want inside {}.

## Basic Example
```python
name = "Nurbeniz"
print(f"Hello {name}")
```

# Why Do We Need f-strings?

Before f-strings existed, people used two methods, and both had problems.

## 1) Concatenation with +
```python
name = "Robert"
age = 25
print("Name: " + name + ", Age: " + str(age))
```

Problems:
- Code becomes long
- Hard to read
- str + int causes errors

## 2) The format() method
```python
name = "Robert"
age = 25
print("Name: {}, Age: {}".format(name, age))
```

Problems:
- Variables inside, .format() outside
- Order can be confusing
- Not natural to read for humans

# How Do f-strings Solve These Problems?

The Python community wanted this:
> "Let us place variables inside text naturally."
And f-strings were created.

# How Does an f-string Work?

An f-string:
- Scans the text
- Detects {}
- Executes the expression inside
- Converts the result to a string

Inside {}, you can write:
- variables
- list items
- math expressions
- function calls

# Real-Life Examples

## A) Cargo Tracking
```python
name = "Ayse"
tracking_no = 123456
status = "Out for delivery"

print(f"Dear {name}, your package {tracking_no} is currently: {status}.")
```

## B) Price Calculation
```python
product = "Headphones"
price = 350
tax = 0.18

print(f"{product} total price with tax: {price + price * tax} TL")
```

## C) Time Formatting
```python
from datetime import datetime

now = datetime.now()
print(f"Current time: {now.hour}:{now.minute}")
```

## D) Log Message
```python
level = "INFO"
message = "Server started"

print(f"[{level}] - {message}")
```

# More Things You Can Do

## 1) Math inside {}
```python
print(f"Value after 3 seconds: {3 * 5}")
```

## 2) List Indexing
```python
numbers = [3, 5, 7]
print(f"First element: {numbers[0]}")
```

## 3) Function Calls
```python
def square(x):
    return x * x

print(f"Square of 5: {square(5)}")
```

# Analogy

Think of a letter template where empty spaces are automatically filled.

Template:
```
Hello {name},
Your package {tracking_no} has been shipped.
```

Example:
```python
name = "Mehmet"
tracking_no = 999888

print(f"Hello {name}, your package {tracking_no} has been shipped.")
```

# Summary

f-strings create a natural bridge between text and variables.

Advantages:
- More readable
- Shorter
- Faster
- Less error-prone

This is why f-strings are the preferred string formatting method in Python.
