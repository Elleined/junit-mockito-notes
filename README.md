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

`assertArrayEquals(T expected, U actual)`: Use for primitive data types.  Will pass if expected and actual are equals.

`assertIterableEquals(T expected, U actual)`: Use for collections. Will pass if expected and actual are deeply equals.

`assertThrows(Class<T> expectedException, Executable executable, `: Will pass if execution
of supplied executable throws the expectedException.  
`assertDoesNotThrows(Executable executable)`: Will pass if execution of supplied executable will not throw any type of exception.

`assertInstance(Class<T> expectedInstance, T object)`: Will pass if supplied object is instance of expectedInstance.

# What is Mocking
- Process of creating mock/dummy/substitute object that will be used instead of real object.
- Proxy of actual object.
  
### Purpose of Mocking
- Used to achieve isolation/ dependent unit testing and focus only in the target unit test and not on external dependecies behavior.
- No need of real database connection, properties file read, and file server read.

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

# Difference between mock, stub, and spy
- **Spy**: A spy is a Mockito feature that allows you to create a partial mock of a real object. When you spy on an object, it retains the original class's method behavior, and you can also stub specific methods if you want to change their behavior. It's a way to partially mock an object, meaning some methods are real (not stubbed), and others can be stubbed as needed.

- **Mock**: Is essentially a dummy or fake implementation of a class or interface. By default, when you create a mock using Mockito, all its methods return default values based on their return types (e.g., null, 0, false). You can then use when() to specify custom behavior for specific methods.

- **Stub**: Is the process of defining how a method should behave when it's called on a mock or spy object. It's akin to overriding a method's behavior for testing purposes.

##### Summary
- So, in summary, a spy retains the original class's behavior and allows you to selectively stub methods, while a mock is a complete dummy with default behaviors that you can customize using when(), and stubbing is the act of defining custom behavior for specific methods during testing. Your understanding is mostly accurate.

# Mockito methods
`mock(T mockObject)`: Used to create substitute/ mock/ dummy object of the supplied mockObject and the methods will return null/ true/ false/ 0 unless you stub the method.  
`when(mockObjectMethod)`: Used to stub or defined the behavior of mockObjectMethod and will returns the thenReturn returnValue.  

`thenReturn(R returnValue)`: Used to specify the return value of specified mockObjectMethod. 

`thenCallRealMethod()`: Used to call the real method behavior of stubbed method.  

`doNothing()`: Used if method returns void.  

`doAnswer(Invocation invocation)`: Commonly used in void methods but can also be used regardless of return type. Used when you want custom action when a specific method is called on a mock object. This is useful when you need to define behavior for a method that doesn't return a value but instead has some side effects like modifying some state or performing some action. invocation is functional interface.

`spy(T mockObject)`: Used to create a mock object that will also have the behavior of the real object but you can stub a specific method.  

`any()`: Used in replace of argument for you to call the method without the valid parameter. Usually used if parameter is not important for testing/

`verify(T mockObject)`: Used to check if method call is really invoked or called.  

`times(int expectedNumberOfTimesCalled)`: Used to check how many times that method is called.

`verifyNoInteractions(T targetMockObject)`: Used to verify that there are no any method is called in targetMockObject.

`verifyNoMoreInteractions(T targetMockObject)`: Used to check if there no more further interactions is called im targetMockObject.

`inOrder(T mockObject)`: Used to check the order of method call is correct or not.  

`atLeast(int minimumNumberOfInvocations)`: Used to verify that method called with minimum or atleast minimumNumberOfInvocations. 

`atMost(int maximumNumberOfInvocations)`: Used to verify that method is call with maximum or at most maximumNumberOfInvocations.  

###### do family methods doNothing(), doThrow(), doAnswer(), and doReturn() are used when you want to define a behavior when mock object method is called that doesn`t return any values or void methods.

###### then family methods thenReturn(), thenThrow(), and thenAnswer(), are used when you want to define the return value of mock object method is called.

# Mockito argument matchers
- Used for behavior verifications without needing to supply the real arguments and also if the argument are not that important for the test to work.

### Argument Matcher methods
`T any()`:  Any object.  
`T any(Class<T> clazz)`: Any object of given type.  

# Mockito Annotations
-**@Mock**: is also the same as mock(). 
-**@ExtendWith**: Always used together with @Mock to tell mockito to create a mock object using annotation.   
-**InjectMocks**: Always used together with @Mock to automatically injects the mocks dependencies.  
=**@MockBean**: Used in conjunction with @SpringBootTest used to replace the real object in application context with mock object.

# Helpful links
[Junit and Mocking by Ashok IT](https://m.youtube.com/watch?v=MEFoGR07qgw&t=11126s&pp=ygUOQXNob2sgaXQganVuaXQ%3D)

[Mockito by Dinesh Viryani](https://m.youtube.com/watch?v=RfErIPo94bc&t=9283s&pp=ygUHTW9ja2l0bw%3D%3D)
