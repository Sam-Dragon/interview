# Programs based questions

1. Given a program, what will be the output of it.? <br>
   int x = 100 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;                          int x = 100 <br>
   a = ++x     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  a = x++ <br>
   print x, a  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;        print x, a <br><br>
A. x = 101,a = 101  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;                                                                           x = 101,a = 100

2. program to understand the output of String and String Buffer.? <br>
   String string = "hello"; <br>
   StringBuffer stringBuffer = new StringBuffer(input);
   
   string.concat("world"); <br>
   stringBuffer.concat("world"); <br>
   
   System.out.println(string + " >> " + stringBuffer); <br><br>
A. hello >> helloworld

3. program to update the value of class with non-private variable.? <br>
   class Example { <br>
       String name; <br>
       public void setName(String name) { <br>
         this.name = name; <br>
      } <br>
      public String getName() { <br>
         return name; <br>
      } <br>
   } <br>

   class Program { <br>
   public static void main(String[] args) { <br>
   Example e = new Example();  <br>
   e.name = "sam"; <br>
   // call any method  <br>
   e.setName("John");  <br>
   System.out.print(e.name); <br>
   }  <br>
   } <br><br>
A. John

4. program to update the value of class variable.? <br>
   class Example { <br>
       String name; <br>
       public Example(String name) { <br>
         this.name = name; <br>
      } <br>
      static void display() { <br>
         System.out.print(name)
      } <br>
   } <br>

   class Program { <br>
   public static void main(String[] args) { <br>
   Example e = new Example();  <br>
   e.display(); <br>
   }  <br>
   } <br><br>
A. Error: non-static to static access not possible
