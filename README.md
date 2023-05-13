# JavaInterviewPrepAssignment

Part 1:Java Platform 

Ques:-Why java is so much popular?

sol:- Java language was developed by james gosling in 1995 at sunmicrosystem which was later on acquired by
oracle in 2010. 
There are lot of reason for java popularity as follow:-
1. Simple:- Java is having quite simple syntax which makes it easy to understand.Also, java is having automatic
memory management which plays a vital role for the same.
2. Secure:- Java is highly secured language,it provides  the implementation for almost all well known security 
networks. It provides a separate middle ware service in JAAS(java authentication and authorization service) which
provides web security Auth. SSO.
3. Robust :- Java is robust which means it is  strongly typed language.It is having very good memory management 
system which is dynamic in nature and do the allocation and deallocation of objects at the run time.
4. Portable and Plaform independent:- During compilation, java source code compiles into byte code or binary code
(i.e .class file got generated). So, we can develop java code on one operating system and compile it now it can be 
runned on mutiple platform no need to compile it again and again i.e Write Once Read Anywhere(WORA). This WORA
makes java an Architecture Neutral Language.These are some of the reasons , that makes java a portable and platform
independent language.
5. Object Oriented:- Java is an object oriented programming language. It supports all the OOPs characterstics.
That makes java code easy to develop and manage ,incomparison of structured language.
6. Multi-Threaded:- Java also supports multi-threaded concept which makes it to do multiple functionalites 
simultaneously.

Ques:- What is platform independence?

sol:- Platform independence means in order to run java code on any Operating System we don't need to compile it
again and again. As, during the compilation of java source code a .class file get generated i.e byte code and
in order to load that file into the memory and for it's execution only JDK/JRE must need to be present in the 
Operating System.  

Ques:-What is ByteCode?

sol:- During compilation, java source code compiles into byte code or binary code (i.e .class file got generated).
 And ,in order to load that file into the memory and for it's execution only JDK/JRE must need to be present in the 
Operating System. 

Ques:- Compare JDK vs JVM VS JRE.

sol:- JDK stands for java development kit , it consists of all the development tools that are required in order
to develop the java code. (JDK=JRE+development tools(like java , javac ,compiler, debugger etc)).
JRE stands for Java Runtime Environment, it consists of JVM which actually runs our java code with the support of
predefined libraries and class packages.(JRE=JVM+Runtime lib+class pacakages)
JVM stands for Java Virtual Machine, which executes our code by calling the main method.If there is no main method
in our program then jvm can not execute our program.It consists of three modules(class loader,memory areas,execution
engine). 

Ques:- What is the role of class loader in java?

sol:- Class loader is basically the subsystem of the JVM(java virtual machine), which loads the .class file into the
memory.
There are three types of class loader mainly in java:-
1. Bootstrap class loader:- It loads the class file code from the <JAVA_HOME>/jre/lib folder.
2. Extension class loader:- It loads the the class file code from the <JAVA_HOME>/jre/lib/external folder to memory.
3. Application class loader/System class loader:- It loads the byte code from the class path which is mapped with
the environment variable(i.e whatever the custom code we develop and exceute it is loaded by the system class loader).

Bootstrap is the parent of the extension and application class loader.Similarly,extension class loader is the parent
of the application loader.

Part 2: Wrapper Classes

Ques 1: What are the Wrapper classes?

Sol:- Wrapper classes are basically the object form of the primitive data types in java.For, each primitive data
type in java there is one wrapper class.In simple words, it means to wrap up the primitive data type in form the 
object.Ex- int- Integer, char- Character and so on.

Ques 2:Why do we need Wrapper Classes in Java?

sol:- There are some of the reason to use wrapper classes in java:-
1. If Objects are required to use at some place in java,where use of primitives data type is not applicable.
(primitives are used to make our code memory efficient)
2. Collection framework or data structures works with Objects only.
3. Generics does not allow primitive data type as Typed Parameter.
4. Mutltithreading needs Object to support synchronization.

Ques 3 : What are the different ways of creating Wrapper Class Instances?

sol:- 1. By use of constructor (Ex-Integer myInt=new Integer(24);)
2. By use of valueOf() method (Ex-Boolean b=Boolean.valueOf(true);)
3. By use of conversion method (Ex-Double a=Double.parseDouble("12.3");)
4. By use of autoboxing (Ex-Integer a=12;)

Ques 4 : What are differences in the two ways of creating wrapper classes ?
 
sol:- 1. Usage:- Previously ,constructor approach was mainly used to create the wrapper classes.But, now a days
valueOf() method is generally used to create the wrapper classes in the java codes.
2. Performance:- In order to create wrapper classes , valueOf() method is faster and efficient in comparison of
constructor approach.
3. Compatibility:- valueOf() method is not available in every wrapper class of java like Character class does not
have valueOf() static method.So, at that point of time we need to use constructor approach only in order to make 
wrapper class object.
4. Object equality:- Whenever we create wrapper class object with the use of constructor approach for the
at that point of time a new Object get created inside the memory heap. So, when we use equality constructor(==)
so, it shows that they are different one's as equality operator compare the address not the content inside the 
object. But, in case of the valueOf() method jvm frequently uses the object space again and again so, that problem 
does not occur as it is happening in constructor approach. 

Ques 5: What is autoboxing?

sol:- Autoboxing may be defined as the automatic conversion of primitive data type to the wrapper classes.
And, unboxing means conversion of wrapper class to the primitive data type.

Ques:- 6 What are the advantages of auto-boxing?

sol:-  Autoboxing makes coding more convenient because it saves developers from having to write boilerplate 
code to convert between primitive data types and their corresponding wrapper classes.And, it also increases the
readability of the code as well.

Ques:- 7 What is casting?

sol:- Casting means the conversion of one primitive data type to another one. 

Ques:- 8 What is implicit casting?

sol:- Implicit casting means conversion of smaller size data type to larger size data type automtically.It is
also known as widening. Ex- conversion of int to float or double or long etc.

Ques:- 9 What is explicit casting? 

sol:-Explicit casting means conversion of larger size data type to smaller one. It is also known as type casting
or narrowing.(it does not happen automatically and also data loss takes place in such casting). Ex-float->int,
long-> int etc.

Part 3: Strings

Ques:- 1 Are all strings immutable in java?

sol: Yes, all strings are immutable in java. Once ,a string is to be made in java then we can not modify it's 
content. So, whenever we try to try to modify it then a new object get formed inside the string pool constant area.

Ques:- 2 Advantages of string immutability?

sol:- 1. Thread safety:- Since , strings are immutable so that they can be shared between the threads without worrying
about race condition.
2. Security:- As, strings are immutable so it ca not be modified with some malicious code,which helps prevent security
vulnerabilites.
3. This thing also reduces the risk of memory leakage and other issues.

Ques :- 3 Where are string values stored in memory?

sol:- Inside spring pool constant area it lies inside the memory heap only.

Ques:- 4 Why should you be careful about String Concatenation(+) operator in Loops?

sol: As, we know that strings are immutable. So , at the time of Concatenation operation a new String object get
formed with the modified content.(So, making of objects again and again is very costly process).

Ques :- 5 How do you solve the above problem?

sol:- In order to solve the above problem , we can use StringBuilder and StringBuffer classes to create the string
and these are mutable one's.

Ques:- 6 What are differences between String and StringBuffer?

sol:-Both String and StringBuffer are used to represent and manipulate sequences of characters in Java, but they 
differ in terms of mutability, performance, and functionality.  

1.Mutability: String objects are immutable, which means their values cannot be changed once they are created. 
StringBuffer, on the other hand, is mutable, which means that you can modify its value by appending, deleting,
 or inserting characters.
2. String objects are thread-safe because they are immutable, but StringBuffer is not thread-safe by default.
3. Performance: Because String objects are immutable, any operation that modifies the contents of a String (such as concatenation) 
requires creating a new String object. This can be slow and memory-intensive, especially when working with 
large strings. StringBuffer, on the other hand, is designed to be more efficient for this kind of manipulation
 because it can modify the contents of the buffer without creating new objects.

Ques:- 7 What are differences between StringBuilder and StringBuffer?

sol:- Both StringBuilder and StringBuffer are used to represent and manipulate sequences of characters in Java,
 but they differ in terms of mutability, performance, and synchronization.

Here are the main differences between StringBuilder and StringBuffer:

1.Mutability: StringBuilder and StringBuffer are both mutable, which means that you can modify their values by 
appending, deleting, or inserting characters. The key difference between them is that StringBuilder is not
 synchronized, while StringBuffer is synchronized.
2. Performance: Because StringBuilder and StringBuffer are mutable, they can modify their contents without creating
 new objects. This makes them more efficient than String for operations that involve a lot of string 
manipulation. However, StringBuilder is generally faster than StringBuffer because it is not synchronized.
3. Synchronization: StringBuffer is synchronized, which means that it is thread-safe. This makes it useful in 
multi-threaded applications where multiple threads might be modifying the same string buffer at the same time. 
StringBuilder, on the other hand, is not synchronized and is generally faster in single-threaded applications.

Ques:- 8 Can you give examples of different utility methods in String class?

sol:-charAt(int index): Returns the character at the specified index.
length(): Returns the length of the string.
substring(int beginIndex): Returns a new string that is a substring of the original string, starting at the 
specified index.
substring(int beginIndex, int endIndex): Returns a new string that is a substring of the original string, 
starting at the specified begin index and ending at the specified end index.
concat(String str): Concatenates the specified string to the end of the original string.
equals(Object obj): Compares the original string to the specified object for equality.
equalsIgnoreCase(String str): Compares the original string to the specified string for equality, ignoring case 
differences.
indexOf(int ch): Returns the index within the original string of the first occurrence of the specified 
character.
lastIndexOf(int ch): Returns the index within the original string of the last occurrence of the specified
 character.
replace(char oldChar, char newChar): Returns a new string that is a copy of the original string with all 
occurrences of the specified old character replaced by the specified new character.
startsWith(String prefix): Tests whether the original string starts with the specified prefix.
endsWith(String suffix): Tests whether the original string ends with the specified suffix.
toLowerCase(): Converts the original string to lowercase.
toUpperCase(): Converts the original string to uppercase.

Part 4:OOPs

Ques: 1 What is class?
sol: class may be defined as the blue-print or template in order to create various objects accordingly.

Ques:2 Which class is super class of all classes in java?
sol: Object class

Ques: 3 What is behavior of an Object?
sol: Behaviour of an Object is nothing but the methods in the classes.Basically, Methods are the set of codes
that perform some tasks.

Ques: 4 Explain about toString method ?
sol:The toString() method returns the String representation of the object. If you print any object, 
Java compiler internally invokes the toString() method on the object. So overriding the toString() 
method, returns the desired output, it can be the state of an object etc. depending on your implementation

Ques: 5 What is the use of equals() methods in java?
sol:The equals() method compares two strings, and returns true if the strings are equal, and false if not. 
 Use the compareTo() method to compare two strings lexicographically.

Ques: 6 What is the use of hashcode method in java?
sol:  The hashCode() method is used to generate the hash values of objects.

Ques: 7 What is the use of hashCode and equals method in Java?
sol: Equals() and Hashcode() in Java. The equals() and hashcode() are the two important methods provided by the 
Object class for comparing objects. Since the Object class is the parent class for all Java objects,
 hence all objects inherit the default implementation of these two methods.

Ques: 8 Is Multiple Inheritance allowed in Java?
sol: Yes, multiple inheritance allowed in java but only in case of interfaces only.But, for the classes
it is not applicable.

Ques: 9 Explain inheritance with Examples.
sol: When one class object inherits some of the properties of the other class object(i.e except private
methods, constructors, final methods etc can not be inherited) this is known as inheritance.

Ques: 10 What is Method Overloading?
sol: When mutiple methods with same name but with different parameter list i.e either in terms of sequence
or data types or number of parameter list inside the same class are declared then this is known as method
overloading.(It is controlled by the java compiler, and it is achieved by static polymorphism(compile
time polymorphism)

Ques: 11 What is Method Overriding?
sol: When multiple methods with same name and same parameter list i.e either in terms of sequence or data
types or number of parameter list inside the different classes which are having IS-A relationship between
them.This is known as method overriding.(It is handled by JVM ,and it is achieved by runtime polymorphism,
also known as dynamic polymorphism)

Ques: 12 Can super class reference variable holds an object of subclass?
sol: Yes, the super class reference variable can hold the sub class object actually, it is widening in
 case of objects (Conversion of lower datatype to a higher datatype).

Ques: 13 What is an Interface ?
sol: Interface may be defined as the blueprint of the class which tells what to do but not how.It is used
in java to achieve abstraction.

Ques: 14 How do you implement an interface ?
sol: access modifier interface name{
  //public abstract methods
//default concrete methods
//public static final fields can be there.
}

Ques: 15 Some tricky things about interfaces?
sol: An interface cannot contain instance fields. The only fields that can appear in an interface must be 
declared both static and final. An interface is not extended by a class; it is implemented by a class. An interface can extend multiple interfaces.

Ques: 16 Can you extend an interface ?
sol: Yes, interface can be extended with other interfaces.

Ques: 17 Can a class implements multiple interfaces ?
sol: Yes, in case of interfaces multiple inheritance is possible in java.

Ques: 18 What is an Abstract Class ?
sol: An abstract class is a class which can have abstract methods(methods  without  implementation or body).
These classes are used for achieving  abstraction in java.

Ques: 19 When do you use an Abstract Class ?
sol: When we want to achieve abstraction in java(abstraction means to hide the internal implementation 
and just highlight the setup services that we are offering).

Ques: 20 How do you define an Abstract Method ?
sol: An abstract method is something which doesn't have the implementation or body.

Ques: 21 Compare Abstract Class vs Interfaces ?
sol: 1. Abstract class can have abstract methods with any access modifier and other concrete methods as well
with any access modifier, but in case of interfaces only public abstract methods and default concrete
methods are allowed.(if we don't provide these keywords in interface then java compiler will put them by own)

2. There is no restriction for fields declared in abstract classes, but in case of interfaces only public
static final fields are allowed.

3. Both of them can not be instansiated and both of them are used for achieving abstraction in java.

4. For inheritance purpose, in abstract class case extends keyword is to be used and in case of interfaces
implements keyword is used.

5. When a class  implements any interface then the overriden methods must have the greater accessibility
or it can be equal to the method defined in interface but it can not be lower, otherwise compilation error will
be there. But, there is no such restriction at all in case of abstract classes.

Ques:22 What is a Constructor?
sol: Constructor is a special type of method, which does not have any kind of return type.The main purpose of the
constructor is to initialize the java object of a class.

Ques: 23 What is default constructor?
sol: It is one of the type of the constructor in java, which is to be created by java compiler when no 
constructor is defined inside the class.It is a zero argument constructor and inside the body it consists
of super keyword only.

Ques: 24 How do you call a Super Class Constructor from a Constructor?
sol: By use of super();

Ques:25 What is the use of this();
sol: it is used to call current class constructor.

Ques: 26 Can a constructor be called directly from a method?
sol: Yes, as mentioned we can call all the members of a class (methods, variables, and constructors) from 
instance methods or, constructors.

Ques: 27 Difference between compile time and run time polymorphism?
sol:  Types of Polymorphism

1. compile time polymorphism
 compile time polymorphism is also known as static polymorphism, from, static polymorphism we can achieve
 method overloading.  Method overloading is handled by  java compiler
2.run time polymorphism
runtime polymorphism is also known as dynamic polymorphism, from runtime polymorphism we 
can achieve method overriding in java.  Method overriding is controlled by JVM.

For method overloading
1. same class
2. same method name
3. Different arguments like either in terms of number; sequence; type of argument may be differ.

For method overridden
1. Different  class
2. same method name
3. same arguments like either in terms of number; sequence;type of argument may be differ.
4. IS-A relationship between parent and child class(inheritance)

Ques: 28 Is a super class constructor called even when there is no explicit call from a sub class 
constructor ?
sol:If a constructor does not explicitly invoke a superclass constructor, the Java compiler automatically 
inserts a call to the no-argument constructor of the superclass. If the super class does not have a 
no-argument constructor, you will get a compile-time error.






