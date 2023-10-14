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
