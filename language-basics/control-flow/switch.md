# switch

A `switch` works with the `byte`, `short`, `char`, and `int` primitive data types. It also works with enumerated types, the [`String`](https://docs.oracle.com/javase/8/docs/api/java/lang/String.html) class, and a few special classes that wrap certain primitive types: [`Character`](https://docs.oracle.com/javase/8/docs/api/java/lang/Character.html), [`Byte`](https://docs.oracle.com/javase/8/docs/api/java/lang/Byte.html), [`Short`](https://docs.oracle.com/javase/8/docs/api/java/lang/Short.html), and [`Integer`](https://docs.oracle.com/javase/8/docs/api/java/lang/Integer.html).

```java
int month = 8;
String monthString;
switch (month) {
   case 1:  monthString = "January";
            break;
   case 2:  monthString = "February";
            break;
   case 3:  monthString = "March";
            break;
   case 4:  monthString = "April";
            break;
   case 5:  monthString = "May";
            break;
   case 6:  monthString = "June";
            break;
   case 7:  monthString = "July";
            break;
   case 8:  monthString = "August";
            break;
   case 9:  monthString = "September";
            break;
   case 10: monthString = "October";
            break;
   case 11: monthString = "November";
            break;
   case 12: monthString = "December";
            break;
   default: monthString = "Invalid month";
            break;
}
System.out.println(monthString);
```

The body of a `switch` statement is known as a switch block. A statement in the `switch` block can be labeled with one or more `case` or `default` labels.

{% hint style="danger" %}
Each `break` statement terminates the enclosing `switch` statement. Control flow continues with the first statement following the `switch` block. The `break` statements are necessary because without them, statements in `switch` blocks _**fall through**_: All statements after the matching `case` label are executed in sequence, regardless of the expression of subsequent `case` labels, until a `break` statement is encountered.
{% endhint %}

```java
java.util.ArrayList<String> futureMonths = new java.util.ArrayList<String>();

int month = 8;

switch (month) {
    case 1:  futureMonths.add("January");
    case 2:  futureMonths.add("February");
    case 3:  futureMonths.add("March");
    case 4:  futureMonths.add("April");
    case 5:  futureMonths.add("May");
    case 6:  futureMonths.add("June");
    case 7:  futureMonths.add("July");
    case 8:  futureMonths.add("August");
    case 9:  futureMonths.add("September");
    case 10: futureMonths.add("October");
    case 11: futureMonths.add("November");
    case 12: futureMonths.add("December");
             break;
    default: break;
}

if (futureMonths.isEmpty()) {
    System.out.println("Invalid month number");
} else {
    for (String monthName : futureMonths) {
       System.out.println(monthName);
    }
}

// This is the output from the code:

August
September
October
November
December
```

```java
int month = 2;
int year = 2000;
int numDays = 0;

switch (month) {
    case 1: case 3: case 5:
    case 7: case 8: case 10:
    case 12:
        numDays = 31;
        break;
    case 4: case 6:
    case 9: case 11:
        numDays = 30;
        break;
    case 2:
        if (((year % 4 == 0) && 
             !(year % 100 == 0))
             || (year % 400 == 0))
            numDays = 29;
        else
            numDays = 28;
        break;
    default:
        System.out.println("Invalid month.");
        break;
}
System.out.println("Number of Days = " + numDays);
```

