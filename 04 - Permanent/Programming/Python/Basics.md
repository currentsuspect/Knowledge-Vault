---
tags: [python, programming, learning, intro-to-python, coding-basics]
aliases: [python-basics, python-fundamentals, python-intro]
cssclasses: [pen-blue]
---

# 🐍 Your Python Programming Fundamentals

> *"Python is an experiment in how much freedom programmers need. Too much freedom and nobody can read another's code; too little and expressiveness is endangered."* - Guido van Rossum

Python is your high-level, interpreted programming language designed for readability and simplicity. It's like having a conversation with your computer—clear, expressive, and powerful. This note covers the foundational concepts that make Python both accessible and powerful for you.

---

## 🎯 **What is Python?**

### **Core Characteristics**
- **High-Level**: Abstracts away complex hardware details
- **Interpreted**: Code runs directly without compilation
- **Dynamic Typing**: Variable types are determined at runtime
- **Readable**: Syntax emphasizes clarity and simplicity
- **Versatile**: Used in web development, data science, AI, automation, and more

### **Python Philosophy**
From the Zen of Python (PEP 20):
- **Explicit is better than implicit**
- **Simple is better than complex**
- **Readability counts**
- **There should be one—and preferably only one—obvious way to do it**

**My Take**: Python's philosophy resonates with me because it values clarity over cleverness. Code should be readable by humans, not just machines.

---

## 🔧 **Basic Syntax and Structure**

### **The Python Way**
Python uses **indentation** to define code blocks, making structure visually clear:

```python
# This is a comment
if condition:
    # This block is indented
    do_something()
    do_something_else()
else:
    # This is another block
    do_alternative()
```

**Key Points**:
- **No semicolons** needed at line endings
- **Indentation matters** - it defines code blocks
- **Consistent indentation** - typically 4 spaces
- **Colons** mark the start of code blocks

**My Take**: I love Python's indentation-based syntax. It forces you to write readable code because the structure is visible. It's like writing poetry—the form enhances the meaning.

### **Variables and Assignment**
Variables in Python are like labels you stick on values:

```python
# Simple assignment
name = "Dylan"
age = 25
height = 1.75
is_student = True

# Multiple assignment
x, y, z = 1, 2, 3

# Dynamic typing - variables can change type
variable = 42        # int
variable = "hello"   # str
variable = [1, 2, 3] # list
```

**My Take**: Python's dynamic typing is liberating. I don't have to declare types upfront, which makes prototyping and experimentation much faster. But I've learned to be careful about type consistency in larger projects.

---

## 📊 **Data Types and Structures**

### **Basic Data Types**

#### **Numbers**
```python
# Integers (whole numbers)
count = 42
negative = -17

# Floating-point (decimal numbers)
pi = 3.14159
temperature = 98.6

# Complex numbers
complex_num = 3 + 4j
```

#### **Strings**
```python
# Basic strings
name = "Dylan"
message = 'Hello, world!'

# Multi-line strings
poem = """
Roses are red,
Violets are blue,
Python is awesome,
And so are you!
"""

# String operations
first = "Hello"
second = "World"
combined = first + " " + second  # "Hello World"
repeated = "Ha" * 3             # "HaHaHa"
```

#### **Booleans**
```python
# True and False (capitalized)
is_active = True
is_finished = False

# Boolean operations
and_result = True and False  # False
or_result = True or False    # True
not_result = not True        # False
```

**My Take**: Python's boolean values are capitalized (True/False), which makes them stand out. I appreciate this clarity—it's immediately obvious what's a boolean and what's a string.

### **Data Structures**

#### **Lists** - Ordered, Mutable Collections
```python
# Creating lists
fruits = ["apple", "banana", "cherry"]
numbers = [1, 2, 3, 4, 5]
mixed = [1, "hello", 3.14, True]

# Accessing elements (zero-indexed)
first_fruit = fruits[0]    # "apple"
last_fruit = fruits[-1]    # "cherry"

# Modifying lists
fruits.append("orange")    # Add to end
fruits.insert(1, "grape")  # Insert at position
fruits.remove("banana")    # Remove by value
del fruits[0]             # Remove by index
```

#### **Dictionaries** - Key-Value Pairs
```python
# Creating dictionaries
person = {
    "name": "Dylan",
    "age": 25,
    "city": "New York"
}

# Accessing values
name = person["name"]           # "Dylan"
age = person.get("age", 0)      # 25 (with default)

# Modifying dictionaries
person["email"] = "dylan@example.com"
person.update({"phone": "123-456-7890"})
del person["age"]
```

#### **Tuples** - Immutable Sequences
```python
# Creating tuples
coordinates = (10, 20)
rgb_color = (255, 128, 0)

# Tuples are immutable
# coordinates[0] = 15  # This would cause an error
```

#### **Sets** - Unordered, Unique Collections
```python
# Creating sets
unique_numbers = {1, 2, 3, 3, 4}  # {1, 2, 3, 4}
fruits_set = set(["apple", "banana", "apple"])  # {"apple", "banana"}

# Set operations
set1 = {1, 2, 3}
set2 = {3, 4, 5}
union = set1 | set2        # {1, 2, 3, 4, 5}
intersection = set1 & set2 # {3}
difference = set1 - set2   # {1, 2}
```

**My Take**: Python's data structures are intuitive. Lists are like arrays, dictionaries are like hash tables, and the syntax is clean. I especially love list comprehensions for transforming data.

---

## 🔄 **Control Flow**

### **Conditional Statements**
```python
# Basic if-else
age = 18
if age >= 18:
    print("You're an adult")
elif age >= 13:
    print("You're a teenager")
else:
    print("You're a child")

# Ternary operator
status = "adult" if age >= 18 else "minor"
```

### **Loops**

#### **For Loops**
```python
# Iterating over sequences
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(f"I like {fruit}")

# Using range
for i in range(5):
    print(i)  # 0, 1, 2, 3, 4

# Enumerate for index and value
for index, fruit in enumerate(fruits):
    print(f"{index}: {fruit}")
```

#### **While Loops**
```python
# Basic while loop
count = 0
while count < 5:
    print(count)
    count += 1

# Break and continue
for i in range(10):
    if i == 3:
        continue  # Skip 3
    if i == 7:
        break     # Stop at 7
    print(i)
```

**My Take**: Python's loops are elegant. The `for` loop works with any iterable, and `enumerate` is perfect when you need both index and value. I use `while` loops sparingly—usually when I need more control over the iteration.

---

## 🏗️ **Functions**

### **Defining Functions**
```python
# Basic function
def greet(name):
    return f"Hello, {name}!"

# Function with default parameters
def greet_with_title(name, title="Mr."):
    return f"Hello, {title} {name}!"

# Function with multiple return values
def get_name_and_age():
    return "Dylan", 25

# Using the function
message = greet("Alice")
name, age = get_name_and_age()
```

### **Lambda Functions**
```python
# Simple lambda function
square = lambda x: x ** 2

# Using lambda with built-in functions
numbers = [1, 2, 3, 4, 5]
squared = list(map(lambda x: x ** 2, numbers))
evens = list(filter(lambda x: x % 2 == 0, numbers))
```

**My Take**: Functions are the building blocks of Python programs. I love how Python makes it easy to create small, focused functions. Lambda functions are great for simple operations, but I prefer named functions for anything more complex.

---

## 🎨 **Pythonic Patterns**

### **List Comprehensions**
```python
# Traditional approach
squares = []
for i in range(10):
    squares.append(i ** 2)

# Pythonic approach
squares = [i ** 2 for i in range(10)]

# With conditions
even_squares = [i ** 2 for i in range(10) if i % 2 == 0]
```

### **Context Managers**
```python
# File handling with context manager
with open("file.txt", "r") as file:
    content = file.read()
# File is automatically closed

# Custom context manager
from contextlib import contextmanager

@contextmanager
def timer():
    import time
    start = time.time()
    yield
    end = time.time()
    print(f"Time taken: {end - start} seconds")

# Using the context manager
with timer():
    # Do some work
    pass
```

**My Take**: Pythonic patterns make code more readable and efficient. List comprehensions are especially powerful—they're like poetry for data transformation. Context managers ensure proper resource management without explicit cleanup.

---

## 🔗 **Connections to Other Knowledge**

### **Programming Concepts**
- **Algorithms**: Python provides tools for implementing algorithms efficiently
- **Data Structures**: Built-in structures support complex data organization
- **Object-Oriented Programming**: Python supports classes and inheritance
- **Functional Programming**: Functions as first-class objects

### **Mathematics**
- **Numerical Computing**: Libraries like NumPy for mathematical operations
- **Statistics**: Tools for data analysis and statistical modeling
- **Algorithms**: Mathematical concepts implemented in code

### **Psychology**
- **Cognitive Load**: Python's readability reduces mental effort
- **Learning Theory**: Simple syntax supports progressive learning
- **Problem Solving**: Systematic approaches to programming challenges

---

## 💡 **Best Practices**

### **Code Style**
- **Follow PEP 8**: Python's style guide
- **Use meaningful names**: Variables and functions should be descriptive
- **Keep functions small**: One function, one responsibility
- **Add comments**: Explain why, not what

### **Error Handling**
```python
# Using try-except
try:
    result = 10 / 0
except ZeroDivisionError:
    print("Cannot divide by zero")
except Exception as e:
    print(f"An error occurred: {e}")
finally:
    print("This always runs")
```

### **Testing**
```python
# Simple testing
def add(a, b):
    return a + b

# Test the function
assert add(2, 3) == 5
assert add(-1, 1) == 0
print("All tests passed!")
```

---

## 🚀 **Next Steps**

### **Immediate Learning**
- [[04 - Permanent/Programming/Python/Dictionaries In Python.md|📚 Advanced Data Structures]]
- [[04 - Permanent/Programming/Python/If-Else Statements.md|🔀 Control Flow Deep Dive]]
- [[04 - Permanent/Programming/Python/high-level Vs low-level.md|⚙️ Language Levels]]

### **Advanced Topics**
- **Object-Oriented Programming**: Classes and inheritance
- **Modules and Packages**: Organizing code
- **File I/O**: Reading and writing files
- **Exception Handling**: Robust error management
- **Testing**: Unit tests and test-driven development

### **Practical Applications**
- **Web Development**: Django, Flask
- **Data Science**: Pandas, NumPy, Matplotlib
- **Automation**: Scripting and task automation
- **API Development**: Building web services

---

*"Python is the second best language for everything."* - Unknown

---

**Related Notes**: [[04 - Permanent/Programming/|💻 Programming]], [[04 - Permanent/Mathematics/Mathematical Thinking|📐 Mathematical Thinking]], [[04 - Permanent/Computer Science/|🖥️ Computer Science]]

**Last Updated**: {{date:YYYY-MM-DD}}
**Status**: 🟢 Active Learning