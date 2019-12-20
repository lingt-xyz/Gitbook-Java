# Member Variables

There are several kinds of variables:

* Member variables in a class—these are called fields.
* Variables in a method or block of code—these are called local variables.
* Variables in method declarations—these are called parameters.

## Access Modifiers

The first \(left-most\) modifier used lets you control what other classes have access to a member field. For the moment, consider only `public` and `private`. Other access modifiers will be discussed later.

* `public` modifier—the field is accessible from all classes.
* `private` modifier—the field is accessible only within its own class.

## Example

```java
class Parent {
    private int age;
    
    public int getAge() {
        return this.age;
    }
        
    public void setAge(int age) {
        this.age = age;
    }
}
```

