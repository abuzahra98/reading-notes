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

[<== Back to Readme](README.md)