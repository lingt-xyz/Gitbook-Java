# Building Java Libraries

## Prerequisites

* JRE &gt;= 1.8
  * `java -version`
* Gradle &gt;= 5.0
  * `gradle -version`

## Initialize a library project

From inside the new project directory, run the `init` task and select `java-library` project type when prompted.

```bash
% mkdir demo
% cd demo
% gradle init

Select type of project to generate:
  1: basic
  2: cpp-application
  3: cpp-library
  4: groovy-application
  5: groovy-library
  6: java-application
  7: java-library
  8: kotlin-application
  9: kotlin-library
  10: scala-library
Enter selection (default: basic) [1..10] 7

Select build script DSL:
  1: groovy
  2: kotlin
Enter selection (default: groovy) [1..2]

Select test framework:
  1: junit
  2: testng
  3: spock
Enter selection (default: junit) [1..3]

Project name (default: demo):

Source package (default: demo):


BUILD SUCCESSFUL in 1s
2 actionable tasks: 2 executed
```

### What Gradle generated for you

```text
├── build.gradle
├── gradle
│   └── wrapper 
│       ├── gradle-wrapper.jar
│       └── gradle-wrapper.properties
├── gradlew
├── gradlew.bat
├── settings.gradle
└── src
    ├── main
    │   └── java 
    │       └── demo
    │           └── Library.java
    └── test
        └── java 
            └── demo
                └── LibraryTest.java
```

* `src/main/java`: Default Java source folder
* `src/test/java`: Default Java test folder

## Review the generated project files

{% code title="settings.gradle" %}
```groovy
rootProject.name = 'building-java-libraries'
```
{% endcode %}

* This assigns the name of the project.

{% code title="build.gradle" %}
```groovy
plugins {
    id 'java-library'
}

repositories {
    jcenter() 
}

dependencies {
    api 'org.apache.commons:commons-math3:3.6.1' 

    implementation 'com.google.guava:guava:27.0.1-jre' 

    testImplementation 'junit:junit:4.12' 
}
```
{% endcode %}

* `repositories`: Public Bintray Artifactory repository
* `api 'org.apache.commons:commons-math3:3.6.1'`: This is an example of a dependency which is exported to consumers, that is to say found on their compile classpath.
* `implementation 'com.google.guava:guava:27.0.1-jre'`: This is an example of a dependency which is used internally, and not exposed to consumers on their own compile classpath.
* `testImplementation 'junit:junit:4.12'`: JUnit testing library

## Assemble the library JAR

```bash
$ ./gradlew build
> Task :compileJava
> Task :processResources NO-SOURCE
> Task :classes
> Task :jar
> Task :assemble
> Task :compileTestJava
> Task :processTestResources NO-SOURCE
> Task :testClasses
> Task :test
> Task :check
> Task :build

BUILD SUCCESSFUL in 11s
4 actionable tasks: 4 executed
```

You can find your newly packaged JAR file in the `build/libs` directory with the name `building-java-libraries.jar`. Verify that the archive is valid by running the following command:

```bash
$ jar tf build/libs/building-java-libraries.jar
META-INF/
META-INF/MANIFEST.MF
Library.class
```

## References

* [Building Java Libraries](https://guides.gradle.org/building-java-libraries/)

