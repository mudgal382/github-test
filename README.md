# github-test
Why encapsulation is important? How you can implement it in python?

What is the need for Encapsulation in Python
The following reasons show why developers find the Encapsulation handy and why the Object-Oriented concept is outclassing many programming languages.

Encapsulation helps in achieving the well-defined interaction in every application.
The Object-Oriented concept focuses on the reusability of code in Python. (DRY – Don’t Repeat Yourself).
The applications can be securely maintained.
It ensures the flexibility of the code through a proper code organization.
It promotes a smooth experience for the users without exposing any back-end complexities.
It improves the readability of the code. Any changes in one part of the code will not disturb another.
Encapsulation ensures data protection and avoids the access of data accidentally. The protected data can be accessed with the methods discussed above.
Encapsulation in Python is, the data is hidden outside the object definition. It enables developers to develop user-friendly experience. This is also helpful in securing data from breaches, as the code is highly secured and cannot be accessed by outside sources.

Implement Encapsulation in Phython:
Using single underscore
Using a single leading underscore is merely a convention. A name prefixed with an underscore in Python (as example _name) should be treated as a non-public part of the API (whether it is a function, a method or a data member).

As mentioned it is just a convention and a leading underscore doesn’t actually make any variable or method private or protected. It’s just that if you see a variable or method with a leading underscore in Python code you should follow the convention that it should be used internally with in a class.

Using double underscore (making it private)
If you really want to make a class member (member or variable) private in Python you can do it by prefixing a variable or method with double underscores. Here note that Python provides a limited support for private modifier using a mechanism called name mangling and it is still possible to access such class member from outside the class.

In Python any identifier of the form __var (at least two leading underscores, at most one trailing underscore) is rewritten by the Python interpreter in the form _classname__var, where classname is the current class name. This mechanism of name changing is known as name mangling in Python.

Using getter and setter methods to access private variables
To access and change private variables accessor (getter) methods and mutator (setter methods) should be used which are part of the class.

class Person:
def __init__(self, name, age=0):
self.name = name
self.__age = age

def display(self):
print(self.name)
print(self.__age)

def getAge(self):
print(self.__age)

def setAge(self, age):
self.__age = age

person = Person('John', 40)
#accessing using class method
person.display()
#changing age using setter
person.setAge(45)
person.getAge()
Output

John
40
45
