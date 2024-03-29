# Inheritance and Interfaces

Inheritance is the process of classes inheriting state and behavior from others. A superclass exists as a broad template from which subclasses can inherit properties, and the subclasses are able to take that blueprint from the superclass and add their own methods that make them unique. There is no limit to the amount of subclasses that can inherit from a superclass.

```Java
class SubclassName extends SuperclassName { //`extends` is the keyword for inheritance, giving the preceding class the methods and properties of the class which follows.
  methods
  some other stuff
}
```

An Object's methods define it's interaction with the outside world, and those methods become the object's interface.

```Java
interface ClassName { // "interface" preceeding a class name in the place of class would specify it then as an interface instead
   void methodName(int name)

   void methodName2(double name2)

   void methodName3(int name3)
}
```

The process of implementing an interface and inherticance from above are similar:

```Java
class NewClassName implements ClassName {
int something = 1
int anotherThing = 2
int oneMore = 3

void methodName (int name) {
  something = name;
}

void methodName2 (int name2) {
  anotherThing = name2;
}

void methodName3 (int name3) {
  oneMore = name3;
}
}
```

The compiler requires the methods from the interface class be present within the class that implements it. MethodName, MethodName2, MethodName 3 must be used else compilation fails.


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