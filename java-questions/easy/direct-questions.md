# Basic Interview Questions

<details>
<summary> GENERAL </summary>

1. Is java case-sensitive language ? <br>
A. No

2. Is java, pass by value or pass by reference ? can you prove it ? <br>
A. It is pass by value. Yes, use swapping program

3. What is the JVM execution flow ? <br>
A. Statics - initializers, variables, methods <br>
   instance - initializers, variables, methods <br>
   then local variables
   
4. How to compile and execute code in java ? <br>
A. use javac for code compilaion and conversion then java for running

5. Can we run any statement without main() ? <br>
A. Yes, static initilzers, static methods

6. what will happen if i call main() inside main() method ? <br>
A. It is recurrsively call itself and run out of memory. heap space

7. What is unicode system ? why two bytes are allocated for each character ? <br>
A. It is system to encoding standard which gives unique number for each character and it requires only byte. <br>
Two bytes are allocated to support other languages
 
8. Can any class be specified as datatype ? For instance 'String' class <br>
A. Yes, all classes are specified as user defined datatype

9. Default datatype for non-fractional numbers & fractional ones ? <br>
A. non-factional - Integer, fractional - Double

10. How datatypes declaration transited from java-8 to java-11 and above ? <br>
A. 'var' keyword is used for representing the datatype reference which will decided at runtime

11. Can you explain with example between operators '|' and '||' ? <br>
A. true & false & true - false [third expression will also evaluated] <br>
   &nbsp;&nbsp;&nbsp; true && false && true - false [third expression is not evaluated due to short circuit]

12. What is ternary operator ? when to use ? any advantage ? <br>
A. Special operator to evaluate expression on condition to produce result [similiar to if/else] <br>
   **Advantage**: Increase code readability <br>
   Example: (a > b) ? a : b; 

13. What is instanceOf operator ? When to use ? any advantage ? <br>
A. instanceOf is special operator which checks object to specific class type <br>
   It is generally used when classes are under inheritance to prevent 'ClassCastException' <br>
   Example: obj instanceOf MyClass

14. What decides the execution flow of expression ? <br>
A. BODMAS rule

15. Can we invoke garbage collector ? <br>
A.  Yes, but when it actually initiates process is not known <br>
    It can be done using System.gc() (OR) Runtime.getRuntime().gc()

16. What are packages and libraries ? <br>
A.  Combining group of similar functionality is called package <br>
    Combining group of similar packages is called library <br>

17. What is the use of import statement, if we can directly use at variable level ? <br>
A.  Its the central area of class where we can define once and use anywhere inside class

18. What is api document ? <br>
A.  It is a reference manual that has all of the information you need to work with the API

19. What is Classpath ? How do you define it ? How is it useful ? <br>
A.  The classpath is an environment variable that specifies the locations where the Java compiler and Java Virtual Machine (JVM) should search for class files and other resources

20. What is JAR file ? How is it different from zip file ? <br>
A.  Compressed version of the code which is readily executable

</details>
<details>
<summary> CONTROL STATEMENTS </summary>

1. what are statements and loops ? <br>
A. Statements executes single execution code [top to bottom] but loops to recurrsively iterates the same execution code <br>
   &nbsp;&nbsp;&nbsp; Statements: if-else, switch, break, continue, return
   &nbsp;&nbsp;&nbsp;      Loops: do-while, while, for, for-each

2. Difference between while and do-while loop ? <br>
A. do-while executes once irrespective of condition where as while adheres to condition. <br>
while is considered as more efficient <br>
   Scenarios: do-while is useful for Menu-Driven Programs, password entry whereas while is Event Handling, Continous monitoring
   
3. How would you write infinite for-loop, while & do-while loop, where are they useful ? <br>
A. for (;;), while(true), do {} while(true) <br>
   Scenarios: In cases where you want to continuesly monitor something use while and do-while

4. What will happen if i run continues loop basically infinite loop ? <br>
A. Heap will run out of memory and out of memory error will come

5. In which cases for loop with indexes are useful ? <br>
A. Generally, when you want to toggle the data with indexes say alternate numbers, every three number of array etc..

6. Give me usecase where we use switch statement ? <br>
A. Switch cases are specifically useful when you want to pre-define values <br>
   &nbsp;&nbsp;&nbsp; Example: bank interest rates, transaction charges, currency values

7. Difference between return and system.exit() ? <br>
A. Generally, return just gracefully terminates the execution but still allows caller method to execute <br>
   &nbsp;&nbsp;&nbsp; whereas system.exit stops the execution either normal [System.exit(0)] or abnormal way [System.exit(1)]

8. In which case finally block executes, if the statements are called before them ? <br>
A. Even if method returns the values, still finally block will be called <br>
   &nbsp;&nbsp;&nbsp; whereas system.exit stops the execution and finally block wont be executed

9. How many ways can we terminate the program ? <br>
A. Currently, there are many ways we can terminate the program <br>
> Graceful way
  - return
  - System.exit(0)
> Abnormal way
  - System.exit(1)
  - Recurrsion
  - Deadlock
  - Sleep infinitely

</details>
<details>
<summary> STRINGS </summary>

1. Is String a class (OR) datatype ? <br>
A. String is a class and all classes are datatype [user-defined datatype]

2. What are the ways in which we you can create string ? <br>
A. It can created as literal, new object, new object(char array), new String(StringBuffer), new String(StringBuildr), toString()

3. How are string stored in below java-8 and after java-8 ? <br>
A. Java-8 before, string literal are stored in String Constant Pool inside Heap, string objects in heap <br>
   Java-8 after, string are stored inside Heap

4. If we dont reference a string, will its value change ? <br>
A. No, because they are immutable

5. What is the danger of String Constant Pool ? <br>
A. String Constant Pool data is not controlled by programmer and lives long. If hacker gain access, its dangerous

6. String class is immutable, are object too immutable ? <br>
A. Obviously, yes

7. What advantage do we get from String being immutable ? <br>
A. Sharing resource

8. How would you search a string from list ? <br>
A. Linear Search, Binary Search etc..

9. How would you modify the content of String ? <br>
A. Either using String Buffer / String Builder

10. Can you explain difference between String Builder and String Buffer ? <br>
A.  String Builder - not synchronized, fast, single-threaded <br>
    String Buffer - synchronized, slow, multi-threaded

11. How to create String Buffer / String Builder ? <br>
A.  It can be created with default constructor or constructor with String args

12. Does String Buffer / String Builder required reference for update ? <br>
A.  No, they are mutable and internally updated

13. Difference between String and String Buffer / String Builder ? <br>
A.  String are immutable objects whereas String Builder / String Buffer are mutable in nature <br>
    String and StringBuffer are thread-safe where as StringBuilder is not <br>
    String can be created many ways whereas String Buffer / String Builder are created using string only

</details>
<details>
<summary> ARRAY </summary>

1. What is array ? <br>
A. array is collection of elements

2. Will array contains same datatype or different type elements ?  <br>
A. same datatype only

3. Where are arrays contents are stored ? <br>
A. Generally, arrays are stored on dynamic memory of heap

4. What are array types ? <br>
A. Arrays are categorized based on dimensions. 1D, 2D, 3D...

5. How many ways can you create arrays ? <br>
A. Arrays can be created using literal or array objects <br>

6. Can we interchange square brackets while declaring arrays ? <br>
A. Yes. int[] arr; (OR) int arr[];


7. What is 2D array ? How to create it <br>
A. It is two dimensional array which is used storing the data <br>
   It is created same way as 1D array

8. What is Jagged Arrays ? Rules to create ? <br>
A. Arrays with variable size but works in multi-dimesional array <br>
   Rules: They are created with initial length

9. Can we change the contents of array even if is marked as final ? <br>
A. Yes, as they are mutable in nature

10. Can i create array in array ? <br>
A.  Yes

11. Can we interchange static & void in main method ? <br>
A.  Yes

12. Can we create main() method of my own ? <br>
A.  Yes

13. Can we call main() method of class from another ? <br>
A.  Yes

14. How are command-line args are read ? <br>
A.  Strings

15. How are escape big string in command-line args ? <br>
A.  Put it inside the quotes

16. Difference between Procedure based vs Object Oriented based approach ? <br>
A.  Procedure based approach hard to understand, increases complexity <br>
    Object Oriented based approach opposite of it also it provides reusability

17. Difference between Object based vs Object Oriented based approach ? <br>
A.  Object based approach similar to Object oriented but it doesnt support inheritance <br>
    Object based - javascript, vbscript <br>
    Object oriented - java, c++

</details>
<details>
<summary> OOPS CONCEPTS </summary>

1. Explain OOPS concepts ? Give some real world example ?
A. Class/Objects <br>
   Encapsulation <br>
   Abstraction <br>
   Inheritance <br>
   Polymorphism <br>

2. Difference between class and object ? where are they stored ? Give Example. <br>
A. Class defines model for objects and it physically doesnt not exists <br>
   whereas object is instance of class <br>
   Class is store in method area whereas objects are stored on heap memory of jvm <br>
   Example: Class - Car, Object - Maruti, Benz etc..

3. Explain Encapsulation ? Advantage ? Example <br>
A. Encapsulation is process of wrapping up variables and methods and securing the data <br>
   variables are marked 'private' and methods as 'public' <br>
   Example - class <br>
   **Advantages**: Security, Reusability of variables, Validation can be placed
    
4. Explain Abstraction ? Advantage ? Example <br>
A. Abstraction is process of hiding the details <br>
   create a method which expose only required details. Say employee basic info but database may contain additional info <br>
   Example - interface <br>
   **Advantages**: Security

5. Explain Inheritance ? Advantage ? Example <br>
A. Inheritance is process of accessing the features <br>
   just extend to class or implement an interface <br>
   Example - King of the kingdom <br>
   **Advantages**: Reusability, Extensibility

6. Explain Polymorphism ? Advantage ? Example <br>
A. Polymorphism is process which means many forms <br>
   method with different arguments or method with same arguments but different types <br>
   Example - Human Beings <br>
   **Advantages**: Flexibility

</details>
<details>
<summary> CLASS </summary>

1. What is hashcode ? How is it useful ? algo used for designing it ? <br>
A. Hashcode is unique hexadecimal representation address of the object <br>
   It is used as key/Id in many cases <br>
   Algo used for hascode can use either HashMap, HashSet or HashTable

2. If i create custom class 'Test' with one variable 'name' & if i create object of it, what will be name value ? <br>
A. It will be 'null' [Defaults will be set for each datatype]

3. What are different memory sections in JVM where object content is stored.? <br> 
A. Stack - local variables, method calls, references to object on heap <br>
   Heap - stores objects and dynamic memory <br>
   Metaspace - metadata of the class

4. Are the object of custom class mutable in nature ? <br>
A. Yes, they are designed for that reason only

5. Can we share objects over the network ? <br>
A. Yes but it must be in the form of bytes [Serialization / Deserialization]

6. What are access specifiers ? Explain its types ? relevance of each of it ? <br>
A. As name suggests, access specifiers are used to provide access to its members & methods of the class <br>
   public - can be accessed from anywhere <br>
   private - can be accessed only within the class <br>
   default - can be accessed only within the package <br>
   **protected** - can be access within and outside package but must be under inheritance <br>

7. Explain constructors ? Types ? Invoked ? <br>
A. They are special method without any return type and used for initializing the object <br>
   **Types**: default & parameterized constructor <br>
   They can be invoked either while creating the object using 'new' keyword <br>
   or it can be invoked via inheritance using 'extends' keyword

8. Advantages of contructors ? <br>
A. Validation, Initialization

9. When is constructor called before or after creation of object? <br>
A. Basically, it is called during the process of creation

10. What is constructor overloading ? <br>
A.  It is the process of creating method with same name but different arguments

11. What is constructor chaining ? <br>
A.  It is the process of chaining the constructor on initilization generally via inheritance

12. Can we return from a constructor ? <br>
A.  Yes, but without any value

13. Is it necessary to define no-args constructor when defining parameterized constructor ? <br>
A.  Yes

14. Difference between default and parameterized constructor ? <br>
A.  default constructor - automatically added by jvm, no args, always one construtor, sets defaults <br>
    parameterzied constructor - must be explicitly defined, some args, multiple constructors, sets provided values <br>

15. Difference between default and no-args constructor ? <br>
A.  default constructor - automatically added by jvm <br>
    no-args constructor - must be explicitly defined, generally used in conjunction with parameterized constructor <br>

16. Difference between constructor and method ? <br>
A.  Constructor - automatically added by jvm / explictly added, used during object construction, same name as class, no return type, no concept of static / non-static<br>
    Method - must be explicitly defined, used after object is constructed, name can be same name or different from class, it can return values, can be static/non-static in nature <br>
  
</details>

<details>
<summary> OBJECTS </summary>

1. Who is the parent of all class ? <br>
A. Object class

2. Important Methods of object class ? <br>
A. equals() - used for matching the content of objects <br>
   hashcode() - generated unique hexadecimal number as reference<br>
   wait() - used for locking the object till it is unlocked by nofity() or notifyAll() <br>
   notify() - used for unlocking the object by sending signal to object <br>
   notifyAll() - used for unlocking the objects by sending signal to objects  <br>
   clone() - used for cloning the objects <br>
   finalize - used for garbage collection <br>
   toString() - convert object to string <br>

3. How many ways can we create an object ? <br>
A. It can be done in following ways
   - Using 'new' keyword
   - Factory classes
   - Cloning
   - Reflection
   - Class.forName()

4. What is Cloning ? How is it useful ? Types ? <br>
A. It the process of creating a new object by copying contents from another object <br>
   It gives resuability of object & reduces developer effort <br>
   Types: Shallow & Deep Copy

6. Difference between shallow and deep copy cloning ? <br>
A. shallow copy is the process of cloning the object where modifications are accepted between cloned and actual object. <br>
   whereas it is opposite for deep copy
   shallow copy uses default clone() method whereas for deep copy we need custom implementation

7. Tell me the contract between hashcode() and equals() method ? <br>
A. If two objects are equal through equals() method, then there hashcode must be same <br>
   If two objects are not equal through equals() method, then there hashcode can be same or different <br>

8. When does hash collision occur ? Resolution ? <br>
A. Generally, when hashcode() method is not properly overridden (OR) same hash values generated for all objects <br>
   Make sure hashcode is properly overridden to produce unique keys

9. Can you explain where to use '==' vs .equals() method ? <br>
A. '==' is mainly used for address comparaision [literals]. useful in case of literals [numbers, characters] <br>
   &nbsp;&nbsp;&nbsp;.equals() is mainly used for value comparision [objects]. useful for any class objects [strings]

</details>

<details>
<summary> INPUT AND OUTPUT </summary>

1. Which class is used for input/output streams ? <br>
A. System.in, System.out, System.err

2. Do you know buffered reader, if yes, why it is used in conjunction with InputStream Reader/ Writer ? <br>
A. Basically, it buffers the input data for efficient reading / writing

3. How many ways can you read input from keyboard ? <br>
A. It can be done using InputStreamReader & Scanner

4. What kind of exception is throwing by Input / Output streams ? <br>
A. IOException - It is checked exception

5. How many ways can you read a character from keyboard ? <br>
A. It can be read using buffered reader or scanner <br>
   Buffered Reader - using read() or readLine().charAt(0) <br>
   Scanner - using next().charAt(0) or nextLine().charAt(0) <br>

6. What is the problem when we use read() followed by readLine().charAt(0) ? <br>
A. read() only takes single character and rest of the character will be pushed to readLine() which is incorrect <br>
   Solution - just use readLine().charAt(0) (OR) bufferedReader.skip(2)

7. What is the problem when we use next().charAt(0) followed by nextLine().charAt(0) ? <br>
A. same problem as read() and readLine() of buffer reader

8. How many ways can you read a characters (OR) string from keyboard ? <br>
A. It can be read using buffered reader or scanner <br>
   Buffered Reader - using readLine() <br>
   Scanner - using nextLine() <br>

9. How many ways can you read numbers from keyboard ? <br>
A. It can be read using buffered reader or scanner <br>
   Buffered Reader - using read() (OR) readLine() in conjuction with wrapper class parse methods <br>
   Scanner - using nextInt() (OR) nextFloat() (OR) nextDouble() and so on.. <br>

10. How many ways can we split string and read the inputs ? <br>
A.  It can be done using 'split()' method of String (OR) use StringTokenizer class

11. Difference between StringTokenizer and String.split() ? which is efficient <br>
A.  StringTokenizer - legacy class, less efficient for single delimiter, doesnt return empty tokens <br>
    split()         - method of string, highly efficient w.r.t delimiters, returns empty tokens

12. How can you format the string output ? <br>
A.  It can be done using String.format() (OR) System.out.printf() 

</details>
<details>
<summary> METHODS </summary>

1. what are instance methods ? How are they called ? where are they stored ? Example <br>
A. They are object methods which are called after object is created <br>
   They are called generally with instance only <br>
   They are stored in heap area of jvm
   Example: setters and getters

2. what are static methods ? How are they called ? where are they stored ? Example <br>
A. They are class methods which are called even before any object is created <br>
   They are called generally with Classname or even instance [interally it resovles to classname] <br>
   They are stored in method area of jvm
   Example: Class.forName("test"), Class.getInstance() etc. <br>

3. Can we access non-static variable in static method ? <br>
A. No

4. Can we access static variable in non-static method ? <br>
A. Yes

5. Where do we use local variables ? Advantage ? <br>
A. Any variables used inside method are local variables, very useful incase of threading 

6. What is shadowing ? <br>
A. It is the practice of using variables in overlapping scopes with the same name

7. Explain the relevance of 'this' ? <br>
A. It is used for referrning the object members. It can be constructor, variable and methods <br>
   It's scope applicable within the class [basically object]

8. Recurrsion ? Adv/disadv ? <br>
A. A function which calls itself <br>
   Adv - Fast execution, less code <br>
   Disadv - If not implemented successfully, it will result in out of memory error

9. What are factory methods ? pattern ? Adv/disadv ?
A. Method used for creating objects by providing class name. <br>
   It uses factory design pattern <br>
   It compares the classname and creates object with new instance <br>
   Adv: one place to create all objects

10. How to define varaible arguments to methods ? rules ? Example <br>
A.  To replace multiple overloaded methods we can use variable arguments <br>
    It can be defined with ... and must be the last argument of the method <br>
    Example: sum of 2'S, 3's, 4's numbers

11. If method return value, is it necessary to consume / read ? <br>
A.  Not necessary

</details>
<details>
<summary> INNER CLASS </summary>

1. What is object graph ? <br>
A. It is the representation of how objects are connected to each other

2. When should we use inner class ? what are adv ? <br>
A. In case we some implmentation to be secured, we can put it in inner class. <br>
   Example: interest of loans

3. Anonymous inner class vs inner class ? <br>
A. Inner classes with have name whereas anonymous wont.  

</details>
<details>
<summary> INHERITANCE </summary>

1. What is the parent of all class either via instance or inheritance way [super] ? <br>
A. Object class

2. Why java doesnt use much of interitance even when it provides reusability ? <br>
A. Code complexity, Readability 

3. Which keywords signifies the class / interface are in inheritance ? <br>
A. extends / implements at class / interface level and super in constructor level 

4. Where can we use 'super' of ? what all can it access ? <br>
A. super is used specially in case of inheritance, it can be access members and constructors

5. What is constructor chaining ? How does it works ? <br>
A. It is the process of chaining all the classes which are under inheritance and it works wth 'super' of call

6. Is there any access specifier designed for inheritance ? <br>
A. Yes, protected

7. Types of inheritance ? Which java supports ? <br>
A. single and multple. java supports single inheritance

8. what is multiple inheritance issue ? why java doesnt support ?
A. It is also called diamond problem of death. It causes confusion on which method to pick and execute <br>
   It add complexity and effects readability

9. Inside constructor, can we have super and this ? what rules are followed ? <br>
A. No, we cannot have both. Rule is to have only one of these and it must be first line of constructor

10. Can i prevent a class from creating object / preventing inheritance ? <br>
A.  Yes, if class has private constructor

</details>
<details>
<summary> POLYMORPHISM </summary>

1. Difference between coercion and conversion ? <br>
A. Automatic conversion between different datatype done by compiler is called coercion <br>
whereas explicit conversion of datatype done using cast operator by coder is called conversion

2. Explain polymorphism ? Types ? Example ? <br>
A. Polymorphism - many forms, variables and methods acts different on different methods <br>
   Types - static and dynamic <br>
   static - The process in which compiler knows the method to execute at compile time [Method Overloading]. <br>
   Example: Fees of bank <br>
   dynamic - The process in which compiler doesnt know the method to execute at compile time,  <br>
   hence it decided at runtime by jvm based on object [Method Overriding]. <br>
   Example - Interest of bank

4. Explain Method Overloading ? Usage ? Example ? <br>
A. It is the process in which multiple methods with same class name but different method signatures <br>
   It may vary by number of args, order of args or datatype of args <br>
   It is mainly used with in the class and used for enhancing the functionality <br>
   Example: skills improvement by employee

5. Explain Method Overriding ? Usage ? Example ? <br>
A. It is the process in which multiple classes with same method name and same method signatures ? <br>
   It must have exact same method signature and is applicable via inheritance <br>
   It is mainly used with in the class and used for enhancing the functionality <br>
   Example: learning different language

6. What can we implement with polymorphism either with static (OR) final (OR) private methods ? <br>
A. Only method overloading 

7. How to make a class immutable ? Adv/dis <br>
A. Make class as final, variable as private and instantitate with constructor and expose getter methods <br>
   throw exception from clone and collections must be copied and then sent <br>
   Adv - security, sharable

</details>
<details>
<summary> ABSTRACT CLASS </summary>

1. Can you explain where can we use abstract class ? Example ? <br>
A. It must be used where new features needs to be added keeping other features intact <br>
   Example: Banking interest on loans

2. Is there any memory allocated for abstract class ? <br>
A. No

3. Can i mark class as 'abstract' even if it doesnt contain abstract methods ? <br>
A. Yes

4. Lets say i create abstract method in concrete class, what changes do i need to make ? <br>
A. Mark the class as abstract

5. Can i create object of abstract class ? <br>
A. No, but it can be used along as anonymous object

6. If i cannot create instance of abstract class, can i access instance methods of it ? <br>
A. Yes, it is possible via Inheritance

7. Can i create protected variable inside abstract class ? <br>
A. Yes, it works well specially it class is accessed via inheritance

8. Why abstract and final doesnt work together ? <br>
A. Abstract requires inheritance whereas final opposes inheritance. Both are opposite in nature

</details>
<details>
<summary> INTERFACES </summary>

1. In case of interface, why methods are public abstract and variables are public static final ? <br>
A. Interface were designed to provide the methods on 'what to do' so methods are abstract in nature <br>
   whereas variables as constants because there is no object so instance variables are eliminated, <br>
   so it can be only accessed statically but things are different in java-8 and above

2. What are marker interface ? what is the use ? Example ? <br>
A. Interfaces with no abstract methods. <br>
   They are useful in specifying compiler that this functionality is applicable <br>
   Example: Clonable, Serializable [But to implement we need to override object methods like clone and serial id]

3. What are functional interface ? what is the use ? Example ? <br> 
A. Interface with single abstract method. <br>
   They are useful in single functionality. It slightly differs in java-8 <br> 
   Example: Runnable, Callable, Comparator, Comparable etc..

4. Can we create object of interface ? <br>
A. No, but it can be done via annonymous inner class

5. What problems is there w.r.t inheritance ? <br>
A. Multiple inheritance

6. How is multiple inheritance resolved ? <br>
A. Interfaces, as they dont provide implementation

7. How is achieve callbacks in java ? <br>
A. Interfaces

8. Difference between classes and interfaces ? <br>
A. classes works both with instance and inheritence way where as interfaces works in inheritance way <br>
   class can extend only one class but multiple interfaces whereas interfaces can extend multiple interfaces <br>
   classes are used to specify 'how to do' whereas interfaces are used to specify 'what to do' <br>
   classes can specify all kinds of methods and variables where as interfaces can only specify methods as abstract
   and variables as constants

9. Can we create a class inside interface ? <br>
A. Yes

10. Can we pass interface reference in methods ? which object does it hold ? <br>
A. Yes, whichever is assigned to it before method call

11. How are interfaces stored after compilation ? <br>
A.  They are stored as .class file only

</details>
<details>
<summary> EXCEPTION </summary>

1. What are Exceptions ? How do you handle it ? <br>
A. Exceptions are abnormal conditions which alters the flow of execution. <br>
   It can be handled with try-catch-finally

2. Difference between compile time vs runtime exceptions ?
A. Exceptions managed by compiler are compile time exception <br>
   whereas exception managed by jvm is called runtime exceptions <br>
   compile time exceptions are enforces method to handle either by try-catch or by throwing <br>
   No such rules for runtime exceptions

3. Difference between error and exceptions <br>
A. Error are irrecoverable conditions and must not be handled. Example: OutOfMemoryError, StackOverflowError <br>
   whereas exceptions are recoverable and must be handled. Example: IOException, NullPointerException <br>

4. Can we handle errors ? If yes, why dont we handle ?
A. Yes, we can but not recommended. <br>
   They are not handled because they are system related issues not program related

5. Which the parent class of all exceptions ? parent of Throwable ? <br>
A. Parent of all exception class is '**Throwable**', parent of throwable is '**Object**' class

6. How do you perform exception handling ? <br>
A. It is generally done using try-catch-finally

7. In case we dont handle exception, how does main method display exception occurred ? <br>
A. Every main method inheritly has exception handling done by JVM. JVM manages exception objects

8. Can we write single catch block and handle multiple exceptions ? <br>
A. Yes, using pipe (|) operator

9. Can we write try without catch block ? <br>
A. Yes, either with finally or use try-with-resources

10. In case developer doesnt want to handle exception, what can he do ? <br>
A.  We can throw the exception mainly checked ones. [We can even throw unchecked exceptions]

11. What are the steps to create custom exceptions ? <br>
A.  Extending to the Exception class <br>
    specify the constructors with arguments else we can't use them

12. Can we throw an exception either thrown from method or create new one ?
A.  Yes, we can throw any exception using 'throw' clause

13. Can we rethrow an exception ? if Yes, what is adv / disadv ? <br>
A.  Yes, but not useful 

14. Can you explain rules for defining the exceptions ?
A.  Make sure all custom exceptions derive from Exceptions class <br>
    Order of exceptions must be from low to high <br>
    
</details>
<details>
<summary>TYPE CASTING</summary>

1. What is type casting ? what is cast operator ? <br>
A. It is process of changing the datatype <br>
   cast operator is used for performing type casting

2. Where can i use type casting ? <br>
A. It is generally used from coverting the dataypes between primitive and reference types

3. What are different types of datatypes ? <br>
A. Primitive and Reference datatypes

4. What is widening and Narrowing ? Example <br>
A. Widening is the process of promoting the object to higher types & is done by compiler. Example - int i = 100;
   Narrowing is the process of demoting the object to lower types & is done by user explicitly. Example - int i = (int) 100.12;

5. What is implicit vs explicit casting ? <br>
A. Automatic casting done by compiler is called implicit casting <br>
   Explicit casting done by the user is called explicit casting <br>
   Explicit casting is error prone where as implicit is not

6. How do you perform primitive casting ? <br>
A. Casting which is between the primitives and its classes

7. How do you perform reference casting ? <br>
A. Casting which is between the classes which are under inheritance

8. What is generalization vs specialization ? <br>
A. Generalization is the process of promoting the classes to higher types <br>
   specialization is the process of promoting the classes to lower types providiing specific functionality

9. Where does narrowing fail ? <br>
A. Narrowing fails in case both reference and object are of parent type and then you demote to subtype

</details>

<details>
<summary> GENERICS </summary>

1. What do you understand by term 'generics' ? where all can we apply ? <br>
A. generics meaning support all types. It is the process of making the class or variable or method, type-safe in nature <br>
   It can be applied on interface, class, method or variable

2. What is generic class / generic method / generic interface.? Explain with example.? <br>
A. Class / methods / interface with support all datatypes except primitives. Make sure they are type-safe <br>
   HumanBeing is generic class and each human becomes specific version
   
3. What is generic type.? <br>
A. It represents a class or interface that is type-safe. It can act upon any datatype

4. What is Erasure.? Any example <br>
A. Creating non-generic version of generic type by java compiler

5. Can we create object of generic class.? <br>
A. No, Generic object creation is not allowed

6. How can generics be applied in java objects.? <br>
A. It is possible because generic types are defined as subtype of object class

7. Any limitations of generic been applied in objects ? <br>
A. Yes, primitives are not supported  

</details>

<details>
<summary> WRAPPER CLASSES </summary>

1. What are wrapper class ? Explaing with usecase ? <br>
A. The classes created for coverting primitives to objects <br>
   They are part of java.lang package <br>
   They are very useful as java deals with objects and it is required while transporting data over network 

2. Are wrapper classes final by nature ? <br>
A. Yes

3. Explain about primitive types and its counter wrapper classes ? <br>
A. byte -> Byte, short -> Short, int -> Integer, long -> Long <br>
   float -> Float, double -> Double <br>
   char -> Chracter <br>
   boolean -> Boolean <br>

4. Which is the parent of all the number classes ? <br>
A. Number class [abstract class]

5. What is Number class ? Tell about its methods ? <br>
A. In order to represent numbers including fractions, number class was created <br>
   Methods <br>
   byteValue(), intValue(), shortValue(), longValue(), floatValue(), doubleValue()

6. Which is better to use for API models ? primitives or wrapper class ? <br>
A. For Api Models, its always good to use wrapper classes as primitives cannot be assigned to missing value

7. What is Character class ? Tell me about the methods ? <br>
A. The counter part for primitive type character <br>
   Methods <br>
   charValue(), compareTo(Character obj), toString(), valueOf(char ch) <br>
   isDigit(char ch), isLetter(char ch), isDigitOrLetter(char ch), isSpaceBar(char ch), isWhiteSpace(char ch),
   isUpperCase(char ch), isLowerCase(char ch) <br>
   toUpperCase(char ch), toLowerCase(char ch)

8. How to convert wrapper class object back to primitive type ? <br>
A. If String, convert using parseXXX method and if number, use XXXValue <br>
   XXX -> can be any primitive type

9. Which wrapper class has only one constructor ? <br>
A. Character Class

10. What are the problems with character class ? <br>
A.  It can be assigned to both character or its associated number. while converting this can create issues

11. What is the relevance of Math class ? <br>
A.  All the mathematical operations are present here. use this as utility

12. What happens when we use Integer i = 10 ? Explain the process ? <br>
A.  When any int value is assigned to wrapper class. Internally it is converted to object using internal cache <br>
    Internal cache works well between byte range. If it goes beyond it, results wont be correct

</details>

<details>
<summary> THREADS </summary>

1. Tell me about theads ? where to use ? adv/dis ? <br>
A. It is seperate path of executing the group of statements <br>
   It is useful in UI responsiveness, web servers, database interaction, data processing <br>
   Advantage:  for faster execution, improving performance, effective utilization of resources, producer-consumer Problem
   Disadavantge: More memory, deadlocks, sync issues

2. Can you explain the Thread content when called using Thread.currentThread() ? <br>
A. It contains three main components. Thread contains [Thread Name, Thread Priority, Thread Group] <br>
   - Thread Name: Name of the thread, if not provided, system will assign it
   - Thread priority: Priority of thread for jvm to execute
   - Thread Group: Group in which threads are present, it can contain many threads

3. Which thread is run by default by java program or main function ? Explain properly ? <br>
A. Every program has a default thread called main thread which is managed by JVM <br>
   Main thread will have its own stack and local variables <br>
   It be specified like this [main, 5, main] --> Thread and group name will be main and priority will be 5

4. Difference between single tasking and multi tasking ?
A. single tasking is a process where it executes one task at a time and goes in sequencial manner <br>
   whereas multi tasking is a process where it executes multiple task at a time and goes in parallel manner <br>
   single tasking is time consuming and does not utilize system resources properly <br>
   whereas multi tasking is time efficient and utilize the system resources properly <br>
   
5. What is CPU intensive vs IO intensive Task ? what to use when ?
A. CPU Intensive Task: A task that requires a lot of computation and uses the CPU heavily. <br>
   Use Cases: Image/video processing, Scientific simulations, Cryptographic calculations, Machine learning model training,      Data compression/encryption

   IO Intensive Task: A task that spends more time waiting for input/output operations than doing computation
   Use Cases: Reading/writing files to disk, Accessing databases, Network communication (APIs, downloading files), Logging      or interacting with hardware

6. Difference between process and threads ? <br>
A. Process is an independent program in execution whereas Thread is a lightweight unit of a process <br>
   Process has its own memory space (heap, stack) whereas Thread shares memory with other threads in the same process <br>
   Process is isolated from other processes	whereas threads are Not isolated – threads can affect each other
   Process communication is Inter-process Communication (IPC), slower whereas threads uses shared memory – fast but risky (race conditions)
  Process Creation Overhead Higher (needs separate memory, resources) whereas threads overhead is Lower (shares context with parent process)
  Process crash affects only that process	whereas Thread crash can affect the whole process (all threads)
  Process run separate applications/tasks whereas Thread	run parts of the same task concurrently

7. How to create threads ? <br>
- It can be created in following ways
  - extends Thread class [NOT RECOMMENDED]
  - implements Runnable interface [RECOMMENDED]
  - implements Callable interface [RECOMMENDED]
  - Executor service [RECOMMENDED]

8. How to run a threads ? Can i run the thread using thread.run() ? <br>
A. It can be run using start() method of thread. <br>
   start() - It creates thread which has its own stack and has its own local variables.
   run() - must not be used as it execution runs in same thread

9. Can i start a thread again ? <br>
A. No, It will throw InterruptedException

10. Can i stop a thread ? <br>
A.  Yes, but not recommended [In case you want to stop, stop using flags not using Thread.stop()]

11. Thread vs Process ? Explain <br>
A.  Thread is used for performing a single task whereas process contains serveral tasks and needs serveral threads <br>
    Threads are lighweight in nature whereas processes are heavier as it requires more cpu and memory <br>
    Example: Process: Payment, Task: check payment mode, deduct from bank account, credit to wallet, process order

12. What exceptions does thread throw ? Do we need to handle ? <br>
A.  Interrupted Exception is thrown by thread methods and yes we need to handle for normal termination

13. Where all memory will be allocated once thread is created ? <br>
A.  Heap, Method Area, Stack

14. Are thread synchronous or Asynchronous in nature ? <br> 
A.  Asynchronous

15. Difference between sleep() and wait() method ? <br>
A.  sleep() is method of Thread class whereas wait() is the method of object class <br>
    sleep() method doesnt required object it just blocks thread whereas wait() requires object hence it needs sync block or method.
    sleep() method doesnt release the lock which is aquired whereas wait() releases the lock if aquired <br>
    sleep() is static method whereas wait() is non-static method <br>
    sleep() pauses for a specific duration whereas wait() waits for notification <br>
    sleep() doesnt required wakeup methods its time based whereas wait() requires wakeup using notify(), notifyAll() <br>
    sleep() is useful in polling or retry logic whereas wait() is useful mainly for Producer-Consumer problem

16. What is race condition ? How does it occur with scenario ?
A.  It is the problem which occurs when multiple threads updates the same shared resource <br>
    Scenario: In bank account, if we perform operations such as deposit or withdrawal at a time, this problem can occur

17. Explain Synchronization process.? Explain with example.? Adv/Disadv
A.  Synchronization in Java is a mechanism used to control the access of multiple threads to shared resources. <br>
    Adv: It sequencializes the thread aquiring shared resource preventing race condition
    DisAdv: Slowers the performance, consumes more memory <br>
    Example: Any distributions like ticket counter, bus counter

18. How many ways can we perform synchronizaton process ? <br>
A.  It can be using sync block (OR) sync method

19. When to use wait(), notify() and notifyAll()
A.  Mainly used for Thread Communication. Must be used in sync block/method <br>
    Example: producer-consumer problem etc..

20. What is mutually exclusive lock ?
A.  When one thread holds the lock and other thread wants to aquire it, they are mutually exclusive in nature. <br>
    (Or) The object is locked mutually on threads. It requires synchronization
     
21. What is deadlock ? How does it occur ? Preventition steps ? Disadvantages ? <br>
A.  Deadlock is a process in which threads lock each other waiting forever, it happens in mutli-threaded enviroment while        threads works with resource with sync block or methods <br>
    It can occur if the two threads waits for each other to release the resource <br>
    Steps: <br>
        - Its generally happens through bad design, it can be corrected at code level <br>
        - Avoid nested locks, unncessary locks & also from thread.join() method <br>
    Disadvantages: <br>
       - It can run the memory out
       - system will hang and slowness can be observerd
 
22. In multi-threaded environment, how will you manipulate strings ?
A.  Use StringBuffer

23. What is deamon threads ? use-case ? how to check if thread is deamon ? <br>
A.  Threads which are not created by user and runs forever. [system threads] <br>
    They are useful for running background process. lets say - updating service package, database service <br>
    isDeamon() of thread method helps in indicating whether it is normal or deamon thread

24. What is Thread group ? Adv/Dis ? How is it represented ?
A.  It is a group of threads where each thread works independently per task and will consume more resources <br>
    It is generally represent with Thread. Thread.currentThread() gives the information <br>
    Adv: <br>
       - We can group different threads into the group. Example: project team <br>
    DisAdv: <br>
       - It may overload consuming more resources and system crashes
    
25. What is Thread Pools ? Adv/Dis ? Use-case ? <br>
A.  It is concept of providing readily available threads for the programmer to use. Internally manages thread communication, effective memory utilization<br>
    Adv: <br>
       - Ready made threads are provided, user just need to use it
       - No need to manage the cycle of threads
   DisAdv: <br>
      - It is possible to have deadlocks
      - Internal issue w.r.t threads are undetermined
   Use-Case:
      - Programmers tend to use ready-made framework such as executer service which manages thread of pools <br>
        It is useful in executing any functionality which is background process [Animation, Gaming]

26. Tell me about different types of thread pools ? <br>
A.  Single Thread Pool - It just contains only one thread & executes task sequencially. Example - Any Program <br>
    Single Scheduled Thread Pool - It contains only one Thread & useful for scheduling **future** tasks. Example - Payment <br>
    Fixed Thread Pool - It contains fixed number of threads and executes tasks parallely<br>
    Cached Thread Pool - It contains multiple threads provided and executes tasks and waits till 1min before thrashing and                            then new threads will be created <br>
    Scheduled Thread Pool - It contains multiple threads provided and executes **future** tasks and waits till 1min before thrashing and then new threads will be created <br>

27. What is Executor Service ? How is it useful ? <br>
A.  It is a framework designed for providing worker threads. It uses **Exeutors** class to create thread pool <br>
    It is useful because it manages the lifecycle of threads <br>

28. What is CPU vs Memeory Intensive Tasks ?
A.  The task which requires more processing power then it is called cpu intensive task. <br>
    Use Process Based Multi=tasking <br>
    Ex: Math calculation
    The task which requires more memory power then it is called memory intensive task. <br>
    Use Thread Based Multi=tasking <br>
    Ex: Games, Animation 

29. Explain Thread Life Cycle ?
A.  New - When the thread is created but not running state [start() method] <br>
    Runnable - When the thread is ready to run [yeild(), notify(), notifyAll() method] <br>
    Not-Runnable - When the thread is blocked/waited [sleep(), wait(), IO Block method] <br>
    Terminate - When the thread is killed [stop() method (OR) run method finishes] <br>

30. Types of locks in threads ? Example <br>
A.  **Intrinsic Locks** - Implicit locks which works with single thread under synchronization <br>
    - Object level lock : lock which works on object instance <br>
    - Class level lock : lock which works on class instance <br>

    **Explicit Locks** - Explicit locks which doesnt need synchronization but is alternative to it
    - ReentrantLock : It provides features like fairness policies, interruptible lock acquisition, and the ability to try                         acquiring a lock with a timeout. It is "reentrant" meaning the thread holding the lock can re-acquire                       it without causing a deadlock.
    - ReadWriteLock : It interface provides separate locks for reading and writing. Multiple threads can acquire the read                         lock concurrently but only one thread can aquire write lock
    - StampedLock   : Introduced in Java 8, StampedLock offers three modes: writing, reading, and optimistic reading. It                          provides a more fine-grained control over locking and can offer better performance in read-heavy                            scenarios compared to ReadWriteLock by allowing optimistic reads that don't block writers<br>

    **Synchronization Aids** - While not strictly "locks" in the same sense as the above, these mechanisms also help manage                                concurrency
    - Semaphore: A signaling mechanism that controls access to a limited number of resources. It maintains a count of                        available permits, and threads acquire a permit to access the resource and release it when done.
    - CountDownLatch: A synchronization aid that allows one or more threads to wait until a set of operations being                               performed in other threads completes. It works like a gate that remains closed until a counter                              reaches zero.
    - Cyclic Barrier: A synchronization aid that allows one or more threads to wait until a set of operations being                               performed in other threads completes. similar to countdown latch but threads are reusable.

</details>
