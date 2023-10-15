# junit-mockito-notes
Notes for Java JUnit testing framework and Mockito

# What is Unit Testing
- Unit testing is a software testing where individual units or components of a software are tested.
- Done during development phase (Coding part) of the project.

### Who writes Unit Test
- Developer will write the unit test cases.

### Why do we need Unit Testing
- To prevent and detect bugs immediately during the development phase so that we can produce quality and production ready code.

### Purpose of Unit Testing
- To validate that each unit of the software code performs as expected.

### Proper way to write unit test
- Start in low level details. First write repository method and test it immediately. Second write service method and test it immediately, And Finally write controller method and test it immediately.

# What is Unit
-  Unit can be anything software code that needed to be tested like method, function, component, class, logic, or object.

# What is JUnit
- Open source, lightweight, easy to use, and powerful unit testing framework for java applications.
- Developed by Kent Beck and Erich Gamma back in 1997.

# JUnit Annotations
`@Test`: Mark the method or class to be JUnit test class.  

`@ParameterizedTest`: Used to have parameter in test method.  
  - `@ValueSource`
  - `MethodSource`
  - `CsvSource`
  - `CsvFileSource`
 
`@BeforeEach`: Execute before every test cases runs.  
`@BeforeAll`: Execute before any of the test case runs.  
 
`@AfterEach`: Execute after every test case runs.  
`@AfterAll`: Execute after all the test case runs.  

`@Disabled`: Skips method or class test case.  
`@Tag`: Used to have a group/ pack of test case.  
`@DisplayName`: Rename test case name in console.  

# What is Assertions
- Static methods from jupiter API to validate the expected result and actual result of the test case.

### Assestions methods
- These methods are available in org.junit.jupiter.Assertions.class
  
`assertEquals(T expected, U actual)`: Will pass if expected and actual are equals.  
  
`assertNotEquals(T expected, U actual)`: Will pass if expected and actual are not equals.   

`assertTrue(boolean condition)`: Will pass if condition returns true.   
`assertFalse(boolean condition)`: Will passs if conditiom returns false.  

`assertNull(T object)`: Will pass if object is null.    
`assertNotNull(T object)`: Will pass if object is not null.  

`assertArrayEquals(T expected, U actual)`: Will pass if expected and actual are equals.

`assertThrows(Class<T> expectedException, Executable executable, `: Will pass if execution
of supplied executable throws the expectedException.
`assertNotThrows(Class<T> expectedException, Executable executable)`: Will pass if execution of supplied executable will not throws expectedException.

`assertInstance(Class<T> expectedInstance, T object)`: Will pass if supplied object is instance of expectedInstance.

# What is Mocking
- Process of creating mock/dummy/substitute object that will be used instead of real object.

### Purpose of Mocking
- Used to achieve isolation/ dependent unit testing and focus only in the target unit test and not on external dependecies behavior.

### Benefits of Mockito
- No need to write your own mock object.
- Safe refactoring because mock object are created at runtime.
- Exception support.
- Annotation support.
- Method order support.

# When to use Mocking
- If you have a component, method, function, class, logic, or object has external depedencies.

# Why use mocking
- You will use mock/ dummy object for that so you can test individual component, method, function, class, logic, or object without interacting or calling the real object.

# Mockito methods
`doNothing()`: Used if method returns void.  
`thenReturn(R returnValue)`: Used to specify the return value of specified mock object method.  
`mock(T targetMockObject)`: Used to create substitute/ mock/ dummy object of the supplied tarketMockObject.  
`when(T methodToHaveMockBehavior)`: Used in conjunction with thenReturn the supplied methodToHaveMockBehavior will returns the thenReturn returnValue.  
`spy()`: Used for private and final methods, classes, and fields.  

# Helpful links
[Junit and Mocking by Ashok IT](https://m.youtube.com/watch?v=MEFoGR07qgw&t=11126s&pp=ygUOQXNob2sgaXQganVuaXQ%3D)
