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

5. Can i create object of IOException ? <br>
A. Exception e = new IOException(); -- TRY

6. Output of the program ? <br>
   class Parent { <br>
       String name; <br>
       public Parent(String name) { <br>
         this.name = name; <br>
      } <br>
      void display() { <br>
         System.out.print(name)
      } <br>
   } <br>

   class Child extends Parent { <br>
       String name; <br>
       public Child(String name) { <br>
         this.name = name; <br>
      } <br>
      void display() { <br>
         System.out.print(name)
      } <br>
   } <br>

   class Program { <br>
   public static void main(String[] args) { <br>
   Parent e = (Child) new Parent();  <br>
   e.display(); <br>
   }  <br>
   } <br><br>
A. Class Cast Exception

7. Output of the program ? <br>
   class Program { <br>
    public static void main(String[] args) { <br>
      int prim_one = 10; <br>
      int prim_two = 10; <br>
      System.out.println(prim_one == prim_two); <br>
		
      Integer ref_one = 10; <br>
      Integer ref_two = 10; <br>
      System.out.println(ref_one == ref_two); <br>
        
      Integer new_ref_one = new Integer(10); <br>
      Integer new_ref_two = new Integer(10); <br>
      System.out.println(new_ref_one == new_ref_two); <br>
        
      // ADHOC Cases
      <br>
      System.out.println(prim_one == ref_one); <br>
      System.out.println(prim_one == new_ref_one); <br>
      
      System.out.println(ref_one == new_ref_one); <br>
    } <br>
} 
<br><br>
A. true <br>
true <br>
false <br>
true <br>
true <br>
false <br>
