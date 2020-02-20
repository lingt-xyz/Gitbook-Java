# Exceptions

## Definition

> [An _exception_ is an **event**, which occurs during the execution of a program, that **disrupts** the normal flow of the program's instructions.](https://docs.oracle.com/javase/tutorial/essential/exceptions/definition.html)

## The Three Kinds of Exceptions

### Checked Exception

These are exceptional conditions that a well-written application should **anticipate and recover from**. For example, suppose an application prompts a user for an input file name, then opens the file by passing the name to the constructor for `java.io.FileReader`. Normally, the user provides the name of an existing, readable file, so the construction of the `FileReader` object succeeds, and the execution of the application proceeds normally. But sometimes the user supplies the name of a nonexistent file, and the constructor throws `java.io.FileNotFoundException`. A well-written program **will catch this exception and notify the user of the mistake, possibly prompting for a corrected file name**.

### Error

These are exceptional conditions that are _**external**_ to the application, and that the application usually _**cannot anticipate or recover from**_. For example, suppose that an application successfully opens a file for input, but is unable to read the file because of a hardware or system malfunction. The unsuccessful read will throw `java.io.IOError`. An application might choose to catch this exception, in order to notify the user of the problem — but it also might make sense for the program to print a stack trace and exit.

### Runtime Exception

These are exceptional conditions that are _**internal**_ to the application, and that the application usually _**cannot anticipate or recover from**_. These usually indicate **programming bugs**, such as logic errors or improper use of an API. For example, consider the application described previously that passes a file name to the constructor for `FileReader`. If a logic error causes a `null` to be passed to the constructor, the constructor will throw `NullPointerException`. The application can catch this exception, but it probably **makes more sense to eliminate the bug** that caused the exception to occur.

## Class Error

An `Error` is a subclass of `Throwable` that indicates serious problems that a reasonable application **should not try to catch**. Most such errors are **abnormal** conditions. 

A method is not required to declare in its `throws` clause any subclasses of `Error` that might be thrown during the execution of the method but not caught, since these errors are abnormal conditions that should never occur. That is, `Error` and its subclasses are regarded as _**unchecked exceptions**_ for the purposes of compile-time checking of exceptions

## Class Exception

The class `Exception` and its subclasses are a form of `Throwable` that indicates conditions that a reasonable application might want to catch.

The class `Exception` and any subclasses that are not also subclasses of [`RuntimeException`](https://docs.oracle.com/javase/8/docs/api/java/lang/RuntimeException.html) are _**checked exceptions**_. Checked exceptions need to be declared in a method or constructor's `throws` clause if they can be thrown by the execution of the method or constructor and propagate outside the method or constructor boundary.

## Class RuntimeException

`RuntimeException` is the superclass of those exceptions that can be thrown during the normal operation of the Java Virtual Machine.

`RuntimeException` and its subclasses are _**unchecked exceptions**_. Unchecked exceptions do _not_ need to be declared in a method or constructor's `throws` clause if they can be thrown by the execution of the method or constructor and propagate outside the method or constructor boundary.

