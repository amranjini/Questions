# Questions

https://javahungry.blogspot.com/2020/05/java-8-coding-and-programming-interview-questions.html

Predicate program example
Optional Program example

Design pattern - Singleton (Double lock)

Find repeater character/ Unique character/ First repeated character/ Max repeated character in String ?

Recursion ( factorial / palindrome)

**************************************************************
Starter springboot jars ?

What happens when springboot application starts?

Spring profiles (Annotations,implementation in code)

Datasource (Db Connection)

Lifecycle of spring bean

Autowiring types

Scope of Bean - Default one

What is ternary operator? Give an example.
Ternary operator , also called conditional operator is used to decide which value to assign to a variable based on a Boolean value evaluation. It’s denoted as ?
------>  if rank is 1, status is assigned a value of “Done” else “Pending”.

Java 8 Features.

What are the advantages of using the Optional class?

Default keyowrd.

What’s the purpose of Static methods and static variables?

Ans: When there is a requirement to share a method or a variable between multiple objects of a class instead of creating separate copies for each object, we use static keyword to make a method or variable shared for all objects.




Given a list of integers, find the maximum value element present in it using Stream functions?
import java.util.*;
import java.util.stream.*;
public class JavaHungry {
    public static void main(String args[]) {
            List<Integer> myList = Arrays.asList(10,15,8,49,25,98,98,32,15);
            int max =  myList.stream()
                             .max(Integer::compare)
                             .get();
            System.out.println(max);                    
    }
}

How to find duplicate elements in a given integers list in java using Stream functions?

import java.util.*;
import java.util.stream.*;
public class JavaHungry {
    public static void main(String args[]) {
            List<Integer> myList = Arrays.asList(10,15,8,49,25,98,98,32,15);
            Set<Integer> set = new HashSet();
            myList.stream()
                  .filter(n -> !set.add(n))
                  .forEach(System.out::println);
    }

Given a list of employees, you need to filter all the employee whose age is greater than 20 and print the employee names.(Java 8 APIs only)
List<String> employeeFilteredList = employeeList.stream()
                  .filter(e->e.getAge()>20)
                  .map(Employee::getName)
                  .collect(Collectors.toList());

Difference between Intermediate and terminal operations in Stream?

*******************************************************************************

Write a function rotate(arr[], d, n) that rotates arr[] of size n by d elements.
Example :

Input :  arr[] = [1, 2, 3, 4, 5, 6, 7]
         d = 2
Output : arr[] = [3, 4, 5, 6, 7, 1, 2]

*************************************************************************

detecting cycles in a linked list data structue (when a node points back to a previous node)

Out of box thinking:

Middle Element in a LinkedList
Problem: Given a singly LinkedList, find its middle element. For example, if our input LinkedList is 1->2->3->4->5, then the output should be 3.

We can also use the two-pointer technique in other data-structures similar to arrays like a LinkedList:


freestar
public <T> T findMiddle(MyNode<T> head) {
    MyNode<T> slowPointer = head;
    MyNode<T> fastPointer = head;

    while (fastPointer.next != null && fastPointer.next.next != null) {
        fastPointer = fastPointer.next.next;
        slowPointer = slowPointer.next;
    }
    return slowPointer.data;
}
In this approach, we traverse the linked list using two pointers. One pointer is incremented by one while the other is incremented by two. When the fast pointer reaches the end, the slow pointer will be at the middle of the linked list. The time complexity of this solution is O(n), and space complexity is O(1).



Spring:

@Qualifier
Authentication mechanism

how do you conenct to database in spring in ur application?

What is Transaction Management in Spring? Explain the different types of Transaction Management.

Answer: Transaction is basically some operation performed on some data in the database. Transaction Management comes under the Relational Database management system and is used to ensure data ethics and consistency.
The core advantage of Transaction Management is that it supports declarative and programmatic Transaction Management and APIs like Hibernate, JTA, and JDBC by correct integration.
There are two types of Transaction Management, which are mentioned below:
Programmatic Transaction Management is used to help the transaction in terms of coding or scripting.
Declarative Transaction Management is used to isolate business code and transactions.

Deploymrent process.


SQL:
What Is a Self Join in SQL?
The self join, as its name implies, joins a table to itself. To use a self join, the table must contain a column (call it X) that acts as the primary key and a different column (call it Y) that stores values that can be matched up with the values in Column X. The values of Columns X and Y do not have to be the same for any given row, and the value in Column Y may even be null.

Group By in SQL is used to arrange similar data into group and Order By in SQL is is used to sort the data in the ascending or descending order.
    
    Collections:

Working of hashmap?
What is difference between Comparable and Comparator interface?
    
How to remove duplicates from ArrayList?
    
What is LinkedHashMap in Java?
    
How can we create a synchronized collection from given collection?
    
What is the difference between HashSet and TreeSet?
    
What is the difference between HashMap and ConcurrentHashMap?
    
How does HashMap handle collisions in java?
    
Difference between fail fast/fail safe collections
    
Questions on ConcurrentModificationException and CopyOnWriteArrayList.
    
What is CopyOnWriteArrayList, how it is different than ArrayList and Vector?
    
how does hashmap Use Hashcode and Equals Methods of Objects?
    
How Can You Use Comparable and Comparator Interfaces to Sort Collections?
    
different types of collections. Difference between set and list. When to use which.
    
Different SQL joins like inner, outer, left etc.

Topics like Rest APIs, Spring boot and java 8 features, annotations, rest template etc

how image is uploaded in spring.
    
how to store images in DB
    
self join.
    
How do you retrieve data from DB.

Junits:
mock
when condition
Injectmock

spy
Mockito //Endpoints testing
    
sql join / inverse join / JPA join types
    
store image in DB
    
add without using operator
    
Jpa annotation
    
spring mvc architecture

ircuit breakdown architecture.

deployment.

integration testing

spring profiles.

zuul
keycloak
eureka

why eureka server is required.

system down .
    
In System.out.println() ehat is system ,what is out,what is println?
If you want to print a name in java how do you print it?
can i overload a main method? If i want to overload a main method how should i do it?
Can i override a main method?If i want to override a main method how should i do it?
How you can sort a list in java?
Answer :by using compareto()
bubble sort


How do you handle production issues?


GCP:
Upload/Download using SSH.

scp <file to upload> <username>@<hostname>:<destination path>
ssh user1@server1 'command'
    
Collection (interface) -- stream/parallel stream
 
Related to Web services and its architecture
    
What is caching in hibernate?
    
What is an functional interface?
    
What is heap memory?

what is rest webservice?
what are the pre defined funtional interface in java


Spring actuator
Spring Starter
Spring boot advantages
fall back and error tolerance method in microservices

Reverse a List
Detect a loop in a list

    what is rest webservice?
what are the pre defined funtional interface in java


Spring actuator
Spring Starter
Spring boot advantages
fall back and error tolerance method in microservices

Reverse a List
Detect a loop in a list
    
    

select * from emp
where name like 'A%';

repate name and count

select count(emp_name) from emp group by name having count(emp_name)>1;

where s.id = d.id;
join student on  dept.id = student.id;

1. Question based on collection
2. comparable and comparator
3. Immutable
4. String handling
5. Difference between local and session storage
6. Difference between setTimeOut and setInterval
7.Javascript unit test framework
can class run without main method ?
collection ,spring hibernate use , difference between jsp servlet

It was nice, mainly interviewed on core part and frame work, 
in spring frame work they are asking about autowiring, 
interface vs abstract class , joins also discussed, polymarphisam types
Interview Questions
About static block, static method, the execution flow

OOPS concepts
Answer Question
Diff bw Hashmap and Concurrent Hashmap?
Answer Question
When will we get ConcurrentModificationException?
Answer Question
What are all the REST methods?
Answer Question
Explain about JSP modules.
Answer Question
Diff bw Comparator and Comparable interface with example.
Answer Question
Iterate a list using lambda expressions
Answer Question
Diff bw Abstract class and Interface?
Answer Question
Custom exception with example
Answer Question
Is custom exception is Runtime exception? and how? with example.
Answer Question
String, String builder, and String buffer

 How did you implement dependency injection.
 The first question in coding round was given a array return sum of maximum and minimum elements.
The second question in coding round was given a string remove duplicate elements from the string.
