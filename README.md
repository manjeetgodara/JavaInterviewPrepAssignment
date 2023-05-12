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



