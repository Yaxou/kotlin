Kotlin
===========

#### How to build and run tests

##### Working with the project using Intellij IDEA or Android Studio:

1. Import the project as Gradle project.
2. To build the project and run the tests use `test` task on the Gradle tool window 
(`View | Tool Windows | Gradle`). 

Here https://www.jetbrains.com/help/idea/gradle.html#gradle_tasks you can read 
how to run Gradle task from the Gradle toolbar in IntelliJ IDEA.

##### Working with the commandline

You can also build the project and run all tests in the terminal:
```
./gradlew test
```
But since running all the tests tend to take longer and the output can be
cluttered, it's more ideal to run selected tests only:
```
$ ./gradlew test --tests i_*          # run tests in part 1
$ ./gradlew test --tests ii_*         # run tests in part 2
$ ./gradlew test --tests ii_*22*      # run test number 22 in part 2
```

#### How the tasks are organized
 
You have 42 tasks to do. 
Each task lives in its own function: from `task0` to `task41`.
For each task, there is an associated unit test that checks your solution.
 
You may navigate to the corresponding test automatically when you read the task.
Open the source file with the task and use the action `Navigate -> Test` to open the test file. 
You may also use `Navigate -> Test Subject` for reversed navigation.

Individual tasks generally require you to change the function `taskX` by completely replacing the body of the function.
Your goal is to solve the problem and allow the associated unit test to pass. 
If you run the unit test for a task that is not correct, the unit test results will be displayed. 
If you have not yet made any changes to a task, the exception will be thrown and the task's TODO message will be displayed. 

In the first example, this means replacing the code

```kotlin
fun task0(): String {
    return todoTask0()
}
```

with the correct, meaningful code in order to solve the problem and allow the associated unit test to pass, such as:

```kotlin
fun task0() = "OK"
```
