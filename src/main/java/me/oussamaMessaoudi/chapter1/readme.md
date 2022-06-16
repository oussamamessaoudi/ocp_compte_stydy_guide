#Chapter 1: Welcome to Java 
##Benefits of using Java 
- **Object-Oriented** (Allowing for functional programing within a class)
- **Encapsulation** (Access modifiers)
- **Platform** Independent (Write once Run everywhere)
- **Robust** (Prevents memory leaks {Garbage Collector})
- **Simple** (No pointers + No operator overloading)
- **Secure** (inside JVM -> SANDBOX)
- **Multithreaded** 
- **Backward Compatibility** (code will work with later versions)
##Class Structure
- **class** basic building block, describe characteristics.
- **object** a runtime instance of a class in memory(instance)
- **reference** is a variable that point to an object.

- **Fields**(Variables) & **Methods** (Functions, Procedures)
- **Fields** hold the state of the programme.
- **Methods** operate on that state.
- **Keyword** a word with special meaning
- **Parameter** ( variable that be passed to a func)
- **Method signature** (method name + parameters types)
- **Method declaration** method signature + return type
- **Comments** (//single line,/\*multi line*/, /** java doc */ )
- **Classes Vs Files** ( one public class per file that match the name of the file)
- **Main Method** Gateway startup of a java process
```shell
javac Zoo.java
java Zoo oneWord "multi word"
#Lunching single-file source-code programs (in memory no .class generated)
java Zoo.java -> To compile and Execute
```
- **WildCards import** (imports all class of a package) 
- **java.lang** is automatically imported
- No need to import a class in the same package
- When a class is found in multiple package (both *) java gives a compiler error.
```java
//Exp 1
import java.util.*;
import java.sql.*;//Compiler Error
//Exp 2
import java.util.Date;
import java.sql.Date;//Compiler Error
//Exp 3
import java.util.Date;//takes precedence 
import java.sql.*;
```

```shell
#-d to put compiled files in XXX forlder
javac -d XXX packagea/ClassA.java packagesb/ClassB.java
#RUN
java -cp XXX packageb.ClassB
java -classpath XXX packageb.ClassB
java --class-path XXX packageb.ClassB

# XXX for run file can globe jar files separated by ; or :
java -cp ".;C:\temp\directoryWithJars\*" myPackage.MyClass
jar -cvf newJar.jar . #create a jar file
jar --create --verbose --file newJar.jar .
jar -cvf newJar.jar -C dir .
```
- package name first line in the file _Optional_
- import immediately after the package _Optional_
- class after the import 
- Field inside class _Optional_
- Method inside class _Optional_
