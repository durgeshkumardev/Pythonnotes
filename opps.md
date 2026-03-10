# What is a Class?
 A class is like a blueprint or template for creating objects6
 Think of a class like the blueprint of a house. It defines what
the house should have (rooms, windows, etc.) but doesn’t
build the house. An object is the actual house built using that
blueprint.

# Syntax of class
- A class is also created with a basic keyword class and a name
in front of it6
```
class Car:
    brand="Toyota"
```

# What is object 
An object is an instance of a class that can access the data (attributes) and methods (functions) defined in the class and represents a real-world entity.

# Real-life example:
- Class = Car Design

- Object = Actual Car

---
### How to Create a Class in Python
# Basic Syntax:
```
class ClassName:
    pass
```
# Example:
```
class Student:
    pas
```

### What Do We Use Inside a Class?
# Inside a class we usually use:
- Attributes (variables)

- Methods (functions)

```
class Student:
    school_name = "ABC School"   # Class Attribute

    def __init__(self, name, age):   # Constructor
        self.name = name             # Instance Attribute
        self.age = age

    def display(self):               # Method
        print("Name:", self.name)
        print("Age:", self.age)
```
---
# Types of Attributes
- Attributes = Variables inside class

- There are mainly 3 types:

# 1 Instance Attribute
- Belongs to object.
```
class Student:
    def __init__(self, name):
        self.name = namen  # instance attribute
```


- self.name is instance attribute
- Every object will have different value 


### 2 Class Attribute
- Common for all objects.
```
class Student:
    school = "ABC School"  # class Attribute
```
- All objects share same value



# Static Attribute
- Same as class attribute (Python does not differentiate strictly)
---

# Types of Methods

- Methods = Functions inside class

- There are 4 main types:

# Instance Method
- Works with object data.
- An instance method Works with instance (object) of the class. This method can access and modify instance attributes.

```
class Student:
    def show(self):
        print("This is instance method")
```
- Needs object to call

# Class Method
- This method works with the class itself it will not target the instance (object). we have to use @classmethod decorator for creating the class method and it takes cls as their first parameter.

```
class Student:
    school = "ABC"

    @classmethod
    def get_school(cls):
        return cls.school
```
# Static Method

- No access to class or instance.
```
class Math:
    @staticmethod
    def add(a, b):
        return a + b
```

# Constructor Method
- Special method used to initialize object.
```
def __init__(self):
    print("Constructor called")
```


# What is constructor
- You saw last example where we wanted material, zips and pockets from the user to create an object.
- If we talk about a function we can ask the user using parameters, but in class we can’t have parameters for that we use constructor.
- A constructor is a method that runs automatically when we call a class and this constructor function will target the objects location

```
class Student:
    def __init__(self,name):
        self.name=name # Instance attribute

# Creating an object with a value
s=Student("Xyz")

# Accessing the attribute
print(s.name)

```
- To target the objects location we use self keyword.



---

# Inheritance
- In general terms Inheritance means property or any possession that comes to an heir
- But our python neither have an old man or a child then inheritance works where ?

- It works between classes

- Inheritance allows a class (child class) to inherit properties and behaviors (attributes and methods) from another class (parent class)

# Benefits of using inheritance is
- Code reusabilit2
- K Organized structurH
- K Easy to maintain and extend

# Syntax of Inheritance
- Syntax is very simple just like you take parameters in functions here you will take parameters but those parameters will be classes

```
class Animal:

    def eat(self):
        print("Animal is eating")

class Dog(Animal):

    def bark(self):
        print("Dog is barking")
```
- Now the inherited class has all the powers of parent class that means all the methods, attributes can be accessed by the instance of child class as well.

# Constructor in Inheritance
- Lets say you have created a parent class with a constructor function inside it and then this class is inherited by another class then the constructor function of parent class will work for the child class as well.

# Constructor WITHOUT Inheritance
- A constructor initializes object data when the object is created.

```
class Student:

    def __init__(self, name, age):
        self.name = name
        self.age = age

    def display(self):
        print("Name:", self.name)
        print("Age:", self.age)


s1 = Student("Durgesh", 22)
s1.display()
```

# Flow
```
Student("Durgesh",22)
        ↓
__init__ constructor called
        ↓
self.name = Durgesh
self.age = 22
        ↓
display() method prints value
```
# Here:
- __init__ is constructor

- self.name and self.age are instance variables


# Add Inheritance

- Parent Class:
```
class Person:

    def __init__(self, name):
        self.name = name
```
- Child Class:

```
class Student(Person):

    def __init__(self, name, age):
        self.age = age
```
- The parent constructor will NOT run automatically because the child has its own constructor.


# Correct Way
- Parent Class:
```
class Person:

    def __init__(self, name):
        self.name = name
```
- Child Class:
```
class Student(Person):

    def __init__(self, name, age):
        super().__init__(name)
        self.age = age
```
- Object:
```
s = Student("Durgesh", 22)

print(s.name)
print(s.age)
```
# Full Example
```
class Person:

    def __init__(self, name):
        self.name = name

    def showName(self):
        print("Name:", self.name)


class Student(Person):

    def __init__(self, name, age):
        super().__init__(name)
        self.age = age

    def showStudent(self):
        print("Age:", self.age)


s = Student("Durgesh", 22)

s.showName()
s.showStudent()
```


### Type of the  Inheritance
# 1 Single Inheritance
- When one child class inherits from one parent class.
- Example
```
class Animal:
    def eat(self):
        print("Animal is eating")

class Dog(Animal):
    def bark(self):
        print("Dog is barking")

d = Dog()

d.eat()
d.bark()
```
# 2 Multiple Inheritance
- When one child class inherits from multiple parent classes.
- Structure
```
Parent1   Parent2
     \     /
      Child
```
- Example 

```
class Father:
    def skills(self):
        print("Programming")

class Mother:
    def hobby(self):
        print("Painting")

class Child(Father, Mother):
    pass

c = Child()

c.skills()
c.hobby()
```
# Multilevel Inheritance
- Example
```
class A:
    def showA(self):
        print("Class A")

class B(A):
    def showB(self):
        print("Class B")

class C(B):
    def showC(self):
        print("Class C")

c = C()

c.showA()
c.showB()
c.showC()
```
# Hierarchical Inheritance
- When multiple child classes inherit from one parent class.
```

class Animal:
    def eat(self):
        print("Animal eating")

class Dog(Animal):
    def bark(self):
        print("Dog barking")

class Cat(Animal):
    def meow(self):
        print("Cat meowing")

d = Dog()
c = Cat()

d.eat()
d.bark()

c.eat()
c.meow()
```
# Hybrid Inheritance
```
class A:
    def showA(self):
        print("A")

class B(A):
    def showB(self):
        print("B")

class C(A):
    def showC(self):
        print("C")

class D(B, C):
    def showD(self):
        print("D")

d = D()

d.showA()
d.showB()
d.showC()
d.showD()
```




