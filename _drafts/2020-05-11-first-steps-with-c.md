---
title: 'First Steps With C#'
last_modified_at: 2020-05-11T06:05:40+00:00
categories:
  - Blog
tags:
  - Post Formats
  - readability
  - standard
---
In this blog post, I am going to start by teaching you the very basics of C#. One of the questions that a lot of beginners ask is **What is the difference between C# and .NET**. __So that&#8217;s the first thing I am going to answer here. Next, I am going to talk about **CLR** or **Common Language Runtime** which is the runtime environment or the applications. Then I am going to talk about the **architecture of .NET Applications** and as part of this, I will introduce you to the concepts such as **classes**, **namespaces**, ****and **assemblies**. Finally, I will introduce you to the very a very **simple C# application** so you can see classes, namespaces, and methods in action.  


## C# vs .NET

What is a .NET framework and how is it different from C#? Some developers who are absolutely new to C# don&#8217;t know the difference. C# is a programming language, whereas .NET is a framework for building applications on Windows. There are different languages that can target .NET framework and build applications using that framework. Examples are F# or VB.NET.

The .NET framework consists of two components. One is called CLR or Common Language Runtime and the other is a class library for building applications.  


## What is CRL?

Before we understand what CRL is and why we need it, let me explain a little bit about the history of C#.

<div data-amp-layout="fixed" class="wp-block-image align-wrap-right alignwide">
  <figure class="alignright size-large is-resized"><a href="https://www.dev-guide.org/wp-content/uploads/2020/05/image.png"><img loading="lazy" src="https://www.dev-guide.org/wp-content/uploads/2020/05/image.png" alt="" class="wp-image-505" width="358" height="146" srcset="https://www.dev-guide.org/wp-content/uploads/2020/05/image.png 937w, https://www.dev-guide.org/wp-content/uploads/2020/05/image-300x122.png 300w, https://www.dev-guide.org/wp-content/uploads/2020/05/image-768x313.png 768w" sizes="(max-width: 358px) 100vw, 358px" /></a></figure>
</div>

Before C# we had two languages in the C family &#8211; the C language and C++. With either of these languages, when we compiled our application the compiler translated our code into the native code for the machine on which it was running. 

This means if I wrote an application in C++ on a Windows machine, the compiler would translate my code into the native code for that machine. But there are different hardware and different operating systems. So what will happen if I run the same application and run it on a different architecture? It would not run. So when Microsoft designed the C# language on the .NET framework, they came up with an idea that they borrowed from the Java community. 

<div class="wp-block-image is-style-default align-wrap-left alignwide">
  <figure class="alignleft size-full is-resized"><a href="https://www.dev-guide.org/wp-content/uploads/2020/05/image-1.png"><img loading="lazy" src="https://www.dev-guide.org/wp-content/uploads/2020/05/image-1.png" alt="" class="wp-image-506" width="290" height="145" srcset="https://www.dev-guide.org/wp-content/uploads/2020/05/image-1.png 692w, https://www.dev-guide.org/wp-content/uploads/2020/05/image-1-300x150.png 300w" sizes="(max-width: 290px) 100vw, 290px" /></a></figure>
</div>

  
In Java, the computer code is not translated directly into the machine code. It is translated into an intermediate language called bytecode. We have the exact same concept in C#.  


  


<div class="wp-block-image is-style-default align-wrap-right alignwide">
  <figure class="alignright size-full is-resized"><a href="https://www.dev-guide.org/wp-content/uploads/2020/05/image-2.png"><img loading="lazy" src="https://www.dev-guide.org/wp-content/uploads/2020/05/image-2.png" alt="" class="wp-image-507" width="317" height="152" srcset="https://www.dev-guide.org/wp-content/uploads/2020/05/image-2.png 578w, https://www.dev-guide.org/wp-content/uploads/2020/05/image-2-300x144.png 300w" sizes="(max-width: 317px) 100vw, 317px" /></a></figure>
</div>

When you compile your C# code the result is what we call **IL** or **Intermediate Language code**.  
This code is independent of the computer on which it&#8217;s running. Now we need something that would translate that code into the native code or the machine that is running the application.  
And that is the job of **CRL** our **Common Language Runtime**. We can say that CRL is essentially an application that is sitting in the memory, which job is to translate the code into the machine code. This process is called **just in time compiler action** or **JIT**.

With this architecture ( .NET framework ), you can write an application in C# and you don&#8217;t have to worry about compiling it into the native code for different machines. As long as a machine has CRL, your application can be run.  


## The Architecture of .NET Applications

When you build an application with C#, your application consists of building blocks called **classes**. These classes collaborate with each other at runtime. And as a result, the application provides some functionality.  
The **class** is a container that has some data which is also called attributes, and functions which are also called methods. Data represents the state of the application. Functions execute code. They do things for us. 

<div class="wp-block-image is-style-default align-wrap-right alignwide">
  <figure class="alignright size-full is-resized"><a href="https://www.dev-guide.org/wp-content/uploads/2020/05/image-3.png"><img loading="lazy" src="https://www.dev-guide.org/wp-content/uploads/2020/05/image-3.png" alt="" class="wp-image-509" width="266" height="109" srcset="https://www.dev-guide.org/wp-content/uploads/2020/05/image-3.png 507w, https://www.dev-guide.org/wp-content/uploads/2020/05/image-3-300x123.png 300w" sizes="(max-width: 266px) 100vw, 266px" /></a></figure>
</div>

Let me use an example. Think of a car. A car has some attributes like its model, its color, etc. These are the attributes of a car. The car also has some functions. We can start it or we can move it. So you can think of a car as a class. In a real-world application, we have hundreds or even thousands of classes. Each class is responsible for a piece of functionality. An example of that is classes that are responsible for getting the data from the user, process the data, and display something to the user.

Now as the number of classes in an application grows, we need a way to organize these classes. That is where we use a namespace.  
The **namespace** is a container for related classes. For example, in the .NET framework, we have namespaces, each containing tens of related classes. We have a namespace for working with data like databases. We also have a namespace for working with graphics and images. We have a namespace for working with security. 

Now in the real-world application, as these namespaces grow, we need a different way of partitioning an application and that is where we use an assembly.  
The **assembly** is a container for related namespaces. Physically it is a file on the disk which can either be an executable or a **DLL** which stands for a dynamically linked library.  
When you compile an application the compiler builds one or more assemblies, depending on how you partition your code. <figure class="wp-block-image size-full is-style-default">

[<img loading="lazy" width="1470" height="404" src="https://www.dev-guide.org/wp-content/uploads/2020/05/image-4.png" alt="" class="wp-image-510" srcset="https://www.dev-guide.org/wp-content/uploads/2020/05/image-4.png 1470w, https://www.dev-guide.org/wp-content/uploads/2020/05/image-4-300x82.png 300w, https://www.dev-guide.org/wp-content/uploads/2020/05/image-4-1024x281.png 1024w, https://www.dev-guide.org/wp-content/uploads/2020/05/image-4-768x211.png 768w" sizes="(max-width: 1470px) 100vw, 1470px" />](https://www.dev-guide.org/wp-content/uploads/2020/05/image-4.png)</figure> 

In the next paragraph, we can write a very simple application and you&#8217;re going to see all these concepts and in action.  


## Your First C# Application

Finally, it is time to show you a real C# application. In the next picture, you will see a program and on the top, there are a bunch of using statements.

<div class="wp-block-image is-style-default">
  <figure class="aligncenter size-large"><a href="https://www.dev-guide.org/wp-content/uploads/2020/05/image-5.png"><img loading="lazy" width="913" height="583" src="https://www.dev-guide.org/wp-content/uploads/2020/05/image-5.png" alt="" class="wp-image-513" srcset="https://www.dev-guide.org/wp-content/uploads/2020/05/image-5.png 913w, https://www.dev-guide.org/wp-content/uploads/2020/05/image-5-300x192.png 300w, https://www.dev-guide.org/wp-content/uploads/2020/05/image-5-768x490.png 768w" sizes="(max-width: 913px) 100vw, 913px" /></a></figure>
</div>

What&#8217;s more, our project is called HelloWorld. So by default visual studio creates a **namespace** called HelloWorld. When you write code in this namespace, you have access to any classes defined in this namespace. So if we want to use a class that is defined in a different namespace we need to import it in our code file. And that&#8217;s why we use the **using statement**.  
By default, Visual Studio adds automatically five using statements. **System** is a namespace from .NET Framework. **System.Collections.Generic** is used to work with lists collections. **System.Linq** is used to work with data. **System.Text** is used to work with text. And **System.Threading** is used to build multithreaded applications. In this tutorial, we are going to create a very simple application and we are not going to use any of these four namespaces.

All right so here&#8217;s our **namespace HelloWorld** and inside them, space. By default, we have a **class** called **Program** so every console application you create with Visual Studio has a class called program. Inside the program, by default, we have a method or a function called **Main** and that&#8217;s the entry point to the application. When you run your application, CLR executes the code inside Main method. This method is declared as **static**, which means that the method can be invoked without instantiating an object.

What you see before the method name, the word **void**, is the return type or the output of the method. Void means that this method does not return any value. It just contains some code and do some functions.

Methods have input and output. What goes inside parentheses is the input to the method, which we call parameter or argument. You should know, that parameters are optional. In this case, the default template, the main method, has a parameter called **args** which is of type String Array. 

Last, we need to surround our block of code with **curly braces** so that it is applicable for methods, for classes and for namespaces.

Now it is time to write a very simple program which prints &#8220;Hello World&#8221;. We have a class called **Console**. It is used to read data from the console or write data to it. Then we have **WriteLine** method. This method can print something to the console and it takes a parameter. In our case, this parameter is the string &#8216;**Hello world**&#8216;.  


<div class="wp-block-image is-style-default align-wrap-right alignwide">
  <figure class="alignright size-large is-resized"><a href="https://www.dev-guide.org/wp-content/uploads/2020/05/image-6.png"><img loading="lazy" src="https://www.dev-guide.org/wp-content/uploads/2020/05/image-6.png" alt="" class="wp-image-516" width="409" height="77" srcset="https://www.dev-guide.org/wp-content/uploads/2020/05/image-6.png 448w, https://www.dev-guide.org/wp-content/uploads/2020/05/image-6-300x56.png 300w" sizes="(max-width: 409px) 100vw, 409px" /></a></figure>
</div>

Let&#8217;s run our application. You will see a black window, which is called a console.

  


And that&#8217;s it, we ran our first C# program. We also covered topics as differences between C# and .NET, what is CLR, and some important things about the architecture of .NET Applications.
