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
```python
if condition:
    statement

age = 20

if age >= 18:
    print("You are eligible to vote")
```
### 2. if-else Statement
- Used when there are two choices.
```Syntax:
if condition:
    statement1
else:
    statement2
```
### Example 
```num = 7

if num % 2 == 0:
    print("Even number")
else:
    print("Odd number")
```

### 3. if-elif-else Statement
- Used when there are multiple conditions.
# Syntax
```if condition1:
    statement1
elif condition2:
    statement2
else:
    statement3
```
# Example
```marks = 85
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
```python
for variable in sequence:
    statement
```

### Example
```for i in range(1, 6):
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
```for i in range(1, 11):
    if i % 2 == 0:
        print(i)
```
--- 

### 2. `while` Loop
Used when we don’t know how many times the loop should run.
It runs until a condition becomes False.

# Syntax:
```while condition:
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

```for i in range(1, 6):
    if i == 3:
        break
    print(i)
```
### Output:
```1
2
4
5
```
--- 

### continue
Skips the current iteration and moves to the next.
```for i in range(1, 6):
    if i == 3:
        continue
    print(i)
```
# Output:
```1
2
4
5
```
--- 
### Nested Loops
```for i in range(1, 4):
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
```for i in range(1, 11):
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
