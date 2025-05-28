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
A. It can created as literal, new object, new object(char array), new String(StringBuffer), , new String(StringBuildr), toString()

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

28. How would you search a string from list ?
A. Linear Search, Binary Search etc.. 
