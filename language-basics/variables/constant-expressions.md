# Constant Expressions

A compile-time _constant expression_ is an expression denoting a value of primitive type or a `String` that does not complete abruptly and is composed using only the following:

* Literals of primitive type and literals of type `String` \([§3.10.1](https://docs.oracle.com/javase/specs/jls/se7/html/jls-3.html#jls-3.10.1), [§3.10.2](https://docs.oracle.com/javase/specs/jls/se7/html/jls-3.html#jls-3.10.2), [§3.10.3](https://docs.oracle.com/javase/specs/jls/se7/html/jls-3.html#jls-3.10.3), [§3.10.4](https://docs.oracle.com/javase/specs/jls/se7/html/jls-3.html#jls-3.10.4), [§3.10.5](https://docs.oracle.com/javase/specs/jls/se7/html/jls-3.html#jls-3.10.5)\)
* Casts to primitive types and casts to type `String` \([§15.16](https://docs.oracle.com/javase/specs/jls/se7/html/jls-15.html#jls-15.16)\)
* The unary operators `+`, `-`, `~`, and `!` \(but not `++` or `--`\) \([§15.15.3](https://docs.oracle.com/javase/specs/jls/se7/html/jls-15.html#jls-15.15.3), [§15.15.4](https://docs.oracle.com/javase/specs/jls/se7/html/jls-15.html#jls-15.15.4), [§15.15.5](https://docs.oracle.com/javase/specs/jls/se7/html/jls-15.html#jls-15.15.5), [§15.15.6](https://docs.oracle.com/javase/specs/jls/se7/html/jls-15.html#jls-15.15.6)\)
* The multiplicative operators `*`, `/`, and `%` \([§15.17](https://docs.oracle.com/javase/specs/jls/se7/html/jls-15.html#jls-15.17)\)
* The additive operators `+` and `-` \([§15.18](https://docs.oracle.com/javase/specs/jls/se7/html/jls-15.html#jls-15.18)\)
* The shift operators `<<`, `>>`, and `>>>` \([§15.19](https://docs.oracle.com/javase/specs/jls/se7/html/jls-15.html#jls-15.19)\)
* The relational operators `<`, `<=`, `>`, and `>=` \(but not `instanceof`\) \([§15.20](https://docs.oracle.com/javase/specs/jls/se7/html/jls-15.html#jls-15.20)\)
* The equality operators `==` and `!=` \([§15.21](https://docs.oracle.com/javase/specs/jls/se7/html/jls-15.html#jls-15.21)\)
* The bitwise and logical operators `&`, `^`, and `|` \([§15.22](https://docs.oracle.com/javase/specs/jls/se7/html/jls-15.html#jls-15.22)\)
* The conditional-and operator `&&` and the conditional-or operator `||` \([§15.23](https://docs.oracle.com/javase/specs/jls/se7/html/jls-15.html#jls-15.23), [§15.24](https://docs.oracle.com/javase/specs/jls/se7/html/jls-15.html#jls-15.24)\)
* The ternary conditional operator `? :` \([§15.25](https://docs.oracle.com/javase/specs/jls/se7/html/jls-15.html#jls-15.25)\)
* Parenthesized expressions \([§15.8.5](https://docs.oracle.com/javase/specs/jls/se7/html/jls-15.html#jls-15.8.5)\) whose contained expression is a constant expression.
* Simple names \([§6.5.6.1](https://docs.oracle.com/javase/specs/jls/se7/html/jls-6.html#jls-6.5.6.1)\) that refer to constant variables \([§4.12.4](https://docs.oracle.com/javase/specs/jls/se7/html/jls-4.html#jls-4.12.4)\).
* Qualified names \([§6.5.6.2](https://docs.oracle.com/javase/specs/jls/se7/html/jls-6.html#jls-6.5.6.2)\) of the form _TypeName_ `.` _Identifier_ that refer to constant variables \([§4.12.4](https://docs.oracle.com/javase/specs/jls/se7/html/jls-4.html#jls-4.12.4)\).

Compile-time constant expressions of type `String` are always "interned" so as to share unique instances, using the method `String.intern`.

```text
true
(short)(1*2*3*4*5*6)
Integer.MAX_VALUE / 2
2.0 * Math.PI
"The integer " + Long.MAX_VALUE + " is mighty big."
```

{% embed url="https://docs.oracle.com/javase/specs/jls/se7/html/jls-15.html\#jls-15.28" %}

