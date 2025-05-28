# Experiment No: 6a – Demonstrate Polymorphism Using Classes Cat and Dog

## AIM  
To write a Python program that demonstrates polymorphism using two classes, `Cat` and `Dog`, which share similar method names and structures.

---

## ALGORITHM  
1. Create a class `Cat` with:
   - Constructor `__init__` to set name and age.
   - Method `make_sound()` to print `'Meow'`.
   - Method `info()` to display cat details.
2. Create a class `Dog` with:
   - Constructor `__init__` to set name and age.
   - Method `make_sound()` to print `'Bark'`.
   - Method `info()` to display dog details.
3. Accept name and age for both `Cat` and `Dog` from the user.
4. Create objects of both classes and pack them into a tuple.
5. Iterate through the tuple and use the `animal` variable to call methods, demonstrating polymorphism.

---

## 🧾 PROGRAM

```python
class Cat:
    def __init__(self, name, age):
        self.name = name
        self.age = age
    def make_sound(self):
        print('Meow')
    def info(self):
        print(f'I am a cat. My name is {self.name}. I am {self.age} years old.')

class Dog:
    def __init__(self, name, age):
        self.name = name
        self.age = age
    def make_sound(self):
        print('Bark')
    def info(self):
        print(f'I am a dog. My name is {self.name}. I am {self.age} years old.')

s1 = input()
a1 = input()
s2 = input()
a2 = input()

cat1 = Cat(s1, a1)
dog1 = Dog(s2, a2)

for animal in (cat1, dog1):
    animal.make_sound()
    animal.info()
    animal.make_sound()

```

### OUTPUT
![image](https://github.com/user-attachments/assets/38cced9a-b7c0-44e4-a108-1996340be9b8)

### RESULT
Thus, the Python program demonstrating polymorphism using common method names in different classes has been executed successfully.


# Experiment No: 6b – Operator Overloading for Adding Two Objects

## AIM  
To write a Python program to demonstrate operator overloading for adding two objects using the `+` operator.

---

## ALGORITHM  
1. Create a class `product` with an initializer `__init__` to set the value.
2. Overload the `+` operator using `__add__` method.
3. In the `__add__` method:
   - If both values are numeric, return their sum.
   - If both values are strings, concatenate them.
   - Otherwise, raise `TypeError`.
4. Take input from the user (numeric and string).
5. Create instances of the class.
6. Add the objects and display the result.

---

## 🧾 PROGRAM

```python
class product:
    def __init__(self, val):
        self.val = val

    def __add__(self, other):
        if isinstance(self.val, (int, float)) and isinstance(other.val, (int, float)):
            return product(self.val + other.val)
        elif isinstance(self.val, str) and isinstance(other.val, str):
            return product(self.val + other.val)
        else:
            raise TypeError("Unsupported operand types for +")

# Integer addition
a = int(input())
b = int(input())
p1 = product(a)
p2 = product(b)
res = p1 + p2
print("amount : " + str(res.val))

# String concatenation
c = input()
d = input()
p3 = product(c)
p4 = product(d)
res2 = p3 + p4
print("location:  " + res2.val)

```

### OUTPUT
![image](https://github.com/user-attachments/assets/2d8336e2-0de8-42d9-9624-ccd2b61dc02c)

### RESULT
Thus, the Python program for operator overloading using the + operator with numeric and string types has been executed successfully.


# Experiment No: 6c – Abstract Base Class and Method Implementation in Subclasses

## AIM  
To define an abstract base class `Polygon` with an abstract method `sides()` and implement this method in various subclasses.

---

## ALGORITHM  
1. Import `ABC` and `abstractmethod` from `abc` module.
2. Define the abstract base class `Polygon` using `ABC`.
3. Define the abstract method `sides()` inside `Polygon`.
4. Create subclasses like `Triangle`, `Square`, `Pentagon`, and `Hexagon` that inherit from `Polygon`.
5. Override and implement the `sides()` method in each subclass.
6. Create objects of each subclass.
7. Call the `sides()` method for each object to demonstrate polymorphism.

---

## 🧾 PROGRAM

```python
from abc import ABC, abstractmethod

class Polygon(ABC):
    @abstractmethod
    def sides(self):
        pass

class Triangle(Polygon):
    def sides(self):
        print("Triangle has 3 sides")

class Square(Polygon):
    def sides(self):
        print("I have 4 sides")

class Pentagon(Polygon):
    def sides(self):
        print("Pentagon has 5 sides")

class Hexagon(Polygon):
    def sides(self):
        print("Hexagon has 6 sides")

# Creating objects and invoking sides method
t = Triangle()
t.sides()

s = Square()
s.sides()

p = Pentagon()
p.sides()

h = Hexagon()
h.sides()

```

### OUTPUT
![image](https://github.com/user-attachments/assets/7f3e5e15-0f53-4f15-90eb-c1a0ada4e5cc)

### RESULT
The abstract base class and its implementation in various subclasses were successfully demonstrated using Python.


# Experiment No: 6d – Class with Instance Variables and Methods

## AIM  
To create an `Employee` class with instance variables `name`, `salary`, and `project`, and implement behaviors using `work()` and `show()` methods.

---

## ALGORITHM  
1. Define a class named `Employee`.
2. Create a constructor `__init__()` to initialize name, salary, and project.
3. Define a method `show()` to print the name and salary.
4. Define another method `work()` to print which project the employee is working on.
5. Create an object of the `Employee` class and invoke both methods.

---

## 🧾 PROGRAM

```python
class Employee:
    # constructor
    def __init__(self, name, salary, project):
        # data members
        self.name = name
        self.salary = salary
        self.project = project

    # method to display employee's details
    def show(self):
        print("Name: ", self.name, 'Salary:', self.salary)

    # method to show what the employee is working on
    def work(self):
        print(self.name, 'is working on', self.project)

# creating an object of Employee class
emp = Employee("Jessa", 8000, 'NLP')
emp.show()
emp.work()

```

### OUTPUT
![image](https://github.com/user-attachments/assets/3f0f4923-6e67-47ba-8d87-767f0cafc7d8)

### RESULT
Thus, the Python program to demonstrate instance variables and methods in a class using the Employee class was successfully executed.


# Experiment No: 6e – Counter Class with Increment, Reset and Value Methods

## AIM:
To write a Python program to create a `Counter` class with an attribute `current` and implement the methods `increment()`, `value()`, and `reset()`.

---

## ALGORITHM:
1. Define a class named `Counter`.
2. Inside the class, initialize an attribute `current` to 0 using a constructor.
3. Define a method `increment()` to increase `current` by 1.
4. Define a method `value()` to return the current value of `current`.
5. Define a method `reset()` to reset `current` to 0.
6. Create an instance of the class.
7. Call the `increment()` method three times.
8. Print the current value using the `value()` method.

---

## PROGRAM:
```python
class Counter:
    def __init__(self):
        self.current = 0

    def increment(self):
        self.current += 1

    def value(self):
        return self.current

    def reset(self):
        self.current = 0

counter = Counter()
c = 0
while c < 3:
    counter.increment()
    c += 1
print(counter.value())

```

### OUTPUT
![image](https://github.com/user-attachments/assets/f7f39abb-189c-4f6e-b23d-f7ad92a2b3b7)

### RESULT
Thus, the Python program to create a Counter class and demonstrate its functionality using class methods was successfully executed.
