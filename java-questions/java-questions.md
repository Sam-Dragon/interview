# Interesting Interview Questions

1. Can we pass String Builder to String Buffer or vice versa <br>
A. Yes

2. How would you access first string from string line input using BufferedReader <br>
A. using reader.readLine().split(" ")[0]; 

3. Can we throw error and catch it <br>
A. Yes, but it is not recommended

4. Do you catch runtime exceptions <br>
A. Yes, catch(Exception e) catches all exceptions

5. Can we make non functional interface point to lamda expression <br>
A. Yes, only if the interface has single abstract method and No, If interface contains more than one abstract method

6. Can we create custom interface similar to runnable interface and pass to thread class ? will it create new thread ? <br>
A. No. it will give Compiler error

7. Can same lamda be referred to multiple Functional interfaces <br>
A. Yes. unless it matches the method signature

8. how lamda gets memory from JVM for non-static & static variables ? <br>
A. using invoke dynamic and invoke static mechanisam

#. why lamda variables are final by nature?
A. 

#. Can we clone singleton class ? <br>
A. 

#. Can we serialize singleton class ? <br>
A. 

8. ConcurrentHashMap With example <br>
A. 

9. Difference between parallel stream and executor framework <br>
A.   

10. Comparable vs comparator ? <br>
A. Comparable interface is used for providing default sorting where as Comparator is used for custom sorting [Multiple sorting]
- Comparable interface requires current instance for comparision where as Comparator just requires any 2 instances
- Comparable interface overridden method is compareTo(this) where as Comparator method it is compare(i1, i2)
Ex. Collections.sort() --> Comparable, Comparator.comparing() --> Comparator

11. HashMap Internal Working ?
A. It is similar to map works on the logic of hashing
- Override equals and hashcode
- Bucket Concept & relate with equals and hashcode
- extends AbstractMap<K,V>
- implements Map<K,V> - Key/Value pair
  Cloneable - Cloning
  java.io.Serializable - Serilizing    

12. Treemap internal working
A. It is similar to map works on the logic of hashing
- Override equals and hashcode
- Bucket Concept & relate with equals and hashcode
- It implements the NavigableMap -> SortedMap -> comparator interface so ensure nulls are not allowed in keys for sorting
- extends AbstractMap<K,V>
- implements NavigableMap<K,V> - Sorting
  Cloneable - Cloning
  java.io.Serializable - Serilizing

13. Deep copy vs Shallow copy
A. shallow copy updates the contents of the collection passed where as deep copy creates a copy of collections and sends
 - deep copy requires extra space due to collection data storage where as shallow copy doesnt
 - deep copy is bit slower compared to shallow copy due to copy operation into collection 

15. 
