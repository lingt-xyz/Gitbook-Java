# String

The Java programming language provides special support for character strings via the [java.lang.String](https://docs.oracle.com/javase/8/docs/api/java/lang/String.html) class. Enclosing your character string within double quotes will automatically create a new `String` object; for example, `String s = "this is a string";`. `String` objects are **immutable**, which means that once created, their values **cannot be changed**. The `String` class is not technically a primitive data type.

String as a field of a class would have `null` as default value.

{% hint style="warning" %}
`==` or `equals`❓ 
{% endhint %}

```java
String s1 = "abc";
String s2 = "abc";
String s3 = new String("abc");
System.out.println(s1 == s2);
System.out.println(s1.equals(s2));
System.out.println(s1 == s3);
System.out.println(s1.equals(s3));

// output
true
true
false
true
```

> Java uses [String interning](https://en.wikipedia.org/wiki/String_interning) to store string literals.

It means:

1. There is a pool, String literal pool, storing all String literals.
2. When a new String literal was created, the JVM will look for this String literal from the String literal pool.
   1. If an equivalent String literal is found, the reference to the newly created String literal would be simply updated. \(That's why `==` would return `true`.\)
   2. If not, this new String literal would be added to the String literal pool and its reference would be returned.

#### What about `new`

If `new` is used, the JVM is obliged to create a new String object. \(That's why `==` would return `false`.\)

## A deeper look

```text
package testPackage;
class Test {
    public static void main(String[] args) {
        String hello = "Hello", lo = "lo";
        System.out.print((hello == "Hello") + " ");
        System.out.print((Other.hello == hello) + " ");
        System.out.print((other.Other.hello == hello) + " ");
        System.out.print((hello == ("Hel"+"lo")) + " ");
        System.out.print((hello == ("Hel"+lo)) + " ");
        System.out.println(hello == ("Hel"+lo).intern());
    }
}
class Other { static String hello = "Hello"; }
```

```text
package other;
public class Other { public static String hello = "Hello"; }
```

The output:

```text
true true true true false true
```

## How many Strings

```java
String s1 = "abc";
String s2 = "abc";

String s3 = new String("def");
```

## Conclusion

* Literal strings within the same class \([§8](https://docs.oracle.com/javase/specs/jls/se7/html/jls-8.html)\) in the same package \([§7](https://docs.oracle.com/javase/specs/jls/se7/html/jls-7.html)\) represent references to the same `String` object \([§4.3.1](https://docs.oracle.com/javase/specs/jls/se7/html/jls-4.html#jls-4.3.1)\).
* Literal strings within different classes in the same package represent references to the same `String` object.
* Literal strings within different classes in different packages likewise represent references to the same `String` object.
* Strings computed by constant expressions \([§15.28](https://docs.oracle.com/javase/specs/jls/se7/html/jls-15.html#jls-15.28)\) are computed at compile time and then treated as if they were literals.
* Strings computed by concatenation at run time are newly created and therefore distinct.
* The result of explicitly interning a computed string is the same string as any pre-existing literal string with the same contents.

{% embed url="https://docs.oracle.com/javase/10/docs/api/java/lang/String.html\#intern\(\)" %}

{% embed url="https://en.wikipedia.org/wiki/String\_interning" %}

{% embed url="https://docs.oracle.com/javase/specs/jls/se7/html/jls-3.html\#jls-3.10.5" %}

