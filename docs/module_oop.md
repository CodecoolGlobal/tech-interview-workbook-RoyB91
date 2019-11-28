# OOP questions

## Software design

### Error handling

#### What does 'fail fast' mean in terms of exception handling? Why is it a good practice?
>Fail fast means,  is to code your software such that, when there is a problem,
>the software fails as soon as and as visibly as possible,
>rather than trying to proceed in a possibly unstable state.

## Computer Science

### Data structures

#### How to find the middle element of singly linked list in O(n)?
>>Traverse linked list using two pointers. Move one pointer by one and other pointer by two. When the fast pointer reaches end slow pointer will reach middle of the linked list.
```java
class Node
{
  int data;
  Node next;

public Node getHead(){
  return this.head;
}

public int getMiddleElement(LinkedList list)
{
    return getMiddleElement(list.getHead());
}

private int getMiddleElement(Node n){
    Node slow = n;
    Node fast = n;

    while(fast!=null && fast.next!=null) {
        fast = fast.next.next;
        slow = slow.next;
    }
    return slow.data;
}


}
```
#### Given an array of integers going from 1 to 100 (both inclusive) there is a duplicated entry. How to find it?
>First option: Sort the array and traverse the array and check for duplicated entry.
```java
public int findDuplicate(int[] arr, int size) {
            for (i = 0; i < size; i++) { 
                for (j = i + 1; j < size; j++) { 
                    if (arr[i] == arr[j])  
                        return arr[i]; 
                } 
            } 
        }
```

#### What is a linked list? How to find if a linked list has a loop?
>Linked lists are basic data structures.
>You have to iterate through it with the next parameter.
>>The basic idea is that you can iterate through the list by checking to see if the list has a next parameter,
> like so: while (currentNode.next != null) { ... }.
 #### What is the Big O time complexity of the common operations in an ArrayList, LinkedList, HashMap? And of a bubble sort, quicksort, finding items in a Binary Search tree?
- ArrayList: O(1): access, search
                O(n): insertion, deletion
- LinkedList: O(1): add(E element), Iterator.remove(), ListIterator.add(E element) (insert/delete)
                 O(n): add(int index, E elem), get(int index), remove(int index) (access/search)
- HashMap: O(1) with high probability, (A hashmap operation is O(1), and depending on implementation Ω(∞), Ω(log N) or Ω(N).)
- Bubble Sort: O(n^2)
- Quicksort: O(n^2)
- Binary Search tree: average: Θ(log(n)), worst: O(n) for all 4 (access, search, insertion, deletion)
#### How does HashMap work?
>HashMap in Java works on hashing principle. It is a data structure which allows us to store object and retrieve it in constant time O(1) provided we know the key.
>>In hashing, hash functions are used to link key and value in HashMap.

#### Why is it important for keys in a map to have an immutable type? (Consider String for example.)
>If immutable, the object's hashcode wont change and it allows caching the hashcode of different keys which makes the overall retrieval process very fast.
>Also for mutable objects ,the hashCode() might be dependent on fields that could change,
>if this happens you wont be able to find the key (and its value) in the HashMap since hashCode() returns different value.

### Other

#### What is a garbage collector, in a nutshell?
>Garbage collector reclaims objects that are no longer being used, clears their memory, and keeps the memory available for future allocations.
>This is done via bookkeeping the references to the objects. Any unreferenced object is a garbage and will be collected.

## Programming paradigms

### Procedural

#### What is casting? What is the difference between up vs downcasting?
Type casting is when you assign a value of one primitive data type to another type.
 Up (or widening) casting is done automatically when passing a smaller size type to a larger size type: 

    byte -> short -> char -> int -> long -> float -> double
    int myInt = 9;
    double myDouble = myInt; 

 Down (or narrowing) casting must be done manually by placing the type in parentheses in front of the value: 

    double -> float -> long -> int -> char -> short -> byte
    double myDouble = 9.78;
    int myInt = (int) myDouble;
#### Which order should we catch the exceptions? Why?
>Catch the most specific first and then the most generic,
as whatever matches first, gets executed. The most generic will always catch.

### Object-oriented

#### What is a class?
 A class is a blueprint or prototype from which objects are created.
 It describes the behavior/state that the object of its type supports.
#### What is an object?
 An object is a software bundle of related state and behavior.
#### What is a constructor?
A constructor initializes an object when it is created.
#### Do we require parameter for constructors?
 No, it is optional. Java allows two types of constructors: No argument Constructors and Parameterized Constructors.
#### What is an interface?
An interface is a contract between a class and the outside world. When a class implements an interface,
it promises to provide the behavior published by that interface.
#### What are access modifiers?
Access modifiers in Java helps to restrict the scope of a class, constructor , variable , method or data member.
These are: public, default (or package-private), protected, and private.
#### What is data hiding?
Data hiding is a mechanism to hide information from the client. The information may be data or implementation or algorithm.
We achieve this using access modifiers.
#### Can a static method use non-static members?
A static method can access non-static methods and fields of any instance it knows of.
However, it cannot access anything non-static if it doesn't know which instance to operate on.
#### What is the difference between hiding a static method and overriding an instance method?
An overridden instance method makes the code in its super's method unavailable in the subclass. 
A static method cannot be overridden, only hidden, therefore accessing the super's code in the subclass is still possible.
#### Define the following terms: Instantiation, Attribute, Method
Instantiate: to create an object from its class using the 'new' keyword.
Attribute: attributes are variables within a class
Method: a method is a block of code which only runs when it is called.
#### Could we access a static variable (or method) from a non-static method? Why?
Yes, a non-static method can access a static variable or call a static method in Java, because of static members i.e. both static
variable and static methods belong to a class and can be called from anywhere, depending on their access modifiers.
#### Could we access a non-static variable (or method) from a static method? Why?
You can not access non static members inside static context. This would result in a compile time error, as static methods are bonded during compile time,
as opposed to binding of the non static method, which happens at runtime.
#### How many instances you have of a static variable of a given class?
Only one copy of static variables are created when a class is loaded; this is shared by all the different objects of a class.
#### Why is it not a good practice to write a lot of static methods?
Interfaces and abstract classes only define non-static methods. Static methods thus don't fit very well into inheritance.

Static methods do not have access to "super" (or "this"), which means that static methods cannot be overridden, only hidden.
#### What are the features of static attributes and static methods of a class? What are the benefits, when to use them?
 They belong to the class, and not to the object(instance). They can be accessed directly by the class name and don’t need any object.
 Static variables are initialized only once, at the start of the execution. These variables will be initialized first, before the initialization of any instance variables.
 A single copy is shared by all instances of the class.
 A static method can access only static data. It can not access non-static data (instance variables). A static method can call only other static methods and can not call a non-static method from it. A static method cannot refer to "this" or "super" keywords in anyway.
#### What is the ‘this’ reference?
The 'this' keyword refers to the current object in a method or constructor.
#### What are base class, subclass and superclass?
Inheritance. A class that is derived from another class is called a subclass (also a derived class, extended class, or child class).
The class from which the subclass is derived is called a superclass (also a base class or a parent class).
#### Draw an object oriented family (as entities, with relations) on the whiteboard.
#### Difference between overloading and overriding?
Overload adds more functionality to an already existing method, overriding redefines the method functionality.
#### What are the Object Oriented Principles? Explain the concepts with realistic examples!
OO principles: encapsulation (data hiding), inheritance, polymorphism, abstraction
 - **encapsulation**:
    -    **Wrapping up data member and method together into a single unit (i.e. Class)**
    -   Also it is a language mechanism for **restricting access to some components**
    (this can be achieved by access modifiers like private,protected etc.)
 - **inheritance**:
    -   **Inheritances expresses “is-a” and/or “has-a” relationship between two objects.** 
    -   Inheritance can be defined as the process where one class acquires the properties (methods and fields) of another. 
    -   In Java, concept of “is-a” is based on class inheritance (using extends) or interface implementation (using implements).
 - **polymorphism**:
    -   **It means one name many forms. It is further of two types — static and dynamic.**
     -  **Static polymorphism** 
       is achieved using method *overloading* and **dynamic polymorphism** using method *overriding*. 
     -  It is closely related to inheritance. We can write a code that works on the superclass,
     and it will work with any subclass type as well.
 - **abstraction**:
    -   **Abstraction is the process of hiding the implementation details**.
     When we want to use another object, most of the time **we only need
     the information** on **what that object does instead of how it does it**.
    -   *In a way, one class should not know the inner details of another in order to use it, 
    just knowing the interfaces should be good enough.*
    
    -   is hiding the information or providing only necessary details to the client.
        
        e.g Car Brakes- You just know that pressing the pedals will stop the vehicle but you don't need to know how it works internally.
#### What is method overloading?
 A type of polymorphism. Method overloading means that there are several methods present,
   in a class having the same name but different types/order/number of parameters.(compile time (static)polymorphism)
#### What is method overriding?
A type of polymorphism. Method overriding means that a subclass has the same method as its super (same name, types/order/number of parameters),
 but with a different method body.(runtime polymorphism)
#### Explain how object oriented languages attempt to simplify memory management for Programmers.
The purpose of garbage collection is to identify and discard objects that are no longer needed by a program so that their resources can be reclaimed and reused.
A Java object is subject to garbage collection when it becomes unreachable to the program in which it is used.
#### Explain the “Single Responsibility” principle!
There should never be more than one reason for a class to change.   
#### What is an object oriented program? Explain, show.
Simply put, OOP focuses on the objects that developers want to manipulate rather than the logic required to manipulate them. This approach to programming is well-suited for programs that are large, complex and actively updated or maintained. Due to the organization of an object-oriented program, this method is also conducive to collaborative development where projects can be divided into groups.
 Additional benefits of OOP include code reusability, scalability  and efficiency
#### How do you make a class immutable? What do you need to watch out for?
 1. Declare the class as final so it can’t be extended.
 2. Make all fields private so that direct access is not allowed.
 3. Don’t provide setter methods for variables
 4. Make all mutable fields final so that it’s value can be assigned only once.
 5. Initialize all the fields via a constructor performing deep copy.
 6. Perform cloning of objects in the getter methods to return a copy rather than returning the actual object reference.
#### How many instances can be created for an abstract class?
None, an abstract class cannot be instantiated. (related:  anonymous subclasses)
#### Describe SOLID PRINCIPLES
-   **Single responsibility principle**
    -   A class should only have a single responsibility, that is, only changes to one part of the software's specification
        should be able to affect the specification of the class.
-   **Open-Closed Principle**
    -   You should be able to extend a class’s behavior, without modifying it.
        This principle is the foundation for building code that is maintainable and reusable.
        -   Open for extension
            This ensures that the class behavior can be extended. 
        -   Closed for modification
            The source code of such a class is set in stone, no one is allowed to make changes to the code.
        -   **How do we achieve this?**
            
            **Through abstractions.**
-   **Liskov Substitution Principle**
    -   Enables you to replace objects of a parent class with objects of a subclass without breaking the application.
     **This requires all subclasses to behave in the same way as the parent class**. To achieve that, your subclasses need to follow these rules:            
        -   Don’t implement any stricter validation rules on input parameters than implemented by the parent class.
        -    Apply at the least the same rules to all output parameters as applied by the parent class.   
        
-   **Interface Segregation Principle**
    -   it is better to have many smaller interfaces, than fewer, fatter interfaces.

-   **Dependency Inversion Principle**
    -   Entities must depend on abstractions not on concretions. It states that the high level module must not depend on the low level module,
     but they should depend on abstractions.
    -    Dependency Inversion increases the reusability and flexibility of our code.
                
####    When to use an abstract class vs. interface 
-   The short answer:
    -   **An abstract class** allows you to create functionality that subclasses can implement or override.
        -   You want to share code among several closely related classes.
        -    You expect that classes that extend your abstract class have many common methods or fields or require access modifiers other than public (such as protected and private).
        -   You want to declare non-static or non-final fields. This enables you to define methods that can access and modify the state of the object to which they belong.
    
    -   **An interface** only allows you to define functionality,
 not implement it. And whereas a class can extend only one abstract class, it can take advantage of multiple interfaces.        
        - You expect that unrelated classes would implement your interface. For example, the interfaces Comparable and Cloneable are implemented by many unrelated classes.
        -  You want to specify the behavior of a particular data type, but not concerned about who implements its behavior.
        - You want to take advantage of multiple inheritances.
        
             
## Programming languages

### Java

#### What is autoboxing and unboxing?
 Autoboxing is the automatic conversion that the Java compiler makes between the primitive types and their corresponding object wrapper classes. For example, converting an int to an Integer,
 a double to a Double, and so on. If the conversion goes the other way, this is called unboxing.
#### If you have a variable, that shall store a positive whole number between 0 and 200, what primitive type would you use to store it?
 byte
#### What is the "golden rule" of variable scoping in Java? What is the lifetime of variables?
 As a general rule, variables that are defined within a block are not accessible outside that block. The lifetime of a variable refers to how long the variable exists before it is destroyed.
#### What is the purpose of the ‘equals()’ method?
 Content comparison. .equals() compares the values in the objects.
#### What is the difference between '==' and 'equals()'?
 We can use == operators for reference comparison (address comparison) and .equals() method for content comparison. In simple words, == checks if both objects point to the same memory location whereas .equals() evaluates to the comparison of values in the objects.
 Also, one is an operator, the other is a method.
#### What does the ‘static’ keyword mean?
In Java, a static member is a member of a class that isn’t associated with an instance of a class. Instead, the member belongs to the class itself. As a result, you can access the static member without first creating a class instance.
#### Why is the main() method declared as static? Explain.
  When you start execution of a Java program, JVM looks for the main method in the provided Java class as that is the entry point for the execution. You don’t have to create an object from a class before you can use static methods defined by the class. So main is static.
  JVM has access to it without having to create an instance of it.
#### What is the default access modifier in a class?
Package-private, as default makes the class visible only in the package.
#### What is the JVM?
 Java Virtual Machine
#### What is the difference between the JRE and the JDK?
 - Java Runtime Environment is needed to run java applications. Contains the JVM and the class libraries.
 - Java Development Kit is for writing java applications. Contains everything the JRE has + the java compiler and dev tools. 
#### What is the difference between long and Long?
 One is a primitive data type, the other is its corresponding wrapper class.
#### Can a long store bigger numbers than a Long?
No, both can store the same numbers. A Long only wraps the long data type, does not expand its capacity.
#### What kind of packages do you know under java.util.* ? Bring at least 3 examples.
Scanner, Arrays, Collections, Date, ArrayList.

#### What are the access modifiers in Java? Which one could we use for class?
Access modifiers in Java: public, default, protected, private
 for classes: public, default (package access)
#### Can an “enum” contain methods in Java? Explain.
yes, e.g.: getters for enum values
#### When would you use a private/protected/public attribute? What is the difference?
 These are access modifiers, used to restrict the access of a class, constructor, data member and method in another class.
-  Private is visible within the class.
-  Protected is visible in the package + subclasses of that class.
-  Public is visible everywhere.
#### How do you prevent developers from subclassing a class?
 By using the "final" keyword.
#### How do you prevent developers from overriding a method in a subclass?
 Private, static, or final methods cannot be overridden.
#### How do you prevent developers from changing the value of a variable?
 By using the "final" keyword and using getter methods for outside read-only access.
#### Think about money ;) How would you store a currency value, that shall support decimal parts? Think it through again, and try to think outside of the box!
 BigDecimal is what's widely used, but some argue that any primitive type will also do the job in 99% of cases. So a double, I guess. 
#### What happens if you try to call something, that you have no access to, because of data hiding?
Actually you cant see the method even to call.
#### What happens if you try to delete/drop an item from an array, while you are iterating over it?
Actually u cant delete while u iterating through because you will get a ConcurrentModificationException.
#### What happens if you try to delete/drop/add an item from a List, while you are iterating over it?
Actually u cant delete while u iterating through because you will get a ConcurrentModificationException.
#### What happens if you try to add an item to the end of an array, while you are iterating over it?
Actually u cant delete while u iterating through because you will get a ConcurrentModificationException.

#### If you need to access the iterator variable after a for loop, how would you do it?
Create a field outside the scope, and while iterating assign the value to that field.
#### Which interfaces extend the Collection interface in Java. Which classes?                                   
interfaces: Set, List, Queue, Deque

classes: ArrayList, Vector, LinkedList, PriorityQueue, HashSet, LinkedHashSet, TreeSet

#### What is the connection between equals() and hashCode()? How are they used in HashMap?
The unicity of keys in a HashMap are calculated according to both .equals() and hashCode().
Objects which are .equals() MUST have the same .hashCode(). 

Also: hashCode() must be overridden in every class which overrides equals() method.
#### What is the difference between checked exceptions and unchecked exceptions? Could you bring example for each?
- Checked exceptions are checked by the compiler (compile time exceptions). These exceptions cannot simply be ignored, the programmer should take care of (handle) these exceptions.

- Unchecked exceptions come up during program run (Runtime Exceptions). These include programming bugs, such as logic errors or improper use of an API. Runtime exceptions are ignored at the time of compilation.
#### What is Error in Java and how does it relate to Exception?
Errors are not exceptions at all. They are problems that arise beyond the control of the user or the programmer.
For example, if a stack overflow occurs, an error will arise.
#### When does 'finally' block run? What it is used for? Could you give an example from your projects when you would use 'finally'?
The finally block follows a try block or a catch block.
A finally block of code always executes, irrespective of occurrence of an Exception.
```java
  try {
            File file = new File(filePath);
            reader = new BufferedReader(new FileReader(file));
        } catch (IOException e) {
            e.printStackTrace();
        } finally {
            try {
                reader.close();
            } catch (IOException e) {
                e.printStackTrace();
            }
        }
```
#### What is the largest number you can work with in Java?
In Java, the integer is  32 bits ranges till 2,147,483,647.
            
            But,actually, limitless?

#### When you use method overriding, can you change the access level of the method, from protected to public? Why?
    yes, access level can be more permissive.
####When you use method overriding, can you change the access level of the method, from public to protected? Why?
    no, access level cannot be more restrictive on the overriding method 
#### Can the main method be overridden? Explain your answer!
    no, main method is static. Static methods cannot be overriden, hiding comes into effect
#### When you use method overriding, can you throw fewer exceptions in the subclass than in the parent class? Why?
    yes, but they cannot be new or broader than the parent class
#### When you use method overriding, can you throw more exceptions in the subclass than in the parent class? Why?
     no, can only contain the already declared exceptions, on the same level
#### What does "final" mean in case of a variable, method or a class?
     it cannot be changed (redeclared or overwritten) 
#### What is the super keyword?
     The super keyword in Java is a reference variable which is used to refer immediate parent class object.
#### What are “generics”? When to use? Show examples.
Java Generic methods and generic classes enable programmers to specify, with a single method declaration, a set of related methods, or with a single class declaration, a set of related types, respectively.
 Generics also provide compile-time type safety that allows programmers to catch invalid types at compile time. (less runtime bugs)
```java

    public class GenericMethodTest {
       // generic method printArray
       public static < E > void printArray( E[] inputArray ) {
          // Display array elements
          for(E element : inputArray) {
             System.out.printf("%s ", element);
          }
          System.out.println();
       }
```
#### What is the benefit of having “generic” containers?
     Stronger type-checking, elimination of casts
#### Given two Java programs on two different machines. How can you communicate between the two? What are the possible ways?
Well, it depends on how the other machine is connected to the internet -- specifically, the machine that will be running
the server side application. If the server is directly connected to the internet, then you can just use the ip address.
The client machine should have no issues resolving the address, assuming that it is connected (directly or indirectly) to the internet.
If the server is not directly connected to the internet, meaning behind a firewall and/or router, and using a NAT server, then ... 
the client needs to connect to the ip address of the machine (router) that is on the internet; and the router and firewalls has to be configured to
forward the needed ports to allow the client to get to the server application. 
    
      do new Socket(address, port), that address has to be reachable from your client computer.
#### What is an annotation? What can be annotated and how? Show examples.
 Annotations are a form of metadata, provide data about a program that is not part of the program itself.
 
 
  Classes, methods, variables, parameters and Java packages may be annotated.
 
 
  example:
   ```java
   @Override
```
  https://en.wikipedia.org/wiki/Java_annotation#Built-in_annotations

### C&#35;

#### Explain the purpose of IL and how does it relate to CLR?
#### What does “managed code” mean?
#### What is an assembly?
#### What is the difference between an EXE and a DLL?
#### What is strong-typing versus weak-typing? Which is preferred? Why?
#### What is a namespace?
#### Explain sealed class in C#?
#### What is explicit vs. implicit conversion? Give examples of both of them.
#### Is a struct stored on the heap or stack?
#### Can a struct have methods?
#### Can DateTimes be null?
#### List out the differences between Array and ArrayList in C#?
#### How is the using() pattern useful? What is IDisposable? How does it support deterministic finalization?
#### How can you make sure that objects using dedicated resources (database connection, files, hardware, OS handle, etc.) are released as early as possible?
#### Why to use keyword “const” in C#? Give an example.
#### What is the difference between “const” and “readonly” variables in C#?
#### What is a property in C#?
#### List out two different types of errors in C#?
#### What is the difference between “out” and “ref” parameters in C#?
#### Can we override private virtual method in C#?
#### What's the difference between IEquatable and just overriding Object.Equals()?
#### Explain the differences between public, protected, private and internal. Explain access modifier – “protected internal” in C#!
#### What’s the difference between using `override` and `new` keywords when defining method in child class?
#### Explain StringBuilder class in C#!
#### How we can sort the array elements in descending order in C#?
#### Can you use a value type as a generic type argument in C#? For example when implementing an interface like (IEquatable).
#### What are Nullable Types in C#?
#### Conceptually, what is the difference between early-binding and late-binding?
#### What is delegate, event, callback, multicast delegate?
#### What is enum in C#?
#### What is null-conditional operator?
#### What is null-coalescing operator?
#### What is serialization?
#### What is the difference between Finalize() and Dispose() methods?
#### How do you inherit a class from another class in C#?
#### What is difference between “is” and “as” operators in C#?
#### What are indexers in C# .NET?
#### What is the difference between returning IQueryable<T> vs. IEnumerable<T>?
#### What is LINQ? Explain the idea of extension methods.
#### What are the advantages and disadvantages of lazy loading?
#### How to use of “yield” keyword? Mention at least one practical scenario where it can be used?
#### What are attributes in C#? Give some examples of usage of them.
#### By what mechanism does NUnit know what methods to test?
#### What is the GAC? What problem does it solve?
#### What is the largest number you can work with in C#?

### Database

#### How can you connect your application to a database server? What are the possible ways?
    JDBC (Java DB Connectivity)
    
    JPA (Java persistence API)
#### What do you know about database normalization?
 Normalization is the process of organizing the data in the database. 
 
 It is used to minimize the redundancy from a relation or set of relations. 
 
 It is also used to eliminate the undesirable characteristics like Insertion, Update and Deletion Anomalies.
 
 It divides the larger table into the smaller table and links them using relationship.
 
 The normal form is used to reduce redundancy from the database table. (Normal forms: 1NF, 2NF, 3NF, BCNF, 4NF)
