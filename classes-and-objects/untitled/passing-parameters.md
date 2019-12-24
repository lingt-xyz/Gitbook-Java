# Passing Parameters

## By Reference or By Value?

{% hint style="warning" %}
Java always passes arguments by **value**.
{% endhint %}

## Definitions

### Reference

> [A data element whose value is an address.](https://docs.oracle.com/javase/tutorial/information/glossary.html#reference)

```java
Object o = new Object();
```

Here, `o` is a reference, and its value is _an address_.

### Value

The literal value.

```java
int i = 1;
```

Here, `i` is a primitive type not a reference, and its value is `1`.

## Passing Primitive Data Type Arguments

Primitive arguments, such as an `int` or a `double`, are passed into methods by **value**.

```java
public class PassPrimitiveByValue {

    public static void main(String[] args) {
           
        int x = 3;
           
        // invoke passMethod() with  x as argument
        passMethod(x);
           
        // print x to see if its value has changed
        System.out.println("After invoking passMethod, x = " + x);
           
    }
        
    // change parameter in passMethod()
    public static void passMethod(int p) {
        p = 10;
    }
}
```

When you run this program, the output is:

```text
After invoking passMethod, x = 3
```

### Passing Reference Data Type Arguments

Reference data type parameters, such as objects, are also passed into methods by **value**.

{% hint style="info" %}
Recall that value is an address.
{% endhint %}

```java
public class Main {
     public static void main(String[] args) {
          Foo f = new Foo("f");
          changeReference(f); // It won't change the reference!
          modifyReference(f); // It will change the object that the reference refers to!
     }
     public static void changeReference(Foo a) {
          Foo b = new Foo("b");
          a = b;
     }
     public static void modifyReference(Foo c) {
          c.setAttribute("c");
     }
}
```

{% embed url="https://stackoverflow.com/questions/7893492/is-java-really-passing-objects-by-value/7893495\#7893495" %}

{% embed url="https://docs.oracle.com/javase/tutorial/java/javaOO/arguments.html" %}

