# Gradle Java Project Template

Gradle expects to find your production source code under src/main/java and your test source code under src/test/java. In addition, any files under src/main/resources will be included in the JAR file as resources, and any files under src/test/resources will be included in the classpath used to run the tests. All output files are created under the build directory, with the JAR file ending up in the build/libs directory.

# Building the project

The Java plugin adds quite a few tasks to your project. However, there are only a handful of tasks that you will need to use to build the project. The most commonly used task is the build task, which does a full build of the project. When you run gradle build, Gradle will compile and test your code, and create a JAR file containing your main classes and resources:


## Output of gradle build
```
gradle build
:compileJava
:processResources
:classes
:jar
:assemble
:compileTestJava
:processTestResources
:testClasses
:test
:check
:build
BUILD SUCCESSFUL

Total time: 1 secs
Some other useful tasks are:
```

## clean
Deletes the build directory, removing all built files.

## assemble
Compiles and jars your code, but does not run the unit tests. Other plugins add more artifacts to this task. For example, if you use the War plugin, this task will also build the WAR file for your project.

## check
Compiles and tests your code. Other plugins add more checks to this task. For example, if you use the checkstyle plugin, this task will also run Checkstyle against your source code.
