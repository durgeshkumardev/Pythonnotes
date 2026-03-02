# 🐍 Introduction to Python Programming

Welcome to Python! This document explains what Python is, where it is used, its advantages and disadvantages, the software used to write Python programs, and important Python libraries.

---

## 📌 What is Python?

Python is a **high-level, interpreted programming language** that is easy to read and write.  
It is widely used for building applications, automating tasks, and working with data.

Python was created by **Guido van Rossum** and released in 1991.

Python focuses on **simple syntax** and **easy understanding**, which makes it very popular among beginners and professionals.

---

## 🌍 Where is Python Mostly Used?

Python is used in many real-world fields:

### 🌐 1. Web Development
Python is used to build websites and web applications.

### 📊 2. Data Science & Data Analysis
Used for data processing, visualization, and analysis.

### 🤖 3. Artificial Intelligence (AI) & Machine Learning
Python is the most popular language for AI and ML projects.

### 🎮 4. Game Development
Used to build simple games and game tools.

### 🧪 5. Scientific Computing
Used in research, simulations, and scientific calculations.

### ⚙️ 6. Automation & Scripting
Used to automate repetitive tasks like file handling and system tasks.

### 📱 7. Desktop Applications
Used to build desktop software applications.

---

## ✅ Advantages of Python

✔ Easy to learn and understand  
✔ Simple and readable syntax  
✔ Large number of built-in libraries  
✔ Works on Windows, Mac, and Linux  
✔ Huge community support  
✔ Good for beginners and professionals  
✔ Supports multiple programming styles (OOP, functional, procedural)

---

## ❌ Disadvantages of Python

✖ Slower than languages like C and Java  
✖ Not ideal for mobile app development  
✖ Uses more memory compared to some languages  
✖ Not the best for high-performance game engines  

---

## 💻 Software Used to Write Python Code

To write Python programs, we use **code editors or IDEs (Integrated Development Environments)**.

### Popular Software for Python:

| Software | Type | Use |
|----------|------|-----|
| VS Code | Code Editor | Most popular and lightweight |
| PyCharm | IDE | Powerful for large projects |
| IDLE | Python’s built-in editor | Good for beginners |
| Jupyter Notebook | Interactive tool | Best for data science |
| Notepad++ | Text editor | Simple coding |

---

## 📚 Important Python Libraries

Libraries are collections of pre-written code that help us do tasks easily.

### 🌐 Web Development
- **Django** → Full-featured web framework  
- **Flask** → Lightweight web framework  

### 📊 Data Science & Analysis
- **NumPy** → Numerical calculations  
- **Pandas** → Data analysis  
- **Matplotlib** → Data visualization  
- **Seaborn** → Advanced charts  

### 🤖 Machine Learning & AI
- **Scikit-learn** → Machine learning tools  
- **TensorFlow** → Deep learning  
- **Keras** → Neural networks  

### 🖼 Image Processing
- **OpenCV** → Image and video processing  
- **Pillow** → Image editing  

### 🎮 Game Development
- **Pygame** → Making games  

### 🖥 Desktop Applications
- **Tkinter** → GUI applications  
- **PyQt** → Advanced GUI apps  

### 🌐 Web Scraping
- **BeautifulSoup** → Extract data from websites  
- **Scrapy** → Web scraping framework  

---

# 🐍 Python Basics: Variables, Data Types, and Input/Output

This guide explains the fundamental building blocks of Python programming.

---

## 📌 1. Variables in Python

A **variable** is used to store data in a program.  
Think of a variable as a **container** that holds a value.

### Rules for Naming Variables
✔ Can contain letters, numbers, and underscores  
✔ Must start with a letter or underscore  
❌ Cannot start with a number  
❌ Cannot use Python keywords (like if, else, for)

### Example:
```python
name = "Rahul"
age = 20
marks = 85.5
```

- name stores text

- age stores a whole number

- marks stores a decimal number

- Python automatically understands the type of variable based on the value.

| Data Type | Description     | Example     |
| --------- | --------------- | ----------- |
| `int`     | Whole numbers   | 10, 25      |
| `float`   | Decimal numbers | 10.5, 99.9  |
| `str`     | Text (String)   | "Hello"     |
| `bool`    | True/False      | True, False |


---

```x = 10          # int
y = 5.5         # float
name = "Python" # str
is_active = True # bool
```




### Operators are symbols used to perform operations on variables and values.

Example:
```python
a = 10
b = 5
print(a + b)  # Output: 15
```

### 1. Arithmetic Operators
- Used to perform mathematical operations.

| Operator | Meaning             | Example | Output |
|----------|---------------------|---------|--------|
| +        | Addition            | 5 + 3   | 8      |
| -        | Subtraction         | 5 - 3   | 2      |
| *        | Multiplication      | 5 * 3   | 15     |
| /        | Division            | 10 / 2  | 5.0    |
| %        | Modulus (Remainder) | 10 % 3  | 1      |
| **       | Exponent (Power)    | 2 ** 3  | 8      |
| //       | Floor Division      | 10 // 3 | 3      |

Example:

```python
a = 10
b = 3
print(a + b)   # 13
print(a // b)  # 3
```

### 📌 2. Comparison Operators
Used to compare two values. The result is always **True or False**.

| Operator | Meaning               | Example |
|----------|-----------------------|---------|
| ==       | Equal to              | a == b  |
| !=       | Not equal             | a != b  |
| >        | Greater than          | a > b   |
| <        | Less than             | a < b   |
| >=       | Greater than or equal | a >= b  |
| <=       | Less than or equal    | a <= b  |

Example:

```python
x = 10
y = 5
print(x > y)  # True
```
---

### 3. Logical Operators
Used to combine multiple conditions.

| Operator | Meaning                                | Example          |
|----------|----------------------------------------|------------------|
| and      | True if both conditions are true       | x > 5 and x < 20 |
| or       | True if at least one condition is true | x < 5 or x > 8   |
| not      | Reverses the condition                 | not(x > 5)       |

Example:

```python
age = 25
print(age > 18 and age < 60)  # True
```

---

### 4. Assignment Operators
Used to assign values to variables.
| Operator | Example | Same As      |
| -------- | ------- | ------------ |
| =        | x = 5   | Assign value |
| +=       | x += 3  | x = x + 3    |
| -=       | x -= 3  | x = x - 3    |
| *=       | x *= 3  | x = x * 3    |
| /=       | x /= 3  | x = x / 3    |
| %=       | x %= 3  | x = x % 3    |
| **=      | x **= 3 | x = x ** 3   |
| //=      | x //= 3 | x = x // 3   |



### 📌 5. Membership Operators
Used to check if a value exists in a sequence.

| Operator | Meaning              | Example            |
| -------- | -------------------- | ------------------ |
| in       | Value exists         | "a" in "apple"     |
| not in   | Value does not exist | "z" not in "apple" |

```fruits = ["apple", "banana"]
print("apple" in fruits)  # True
```
---

### 6. Identity Operators
Used to compare memory locations of two objects.

| Operator | Meaning           | Example    |
| -------- | ----------------- | ---------- |
| is       | Same object       | a is b     |
| is not   | Different objects | a is not b |

```
x = [1, 2]
y = x
print(x is y)  # True
```


---

## 📌 What is a Condition?

A **condition** is a statement that checks whether something is **True or False**.

Conditions help a program make decisions.

In simple words:  
👉 A condition allows the program to choose what to do next.

---

## 🌍 Real-Life Example of a Condition

- If it is raining → Take an umbrella  
- If marks ≥ 40 → Pass  
- If age ≥ 18 → Can vote  

Just like in real life, computers also make decisions using conditions.

---

## 🎯 Why Are Conditions Used?

Conditions are used to:
- Make decisions in a program  
- Control the flow of the program  
- Run different code based on different situations  

Without conditions, a program would run the same way every time and could not make choices.

---

## 📌 Types of Conditions in Python

Python mainly uses:

1. `if` statement  
2. `if-else` statement  
3. `if-elif-else` statement  

---

## 🔹 1. `if` Statement

Used when we want code to run **only if a condition is true**.

### Syntax:
```
if condition:
    statement

age = 20

if age >= 18:
    print("You are eligible to vote")
```
### 2. if-else Statement
- Used when there are two choices.
### Syntax:
```

if condition:
    statement1
else:
    statement2
```
### Example 
```
num = 7

if num % 2 == 0:
    print("Even number")
else:
    print("Odd number")
```

### 3. if-elif-else Statement
- Used when there are multiple conditions.
# Syntax
```
if condition1:
    statement1
elif condition2:
    statement2
else:
    statement3
```
# Example
```
marks = 85
if marks >= 90:
    print("Grade A")
elif marks >= 75:
    print("Grade B")
elif marks >= 50:
    print("Grade C")
else:
    print("Fail")

```

### Conditions Use Comparison Operators
| Operator | Meaning               |
| -------- | --------------------- |
| ==       | Equal to              |
| !=       | Not equal             |
| >        | Greater than          |
| <        | Less than             |
| >=       | Greater than or equal |
| <=       | Less than or equal    |



### Conditions Can Use Logical Operators

| Operator | Meaning                             |
| -------- | ----------------------------------- |
| and      | Both conditions must be true        |
| or       | At least one condition must be true |
| not      | Reverses the condition              |

---

# 🔁 Loops in Python 

---

## 📌 What is a Loop?

A **loop** is used to repeat a block of code multiple times.

Instead of writing the same code again and again, we use a loop to do the repetition automatically.

---

## 🌍 Real-Life Example of a Loop

- Taking attendance of 50 students one by one  
- Printing numbers from 1 to 100  
- Asking for password until correct  

These repeated actions are similar to loops in programming.

---

## 🎯 Why Are Loops Used?

Loops help to:
- Save time and code  
- Avoid repeating the same instructions  
- Perform tasks multiple times automatically  

---

## 📌 Types of Loops in Python

Python mainly has two loops:

1. `for` loop  
2. `while` loop  

---

# 🔹 1. `for` Loop

Used when we know **how many times** we want to repeat something.

### Syntax:
```
for variable in sequence:
    statement
```

### Example
```
for i in range(1, 6):
    print(i)
```

### range() Function
 range() generates a sequence of numbers.

| Code          | Output    |
| ------------- | --------- |
| range(5)      | 0,1,2,3,4 |
| range(1,6)    | 1,2,3,4,5 |
| range(1,10,2) | 1,3,5,7,9 |

### Example : Even Numbers from 1 to 10
```
for i in range(1, 11):
    if i % 2 == 0:
        print(i)
```
--- 

### 2. `while` Loop
Used when we don’t know how many times the loop should run.
It runs until a condition becomes False.

# Syntax:
```
while condition:
    statement
```

### Example: Print Numbers 1 to 5
```
i = 1
while i <= 5:
    print(i)
    i += 1
```
---
### Infinite Loop
- If we forget to update the variable inside a while loop, the loop will run forever.
# Example of infinite loop:
```
i = 1
while i <= 5:
    print(i)   # i never changes
```
---

### 🔹 Loop Control Statements
These help control the loop flow.

### 1🔸 break
Stops the loop immediately.

```
for i in range(1, 6):
    if i == 3:
        break
    print(i)
```
### Output:
```
1
2
4
5
```
--- 

### continue
Skips the current iteration and moves to the next.
```
for i in range(1, 6):
    if i == 3:
        continue
    print(i)
```
# Output:
```
1
2
4
5
```
--- 
### Nested Loops
```
for i in range(1, 4):
    for j in range(1, 3):
        print(i, j)
```
# Output:
```
1 1
1 2
2 1
2 2
3 1
3 2
```
---

### Loop with Condition
We can use conditions inside loops
```
for i in range(1, 11):
    if i > 5:
        print(i)
```
## ⭐ Important Points to Remember

- `for` loop is used when the number of repetitions is known  
- `while` loop runs based on a condition  
- Always update variables in `while` loops  
- `break` stops the loop immediately  
- `continue` skips the current loop cycle  
- Loops reduce repeated code and save time  

----   

# 🔁 `break` and `continue` in Python

When working with loops, sometimes we want to **change the normal flow** of the loop.  
Python provides two special statements for this:

- `break`
- `continue`

---

## 🛑 `break` Statement

The **break** statement is used to **stop the loop immediately**, even if the loop condition is still true.

👉 It completely exits the loop.

### Syntax:
```python
for variable in sequence:
    if condition:
        break
```

# Example Using break in a for loop
```
for i in range(1, 6):
    if i == 3:
        break
    print(i)
```
### Example Using break in a while loop
```
i = 1
while i <= 5:
    if i == 4:
        break
    print(i)
    i += 1
```
----
### continue Statement
- The continue statement is used to skip the current iteration and move to the next one.

# Syntax:
```
for variable in sequence:
    if condition:
        continue
```
# Example Using continue in a for loop
```
for i in range(1, 6):
    if i == 3:
        continue
    print(i)
```
# Example Using continue in a while loop
```
i = 0
while i < 5:
    i += 1
    if i == 3:
        continue
    print(i)

```
---

# Important Points to Remember

- `break` is used to exit a loop early

- `continue` is used to skip one iteration

- Both are used inside loops (for or while)

These help control loop behavior more efficiently

----


# 🔤 String Operations in Python 

---

## 📌 What is a String?

A **string** is a sequence of characters (letters, numbers, symbols) enclosed in quotes.

Examples:
```python
name = "Rahul"
message = 'Hello World'
```

### 1. String Concatenation (Joining Strings)
# We use + to join two strings.

# Example 

```
first = "Hello"
second = "World"
result = first + " " + second
print(result)
```

# 2. String Repetition
```
word = "Hi "
print(word * 3)
```

# 3. Finding Length of a String
- We use the len() function.
```
text = "Python"
print(len(text))
```
# 4. Accessing Characters (Indexing)
- Each character in a string has an index number.
- Example
```
text = "Python"
print(text[0])  # First character
print(text[3])  # Fourth character

```
---

# 5. String Slicing
- Slicing is used to get part of a string.
```
text = "Python"
print(text[0:4])
```
---
###  6. Changing Case
```
text = "python"
print(text.upper())   # PYTHON
print(text.lower())   # python
print(text.capitalize())  # Python
```
# Checking Text
```
text = "Hello Python"

print("Python" in text)   # True
print("Java" not in text) # True
```

# 8. Replacing Text
```
text = "I like Java"
print(text.replace("Java", "Python"))
```
---

# 9. Removing Spaces
```
text = "  Hello  "
print(text.strip())
```
# Splitting a String
```
text = "apple,banana,orange"
fruits = text.split(",")
print(fruits)
```
- output

['apple', 'banana', 'orange']


# 11. Joining Strings from a List
```
words = ["Python", "is", "fun"]
sentence = " ".join(words)
print(sentence)
```

----

# Strings have many built-in functions that make text processing easy.

## 📌 Case Conversion Functions

| Function | Description | Example |
|----------|-------------|---------|
| `upper()` | Converts string to uppercase | `"python".upper()` → `PYTHON` |
| `lower()` | Converts string to lowercase | `"PYTHON".lower()` → `python` |
| `capitalize()` | First letter capital | `"python".capitalize()` → `Python` |
| `title()` | Capitalizes each word | `"hello world".title()` → `Hello World` |
| `swapcase()` | Swaps upper & lower case | `"PyThOn".swapcase()` → `pYtHoN` |

---

## 📌 Searching Functions

| Function | Description | Example |
|----------|-------------|---------|
| `find()` | Returns index of substring | `"hello".find("e")` → `1` |
| `rfind()` | Finds from right | `"hello".rfind("l")` → `3` |
| `index()` | Like find but gives error if not found | `"hello".index("e")` → `1` |
| `count()` | Counts occurrences | `"banana".count("a")` → `3` |
| `startswith()` | Checks starting text | `"python".startswith("py")` → `True` |
| `endswith()` | Checks ending text | `"python".endswith("on")` → `True` |

---

## 📌 Checking (Boolean) Functions

| Function | Description | Example |
|----------|-------------|---------|
| `isalpha()` | Only letters | `"Hello".isalpha()` → `True` |
| `isdigit()` | Only numbers | `"123".isdigit()` → `True` |
| `isalnum()` | Letters & numbers | `"abc123".isalnum()` → `True` |
| `islower()` | All lowercase | `"hello".islower()` → `True` |
| `isupper()` | All uppercase | `"HELLO".isupper()` → `True` |
| `isspace()` | Only spaces | `"   ".isspace()` → `True` |
| `istitle()` | Title case | `"Hello World".istitle()` → `True` |

---

## 📌 Modification Functions

| Function | Description | Example |
|----------|-------------|---------|
| `replace()` | Replaces text | `"I like Java".replace("Java","Python")` |
| `strip()` | Removes spaces both sides | `"  hi  ".strip()` → `"hi"` |
| `lstrip()` | Removes left spaces | `"  hi".lstrip()` → `"hi"` |
| `rstrip()` | Removes right spaces | `"hi  ".rstrip()` → `"hi"` |
| `split()` | Splits into list | `"a,b,c".split(",")` |
| `join()` | Joins list into string | `" ".join(["Hi","All"])` |

---

## 📌 Alignment Functions

| Function | Description | Example |
|----------|-------------|---------|
| `center()` | Center align text | `"hi".center(10)` |
| `ljust()` | Left align | `"hi".ljust(10)` |
| `rjust()` | Right align | `"hi".rjust(10)` |
| `zfill()` | Fills with zeros | `"5".zfill(3)` → `"005"` |

---

## 📌 Other Useful Functions

| Function | Description | Example |
|----------|-------------|---------|
| `len()` | Length of string | `len("Python")` → `6` |
| `format()` | String formatting | `"My name is {}".format("Rahul")` |
| `encode()` | Converts to bytes | `"hello".encode()` |

---

## ⭐ Important Points

- Strings are **immutable** (cannot be changed directly)
- Most string functions return a **new string**
- Indexing starts from **0**
- Strings support slicing like `text[0:3]`


---

## 📌 What is a Function?

A **function** is a reusable block of code that performs a specific task.

Instead of writing the same code again and again, we write it once inside a function and call it whenever needed.

Think of a function like a **machine**:
Input ➜ Process ➜ Output

---

## ❓ Why Do We Need Functions?

Without functions:
- Code becomes very long
- Hard to understand
- Repetition of code

With functions:
- Code becomes short
- Easy to understand
- Reusable
- Well organized

---

## 🌟 Advantages of Functions

✔ Code Reusability  
✔ Easy Debugging  
✔ Better Readability  
✔ Saves Time  
✔ Breaks big problems into small parts  
✔ Helpful in teamwork  

---

## 🔢 Types of Functions in Python

### 1️⃣ Built-in Functions
These are already provided by Python.

Examples:
```python
print()
len()
type()
sum()
max()
min()
```
# 2️⃣ User-Defined Functions
- Functions created by the programmer using def.
```
def greet():
    print("Hello!")
```

### Functions Based on Arguments and Return Value
# A) No Arguments, No Return Value
```
def hello():
    print("Hello World")

hello()
```
# B) Arguments, No Return Value
```
def greet(name):
    print("Hello", name)

greet("XYZ")

```
### No Arguments, With Return Value
```
def get_number():
    return 10

print(get_number())
```
# D) Arguments, With Return Value
```
def add(a, b):
    return a + b

result = add(5, 3)
print(result)
```


### How to Define a Function
- Syntax:
```
def function_name(parameters):
    # code block
    return value   # optional
```
### How to Call a Function
- After defining a function, you must call it.
```
function_name(arguments)
```

----
# Example Combining Everything
```
def student_info(name, age):
    print("Name:", name)
    print("Age:", age)
    return "Data Saved"

msg = student_info("Durgesh", 22)
print(msg)
```


---


## 📌 What is a Data Structure?

A **data structure** is a way to **store, organize, and manage data** efficiently
so that it can be accessed and modified easily.

Example:
- List of students
- Marks of subjects
- User details (name, age, email)

---

## ❓ Why Do We Use Data Structures?

Without data structures:
- Data is unorganized
- Searching is slow
- Updating is difficult

With data structures:
- Data is organized
- Faster access
- Easy modification
- Better performance

---

## 🔢 Types of Data Structures in Python

Python has **4 built-in data structures**:

| Data Structure | Ordered | Mutable | Allows Duplicates |
|---------------|--------|---------|-------------------|
| List | Yes | Yes | Yes |
| Tuple | Yes | No | Yes |
| Set | No | Yes | No |
| Dictionary | Yes | Yes | No (keys) |

---

# 1️⃣ List

## 📌 What is a List?
A **list** is an ordered and mutable collection of items.

### Syntax
```python
my_list = [1, 2, 3, "Python"]
```
---

# 2️⃣ Tuple
# What is a Tuple?
- A tuple is an ordered but immutable collection.

# Syntax
```
my_tuple = (1, 2, 3)
```
# Example
```
colors = ("red", "green", "blue")

```
# Where Tuple is Used?
-Fixed data

-Coordinates (x, y)

-Configuration values
---

# 3️⃣ Set
# What is a Set?
-A set is an unordered collection of unique elements.

# Syntax
```
my_set = {1, 2, 3}
```
# Where Set is Used?

- Removing duplicates

- Membership testing

- Mathematical operations


---
# 4️⃣ Dictionary

#  What is a Dictionary?
- A dictionary stores data in key–value pairs.
# Syntax
```
student = {
    "name": "Durgesh",
    "age": 22,
    "course": "Python"
}

```

--- 
# All Operations & Functions
# 🔹 1. LIST (Ordered, Mutable, Allows Duplicates)

# ✅ Create a List

- syntax

```
numbers = [10, 20, 30, 40]

```

# List Functions & Operations

# Add Elements
```
numbers.append(50)
numbers.insert(1, 15)
numbers.extend([60, 70])
```
# Remove Elements
```
numbers.remove(20)   # remove by value
numbers.pop()        # remove last
numbers.pop(1)       # remove by index
numbers.clear()      # remove all
```
# Access Elements

```
numbers[0]
numbers[-1]
numbers[1:4]

```
# Update Elements

```
numbers[0] = 100
```
# List Information
```
len(numbers)
max(numbers)
min(numbers)
sum(numbers)
```
# Sort & Reverse

```
numbers.sort()
numbers.sort(reverse=True)
numbers.reverse()
```
# Search
```
numbers.index(30)
numbers.count(10)
```
# 🔄 Loop
```
for n in numbers:
    print(n)
```
# Where List is Used?

- Dynamic data
-  Student lists
- Shopping carts

---

# 2. TUPLE (Ordered, Immutable, Allows Duplicates)
# Create a Tuple
```
colors = ("red", "green", "blue", "red")

```
# Tuple Functions & Operations
# Access
```
colors[0]
colors[-1]
colors[1:3]
```

# Tuple Information
- syntax
```
len(colors)
colors.count("red")
colors.index("green")
```

# Loop
```
for c in colors:
    print(c)
```

# Convert Tuple

```
list(colors)
tuple([1, 2, 3])
```

# Cannot modify:
```
colors[0] = "black"  # ERROR
```
# Where Tuple is Used?

- Fixed data
- Coordinates
- Read-only values
---- 

# 3. SET (Unordered, Mutable, No Duplicates)

# Create a Set
```
nums = {1, 2, 3, 4}
```

# Set Functions & Operations
# Add Elements
```
nums.add(5)
nums.update([6, 7])
```
# Remove Elements
```
nums.remove(3)
nums.discard(10)  # no error if not found
nums.pop()
nums.clear()
```
# Membership
```
2 in nums
```
# Set Mathematical Operations

```
a = {1, 2, 3}
b = {3, 4, 5}

a.union(b)
a.intersection(b)
a.difference(b)
a.symmetric_difference(b)

```
# Loop
```
for n in nums:
    print(n)
```

# Where Set is Used?


---
4. DICTIONARY (Key–Value Pairs)

# Create Dictionary
```
student = {
    "name": "Durgesh",
    "age": 22,
    "course": "Python"
}
```
# Dictionary Functions & Operations
```
student["name"]
student.get("age")
```
# Add / Update
```
student["city"] = "Delhi"
student["age"] = 23
```

# Remove
```
student.pop("age")
del student["course"]
student.clear()
```

# Dictionary Info
```
student.keys()
student.values()
student.items()
len(student)
```
# Loop Dictionary
```
for key, value in student.items():
    print(key, value)
```
----

# What is List Comprehension?
-List comprehension is a short and clean way to create lists using a single line of code instead of writing long loops.

-It replaces:

-for loop

-append()

-Multiple lines of code

-with one readable line.

# Why Do We Use List Comprehension?
-Without list comprehension:

-❌ More code
-❌ Less readable
-❌ Slower to write

# With list comprehension:

-✅ Short code
-✅ More readable
-✅ Faster execution
-✅ Pythonic way (preferred in Python)

# Basic Syntax
```
[expression for item in iterable]
```
#  Meaning:
-expression → What you want to store

-item → Each value from loop

-iterable → List / range / string etc.

# Example 1: Without vs With List Comprehension

```
numbers = []
for i in range(5):
    numbers.append(i)

print(numbers)
```
# Using List Comprehension
```
numbers = [i for i in range(5)]
print(numbers)

```

# Example 2: Square of Numbers
# Using Loop
```
squares = []
for i in range(1, 6):
    squares.append(i*i)
```
# Using List Comprehension
```
squares = [i*i for i in range(1, 6)]
```

# Example 3: With Condition (if)

# Syntax
```
[expression for item in iterable if condition]
```

# Get Only Even Numbers

```
evens = [i for i in range(10) if i % 2 == 0]
print(evens)
```
# Example 4: Convert Strings to Uppercase

```
names = ["durgesh", "aman", "ravi"]

upper_names = [name.upper() for name in names]
print(upper_names)
```

# Example 5: Filter Data
```
names = ["Ram", "Durgesh", "Amit", "Shiv"]

long_names = [n for n in names if len(n) > 4]
print(long_names)
```

# Normal Loop vs List Comprehension

| Feature     | Loop   | List Comprehension |
| ----------- | ------ | ------------------ |
| Code Length | Long   | Short              |
| Readability | Medium | High               |
| Speed       | Slower | Faster             |
| Pythonic    | No     | Yes                |

---

# What is Exception Handling in Python?
-Exception Handling is a way to handle runtime errors so that the program does not stop suddenly and can continue safely.

# It allows you to manage errors using:
```
try → except → else → finally
```

# Why Do We Need Exception Handling?
Without exception handling:
❌ Program crashes
❌ User sees error messages
❌ Application stops working

With exception handling:
✅ Prevent crashes
✅ Show friendly messages
✅ Handle invalid input
✅ Safe execution

# Basic Syntax
```
try:
    # Code that may cause error
except:
    # Code to handle error
```

# Example 1: Handling Division Error
```
try:
    a = int(input("Enter number: "))
    b = int(input("Enter number: "))
    print(a / b)
except:
    print("Error occurred!")
```

# Catch Specific Exception (Best Practice)

```
try:
    x = int("abc")
except ValueError:
    print("Invalid conversion!")
```

# Multiple Exceptions

```
try:
    a = int(input())
    b = int(input())
    print(a / b)
except ValueError:
    print("Enter valid number!")
except ZeroDivisionError:
    print("Cannot divide by zero!")
```

# Using else Block

```
try:
    x = int(input("Enter number: "))
except ValueError:
    print("Invalid input")
else:
    print("You entered:", x)
```
# Using finally Block
-Always runs whether error occurs or not.
```
try:
    print("Trying...")
except:
    print("Error")
finally:
    print("This always runs")
```

# Full Structure

```
try:
    # risky code
except ExceptionType:
    # handle error
else:
    # runs if no error
finally:
    # always runs
```

# Example: Real-Life Input Validation
```
try:
    age = int(input("Enter age: "))
    if age < 0:
        raise ValueError("Age cannot be negative")
except ValueError as e:
    print("Error:", e)
else:
    print("Age saved successfully")
```
# Raising Custom Exception

```
x = -5

if x < 0:
    raise Exception("Negative value not allowed")
```
# Exception Object (as e)
```
try:
    10 / 0
except ZeroDivisionError as e:
    print("Error message:", e)
```

# File Handling with Exception (Real Use)

```
try:
    f = open("data.txt")
except FileNotFoundError:
    print("File not found!")
finally:
    print("Execution complete")
```
--- 
# 
# What is File Handling?
# File Handling means working with files to:
-Create files

-Read data

-Write data

-Update data

-Delete data

-Python provides built-in functions to do this.
---
# Why Do We Use File Handling?
# Without files:
#❌ Data is temporary (lost after program ends)

#With files:
-✅ Data is saved permanently
-✅ Used for logs, reports, user data
-✅ Helps in real-world applications

# Opening a File
# Syntax:
```
open("filename", "mode")
```

# File Modes

| Mode | Meaning             |
| ---- | ------------------- |
| `r`  | Read file           |
| `w`  | Write (overwrite)   |
| `a`  | Append              |
 
| `b`  | Binary mode         |
| `t`  | Text mode (default) |


# Reading a File

# Read Entire File
```
f = open("data.txt", "r")
print(f.read())
f.close()
```
# Read One Line

```
print(f.readline())
```
# Read All Lines as List

```
print(f.readlines())
```

# Writing to a File
# Overwrite Content
```
f = open("data.txt", "w")
f.write("Hello Python\n")
f.write("File handling example")
f.close()
```
-w deletes old data.

# Append Data (Recommended)
```
f = open("data.txt", "a")
f.write("\nNew Line Added")
f.close()
```
# Using with (Best Practice ✅)
# Automatically closes file.
```
with open("data.txt", "r") as f:
    print(f.read())
```

# Writing Using with
```
with open("data.txt", "w") as f:
    f.write("Safe writing using with")
```

# Loop Through File
```
with open("data.txt") as f:
    for line in f:
        print(line.strip())
```

# Check if File Exists
```
import os

if os.path.exists("data.txt"):
    print("File exists")
else:
    print("File not found")
```
# Delete a File
```
import os
os.remove("data.txt")
```

# File Handling with Exception (Important)
```
try:
    with open("data.txt", "r") as f:
        print(f.read())
except FileNotFoundError:
    print("File does not exist!")
```
# Real-Life Example: Save User Input
```
name = input("Enter name: ")

with open("users.txt", "a") as f:
    f.write(name + "\n")
```
# What is a Decorator in Python?

-A decorator is a function that modifies the behavior of another function without changing its code.
# In simple words:
#  Decorator = Wrapper around a function
-It allows you to:

-Add extra functionality

-Reuse code

-Keep original function clean

# Real-Life Analogy
Think of a gift box 
-Original function = gift
-Decorator = gift wrapping
The gift is same, but behavior/appearance improves.

# Why Do We Use Decorators?
-Without decorators:
-Repeated code
-Messy functions
-Hard maintenance
# With decorators:
Code reuse
-Clean functions
-Separation of concerns
-Used in authentication, logging, timing

---


# Structure of a Decorator
```
def decorator_function(original_function):
    def wrapper():
        # extra work
        original_function()
        # extra work
    return wrapper
```

# First Important Concept (Functions are Objects)
# In Python:

-Functions can be stored in variables
-Functions can be passed to other functions
-Functions can return functions

# Example
```
def greet():
    print("Hello")

say_hello = greet
say_hello()
```
# How Decorator Works
# Simple Function
```
def my_func():
    print("Hello Durgesh")
```
# 2 Create Wrapper Function
```
def decorator_func(func):
    def wrapper():
        print("Before function call")
        func()
        print("After function call")
    return wrapper
```
# 3 Apply Decorator (Manual Way)
```
def my_func():
    print("Hello Durgesh")

my_func = decorator_func(my_func)

my_func()
```
# 4 Using @ Decorator Syntax (Important)
-Python gives shortcut syntax.
# example
```
def decorator_func(func):
    def wrapper():
        print("Before function call")
        func()
        print("After function call")
    return wrapper

@decorator_func
def my_func():
    print("Hello Durgesh")

my_func()
```
---
# Decorator with Arguments (VERY IMPORTANT)
# Problem (Without args support)
```
@decorator_func
def add(a, b):
    print(a + b)
```
# Correct Way (Use *args, **kwargs)
```
def decorator_func(func):
    def wrapper(*args, **kwargs):
        print("Before execution")
        func(*args, **kwargs)
        print("After execution")
    return wrapper

@decorator_func
def add(a, b):
    print(a + b)

add(5, 3)
```
---

# Decorator with Return Value
```
def decorator_func(func):
    def wrapper(*args, **kwargs):
        result = func(*args, **kwargs)
        return result
    return wrapper

@decorator_func
def add(a, b):
    return a + b

print(add(2, 3))
```

# Multiple Decorators
```
def deco1(func):
    def wrapper():
        print("Deco1")
        func()
    return wrapper

def deco2(func):
    def wrapper():
        print("Deco2")
        func()
    return wrapper

@deco1
@deco2
def say_hi():
    print("Hi")

say_hi()
```
---

# What is a Module in Python?
# A module is simply a Python file (.py) that contains:
-functions

-variables

-classes

-which you can reuse in another Python file using import.

# In simple words:
-Module = Python file for reusable code
# Why Do We Use Modules?
# Without modules:

-Big messy file
-Code duplication
-Hard to maintain

# With modules:
-Code reuse
-Better organization
-Easy maintenance
-Used in large projects
--- 

# Types of Modules
# Python has three main types:
# 1 Built-in Modules
# Examples:
-math
-random
-datetime
-os
-sys
--- 
# User-Defined Modules
# Created by you.
-Example file: mymodule.py

---
# External Modules (Third-party)
# Installed using pip.

# Examples:
-requests

-numpy

-pandas

-django

# How to Import a Module

# Example
```
import math
print(math.sqrt(16))

```

# Most Important Built-in Modules
#  1. math Module

# Used for mathematical operations.
# Example
```
import math

math.sqrt(16)
math.pow(2, 3)
math.ceil(4.2)
math.floor(4.8)
math.pi
math.factorial(5)
```
# 2 random Module
-Used to generate random values.
# Examples
```
import random

random.randint(1, 10)
random.random()
random.choice([10, 20, 30])
random.shuffle(list1)
```
- Used in:
-Games

-OTP generation

-Simulations

# datetime Module ⭐ VERY IMPORTANT
# Example 
```
from datetime import datetime

now = datetime.now()
print(now)

print(now.date())
print(now.time())
```
---

# os Module ⭐ IMPORTANT
# Used for operating system tasks.
# Examples
```
import os

os.getcwd()
os.listdir()
os.mkdir("test")
os.remove("file.txt")
os.path.exists("file.txt")
```
# sys Module
# Used for Python runtime environment.
# Examples
```
import sys

print(sys.version)
print(sys.argv)
sys.exit()
```
---

# Module vs Package in Python
# What is a Module?
-A module is a single Python file (.py) that contains:
-functions
-classes
-variables
#  Example
# File: math_utils.py
```
def add(a, b):
    return a + b
```
# Use it:
```
import math_utils
print(math_utils.add(2, 3))
```
---
# What is a Package?
# A package is a folder that contains multiple modules (and possibly sub-packages).
-Package = directory of modules
# Usually contains:
-many .py files
-an __init__.py file (optional in modern Python but common)

# Package Structure Example
```
myproject/
│
├── calculator/
│   ├── __init__.py
│   ├── add.py
│   └── subtract.py
│
└── main.py
```

# Using Package
```
from calculator.add import add
```


---

# What is JSON?
-JSON = JavaScript Object Notation

-It is a lightweight data format used to store and exchange data between systems.

# Simple meaning:
# JSON = text format to represent structured data

# JSON Example
```
{
  "name": "XYZ",
  "age": 0,
  "is_student": true
}
```

-Looks like a Python dictionary, but it is string-based text.
# Why JSON is Used?
- JSON is used because it is:
Easy to read
-Easy to write
-Lightweight
-Language independent
-Perfect for APIs
---
# Where JSON is Used (Real World)
Web APIs
-Frontend ↔ Backend communication
-Configuration files
-Data storage
-NoSQL databases
-Mobile apps

# JSON vs Python Dictionary

---
| Feature | JSON               | Python Dict   |
| ------- | ------------------ | ------------- |
| Quotes  | Double quotes only | Single/double |
| Boolean | true/false         | True/False    |
| Null    | null               | None          |
| Type    | String format      | Python object |

---


# JSON in Python

-Python uses the built-in json module.

```
import json
```
# Two Most Important Functions

# 1. json.dumps() → Python → JSON string

-dumps = dump string
# Example
```
import json

data = {"name": "Durgesh", "age": 22}

json_data = json.dumps(data)
print(json_data)
```

# 2. json.loads() → JSON string → Python

# loads = load string

# Example


```
import json

json_data = '{"name": "Durgesh", "age": 22}'

python_obj = json.loads(json_data)
print(python_obj["name"])

```

# File-Based JSON Functions
# json.dump() → Python → JSON file

```
import json

data = {"name": "Durgesh", "age": 22}

with open("data.json", "w") as f:
    json.dump(data, f, indent=4)
```
# json.load() → JSON file → Python

```
import json

with open("data.json", "r") as f:
    data = json.load(f)

print(data)

```
# dumps vs dump (Very Important)

| Function   | Works With | Purpose                |
| ---------- | ---------- | ---------------------- |
| json.dumps | string     | convert to JSON string |
| json.dump  | file       | write JSON to file     |
| json.loads | string     | JSON string → Python   |
| json.load  | file       | JSON file → Python     |


# Pretty Print JSON
-json.dumps(data, indent=4)

# Sorting Keys

```
json.dumps(data, indent=4, sort_keys=True)
```

# Convert Complex Data
```
data = {
    "students": ["Durgesh", "Aman"],
    "marks": [90, 85]
}

print(json.dumps(data, indent=4))
```
# Common Errors

-Invalid JSON quotes
```
{'name': 'Durgesh'}
```
# Right:

```
{"name": "Durgesh"}
```
---

# Advantages of JSON
Lightweight
-Human readable
-Language independent
-Easy parsing
-Widely supported
-Perfect for APIs
-Faster than XML

---
# Disadvantages of JSON
No comments support
-Only basic data types
-Not good for very large binary data
-Less secure if not validated
-No schema enforcement (by default)

---

# Real-Life Example: API Response

```
import json

response = '{"status":"success","data":{"name":"Durgesh"}}'

data = json.loads(response)
print(data["data"]["name"])
```

----

import json
import os
 
FILE_NAME = "students.json"
 
 
# ===============================
# 🔹 Load Data
# ===============================
```
def load_data():
    if os.path.exists(FILE_NAME):
        try:
            with open(FILE_NAME, "r") as file:
                return json.load(file)
        except json.JSONDecodeError:
            return {}
    return {}
```    
 
 
# ===============================
# 🔹 Save Data
# ===============================
```
def save_data(data):
    with open(FILE_NAME, "w") as file:
        json.dump(data, file, indent=4)
```        
 
---

# Default Parameters
-Definition
A default parameter is a parameter that already has a value assigned.
If the user does not provide a value, Python uses the default.

# Example

```
def greet(name="Student"):
    print("Hello", name)

greet("Aman")   # uses given value
greet()         # uses default value
```
# Default parameters must always come after normal parameters.
# Wrong
```
def fun(a=10, b):   # SyntaxError
    pass
```
# Correct
```
def fun(a, b=10):
    pass
```
---


# Function vs Method 
# Function
-A function is defined outside any class.

```
def add(a, b):
    return a + b
```

# Method
# A method is a function defined inside a class.
```
class Demo:
    def show(self):
        print("This is a method")
```

# What is OOP?
-Object-Oriented Programming (OOP) is a programming style that organizes code using objects and classes to model real-world entities.


# OOP is a programming paradigm based on the concept of classes and objects.

# Real-World Example (Best for Teaching)

-Consider a Car:
---
| Real World       | OOP Concept |
| ---------------- | ----------- |
| Car design       | Class       |
| My car           | Object      |
| Color, speed     | Attributes  |
| Drive(), brake() | Methods     |
---


# Four Pillars of OOP (Very Important)
-OOP is built on four main pillars:

# 1 Encapsulation
-Wrapping data and methods together
-Data hiding and protection

-One-line: Protect the data.
---
# 2 Inheritance
-One class acquires properties of another class
-One-line: Child uses parent features.

# 3 Polymorphism
-Same method name behaves differently

# 4 Abstraction
-Hiding internal implementation details
---


# What is a Class?
-A class is a blueprint or template used to create objects

-It defines:
-attributes (data)

-methods (functions)

# Basic Syntax
```
class Student:
    pass
```

# What is an Object?
-An object is an instance of a class.

s1 = Student()

---

# What is an Attribute?
-n attribute is a variable that belongs to a class or object.

---
```
class Student:
    def __init__(self, name):
        self.name = name
```
-name → parameter

-self.name → attribute (object data)        


# What is a Method?
-A method is a function defined inside a class that operates on objects.

```
class Student:
    def greet(self):
        print("Hello Student")
```        

---




 





