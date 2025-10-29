---
tags:
  - PythonBasics
  - Syntax
  - DataTypes
  - Modules
  - Operators
  - ControlFlow
  - Functions
  - Lists
  - Dictionaries
  - Exceptions
  - FileHandling
  - Classes
aliases:
  - Python Basics
  - PythonBasicsSyntax
  - SyntaxVariables and Data Types
  - DataTypesOperators
  - OperatorsControl Flow
  - ControlFlowFunctions
  - FunctionsLists
  - ListsDictionaries
  - DictionariesModules and Importing
  - ModulesException Handling
  - ExceptionsFile Handling
  - FileHandlingClasses and Objects
  - CheatSheet
  - Python Cheatsheet
cssclasses:
  - pen-purple
---
---

## Python Introduction Cheatsheet

### **Overview**

Python is a versatile, high-level programming language known for its readability and ease of use. This cheatsheet provides a quick reference to the core concepts and syntax of Python.

---

### **1. Basic Syntax**

- **Print Statement:**
  ```python
  print("Hello, World!")
  ```
  - *Usage:* Outputs the string `"Hello, World!"` to the console.

- **Comments:**
  ```python
  # This is a single-line comment
  """
  This is a
  multi-line comment
  """
  ```
  - *Single-Line Comment:* Starts with `#` and is used for brief explanations.
  - *Multi-Line Comment:* Enclosed in triple quotes `"""` and used for longer descriptions or docstrings.

---
### **2. Variables and Data Types**

- **Variable Assignment:**
  ```python
  x = 10          # Integer
  y = 3.14        # Float
  name = "Alice"  # String
  is_active = True  # Boolean
  ```
  - *Variables:* Store data values.
  - *Data Types:* Include integers, floats, strings, and booleans.

- **Data Types:**
  ```python
  # Integer
  x = 10  # Whole number

  # Float
  y = 3.14  # Decimal number

  # String
  name = "Alice"  # Sequence of characters

  # Boolean
  is_active = True  # Represents True or False
  ```

---
### **3. Basic Operators**

- **Arithmetic Operators:**
  ```python
  addition = 5 + 3       # Output: 8
  subtraction = 10 - 4   # Output: 6
  multiplication = 2 * 6 # Output: 12
  division = 8 / 2       # Output: 4.0
  modulus = 7 % 3        # Output: 1
  exponentiation = 2 ** 3 # Output: 8
  ```
  - *Operators:* Used to perform mathematical operations.

- **Comparison Operators:**
  ```python
  x == y  # Equal to: Checks if x is equal to y
  x != y  # Not equal to: Checks if x is not equal to y
  x > y   # Greater than: Checks if x is greater than y
  x < y   # Less than: Checks if x is less than y
  x >= y  # Greater than or equal to: Checks if x is greater than or equal to y
  x <= y  # Less than or equal to: Checks if x is less than or equal to y
  ```
  - *Operators:* Used for comparing values.

---
### **4. Control Flow**

- **Conditional Statements:**
  ```python
  if condition:
      # Executes if condition is true
  elif another_condition:
      # Executes if another_condition is true
  else:
      # Executes if none of the above conditions are true
  ```
  - *If-Else Statements:* Control the flow of execution based on conditions.

- **Loops:**

  - **For Loop:**
    ```python
    for i in range(5):
        print(i)  # Prints numbers 0 to 4
    ```
    - *For Loop:* Iterates over a sequence (e.g., a range of numbers).

  - **While Loop:**
    ```python
    count = 0
    while count < 5:
        print(count)
        count += 1  # Increments count
    ```
    - *While Loop:* Repeats as long as a condition is true.

---
### **5. Functions**

- **Defining a Function:**
  ```python
  def greet(name):
      """Function to greet a person by name."""
      print(f"Hello, {name}!")
  ```
  - *Function Definition:* Defines a reusable block of code.
  - *Docstring:* Provides a brief explanation of the function.

- **Calling a Function:**
  ```python
  greet("Alice")  # Calls the greet function with "Alice" as the argument
  ```
  - *Function Call:* Executes the function with specified arguments.

---
### **6. Lists**

- **Creating a List:**
  ```python
  fruits = ["apple", "banana", "cherry"]
  ```
  - *List:* An ordered collection of items.

- **Accessing Elements:**
  ```python
  first_fruit = fruits[0]  # "apple"
  ```
  - *Indexing:* Access elements by their position in the list.

- **Modifying Elements:**
  ```python
  fruits[1] = "blueberry"  # Changes "banana" to "blueberry"
  ```

- **Adding Elements:**
  ```python
  fruits.append("orange")  # Adds "orange" to the end of the list
  ```

- **List Comprehension:**
  ```python
  squares = [x ** 2 for x in range(5)]  # [0, 1, 4, 9, 16]
  ```
  - *List Comprehension:* Creates lists using concise expressions.

---
### **7. Dictionaries**

- **Creating a Dictionary:**
  ```python
  person = {
      "name": "Alice",
      "age": 30,
      "city": "New York"
  }
  ```
  - *Dictionary:* A collection of key-value pairs.

- **Accessing Values:**
  ```python
  name = person["name"]  # "Alice"
  ```

- **Adding/Updating Entries:**
  ```python
  person["email"] = "alice@example.com"  # Adds new entry
  ```

---
### **8. Modules and Importing**

- **Importing a Module:**
  ```python
  import math
  print(math.sqrt(16))  # 4.0
  ```
  - *Importing:* Includes external code libraries.

- **Importing Specific Functions:**
  ```python
  from math import sqrt
  print(sqrt(25))  # 5.0
  ```

---
### **9. Exception Handling**

- **Try-Except Block:**
  ```python
  try:
      result = 10 / 0  # Raises ZeroDivisionError
  except ZeroDivisionError:
      print("Cannot divide by zero!")
  finally:
      print("This will always execute.")
  ```
  - *Exception Handling:* Manages errors and ensures clean execution.

---
### **10. File Handling**

- **Reading a File:**
  ```python
  with open("file.txt", "r") as file:
      content = file.read()
      print(content)
  ```
  - *Reading Files:* Opens and reads file content.

- **Writing to a File:**
  ```python
  with open("file.txt", "w") as file:
      file.write("Hello, World!")
  ```
  - *Writing Files:* Creates or updates a file with content.

---
### **11. Classes and Objects**

- **Defining a Class:**
  ```python
  class Dog:
      def __init__(self, name):
          self.name = name
      
      def bark(self):
          print(f"{self.name} says woof!")
  
  # Creating an instance
  my_dog = Dog("Buddy")
  my_dog.bark()  # Buddy says woof!
  ```
  - *Classes:* Define blueprints for creating objects.
  - *Objects:* Instances of classes with properties and methods.

---
> Last Modified On 17-09-24  
> Best cheatsheet ever: [[The Cheatsheet Of Cheatsheets|CheatSheet]]
---

