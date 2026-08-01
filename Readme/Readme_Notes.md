# Python Interview Questions (Part 1)

## 1. What is Python?

**Answer**

Python is a high-level, interpreted, dynamically typed, object-oriented, and general-purpose programming language. It emphasizes readability and simplicity, making it suitable for web development, automation, data science, AI/ML, scripting, and backend development.

---

## 2. Why is Python so popular?

**Answer**

Python is popular because:

* Easy to learn and read
* Large standard library
* Cross-platform
* Supports multiple programming paradigms
* Huge ecosystem (NumPy, Pandas, Django, Flask, TensorFlow, PyTorch)
* Strong community support

---

## 3. What are the features of Python?

* High-level language
* Interpreted
* Dynamically typed
* Object-oriented
* Cross-platform
* Automatic memory management
* Large standard library
* Open source

---

# Variables

---

## 4. What is a variable?

**Answer**

A variable is a named reference to an object in memory. It allows a program to store, access, and manipulate data during execution.

---

## 5. Why is Python dynamically typed?

**Answer**

Python is dynamically typed because the type of a variable is determined at runtime. A variable can reference objects of different data types without explicit type declarations.

Example:

```python
x = 10
x = "Hello"
```

---

## 6. Difference between variable and object?

| Variable         | Object                |
| ---------------- | --------------------- |
| Reference        | Actual data           |
| Stores reference | Stores value and type |

---

## 7. Difference between dynamically typed and statically typed languages?

| Dynamic                 | Static                       |
| ----------------------- | ---------------------------- |
| Type decided at runtime | Type decided at compile time |
| Example: Python         | Example: Java, C++           |

---

# Data Types

---

## 8. What are Python's built-in data types?

* int
* float
* complex
* bool
* str
* list
* tuple
* dict
* set
* frozenset
* bytes
* bytearray
* range

---

## 9. What is mutable and immutable?

### Mutable

Objects whose contents can be modified.

Examples:

* list
* dict
* set

### Immutable

Objects whose contents cannot be modified after creation.

Examples:

* int
* float
* str
* tuple
* bool

---

## 10. Why are strings immutable?

**Answer**

Strings are immutable to improve memory optimization, hashing efficiency, thread safety, and to allow them to be used safely as dictionary keys.

---

## 11. Difference between List and Tuple?

| List        | Tuple       |
| ----------- | ----------- |
| Mutable     | Immutable   |
| []          | ()          |
| More memory | Less memory |
| Slower      | Faster      |

---

## 12. Difference between type() and isinstance()?

`type()`

Checks the exact type.

```python
type(5)
```

`isinstance()`

Checks inheritance as well.

```python
isinstance(5, int)
```

---

# Operators

---

## 13. Difference between == and is?

`==`

Compares values.

`is`

Compares object identity (memory reference).

Example:

```python
a = [1,2]
b = [1,2]

a == b     # True
a is b     # False
```

---

## 14. Difference between / and //?

`/`

Floating-point division.

```python
5 / 2 = 2.5
```

`//`

Floor division.

```python
5 // 2 = 2
```

---

## 15. What is short-circuit evaluation?

Python stops evaluating a logical expression as soon as the final result is known.

Example:

```python
True or anything
```

Python doesn't evaluate `anything`.

---

# Input & Output

---

## 16. Why does input() always return a string?

Keyboard input is read as text by default. Convert it using `int()`, `float()`, etc., if needed.

---

## 17. Difference between print() and return()?

| print()                  | return()                       |
| ------------------------ | ------------------------------ |
| Displays output          | Sends value back to the caller |
| Used for display         | Used inside functions          |
| Doesn't end the function | Ends the function              |

---

# Conditions

---

## 18. What is a conditional statement?

A conditional statement controls the flow of execution based on whether a Boolean expression evaluates to `True` or `False`.

---

## 19. Difference between if, elif, and else?

* `if` checks the first condition.
* `elif` checks additional conditions if previous ones are false.
* `else` executes when all previous conditions are false.

---

## 20. What are Truthy and Falsy values?

Falsy values:

```python
False
None
0
0.0
''
[]
{}
set()
```

Everything else is Truthy.

---

# Loops

---

## 21. Difference between for and while?

| for                      | while                                |
| ------------------------ | ------------------------------------ |
| Known iterations         | Unknown iterations                   |
| Iterates over a sequence | Runs until a condition becomes false |

---

## 22. Difference between break, continue, and pass?

### break

Terminates the loop immediately.

### continue

Skips the current iteration and proceeds to the next.

### pass

Acts as a placeholder and performs no operation.

---

## 23. What does range() return?

A `range` object that generates numbers lazily.

---

## 24. What is enumerate()?

Returns both the index and value while iterating.

---

## 25. What is zip()?

Combines multiple iterables element-wise into tuples.

---

# Functions

---

## 26. What is a function?

A reusable block of code that performs a specific task.

---

## 27. Difference between parameter and argument?

Parameters are variables defined in the function definition.

Arguments are actual values passed during the function call.

---

## 28. What is recursion?

A technique where a function calls itself until a base condition is reached.

---

## 29. What is a lambda function?

An anonymous function created using the `lambda` keyword, typically used for simple, short operations.

---

## 30. What are *args and **kwargs?

### *args

Accepts a variable number of positional arguments.

### **kwargs

Accepts a variable number of keyword arguments.

---

# File Handling

---

## 31. What is file handling?

The process of reading, writing, creating, updating, and managing files stored on secondary storage.

---

## 32. Difference between read(), readline(), and readlines()?

| Method        | Purpose                     |
| ------------- | --------------------------- |
| `read()`      | Reads the entire file       |
| `readline()`  | Reads one line              |
| `readlines()` | Returns a list of all lines |

---

## 33. Difference between w and a mode?

`w`

Overwrites existing content.

`a`

Appends data while preserving existing content.

---

## 34. Why should we use with open()?

It automatically closes the file, even if an exception occurs.

---

# Exception Handling

---

## 35. What is an exception?

An exception is a runtime event that interrupts the normal flow of program execution.

---

## 36. Difference between Error and Exception?

Errors are generally unrecoverable programming issues, while exceptions are runtime conditions that can be handled.

---

## 37. Difference between try, except, else, and finally?

* `try`: Contains code that might raise an exception.
* `except`: Handles the exception.
* `else`: Executes if no exception occurs.
* `finally`: Always executes, making it ideal for cleanup.

---

## 38. Why do we use exception handling?

To prevent unexpected program termination and handle runtime errors gracefully.

---

## 39. What is raise?

The `raise` statement is used to explicitly trigger an exception.

---

# Generators

---

## 40. What is a generator?

A generator is a special type of iterator that produces values lazily using the `yield` keyword, generating one value at a time instead of storing all values in memory.

---

## 41. Why are generators memory efficient?

Because they generate values on demand rather than creating the entire sequence at once.

---

## 42. Difference between yield and return?

| yield                              | return            |
| ---------------------------------- | ----------------- |
| Pauses the function                | Ends the function |
| Produces multiple values over time | Returns one value |
| Preserves state                    | Discards state    |

---

## 43. What is lazy evaluation?

A technique where values are generated only when requested, reducing memory usage.

---

## 44. Difference between List and Generator?

| List              | Generator                          |
| ----------------- | ---------------------------------- |
| Stores all values | Produces values on demand          |
| More memory       | Less memory                        |
| Supports indexing | Does not support indexing directly |

---

# Iterators

---

## 45. What is an iterator?

An object that returns one element at a time using the iterator protocol (`__iter__()` and `__next__()`).

---

## 46. Difference between Iterable and Iterator?

| Iterable                            | Iterator                           |
| ----------------------------------- | ---------------------------------- |
| Can be looped over                  | Produces elements one by one       |
| Uses `iter()` to create an iterator | Uses `next()` to retrieve elements |

---

## 47. Is every generator an iterator?

Yes.

---

## 48. Is every iterator a generator?

No.

---

# Decorators

---

## 49. What is a decorator?

A decorator is a function that accepts another function, extends or modifies its behavior, and returns a new wrapped function without changing the original function.

---

## 50. Why are decorators used?

* Logging
* Authentication
* Authorization
* Caching
* Timing functions
* Code reuse
* Avoiding duplication (DRY principle)

---

## 51. What does @decorator mean?

It is syntactic sugar for:

```python
function = decorator(function)
```

---

## 52. Why are functions called first-class objects?

Because they can be assigned to variables, passed as arguments, returned from other functions, and stored in data structures.

---

# Copying

---

## 53. What happens when you write b = a?

Both variables refer to the same object. No new object is created.

---

## 54. What is a shallow copy?

A shallow copy creates a new outer object but shares references to nested objects.

---

## 55. What is a deep copy?

A deep copy creates a completely independent copy of an object, including all nested objects.

---

## 56. Difference between assignment, shallow copy, and deep copy?

| Feature               | Assignment | Shallow Copy | Deep Copy |
| --------------------- | ---------- | ------------ | --------- |
| New outer object      | ❌          | ✅            | ✅         |
| New nested objects    | ❌          | ❌            | ✅         |
| Shares nested objects | ✅          | ✅            | ❌         |

---

# ⭐ Top 15 Questions You Must Answer Perfectly

These are the ones interviewers ask most often:

1. What is Python?
2. Why is Python dynamically typed?
3. Mutable vs Immutable?
4. List vs Tuple?
5. `==` vs `is`?
6. `print()` vs `return()`?
7. `for` vs `while`?
8. `break` vs `continue` vs `pass`?
9. Parameter vs Argument?
10. What is Recursion?
11. What is Exception Handling?
12. What is a Generator?
13. `yield` vs `return`?
14. What is a Decorator?
15. Shallow Copy vs Deep Copy?

---

