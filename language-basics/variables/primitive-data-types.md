# Primitive Data Types

## Eight Primitive Data Types

* **byte**: The `byte` data type is an 8-bit signed two's complement integer. 
  * $$2^8=256$$
  * It has a minimum value of -128 and a maximum value of 127 \(inclusive\).
* **short**: The `short` data type is a 16-bit signed two's complement integer. 
  * $$2^{16}=65536$$
  * It has a minimum value of -32,768 and a maximum value of 32,767 \(inclusive\).
* **int**: By default, the `int` data type is a 32-bit signed two's complement integer.
  * It has a minimum value of$$-2^{31}$$and a maximum value of$$2^{31}-1$$.
  * In Java SE 8 and later, you can use the `int` data type to represent an unsigned 32-bit integer, which has a minimum value of$$0$$and a maximum value of $$2^{32}-1$$. Use the Integer class to use `int` data type as an unsigned integer. Static methods like `compareUnsigned`, `divideUnsigned` etc have been added to the [`Integer`](https://docs.oracle.com/javase/8/docs/api/java/lang/Integer.html) class to support the arithmetic operations for unsigned integers.
* **long**: The `long` data type is a 64-bit two's complement integer. 
  * The signed long has a minimum value of $$-2^{63}$$ and a maximum value of $$2^{63}-1$$. 
  * In Java SE 8 and later, you can use the `long` data type to represent an unsigned 64-bit long, which has a minimum value of $$0$$ and a maximum value of $$2^{64}-1$$. The [`Long`](https://docs.oracle.com/javase/8/docs/api/java/lang/Long.html) class also contains methods like `compareUnsigned`, `divideUnsigned` etc to support arithmetic operations for unsigned long.
* **float**: The `float` data type is a single-precision 32-bit IEEE 754 floating point. 
  * Its range of values is specified in the [Floating-Point Types, Formats, and Values](https://docs.oracle.com/javase/specs/jls/se7/html/jls-4.html#jls-4.2.3) section of the Java Language Specification.
  * This data type should _**never**_ be used for precise values, such as currency. For that, you will need to use the [java.math.BigDecimal](https://docs.oracle.com/javase/8/docs/api/java/math/BigDecimal.html) class instead.
* **double**: The `double` data type is a double-precision 64-bit IEEE 754 floating point. 
  * Its range of values is specified in the [Floating-Point Types, Formats, and Values](https://docs.oracle.com/javase/specs/jls/se7/html/jls-4.html#jls-4.2.3) section of the Java Language Specification. 
  * For decimal values, this data type is generally the default choice.
  * This data type should _**never**_ be used for precise values, such as currency.
* **boolean**: The `boolean` data type has only two possible values: `true` and `false`.
  * This data type represents one bit of information, but its "size" isn't something that's precisely defined.
* **char**: The `char` data type is a single 16-bit Unicode character. 
  * It has a minimum value of `'\u0000'` \(or 0\) and a maximum value of `'\uffff'` \(or 65,535 inclusive\).

### String

The Java programming language also provides special support for character strings via the [java.lang.String](https://docs.oracle.com/javase/8/docs/api/java/lang/String.html) class. Enclosing your character string within double quotes will automatically create a new `String` object; for example, `String s = "this is a string";`. `String` objects are **immutable**, which means that once created, their values **cannot be changed**. The `String` class is not technically a primitive data type.

## Default Values

### Fields

| **Data Type** | **Default Value \(for fields\)** |
| :--- | :--- |
| byte | 0 |
| short | 0 |
| int | 0 |
| long | 0L |
| float | 0.0f |
| double | 0.0d |
| char | '\u0000' |
| String \(or any object\)   | null |
| boolean | false |

### Local Variables

The compiler never assigns a default value to an uninitialized local variable. Accessing an uninitialized local variable will result in a compile-time error.

[https://docs.oracle.com/javase/tutorial/java/nutsandbolts/datatypes.html](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/datatypes.html)

