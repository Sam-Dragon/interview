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
   **Advantage**: Increase code readability
   &nbsp;&nbsp;&nbsp;  (a > b) ? a : b; 

10. What is instanceOf operator ? When to use ? any advantage ? <br>
A. instanceOf is special operator which checks object to specific class type <br>
   It is generally used when classes are under inheritance to prevent 'ClassCastException'
   &nbsp;&nbsp;&nbsp;  obj instanceOf MyClass

11. what decides the execution flow of expression ?
A. BODMAS rule
