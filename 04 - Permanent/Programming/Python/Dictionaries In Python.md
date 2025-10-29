---
tags:
  - Dictionaries
  - python
  - Learning
  - Programming
  - coding
cssclasses:
  - pen-purple
aliases:
  - Dictionaries in python
---
**Dictionaries** in Python are versatile, mutable data structures that store key-value pairs. They are analogous to real-world dictionaries, where you look up a word (key) to find its definition (value). Here’s a detailed breakdown of dictionaries in Python:

#### 1. **Creating a Dictionary**

You can create a dictionary using curly braces `{}` with key-value pairs separated by colons `:`.

```python
# Basic dictionary
my_dict = {
    "name": "Alice",
    "age": 30,
    "city": "New York"
}
```

Alternatively, you can use the `dict()` constructor:

```python
# Using dict() constructor
my_dict = dict(name="Alice", age=30, city="New York")
```

#### 2. **Accessing Values**

To access a value, use the key inside square brackets `[]`. If the key does not exist, Python will raise a `KeyError`.

```python
print(my_dict["name"])  # Output: Alice
```

You can also use the `get()` method to avoid exceptions if the key is missing:

```python
print(my_dict.get("name"))  # Output: Alice
print(my_dict.get("job", "Not Found"))  # Output: Not Found
```

#### 3. **Adding and Updating Items**

You can add new key-value pairs or update existing ones by assigning a value to a key.

```python
# Adding a new key-value pair
my_dict["job"] = "Engineer"

# Updating an existing key-value pair
my_dict["age"] = 31
```

#### 4. **Removing Items**

To remove items, you can use the `del` statement, `pop()` method, or `popitem()` method:

```python
# Using del to remove a key-value pair
del my_dict["city"]

# Using pop() to remove a key and return its value
age = my_dict.pop("age")

# Using popitem() to remove and return the last key-value pair
item = my_dict.popitem()
```

#### 5. **Iterating Over Dictionaries**

You can iterate over keys, values, or both using methods like `keys()`, `values()`, and `items()`.

```python
# Iterating over keys
for key in my_dict.keys():
    print(key)

# Iterating over values
for value in my_dict.values():
    print(value)

# Iterating over key-value pairs
for key, value in my_dict.items():
    print(f"{key}: {value}")
```

#### 6. **Dictionary Comprehensions**

Dictionary comprehensions provide a concise way to create dictionaries. They are similar to list comprehensions.

```python
# Creating a dictionary where keys are numbers and values are their squares
squares = {x: x**2 for x in range(5)}
```

#### 7. **Nested Dictionaries**

Dictionaries can contain other dictionaries, allowing for more complex data structures.

```python
# Nested dictionary
people = {
    "Alice": {"age": 30, "city": "New York"},
    "Bob": {"age": 25, "city": "Los Angeles"}
}
```

#### 8. **Common Dictionary Methods**

- `clear()`: Removes all items from the dictionary.
- `copy()`: Returns a shallow copy of the dictionary.
- `fromkeys(iterable, value)`: Creates a new dictionary with keys from `iterable` and a specified value.
- `setdefault(key, default)`: Returns the value of `key` if it exists, otherwise inserts `key` with a `default` value.
- `update(dict)`: Updates the dictionary with key-value pairs from another dictionary.

#### Example Code

```python
# Example dictionary
my_dict = {
    "name": "Alice",
    "age": 30,
    "city": "New York"
}

# Accessing a value
print(my_dict["name"])  # Output: Alice

# Adding a new item
my_dict["job"] = "Engineer"

# Iterating over key-value pairs
for key, value in my_dict.items():
    print(f"{key}: {value}")

# Using get() with a default value
print(my_dict.get("salary", "Not Available"))  # Output: Not Available
```

Dictionaries are an essential part of Python and are used widely for their efficiency and versatility in handling key-value data. They are particularly useful for cases where fast lookups and easy data management are needed.