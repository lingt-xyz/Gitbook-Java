# Inheritance

## **Definitions**

A class that is derived from another class is called a subclass \(also a derived class, extended class, or child class\). The class from which the subclass is derived is called a superclass \(also a base class or a parent class\).

* Superclass$$\equiv$$Base class$$\equiv$$Parent class
* Subclass$$\equiv$$Derived class$$\equiv$$Child class

Excepting `Object`, which has no superclass, every class has one and only one direct superclass \(single inheritance\).

A subclass inherits all the members \(fields, methods, and nested classes\) from its superclass. Constructors are not members, so they are not inherited by subclasses, but the constructor of the superclass can be invoked from the subclass.

## Subclass

What You Can Do in a Subclass?

A subclass inherits all of the public and protected members of its parent, no matter what package the subclass is in. If the subclass is in the same package as its parent, it also inherits the package-private members of the parent. You can use the inherited members as is, replace them, hide them, or supplement them with new members:

* You can declare a **field** in the subclass with the same name as the one in the superclass, thus **hiding** it \(not recommended\).
* You can declare new fields in the subclass that are not in the superclass.
* The inherited methods can be used directly as they are.
* You can write a new **instance method** in the subclass that has the same signature as the one in the superclass, thus **overriding** it.
* You can write a new **static method** in the subclass that has the same signature as the one in the superclass, thus **hiding** it.
* You can declare new methods in the subclass that are not in the superclass.
* You can write a subclass constructor that invokes the constructor of the superclass, either implicitly or by using the keyword `super`.

A nested class has access to all the private members of its enclosing class—both fields and methods. Therefore, a public or protected nested class inherited by a subclass has indirect access to all of the private members of the superclass.

