# Python-oop_Assiangment

Q1. What is the purpose of Python's OOP?

Ans: The primary purpose of Python's object-oriented programming (OOP) is to provide a way to organize and structure your code in a logical and modular manner. OOP allows you to define classes, which are templates for creating objects. These objects can be used to represent real-world entities or abstract concepts, and they can contain both data (attributes) and behavior (methods).

# Using OOP in Python has several benefits, including:

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
    x = 5
    
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

Q7. What is the process for creating a class?

Q8. How would you define the superclasses of a class?

Q9. What is the relationship between classes and modules?

Q10. How do you make instances and classes?

Q11. Where and how should be class attributes created?

Q12. Where and how are instance attributes created?

Q13. What does the term "self" in a Python class mean?

Q14. How does a Python class handle operator overloading?

Q15. When do you consider allowing operator overloading of your classes?

Q16. What is the most popular form of operator overloading?

Q17. What are the two most important concepts to grasp in order to comprehend Python OOP code?

Q18. Describe three applications for exception processing.

Q19. What happens if you don't do something extra to treat an exception?

Q20. What are your options for recovering from an exception in your script?

Q21. Describe two methods for triggering exceptions in your script.

Q22. Identify two methods for specifying actions to be executed at termination time, regardless of  
whether or not an exception exists.

Q23. What is the purpose of the try statement?

Q24. What are the two most popular try statement variations?

Q25. What is the purpose of the raise statement?

Q26. What does the assert statement do, and what other statement is it like?

Q27. What is the purpose of the with/as argument, and what other statement is it like?

Q28. What are *args, **kwargs?

Q29. How can I pass optional or keyword parameters from one function to another?

Q30. What are Lambda Functions?

Q31. Explain Inheritance in Python with an example?

Q32. Suppose class C inherits from classes A and B as class C(A,B).Classes A and B both have their own versions of method func(). If we call func() from an object of 
class C, which version gets invoked?

Q33. Which methods/functions do we use to determine the type of instance and inheritance?

Q34.Explain the use of the 'nonlocal' keyword in Python.

Q35. What is the global keyword?
