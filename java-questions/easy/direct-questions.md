# Basic Interview Questions

1. Is java case-sensitive language ? <br>
A. No

2. What is unicode system ? why two bytes are allocated for each character ? <br>
A. It is system to encoding standard which gives unique number for each character and it requires only byte. <br>
Two bytes are allocated to support other languages
 
3. Can any class be specified as datatype ? For instance 'String' class <br>
A. Yes, all classes are specified as user defined datatype

4. Default datatype for non-fractional numbers & fractional ones ? <br>
A. non-factional - Integer, fractional - Double

5. How datatypes declaration transited from java-8 to java-11 and above ? <br>
A. 'var' keyword is used for representing the datatype reference which will decided at runtime

6. Can you explain where to use '==' vs .equals() method ? <br>
A. '==' is mainly used for address comparaision [literals]. useful in case of literals [numbers, characters] <br>
   &nbsp;&nbsp;&nbsp;.equals() is mainly used for value comparision [objects]. useful for any class objects [strings]

8. Can you explain with example between operators '|' and '||' ? <br>
A. true & false & true - false [third expression will also evaluated] <br>
   &nbsp;&nbsp;&nbsp; true && false && true - false [third expression is not evaluated due to short circuit]

9. What is ternary operator ? when to use ? any advantage ? <br>
A. Special operator to evaluate expression on condition to produce result [similiar to if/else] <br>
   **Advantage**: Increase code readability <br>
   Example: (a > b) ? a : b; 

10. What is instanceOf operator ? When to use ? any advantage ? <br>
A. instanceOf is special operator which checks object to specific class type <br>
   It is generally used when classes are under inheritance to prevent 'ClassCastException' <br>
   Example: obj instanceOf MyClass

11. What decides the execution flow of expression ? <br>
A. BODMAS rule

12. what are statements and loops ? <br>
A. Statements executes single execution code [top to bottom] but loops to recurrsively iterates the same execution code <br>
   &nbsp;&nbsp;&nbsp; Statements: if-else, switch, break, continue, return
   &nbsp;&nbsp;&nbsp;      Loops: do-while, while, for, for-each

13. Difference between while and do-while loop ? <br>
A. do-while executes once irrespective of condition where as while adheres to condition. <br>
while is considered as more efficient <br>
   Scenarios: do-while is useful for Menu-Driven Programs, password entry whereas while is Event Handling, Continous monitoring
   
14. How would you write infinite for-loop, while & do-while loop, where are they useful ? <br>
A. for (;;), while(true), do {} while(true) <br>
   Scenarios: In cases where you want to continuesly monitor something use while and do-while

15. What will happen if i run continues loop basically infinite loop ? <br>
A. Heap will run out of memory and out of memory error will come

16. In which cases for loop with indexes are useful ? <br>
A. Generally, when you want to toggle the data with indexes say alternate numbers, every three number of array etc..

17. Give me usecase where we use switch statement ? <br>
A. Switch cases are specifically useful when you want to pre-define values <br>
   &nbsp;&nbsp;&nbsp; Example: bank interest rates, transaction charges, currency values

18. Difference between return and system.exit() ? <br>
A. Generally, return just gracefully terminates the execution but still allows caller method to execute <br>
   &nbsp;&nbsp;&nbsp; whereas system.exit stops the execution either normal [System.exit(0)] or abnormal way [System.exit(1)]

19. In which case finally block executes, if the statements are called before them ? <br>
A. Even if method returns the values, still finally block will be called <br>
   &nbsp;&nbsp;&nbsp; whereas system.exit stops the execution and finally block wont be executed

20. How many ways can we terminate the program ? <br>
A. Currently, there are many ways we can terminate the program <br>
> Graceful way
  - return
  - System.exit(0)
> Abnormal way
  - System.exit(1)
  - Recurrsion
  - Deadlock
  - Sleep infinitely

21. Is String a class (OR) datatype ? <br>
A. String is a class and all classes are datatype [user-defined datatype]

22. What are the ways in which we you can create object ? <br>
A. It can created as literal, new object, new object(char array), new String(StringBuffer), new String(StringBuildr), toString()

23. How are string stored in below java-8 and after java-8 ? <br>
A. Java-8 before, string literal are stored in String Constant Pool inside Heap, string objects in heap <br>
   Java-8 after, string are stored inside Heap

24. If we dont reference a string, will its value change ? <br>
A. No, because they are immutable

25. What is the danger of String Constant Pool ? <br>
A. String Constant Pool data is not controlled by programmer and lives long. If hacker gain access, its dangerous

26. String class is immutable, are object too immutable ? <br>
A. Obviously, yes

27. What advantage do we get from String being immutable ? <br>
A. Sharing resource

28. How would you search a string from list ? <br>
A. Linear Search, Binary Search etc..

29. How would you modify the content of String ? <br>
A. Either using String Buffer / String Builder

30. Can you explain difference between String Builder and String Buffer ? <br>
A. String Builder - not synchronized, fast, single-threaded <br>
   String Buffer - synchronized, slow, multi-threaded

31. How to create String Buffer / String Builder ? <br>
A. It can be created with default constructor or constructor with String args

32. Does String Buffer / String Builder required reference for update ? <br>
A. No, they are mutable and internally updated

33. Difference between String and String Buffer / String Builder ? <br>
A. String are immutable objects whereas String Builder / String Buffer are mutable in nature <br>
String and StringBuffer are thread-safe where as StringBuilder is not <br>
String can be created many ways whereas String Buffer / String Builder are created using string only

34. What is array ? <br>
A. array is collection of elements

35. Will array contains same datatype element or different type ?  <br>
A. same datatype only

36. Where are arrays contents are stored ? <br>
A. Generally, arrays are stored on dynamic memory of heap

37. What are array types ? <br>
A. Arrays are categorized based on dimensions. 1D, 2D, 3D...

38. How many ways can you create arrays ? <br>
A. Arrays can be created using literal or array objects <br>

39. Can we interchange square brackets while declaring arrays ? <br>
A. Yes. int[] arr; (OR) int arr[];

40. What is type casting ? what is cast operator ? <br>
A. It is process of changing the datatype <br>
   cast operator is used for performing type casting

41. What is 2D array ? How to create it <br>
A. It is two dimensional array which is used storing the data <br>
   It is created same way as 1D array

42. What is Jagged Arrays ? Rules to create ? <br>
A. Arrays with variable size but works in multi-dimesional array <br>
   Rules: They are created with initial length

43. Can we change the contents of array even if is marked as final ? <br>
A. Yes, as they are mutable in nature

44. Can i create array in array ? <br>
A. Yes

45. Can we interchange static & void in main method ? <br>
A. Yes

46. Can we create main() method of my own ? <br>
A. Yes

47. Can we call main() method of class from another ? <br>
A. Yes

48. How are command-line args are read ? <br>
A. Strings

49. How are escape big string in command-line args ? <br>
A. Put it inside the quotes

50. Difference between Procedure based vs Object Oriented based approach ? <br>
A. Procedure based approach hard to understand, increases complexity <br>
   Object Oriented based approach opposite of it also it provides reusability

51. Difference between Object based vs Object Oriented based approach ? <br>
A. Object based approach similar to Object oriented but it doesnt support inheritance <br>
   Object based - javascript, vbscript <br>
   Object oriented - java, c++

52. Explain OOPS concepts ? Give some real world example ?
A.  Class/Objects <br>
    Encapsulation <br>
    Abstraction <br>
    Inheritance <br>
    Polymorphism <br>

53. Difference between class and object ? where are they stored ? Give Example. <br>
A.  Class defines model for objects and it physically doesnt not exists <br>
    whereas object is instance of class <br>
    Class is store in method area whereas objects are stored on heap memory of jvm <br>
    Example: Class - Car, Object - Maruti, Benz etc..

54. Explain Encapsulation ? Advantage ? Example <br>
A.  Encapsulation is process of wrapping up variables and methods and securing the data <br>
    variables are marked 'private' and methods as 'public' <br>
    Example - class <br>
    **Advantages**: Security, Reusability of variables, Validation can be placed
    
55. Explain Abstraction ? Advantage ? Example <br>
A.  Abstraction is process of hiding the details <br>
    create a method which expose only required details. Say employee basic info but database may contain additional info <br>
    Example - interface <br>
    **Advantages**: Security

56. Explain Inheritance ? Advantage ? Example <br>
A.  Inheritance is process of accessing the features <br>
    just extend to class or implement an interface <br>
    Example - King of the kingdom <br>
    **Advantages**: Reusability, Extensibility

57. Explain Polymorphism ? Advantage ? Example <br>
A.  Polymorphism is process which means many forms <br>
    method with different arguments or method with same arguments but different types <br>
    Example - Human Beings <br>
    **Advantages**: Flexibility

58. What is hashcode ? How is it useful ? algo used for designing it ? <br>
A. Hashcode is unique hexadecimal representation address of the object <br>
   It is used as key/Id in many cases <br>
   Algo used for hascode can use either HashMap, HashSet or HashTable

59. If i create custom class 'Test' with one variable 'name' & if i create object of it, what will be name value ? <br>
A. It will be 'null' [Defaults will be set for each datatype]

60. What are different memory sections in JVM where object content is stored.? <br> 
A. Stack - local variables, method calls, references to object on heap <br>
   Heap - stores objects and dynamic memory <br>
   Metaspace - metadata of the class

61. Are the object of custom class mutable in nature ? <br>
A. Yes, they are designed for that reason only

62. Can we share objects over the network ? <br>
A. Yes but it must be in the form of bytes [Serialization / Deserialization]

63. What are access specifiers ? Explain its types ? relevance of each of it ? <br>
A. As name suggests, access specifiers are used to provide access to its members & methods of the class <br>
   public - can be accessed from anywhere <br>
   private - can be accessed only within the class <br>
   default - can be accessed only within the package <br>
   **protected** - can be access within and outside package but must be under inheritance <br>

64. Explain constructors ? Types ? Invoked ? <br>
A.  They are special method without any return type and used for initializing the object <br>
    **Types**: default & parameterized constructor <br>
    They can be invoked either while creating the object using 'new' keyword <br>
    or it can be invoked via inheritance using 'extends' keyword

65. Advantages of contructors ? <br>
A.  Validation, Initialization

66. When is constructor called before or after creation of object? <br>
A. Basically, it is called during the process of creation

67. What is constructor overloading ? <br>
A. It is the process of creating method with same name but different arguments

68. What is constructor chaining ? <br>
A. It is the process of chaining the constructor on initilization generally via inheritance

69. Can we return from a constructor ? <br>
A. Yes, but without any value

70. Is it necessary to define no-args constructor when defining parameterized constructor ? <br>
A. Yes

71. 
