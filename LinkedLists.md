# Class 05

## references 

https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/singly_linked_list.html

https://medium.com/basecs/whats-a-linked-list-anyway-part-1-d8b7e6508b9d

https://www.geeksforgeeks.org/linked-list-set-1-introduction/


## Linked Lists

There are two types of linked lists, singly linked, and doubly linked. 

Singly means that each node has one reference in them
doubly means there are two references in each node. 

When traversing a linked list, you cant use for or foreach loops, we depend on the "Next" value of each node. 

Make sure that each node has a value, and points to the next node in the sequence. 






A linked list is a series of nodes tied together like links in a chain, with each node referencing the next in line.

- Singly is the number of references a node has, and a singly-linked list has only one reference which points to the next node
- Doubly linked lists , as you might have guessed have double the references, one with the next node and one with the prior node as well
- Nodes, oft mentioned thus far, are the individual links in the chain and contain their data
- Next is a property of each node that refers to the next node in the link
- Head is a reference to the first node in a linked list
- Current is a reference to the node currently being looked at

Similar to arrays in concept, Linked Lists cannot be traversed through for/forEach loops, and must use a While loop while depending on the Next property defined above.

Sample Code

```Java
public static boolean includes(int value)

Current = Head // makes sure the loop starts at the beginning of the LL

while (Current != null) { //only runs if the current node has a value
  if (Current.value == value){ // checking if the value of current is the value we want. if it is, the loop ends and the method returns true
    return true
  }
  else (Current = Current.Next){ // if it is not the value we are looking for, the value of current is changed to look at the next link
  }
}
    return false // if the value never returns true then the value is not in the LL, therefore the method is false
```

## Object


An object is a software bundle of related state and behavior. Software objects are often used to model the real-world objects that you find in everyday life. This lesson explains how state and behavior are represented within an object, introduces the concept of data encapsulation, and explains the benefits of designing your software in this manner.


## Class
A class is a blueprint or prototype from which objects are created. This section defines a class that models the state and behavior of a real-world object. It intentionally focuses on the basics, showing how even a simple class can cleanly model state and behavior.

Inheritance

ses inherit state and behavior from their superclasses, and explains how to derive one class from another using the simple syntax provided by the Java programming language
Object-oriented programming allows classes to inherit commonly used state and behavior from other classes.

In the Java programming language, each class is allowed to have one direct superclass, and each superclass has the potential for an unlimited number of subclasses.


What You Can Do in a Subclass
A subclass inherits all of the public and protected members of its parent, no matter what package the subclass is in. If the subclass is in the same package as its parent, it also inherits the package-private members of the parent. You can use the inherited members as is, replace them, hide them, or supplement them with new members:

* The inherited fields can be used directly , just like any other fields.

* You can declare a field in the subclass with the same name as the one in the superclass , thus hiding it (not recommended).

* You can declare new fields in the subclass that are not in the superclass.
The inherited methods can be used directly as they are.
* You can write a new instance method in the subclass that has the same signature as the one in the superclass, thus overriding it.

* You can write a new static method in the subclass that has the same signature as the one in the superclass, thus hiding it.
 * You can declare new methods in the subclass that are not in the superclass.

* You can write a subclass constructor that invokes the constructor of the superclass, either implicitly or by using the keyword super.

## Package

A package is a namespace for organizing classes and interfaces in a logical manner. Placing your code into packages makes large software projects easier to manage. This section explains why this is useful, and introduces you to the Application Programming Interface (API) provided by the Java platform


## Interfaces
Implementing an interface allows a class to become more formal about the behavior it promises to provide.


* Interfaces form a contract between the class and the outside world , and this contract is enforced at build time by the compiler.

* If your class claims to implement an interface, all methods defined by that interface must appear in its source code before the class will successfully compile.
* In the Java programming language, an interface is a reference type, similar to a class, that can contain only constants, method signatures, default methods, static methods, and nested types.
Method bodies exist only for default methods and static methods.
* Interfaces cannot be instantiated—they can only be implemented by classes or extended by other interfaces.
* An interface can extend other interfaces, just as a class subclass or extend another class . However, whereas a class can extend only one other class, an interface can extend any number of interfaces.
* The interface declaration includes a comma-separated list of all the interfaces that it extends.
* If you define a reference variable whose type is an interface, any object you assign to it must be an instance of a class that  
implements the interface.

* Interfaces as APIs

* The robotic car example shows an interface being used as an industry standard Application Programming Interface (API). APIs are also common in commercial software products. Typically, a company sells a software package that contains complex methods that another company wants to use in its own software product. An example would be a package of digital image processing methods that are sold to companies making end-user graphics programs. The image processing company writes its classes to implement an interface, which it makes public to its customers. The graphics company then invokes the image processing methods using the signatures and return types defined in the interface. While the image processing company’s API is made public (to its customers), its implementation of the API is kept as a closely guarded secret—in fact, it may revise the implementation at a later date as long as it continues to implement the original interface that its customers have relied on.