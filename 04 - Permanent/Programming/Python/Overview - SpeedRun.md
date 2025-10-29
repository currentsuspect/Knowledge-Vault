---
tags:
  - python
  - Learning
  - Intro-to-python
cssclasses:
  - pen-purple
aliases:
  - Python Overview
---

### **Introduction to Python**

#### **1. What is Python? Why Use It?**
- **Definition**: [[|Python]] is a [[high-level Vs low-level|high-level]], interpreted [[programming language]] known for its readability and simplicity. It supports multiple programming paradigms including procedural, [[ |object-oriented]], and functional programming.
- **Why Use It?**: Python's readability, extensive standard library, and large community make it ideal for beginners and professionals alike. It's used in web development, data analysis, artificial intelligence, automation, and more.

#### **2. Setting Up Python Environment**
- **Windows**:
  1. Download Python installer from [python.org](https://www.python.org/downloads/).
  2. Run the installer, make sure to check "Add Python to PATH".
  3. Verify installation using `python --version` in Command Prompt.
- **Mac**:
  1. Use Homebrew with `brew install python`.
  2. Verify installation with `python3 --version`.
- **Linux**:
  1.Use your [[Package Managers in Linux|Package Manager]], e.g., `sudo pacman -S python3`.
  2. Verify with `python3 --version`.

#### **3. Basic Syntax, Indentation, and Comments**
- **Syntax**: Python uses indentation to define code blocks. Consistent indentation is crucial.
```python
def greet(name):
print(f"Hello,{name}!")
```
### Overly Explained Code Of Above
  ```python
     # This function sends a personalized greeting to a person based on their name.
  def greet(name): # Function definition: `greet`
    # Takes one parameter:
    # - `name`: a string representing the name of the person who will receive the greeting
    
    # The function uses the `print` function to display a message.
    # Inside the `print` function:
    # - `f"Hello, {name}!"` is an f-string (formatted string literal) that incorporates the value of the `name` parameter.
    # - The `{name}` within the f-string is replaced with the actual value of the `name` parameter when the message is printed.
    print(f"Hello, {name}!")  

```
- **Comments**: Use `#` for single-line comments and triple quotes `"""` or `'''` for multi-line comments.
  ```python
  # This is a single-line comment
  """
  This is a multi-line comment
  spanning multiple lines
  """
  ```

### **Variables and Data Types**

#### **1. Explanation of Variables and Assignment**
- **Variables**: Containers for storing data values. They do not need explicit declaration.
  ```python
  x = 10  # Integer
  name = "Alice"  # String
  ```

#### **2. Data Types**
- **Integers**: Whole numbers.
  ```python
  num = 42
  ```
- **Floats**: Numbers with decimal points.
  ```python
  pi = 3.14
  ```
- **Strings**: Text data enclosed in quotes.
  ```python
  message = "Hello, World!"
  ```
- **Booleans**: True or False values.
  ```python
  is_valid = True
  ```

#### **3. Type Conversion and Dynamic Typing**
- **Conversion**: Convert between types using functions like `int()`, `float()`, and `str()`.
  ```python
  num_str = "123"
  num_int = int(num_str)  # Converts string to integer
  ```
- **Dynamic Typing**: Python determines the type of a variable at runtime.

### **Basic Operators**

#### **1. Arithmetic Operators**
- **Operators**: `+`, `-`, `*`, `/`, `//` (floor division), `%` (modulus), `**` (exponentiation).
  ```python
  sum = 10 + 5  # 15
  ```

#### **2. Comparison Operators**
- **Operators**: `==`, `!=`, `>`, `<`, `>=`, `<=`.
  ```python
  is_equal = (10 == 10)  # True
  ```

#### **3. Logical Operators**
- **Operators**: `and`, `or`, `not`.
  ```python
  is_true = (True and False)  # False
  ```

#### **4. Bitwise Operators**
- **Operators**: `&` (and), `|` (or), `^` (xor), `~` (not), `<<` (left shift), `>>` (right shift).
  ```python
  bitwise_and = 5 & 3  # 1
  ```

#### **5. Operator Precedence and Associativity**
- **Precedence**: Determines the order of operations (e.g., multiplication before addition).
- **Associativity**: Determines the order of operations with the same precedence (e.g., left-to-right for addition and multiplication).

### **Strings**

#### **1. String Manipulation and Methods**
- **Concatenation**: Using `+` operator.
  ```python
  full_name = "John" + " " + "Doe"
  ```
- **Methods**: `upper()`, `lower()`, `strip()`, `replace()`, `split()`.
  ```python
  greeting = "hello".capitalize()  # "Hello"
  ```

#### **2. String Formatting**
- **f-strings** (formatted string literals):
  ```python
  name = "Alice"
  greeting = f"Hello, {name}!"
  ```
- **.format() method**:
  ```python
  template = "Hello, {}!"
  greeting = template.format(name)
  ```

#### **3. Escape Characters and Raw Strings**
- **Escape Characters**: `\n` (newline), `\t` (tab), `\\` (backslash).
  ```python
  path = "C:\\Users\\Alice"
  ```
- **Raw Strings**: Prefix with `r` to avoid escape character interpretation.
  ```python
  path = r"C:\Users\Alice"
  ```

### **Data Structures**

#### **1. Lists**
- **Definition**: Ordered, mutable collection of items.
  ```python
  fruits = ["apple", "banana", "cherry"]
  ```
- **Operations**: `append()`, `remove()`, `sort()`, `slice`.
  ```python
  fruits.append("date")
  ```

#### **2. Tuples**
- **Definition**: Ordered, immutable collection of items.
  ```python
  coordinates = (10, 20)
  ```

#### **3. Sets**
- **Definition**: Unordered collection of unique items.
  ```python
  unique_numbers = {1, 2, 3, 3}
  ```

#### **4. Dictionaries**
- **Definition**: Key-value pairs.
  ```python
  person = {"name": "Alice", "age": 30}
  ```

#### **5. Mutable vs Immutable Types**
- **Mutable**: Lists, sets, dictionaries.
- **Immutable**: Integers, floats, strings, tuples.

#### **6. Comprehensions**
- **List Comprehensions**:
  ```python
  squares = [x**2 for x in range(10)]
  ```
- **Dictionary Comprehensions**:
  ```python
  square_dict = {x: x**2 for x in range(10)}
  ```

### **Control Flow**

#### **1. Conditionals**
- **Syntax**:
  ```python
  if x > 10:
      print("x is greater than 10")
  elif x == 10:
      print("x is 10")
  else:
      print("x is less than 10")
  ```

#### **2. Loops**
- **For Loop**:
  ```python
  for i in range(5):
      print(i)
  ```
- **While Loop**:
  ```python
  i = 0
  while i < 5:
      print(i)
      i += 1
  ```

#### **3. Break, Continue, and Else Clauses**
- **Break**: Exits the loop.
  ```python
  for i in range(5):
      if i == 3:
          break
      print(i)
  ```
- **Continue**: Skips the rest of the current iteration.
  ```python
  for i in range(5):
      if i == 3:
          continue
      print(i)
  ```
- **Else**: Executes when loop completes normally (without a break).
  ```python
  for i in range(5):
      print(i)
  else:
      print("Loop completed")
  ```

### **Functions**

#### **1. Defining Functions and Function Arguments**
- **Syntax**:
  ```python
  def greet(name):
      return f"Hello, {name}!"
  ```

#### **2. Return Values, Variable Scope, and Default Parameters**
- **Return Values**:
  ```python
  def add(a, b):
      return a + b
  ```
- **Scope**: Variables defined inside a function are local to that function.
  ```python
  def func():
      local_var = 10
  ```
- **Default Parameters**:
  ```python
  def multiply(a, b=1):
      return a * b
  ```

#### **3. Lambda Functions**
- **Syntax**:
  ```python
  square = lambda x: x**2
  ```

#### **4. Recursion and Function Decorators**
- **Recursion**:
  ```python
  def factorial(n):
      if n == 0:
          return 1
      else:
          return n * factorial(n-1)
  ```
- **Decorators**: Functions that modify other functions.
  ```python
  def decorator(func):
      def wrapper():
          print("Something is happening before the function.")
          func()
          print("Something is happening after the function.")
      return wrapper

  @decorator
  def say_hello():
      print("Hello!")
  ```

### **Modules and Libraries

**

#### **1. Importing Built-in Modules**
- **Example**:
  ```python
  import math
  print(math.sqrt(16))
  ```

#### **2. Writing and Importing Custom Modules**
- **Custom Module**: Create a file `mymodule.py` with functions and import it.
  ```python
  # mymodule.py
  def say_hello():
      print("Hello from mymodule!")

  # main.py
  import mymodule
  mymodule.say_hello()
  ```

#### **3. Using pip to Install Third-Party Libraries**
- **Example**:
  ```bash
  pip install requests
  ```
  ```python
  import requests
  response = requests.get('https://api.github.com')
  ```

### **Error Handling**

#### **1. Exception Handling**
- **Syntax**:
  ```python
  try:
      result = 10 / 0
  except ZeroDivisionError:
      print("Cannot divide by zero!")
  finally:
      print("Execution completed.")
  ```

#### **2. Raising Exceptions and Creating Custom Exceptions**
- **Raising Exceptions**:
  ```python
  raise ValueError("A value error occurred!")
  ```
- **Custom Exceptions**:
  ```python
  class CustomError(Exception):
      pass

  raise CustomError("This is a custom error.")
  ```

### **File I/O**

#### **1. Reading from and Writing to Files**
- **Example**:
  ```python
  with open('file.txt', 'w') as file:
      file.write("Hello, World!")

  with open('file.txt', 'r') as file:
      content = file.read()
  ```

#### **2. Working with File Modes**
- **Modes**: `r` (read), `w` (write), `a` (append), `b` (binary).
  ```python
  with open('file.bin', 'wb') as file:
      file.write(b'\x00\x01\x02')
  ```

#### **3. Best Practices for File Handling**
- **Use Context Managers** to handle files:
  ```python
  with open('file.txt', 'r') as file:
      content = file.read()
  ```

### **Object-Oriented Programming (OOP)**

#### **1. Classes, Objects, and Instances**
- **Syntax**:
  ```python
  class Dog:
      def __init__(self, name):
          self.name = name

      def bark(self):
          return f"{self.name} barks!"

  my_dog = Dog("Buddy")
  print(my_dog.bark())
  ```

#### **2. Attributes and Methods**
- **Instance Methods**: Operate on instance data.
- **Class Methods**: Operate on class data.
  ```python
  class MyClass:
      class_attr = 0

      def __init__(self, value):
          self.instance_attr = value

      @classmethod
      def class_method(cls):
          return cls.class_attr

      def instance_method(self):
          return self.instance_attr
  ```

#### **3. Inheritance, Polymorphism, and Encapsulation**
- **Inheritance**:
  ```python
  class Animal:
      def speak(self):
          pass

  class Dog(Animal):
      def speak(self):
          return "Woof!"
  ```
- **Polymorphism**: Different classes can be accessed through the same interface.
- **Encapsulation**: Hiding internal state and requiring all interaction to be performed through an object's methods.

#### **4. Dunder Methods**
- **Examples**:
  ```python
  class Person:
      def __init__(self, name):
          self.name = name

      def __str__(self):
          return f"Person named {self.name}"

  p = Person("Alice")
  print(p)  # Output: Person named Alice
  ```

#### **5. Advanced OOP Topics**
- **Abstract Classes**:
  ```python
  from abc import ABC, abstractmethod

  class AbstractShape(ABC):
      @abstractmethod
      def area(self):
          pass
  ```
- **Mixins** and **Multiple Inheritance**: Provide a way to add functionality to classes without using inheritance directly.

### **Advanced Topics**

#### **1. Iterators and Generators**
- **Iterators**: Implement `__iter__()` and `__next__()` methods.
  ```python
  class CountDown:
      def __init__(self, count):
          self.count = count

      def __iter__(self):
          return self

      def __next__(self):
          if self.count <= 0:
              raise StopIteration
          self.count -= 1
          return self.count + 1
  ```
- **Generators**: Use `yield` to create iterators.
  ```python
  def count_down(count):
      while count > 0:
          yield count
          count -= 1
  ```

#### **2. Context Managers and the `with` Statement**
- **Context Managers**:
  ```python
  class MyContext:
      def __enter__(self):
          return "Entered context"

      def __exit__(self, exc_type, exc_value, traceback):
          print("Exited context")

  with MyContext() as value:
      print(value)
  ```

#### **3. Regular Expressions**
- **Using `re` Module**:
  ```python
  import re
  pattern = r"\d+"
  matches = re.findall(pattern, "There are 12 apples and 15 oranges.")
  ```

#### **4. Functional Programming Concepts**
- **Map, Filter, Reduce**:
  ```python
  from functools import reduce

  numbers = [1, 2, 3, 4, 5]
  squares = map(lambda x: x**2, numbers)
  evens = filter(lambda x: x % 2 == 0, numbers)
  sum_of_squares = reduce(lambda x, y: x + y, squares)
  ```

#### **5. Understanding Closures and Decorators**
- **Closures**:
  ```python
  def outer():
      x = 10
      def inner():
          return x
      return inner

  my_closure = outer()
  print(my_closure())  # Output: 10
  ```
- **Decorators**: Modify functions.
  ```python
  def add_one(func):
      def wrapper(x):
          return func(x) + 1
      return wrapper

  @add_one
  def square(x):
      return x ** 2

  print(square(4))  # Output: 17
  ```

### **Concurrency and Parallelism**

#### **1. Multithreading with `threading` Module**
- **Basic Example**:
  ```python
  import threading

  def print_numbers():
      for i in range(5):
          print(i)

  thread = threading.Thread(target=print_numbers)
  thread.start()
  ```

#### **2. Multiprocessing Basics**
- **Basic Example**:
  ```python
  from multiprocessing import Process

  def print_numbers():
      for i in range(5):
          print(i)

  process = Process(target=print_numbers)
  process.start()
  ```

#### **3. Async Programming with `asyncio`**
- **Basic Example**:
  ```python
  import asyncio

  async def say_hello():
      await asyncio.sleep(1)
      print("Hello")

  asyncio.run(say_hello())
  ```

### **Testing and Debugging**

#### **1. Writing Unit Tests with `unittest` and `pytest`**
- **unittest**:
  ```python
  import unittest

  class TestMath(unittest.TestCase):
      def test_add(self):
          self.assertEqual(1 + 1, 2)

  if __name__ == "__main__":
      unittest.main()
  ```
- **pytest**: Use similar syntax; simply write functions prefixed with `test_`.

#### **2. Debugging Techniques and Tools**
- **pdb**: Python's built-in debugger.
  ```python
  import pdb

  def faulty_function():
      x = 1
      pdb.set_trace()
      x += 1
      return x
  ```
- **Logging**:
  ```python
  import logging

  logging.basicConfig(level=logging.DEBUG)
  logging.debug("This is a debug message")
  ```

### **Working with APIs and Web Scraping**

#### **1. Making HTTP Requests with `requests` Module**
- **Example**:
  ```python
  import requests

  response = requests.get('https://api.github.com')
  print(response.json())
  ```

#### **2. Parsing HTML with BeautifulSoup**
- **Example**:
  ```python
  from bs4 import BeautifulSoup
  import requests

  response = requests.get('https://example.com')
  soup = BeautifulSoup(response.text, 'html.parser')
  print(soup.title.text)
  ```

#### **3. Understanding RESTful APIs**
- **Concept**: REST (Representational State Transfer) is a web service architecture that uses HTTP methods to interact with resources.

### **Final Projects**

#### **1. Build a Basic Command-Line Tool**
- **Project**: Create a CLI tool that performs a specific function, like a simple calculator or a file organizer.

#### **2. Create a Simple Web Scraper**
- **Project**: Write a script that extracts data from a webpage, such as scraping headlines from a news site.

#### **3. Automate a Task**
- **Project**: Develop a script to automate a repetitive task, like renaming files or sending automated emails.

#### **4. Capstone Project**
- **Project**: Combine multiple concepts to create a comprehensive application, such as a small web app, game, or data analysis tool.
