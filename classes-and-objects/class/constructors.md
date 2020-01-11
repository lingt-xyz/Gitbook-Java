# Constructors

Constructor declarations look like method declarations—except that they use the **name of the class** and have **no return type**.

Constructors can be:

* Default constructor: if you did not define a constructor, the compiler will create a default one with no parameters.
* No-argument constructor: a constructor without any parameters.
* Parameterized constructor: a constructor accepts parameters.
* Copy constructor: a constructor accepts an object with the same type as its parameter.

```java
class Parent {
    private String name;
    private int age;
    
    // No-argument constructor
    public Parent(){
    }
    
    // Parameterized Constructor
    public Parent(String name){
        this.name = name;
    }
    
    // Parameterized Constructor
    public Parent(String name, int age){
        this.name = name;
        this.age = age;
    }
    
    // Copy Constructor
    public Parent(Parent p){
        this.name = p.name;
        this.age = age;
    }
}
```

