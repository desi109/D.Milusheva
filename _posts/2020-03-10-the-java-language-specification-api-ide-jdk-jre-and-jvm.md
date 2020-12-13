---
title: 'The Java Language Specification, API, IDE, JDK,  JRE and JVM'
last_modified_at: 2020-03-10T06:07:02+00:00
categories:
  - Blog
tags:
  - Post Formats
  - readability
  - standard
---
In this post, you will learn more about Java Language Specifications, Java editions, what are the differences between JRE and JDK and how your computer executes a Java program.

#### Java Language Specification and API

The **Java language specification** is a technical definition of the Java programming language’s syntax and semantics. You can find the complete Java language specification [here](https://docs.oracle.com/javase/specs/).  
The **A**pplication **P**rogram **I**nterface (**API**), also known as Java library, contains predefined classes and interfaces for developing Java programs. The API is still expanding. You can view and download the latest version of the Java API <a rel="noreferrer noopener" aria-label="here (opens in a new tab)" href="http://download.java.net/jdk8/docs/api/" target="_blank">here</a>.  
Computer languages have strict rules of usage. If you do not follow the rules when writing a program, the computer will not be able to understand it. The Java language specification and the Java API define the Java standards.  


#### IDE

An **IDE** is an **I**ntegrated **D**evelopment **E**nvironment for rapidly developing Java programs quickly. Editing, compiling, building, debugging, and online help are integrated in one graphical user interface. You simply enter source code in one window or open an existing file in a window, and then click a button or menu item or press a function key to compile and run the program. Of course, you can run the JDK tools by typing commands in a terminal window. However, many programmers prefer the comfort of an integrated development environment.  
For example, software that provides an integrated development environment is NetBeans or Eclipse, or you can just use TextPad.  


#### Java Editions

Java is a full-fledged and powerful language that can be used in many ways. It comes in three editions:

  * Java Standard Edition (**Java SE**) to develop client-side applications. The applications can run on a desktop.
  * Java Enterprise Edition (**Java EE**) to develop server-side applications, such as Java servlets, JavaServer Pages (JSP), and JavaServer Faces (JSF).
  * Java Micro Edition (**Java ME**) to develop applications for mobile devices, such as cell phones.

We will use Java SE. There are many versions of Java SE and the latest you can download from <a rel="noreferrer noopener" aria-label="here (opens in a new tab)" href="https://www.oracle.com/java/technologies/javase-downloads.html" target="_blank">here</a>. Oracle releases each version with a Java Development Toolkit (JDK).  
_**NOTE:**_ Java SE 8, the Java Development Toolkit is called JDK 1.8 (also known as Java 8 or JDK 8).  


### What is Java Virtual Machine (JVM)?

Imagine that you want to run a Java program on your computer, what will happen? 

<div class="wp-block-image">
  <figure class="aligncenter size-large"><a href="https://www.dev-guide.org/wp-content/uploads/2020/03/the-java-language-specification-api-ide-jdk-jre-and-jvm-2-1.jpg" target="_blank" rel="noreferrer noopener"><img loading="lazy" width="1024" height="402" src="https://www.dev-guide.org/wp-content/uploads/2020/03/the-java-language-specification-api-ide-jdk-jre-and-jvm-2-1-1024x402.jpg" alt="" class="wp-image-411" srcset="https://www.dev-guide.org/wp-content/uploads/2020/03/the-java-language-specification-api-ide-jdk-jre-and-jvm-2-1-1024x402.jpg 1024w, https://www.dev-guide.org/wp-content/uploads/2020/03/the-java-language-specification-api-ide-jdk-jre-and-jvm-2-1-300x118.jpg 300w, https://www.dev-guide.org/wp-content/uploads/2020/03/the-java-language-specification-api-ide-jdk-jre-and-jvm-2-1-768x301.jpg 768w, https://www.dev-guide.org/wp-content/uploads/2020/03/the-java-language-specification-api-ide-jdk-jre-and-jvm-2-1.jpg 1377w" sizes="(max-width: 1024px) 100vw, 1024px" /></a></figure>
</div>

  1. **Java compiler** (also known as **javac**) compiles the **Java source code (.java file)** into a binary format known as **bytecode (.class file)**. Java bytecode is platform independent instruction set, which contains instructions (opcode) and parameter information.
  2. Bytecode is translated by the Operating System specific **Java Virtual Machine (JVM)**  
    into the platform specific **machine code**.
  3. Class loader in JVM loads the binary representation of the classes into memory.
  4. Execution engine in JVM executes the byte code and generates Operating System specific machine instructions. These machine instructions are executed directly by the central processing unit (CPU).

**The JVM is the interpreter, which translates the bytecode into machine code.** 

### JDK and JRE

**Java Development Kit** (JDK) is the software for programmers who want to write Java programs.  
The JDK consists of a set of separate programs for compiling, running, and testing Java programs. So as you can see on the diagram down, JDK contains JRE and Development Tools (e.g. javac, java, etc.)

##### JDK = JRE + Development Tools  
 {.has-text-align-center}

**Java Runtime Environment** (JRE) is the software for consumers who want to run Java programs. It contains the API (Java libraries), Java Virtual Machine (JVM) and other files. 

##### JRE = API + JVM + other files  {.has-text-align-center}<figure class="wp-block-image size-large">

<a href="https://www.dev-guide.org/wp-content/uploads/2020/03/the-java-language-specification-api-ide-jdk-jre-and-jvm-1.png" target="_blank" rel="noreferrer noopener"><img loading="lazy" width="1024" height="671" src="https://www.dev-guide.org/wp-content/uploads/2020/03/the-java-language-specification-api-ide-jdk-jre-and-jvm-1-1024x671.png" alt="" class="wp-image-399" srcset="https://www.dev-guide.org/wp-content/uploads/2020/03/the-java-language-specification-api-ide-jdk-jre-and-jvm-1-1024x671.png 1024w, https://www.dev-guide.org/wp-content/uploads/2020/03/the-java-language-specification-api-ide-jdk-jre-and-jvm-1-300x197.png 300w, https://www.dev-guide.org/wp-content/uploads/2020/03/the-java-language-specification-api-ide-jdk-jre-and-jvm-1-768x503.png 768w, https://www.dev-guide.org/wp-content/uploads/2020/03/the-java-language-specification-api-ide-jdk-jre-and-jvm-1.png 1149w" sizes="(max-width: 1024px) 100vw, 1024px" /></a></figure> 



Now you know more about Java Development Kit and the whole process of executing a Java code. If you want to learn how to install and set up the JDK, check out <a href="https://www.dev-guide.org/how-to-install-and-set-up-jdk-windows-10/?preview=true&_thumbnail_id=427" target="_blank" rel="noreferrer noopener" aria-label="this blog post (opens in a new tab)">this blog post</a>.
