# Python-oop_Assiangment

Q1. What is the purpose of Python's OOP?

Ans: The primary purpose of Python's object-oriented programming (OOP) is to provide a way to organize and structure your code in a logical and modular manner. OOP allows you to define classes, which are templates for creating objects. These objects can be used to represent real-world entities or abstract concepts, and they can contain both data (attributes) and behavior (methods).

Using OOP in Python has several benefits, including:

Code reusability: By creating classes, you can define reusable code that can be used to create multiple objects. This reduces the need to write repetitive code and
makes your code more efficient and maintainable.
Code modularity: OOP allows you to organize your code into logical and independent units (classes and objects), which makes it easier to understand, debug, and modify.
Code encapsulation: OOP allows you to hide the implementation details of your code, which helps to prevent unwanted access to or modification of your data. This helps
to maintain the integrity of your code and makes it more robust.
Code polymorphism: OOP allows you to define classes that share a common interface but have different implementations. This allows you to write code that can be used 
with different objects without knowing their specific details.



Q2. Where does an inheritance search look for an attribute?

Ans: The inheritance search looks for an attribute first in the object's own attributes, then in the object's class attributes and parent classes' attributes, in that
  order. This process continues until the attribute is found or until the end of the inheritance tree is reached.
  

Q3. How do you distinguish between a class object and an instance object?

Ans:  A class object is a template that defines the attributes and methods of a class, whereas an instance object is an actual object that is created from a class. In
other words, a class object describes the general characteristics of a class, while an instance object represents a specific instance of that class.
Eg:
class MyClass:
    # this is a class object
    x =5
    
    def __init__(self, y):
        self.y = y
        
    def my_method(self):
        print(self.x + self.y)
        
# create an instance object of class MyClass
obj = MyClass(10)

# print the attributes of the instance object
print(obj.x)
print(obj.y)

# call the instance object's method
obj.my_method()


Q4. What makes the first argument in a class’s method function special?

Ans:  The first argument in a class's method function is special because it is a reference to the instance object on which the method is being called. This argument is
usually named ' self' , but you can use any valid Python identifier.
The 'self' argument is used to access the attributes and methods of the instance object from within the method. This allows you to define methods that can operate on the instance object's data and behavior.


Q5. What is the purpose of the init method?

Ans:  The '__init__()' method, also known as the initializer method, is a special method in Python classes that is called when an instance object is created. The
'__init__()' method is used to initialize the attributes of the instance object and to set their initial values.


Q6. What is the process for creating a class instance?

Ans:
In Python, creating a class instance (also known as an object) follows these steps:

Define a class using the class keyword, followed by the name of the class.
Inside the class definition, define the __init__() method, which is the constructor for the class. This method is called when the class is instantiated, and it allows you to set initial values for the object's attributes.
Inside the __init__() method, use the self keyword to reference the current instance of the class, and to set initial values for the object's attributes.
Outside the class definition, create an instance of the class by calling the class name followed by parentheses.
Inside the parentheses, provide any required arguments for the __init__() method.
Eg:
class MyClass:
  def __init__(self, name, age):
    self.name = name
    self.age = age

my_instance = MyClass("Kumar", 25)


Q7. What is the process for creating a class?

Ans:
In Python, creating a class follows these steps:

Use the class keyword, followed by the name of the class, to define a new class.
Inside the class definition, use the def keyword to define a method. The first argument to the method should be self, which is a reference to the current instance of the class.
Inside the method, use the self keyword to access or modify the attributes of the current instance of the class.
Optionally, define the __init__() method, which is the constructor for the class. This method is called when the class is instantiated, and it allows you to set initial values for the object's attributes.
Eg:
class MyClass:
  def __init__(self, name, age):
    self.name = name
    self.age = age

  def say_hello(self):
    print("Hello, my name is " + self.name)


Q8. How would you define the superclasses of a class?

Ans:
In Python, a class can have one or more superclasses, which are classes from which it inherits attributes and methods. To define the superclasses of a class, you use the class keyword followed by the name of the class, and then a tuple containing the names of the superclasses within parentheses.
Eg:
class MyClass(SuperClass1, SuperClass2):


Q9. What is the relationship between classes and modules?

Ans:
In Python, a class is a type of object that can be defined and used within a module. A module is a file containing Python code, and it can contain one or more classes, as well as other types of objects such as functions and variables.

The relationship between classes and modules is similar to the relationship between objects and classes. Just as an object is an instance of a class, a module is a container for classes and other objects. Just as an object can access and use the attributes and methods of its class, a module can access and use the objects (including classes) that it contains.
Eg:
# my_module.py

class MyClass:
  def __init__(self, name, age):
    self.name = name
    self.age = age

  def say_hello(self):
    print("Hello, my name is " + self.name)


Q10. How do you make instances and classes?

Ans:
To create an instance of a class in Python, you first need to define the class using the 'class' keyword, followed by the name of the class. Inside the class definition, you can define methods, which are functions that are associated with the class and can be called on instances of the class.

Once the class is defined, you can create an instance of the class by calling the class name followed by parentheses. Inside the parentheses, you can provide any required arguments for the class's __init__() method, which is the constructor for the class.
Eg:
class MyClass:
  def __init__(self, name, age):
    self.name = name
    self.age = age

  def say_hello(self):
    print("Hello, my name is " + self.name)

my_instance = MyClass("Kumar", 25)


Q11. Where and how should be class attributes created?

Ans:
Class attributes in Python should be created inside the class definition, and should be assigned a default value. To create a class attribute, you simply assign a value to a variable within the class definition, using the same syntax as you would use to assign a value to a variable outside of a class.
Eg:
class MyClass:
  my_attribute = "This is a class attribute"

  def __init__(self, name, age):
    self.name = name
    self.age = age


Q12. Where and how are instance attributes created?

Ans:
Instance attributes in Python should be created inside the class's __init__() method, which is the constructor for the class. To create an instance attribute, you simply assign a value to a variable using the self keyword, which is a reference to the current instance of the class.
Eg:
class MyClass:
  def __init__(self, name, age):
    self.name = name
    self.age = age


Q13. What does the term "self" in a Python class mean?

Ans:
In a Python class, the self keyword is used to refer to the current instance of the class. It is equivalent to the this keyword in other programming languages, and it is used to access the attributes and methods of the current instance of the class.
Eg:
class MyClass:
  def __init__(self, name, age):
    self.name = name
    self.age = age

  def say_hello(self):
    print("Hello, my name is " + self.name)


Q14. How does a Python class handle operator overloading?

Ans:
In Python, operator overloading is the ability to define how operators (such as +, -, *, etc.) behave when applied to objects of a certain class. This allows you to customize the behavior of these operators for your own classes, and to make them work more intuitively with your class's data and methods.

To handle operator overloading in a Python class, you need to define special methods in the class that have the same name as the operator you want to overload.
For example: to overload the '+' operator, you would define a method named '__add__()' . To overload the ' - 'operator, you would define a method named '__sub__()',
and so on.
Eg:
class MyClass:
  def __init__(self, value):
    self.value = value

  def __add__(self, other):
    return self.value + other.value


Q15. When do you consider allowing operator overloading of your classes?

Ans:
Operator overloading can be a useful feature in a Python class, as it allows you to customize the behavior of operators when applied to instances of your class. This 
can make your class's methods and data more intuitive and easier to use.
However, operator overloading can also make your code more difficult to understand and maintain, especially for other programmers who are not familiar with your class.
It can also make it harder to predict how your class will behave in different situations.
Therefore, you should consider allowing operator overloading in your classes if you have a clear and well-defined use case for it, and if you can make sure that the
overloaded operators will behave in a consistent and predictable way. Otherwise, you may want to avoid operator overloading to keep your code simpler and more
readable.


Q16. What is the most popular form of operator overloading?

Ans:
The most popular form of operator overloading in Python is to define special methods in a class that have the same name as the operator you want to overload.
For example: to overload the '+' operator, you would define a method named '__add__()'. To overload the '-' operator, you would define a method named '__sub__()', and so on.
Eg:
class MyClass:
  def __init__(self, value):
    self.value = value

  def __add__(self, other):
    return self.value + other.value


Q17. What are the two most important concepts to grasp in order to comprehend Python OOP code?

Ans:
The two most important concepts to grasp in order to comprehend Python OOP code are classes and objects.
> A class in Python is a template or blueprint for creating objects. It defines the attributes and methods that objects of that class will have, and provides a way to
initialize those attributes and access and modify them.
> An object is an instance of a class. It contains the specific data and behavior that are defined by the class, and it can be used to perform actions and manipulate
data using the methods of the class.
Understanding these two concepts is essential for comprehending Python OOP code, as most Python OOP code is organized into classes and objects. Once you understand how
classes and objects work in Python, you will be able to understand how the code uses them to define data and behavior, and how to create and use objects of those
classes in your own code.


Q18. Describe three applications for exception processing.

Ans:
Exception processing is a mechanism in Python (and other programming languages) that allows you to handle errors and exceptional situations in your code. Exception
processing is useful in a variety of applications, including:
1. Validating user input: When your program accepts input from a user or another source, you can use exception processing to validate that the input is in the correct
format and meets certain criteria. For example, you can use exception handling to check that a user has entered a valid email address, or that a number they have
entered is within a certain range.
2. Handling network and file operations: When your program performs operations on external resources, such as a network or a file system, there is a risk that the 
operation could fail due to a network outage, a file not being found, or other issues. Using exception processing, you can handle these failures gracefully and provide
feedback to the user, or take other appropriate actions.
3. Debugging and testing: Exception processing can also be used as a tool for debugging and testing your code. By using try-except blocks and raising specific
exceptions, you can identify and isolate specific problems in your code, and test how your code behaves when it encounters those problems. This can help you find and
fix errors, and ensure that your code is robust and reliable.


Q19. What happens if you don't do something extra to treat an exception?

Ans:
If you don't do something extra to treat an exception in Python, the exception will be raised and your program will stop executing. When an exception is raised, the interpreter will look for a try-except block that can handle the exception, starting from the point where the exception was raised and working its way up the call stack.
If no try-except block is found that can handle the exception, the interpreter will print an error message and the traceback, which shows the sequence of function calls that led to the exception being raised. This can provide useful information for debugging the problem, but it will also cause your program to terminate.
Therefore, it is important to use try-except blocks to handle exceptions in your Python code, so that your program can continue running even if an error or exceptional situation occurs. Otherwise, your program will stop executing when an exception is raised, and it will not be able to recover from the error.


Q20. What are your options for recovering from an exception in your script?

Ans:
There are several options for recovering from an exception in a Python script:
1. Use a try-except block: The most common way to recover from an exception in Python is to use a try-except block. This allows you to catch the exception when it is raised, and provide an alternative course of action to take instead of letting the exception propagate and cause your program to terminate.
2. Use a try-except-else block: In addition to the try-except block, you can also use a try-except-else block to handle exceptions in your Python code. This allows you to specify a block of code that will be executed if no exceptions are raised in the try block, and a separate except block that will be executed if an exception is raised.
3. Use a try-except-finally block: Another option for handling exceptions in Python is to use a try-except-finally block. This allows you to specify a try block of code that will be executed, an except block that will be executed if an exception is raised, and a finally block that will be executed regardless of whether an exception is raised or not.


Q21. Describe two methods for triggering exceptions in your script.

Ans:
There are several methods for triggering exceptions in a Python script:
1. Use the raise keyword: To trigger an exception in Python, you can use the raise keyword, followed by the type of exception you want to raise. 
For example:  to raise a ValueError exception, you can use the following code:
Eg.
raise ValueError("Invalid input")

2. Use the assert keyword: Another way to trigger an exception in Python is to use the assert keyword, followed by a condition that you want to test. If the condition evaluates to False, an AssertionError exception will be raised.
For example:  you can use the following code to trigger an AssertionError exception if the variable x is not equal to 5.
assert x == 5, "x must be 5"
Eg:
assert x == 5, "x must be 5"


Q22. Identify two methods for specifying actions to be executed at termination time, regardless of  
whether or not an exception exists.

Ans:
There are two methods for specifying actions to be executed at termination time in Python, regardless of whether or not an exception exists:
1. Use a finally block: The first method for specifying actions to be executed at termination time is to use a finally block. This block of code can be used in conjunction with a try-except block, and it will be executed regardless of whether an exception is raised or not.
For example:
try:
  # Some code here
except SomeException:
  # Handle the exception here
finally:
  # This code will always be executed
  
2. Use a with statement: Another way to specify actions to be executed at termination time is to use a with statement. This statement allows you to define a context for a block of code, and specify actions to be taken when the block of code starts and when it ends.
For example:
with open("file.txt") as f:
  # Code to read from the file here
  # This code will be executed when the with statement starts

# This code will be executed when the with statement ends,
# regardless of whether an exception was raised or not


Q23. What is the purpose of the try statement?

Ans:
The purpose of the try statement in Python is to allow you to test a block of code for errors, and specify how to handle any errors that are raised.
The try statement consists of a try block, which is the block of code that you want to test for errors, and one or more except blocks, which specify how to handle any errors that are raised in the try block.
Eg:
try:
  # Some code here
except SomeException:
  # Handle the exception here


Q24. What are the two most popular try statement variations?

Ans:
The two most popular variations of the try statement in Python are the try-except block and the try-finally block.
1. The try-except block: The try-except block is the most commonly used variation of the try statement. It consists of a try block, which is the block of code that you want to test for errors, and one or more except blocks, which specify how to handle any errors that are raised in the try block.
Eg:
try:
  # Some code here
except SomeException:
  # Handle the exception here

2. The try-finally block: The try-finally block is another variation of the try statement. It consists of a try block, which is the block of code that you want to test for errors, and a finally block, which specifies code that will be executed regardless of whether an exception is raised or not.
Eg:
try:
  # Some code here
finally:
  # This code will always be executed


Q25. What is the purpose of the raise statement?

Ans:
The purpose of the raise statement in Python is to raise an exception. This allows you to explicitly trigger an exception in your code, and specify how the exception should be handled.
The raise statement consists of the raise keyword, followed by the type of exception you want to raise and any additional arguments or information that you want to include with the exception. For example, to raise a ValueError exception with the message "Invalid input".
Eg:
raise ValueError("Invalid input")


Q26. What does the assert statement do, and what other statement is it like?

Ans:
The assert statement in Python allows you to test a condition, and trigger an AssertionError exception if the condition evaluates to False. This can be useful for checking the validity of arguments or input data, and for ensuring that your code is working correctly.

The assert statement consists of the assert keyword, followed by a condition that you want to test, and an optional message that will be included with the AssertionError exception if the condition evaluates to False. For example, to trigger an AssertionError exception if the variable x is not equal to 5.
Eg:
assert x == 5, "x must be 5"

The assert statement is similar to the if statement, as it allows you to specify a condition and take different actions depending on whether the condition is True or False. However, while the if statement allows you to execute different code blocks depending on the result of the condition, the assert statement always triggers an AssertionError exception if the condition evaluates to False. This makes it useful for testing and debugging your code, but it also means that you should use it carefully, as it can cause your program to terminate if the condition evaluates to False.


Q27. What is the purpose of the with/as argument, and what other statement is it like?

Ans:
The with statement in Python allows you to define a context for a block of code, and specify actions to be taken when the block of code starts and when it ends. This is useful for managing resources, such as files or network connections, and ensuring that they are properly closed and released when they are no longer needed.
The with statement consists of the with keyword, followed by an expression that returns an object that defines the context for the code, and the as keyword, followed by a variable that will be bound to the object returned by the expression. For example, to open a file and read its contents.
Eg:
with open("file.txt") as f:
  # Code to read from the file here

The with statement is similar to the try statement, as it allows you to specify a block of code and take different actions depending on whether an exception is raised or not. However, while the try statement allows you to handle exceptions that are raised in the code block, the with statement allows you to specify actions to be taken when the code block starts and when it ends, regardless of whether an exception is raised or not. This makes it useful for managing resources and ensuring that they are properly handled and released.


Q28. What are *args, **kwargs?

Ans:
In Python, the *args and **kwargs syntax is used to define functions that can take a variable number of arguments.
1.  *args is used to specify that a function can take a variable number of positional arguments. This means that the function can be called with any number of arguments, and they will be packed into a tuple and assigned to the args variable.
Eg:
def func(*args):
  # Code to handle the arguments here

# Call the function with three arguments
func(1, 2, 3)

2. **kwargs is used to specify that a function can take a variable number of keyword arguments. This means that the function can be called with any number of keyword arguments, and they will be packed into a dictionary and assigned to the kwargs variable. 
Eg:
def func(**kwargs):
  # Code to handle the keyword arguments here

# Call the function with three keyword arguments
func(arg1=1, arg2=2, arg3=3)


Q29. How can I pass optional or keyword parameters from one function to another?

Ans:
In Python, you can pass optional or keyword parameters from one function to another by using the * and ** syntax to unpack the arguments and keyword arguments.
 suppose you have a function func1() that takes two optional arguments and one keyword argument, and you want to call another function func2() with the same arguments and keyword arguments.
 Eg:
 def func1(arg1, arg2, kwarg1=None):
  # Code for func1() here

def func2(arg1, arg2, kwarg1=None):
  # Code for func2() here

# Call func1() with three arguments
func1(1, 2, kwarg1=3)

# Call func2() with the same arguments and keyword arguments
# as func1() was called with
func2(*(1, 2), **{'kwarg1': 3})


Q30. What are Lambda Functions?

Ans:
In Python, lambda functions are anonymous functions that are defined without a name. These functions are typically used as one-time, throwaway functions, and they are often used in combination with other functional programming concepts, such as map, filter, and reduce.
Lambda functions are defined using the lambda keyword, followed by a list of arguments, a colon, and the function body. The function body can contain any valid Python expression, and it is typically a single line of code that returns a value.
Eg:
# Define a lambda function that takes two arguments
# and returns their sum
sum = lambda x, y: x + y

# Call the lambda function
result = sum(1, 2)

> Lambda functions are useful for defining simple, one-time functions that are used for specific tasks. They are often used in combination with other functional programming concepts, such as map, filter, and reduce, to perform operations on sequences of data. However, they can also be used on their own, as a concise and convenient way to define functions without giving them a name.


Q31. Explain Inheritance in Python with an example?

Ans:
Inheritance is a concept in object-oriented programming that allows a class to inherit attributes and behavior from a parent class. This allows you to define a hierarchy of classes, where classes at lower levels inherit from classes at higher levels, and can add or override attributes and behavior as needed.
In Python, inheritance is implemented using the class keyword, followed by the name of the new class, the (ParentClass) syntax to specify the parent class, and a colon.
Eg:
class ChildClass(ParentClass):
  # Code for the child class here

To demonstrate inheritance in Python, consider the following example:
# Define the parent class
class Animal:
  def __init__(self, name, species):
    self.name = name
    self.species = species

  def speak(self):
    print("I'm an animal!")

# Define the child class
class Cat(Animal):
  def __init__(self, name, species, color):
    # Call the parent class constructor
    super().__init__(name, species)
    # Add a new attribute to the child class
    self.color = color

  def speak(self):
    # Override the parent class method
    print("Meow!")

# Create an instance of the child class
cat = Cat("Whiskers", "Cat", "Gray")

# Access attributes and behavior inherited from the parent class
print(cat.name)     # Output: "Whiskers"
print(cat.species)  # Output: "Cat"
cat.speak()         # Output: "Meow!"

# Access attributes and behavior defined in the child class
print(cat.color)    # Output: "Gray"

Above example demonstrates how inheritance allows you to define a hierarchy of classes, where lower-level classes inherit from higher-level classes, and can add or override attributes and behavior as needed. This can make it easier to reuse and extend existing code, and it can help you organize your code into logical and modular units.


Q32. Suppose class C inherits from classes A and B as class C(A,B).Classes A and B both have their own versions of method func(). If we call func() from an object of 
class C, which version gets invoked?

Ans:
In Python, when a class inherits from multiple parent classes, the method resolution order (MRO) determines which version of a method will be invoked when it is called from an object of the child class.
In the case of the example you provided, where class C inherits from classes A and B as class C(A,B), and both classes A and B have their own versions of the func() method, the MRO will determine which version of the func() method gets invoked when it is called from an object of class C.



Q33. Which methods/functions do we use to determine the type of instance and inheritance?

Ans:
In Python, you can use the type() function to determine the type of an instance, and the issubclass() function to determine whether one class is a subclass of another.


Q34.Explain the use of the 'nonlocal' keyword in Python.

Ans:
In Python, the nonlocal keyword is used to indicate that a variable is nonlocal, and it is defined in an outer, but non-global, scope. This keyword is typically used in nested functions, where a variable defined in an outer function is accessed and modified in a nested function.
To demonstrate the use of the nonlocal keyword, consider the following example:
# Define an outer function
def outer_func():
  # Define a local variable in the outer function
  x = 1

  # Define a nested function
  def inner_func():
    # Modify the local variable in the outer function
    x = 2
    print(f"Inner function: x = {x}")

  # Call the nested function
  inner_func()
  print(f"Outer function: x = {x}")

# Call the outer function
outer_func()


Q35. What is the global keyword?

Ans:
In Python, the global keyword is used to indicate that a variable is global, and it is defined in the global scope. This keyword is typically used in nested functions, where a variable defined in the global scope is accessed and modified in a nested function.
To demonstrate the use of the global keyword, consider the following example:
# Define a global variable
x = 1

# Define a function
def my_func():
  # Modify the global variable
  x = 2
  print(f"Function: x = {x}")

# Call the function
my_func()

# Print the global variable.
print(f"Global: x = {x}")

