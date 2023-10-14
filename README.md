# junit-notes
Notes for Java JUnit testing framework

# What is Unit Testing
- Unit testing is a software testing where individual units or components of a software are tested.
- Done during development phase (Coding part) of the project.

### Who writes Unit Test
- Developer will write the unit test cases.

### Why do we need Unit Testing
- To prevent and detect bugs immediately during the development phase so that we can product quality and production ready code.

### Purpose of Unit Testing
- To validate that each unit of the software code performs as expected.

### Proper way to write unit test
- Start in low level details. First write repository method and test it immediately. Second write service method and test it immediately, And Finally write controller method and test it immediately.

# What is Unit
-  Unit can be anything software code that needed to be tested like method, function, component, class, logic, or object.

# What is JUnit
- Open source, lightweight, easy to use, and powerful unit testing framework for java applications.
- Developed by Kent Beck and Erich Gamma back in 1997.
  
# [JUnit Annotations](https://github.com/Elleined/all-spring-boot-annotations)

# What is Assertions
- Static methods from jupyter API to validate the expected result and actual result of the test case.

### Assestions methods
```
assertEquals(T expected, U actual)
assertNotEquals(T expected, U actual)

assertTrue(boolean condition)
assertFalse(boolean condition)

assertNull(T object)
assertNotNull(T object)

assertArrayEquals(T expected, U actual)
```
