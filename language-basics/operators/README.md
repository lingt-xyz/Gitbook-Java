# Operators

## Assignment Operator

The assignment operator "`=`" assigns the value on its right to the operand on its left:

```java
int cadence = 0;
 int speed = 0;
 int gear = 1;
```

## Arithmetic Operators

| Operator | Description |
| :--- | :--- |
| `+` | Additive operator \(also used for String concatenation\) |
| `-` | Subtraction operator |
| `*` | Multiplication operator |
| `/` | Division operator |
| `%` | Remainder operator |

## Unary Operators

| Operator | Description |
| :--- | :--- |
| `+` | Unary plus operator; indicates positive value \(numbers are positive without this, however\) |
| `-` | Unary minus operator; negates an expression |
| `++` | Increment operator; increments a value by 1 |
| `--` | Decrement operator; decrements a value by 1 |
| `!` | Logical complement operator; inverts the value of a boolean |

## Relational Operators

| Operator | Description |
| :--- | :--- |
| `==` | equal to |
| `!=` | not equal to |
| `>` | greater than |
| `>=` | greater than or equal to |
| `<` | less than |
| `<=` | less than or equal to |

## Conditional Operators

| Operator | Description |
| :--- | :--- |
| `&&` | and |
| `||` | or |

These operators exhibit "short-circuiting" behavior, which means that the second operand is evaluated only if needed.

### Ternary operator

`?:`is known as the ternary operator because it uses three operands.

If `someCondition` is `true`, assign the value of `value1` to `result`. Otherwise, assign the value of `value2` to `result`.

```java
result = someCondition ? value1 : value2;
```

## Type Comparison Operator

The `instanceof` operator compares an object to a specified type.



[https://docs.oracle.com/javase/tutorial/java/nutsandbolts/operators.html](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/operators.html)

