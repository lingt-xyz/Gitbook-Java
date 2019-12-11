# Control Flow

## if-then

```java
if (condition1) {
    statement1;
} else if (statement2) {
    statement2;
} else {
    statement3;
}
```

## while

You can implement an infinite loop using the `while` statement as follows:

```java
while (true){
    // your code goes here
}
```

The Java programming language also provides a `do-while` statement, which can be expressed as follows:

```java
do {
     statement(s)
} while (expression);
```

## for

```java
for (initialization; termination;
     increment) {
    statement(s)
}
```

When using this version of the `for` statement, keep in mind that:

* The _initialization_ expression initializes the loop; it's executed _**once**_, as the loop begins.
* When the _termination_ expression evaluates to `false`, the loop terminates.
* The _increment_ expression is invoked _**after**_ each iteration through the loop; it is perfectly acceptable for this expression to increment or decrement a value.

## Branching

### break

The `break` statement has two forms: labeled and unlabeled. 

* An unlabeled `break` statement terminates the _**innermost**_ `switch`, `for`, `while`, or `do-while` statement,
* but a labeled `break` terminates an outer statement.  

### continue

The `continue` statement skips the current iteration of a `for`, `while` , or `do-while` loop. 

* The unlabeled form skips to the end of the _**innermost**_ loop's body and evaluates the `boolean` expression that controls the loop.
* A labeled `continue` statement skips the current iteration of an outer loop marked with the given label.

### return

The `return` statement exits from the current method, and control flow returns to where the method was invoked.



[https://docs.oracle.com/javase/tutorial/java/nutsandbolts/flow.html](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/flow.html)



