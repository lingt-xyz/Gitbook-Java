---
description: A generic example
---

# Getting Started

## Prerequisites

* JRE &gt;= 1.8
  * `java -version`
* Gradle &gt;= 4.10.3
  * `gradle -version`

## Initialize a project

```text
% mkdir basic-demo
% cd basic-demo
% gradle init
```

### What Gradle generated for you

```groovy
├── build.gradle  
├── gradle
│   └── wrapper
│       ├── gradle-wrapper.jar  
│       └── gradle-wrapper.properties  
├── gradlew  
├── gradlew.bat  
└── settings.gradle  
```

* `build.gradle` : Gradle build script for configuring the current project
* `gradle-wrapper.jar`: [Gradle Wrapper](https://docs.gradle.org/4.10.3/userguide/gradle_wrapper.html) executable JAR
* `gradle-wrapper.properties`: Gradle Wrapper configuration properties
* `gradlew`: Gradle Wrapper script for Unix-based systems
* `gradlew.bat`: Gradle Wrapper script for Windows
* `settings.gradle`: Gradle settings script for configuring the Gradle build

## Create a task

1. Create a directory called `src`.
2. Add a file called `myfile.txt` in the `src` directory. Add the single line `Hello, World!` to it.
3. Define a task called `copy` of type `Copy` in your build file `build.gradle` that copied the `src` directory to a new directory called `dest`. \(You don't have to create the `dest` directory, the task will do it for you.\)

{% code title="build.gradle" %}
```groovy
task copy(type: Copy, group: "Custom", description: "Copies sources to the dest directory") {
    from "src"
    into "dest"
}
```
{% endcode %}

### Run a task

```bash
% ./gradlew copy
> Task :copy

BUILD SUCCESSFUL in 0s
1 actionable task: 1 executed
```



## References

* [Creating New Gradle Builds](https://guides.gradle.org/creating-new-gradle-builds/)

