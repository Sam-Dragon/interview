# Star Questions

1. Can we access variables/methods outside the package without making it as public ? <br>
   A. Yes, using protected but condition is class must be inherited 

2. If all try / catch & finally throws exception, which exception message is printed to caller method ? <br>
   [Assume exception message contains text as try for try block and so on.] <br>
   A. It will show messages thrown from finally block

3. If functional interfaces can define static & default methods, does it mean abstract classes are deprecated? <br>
   A. No. <br>
   > Reasons
      - abstract class is a class, along with **instance** it can access all features of class such as clone, serilization etc..
      - abstract class variables can be private, protected, default where as interface remians **public** in nature [public static final] 
      - abstract class methods can be private, protected, default where as interface remians **public** in nature for default or static method

4. Can we pass any other custom interface similar to runnable interface to Thread class for instantiating ? <br>
   A. No, as thread class accepts Runnable interaface only but u can pass directly lamda expression for excecution
   
#. Difference b/w Out Of Memory error raised by pemgen or by heap space [Variation in JDK versions]
   A.
