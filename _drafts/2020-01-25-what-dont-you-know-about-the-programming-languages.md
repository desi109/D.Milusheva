---
title: 'What Don&#8217;t You Know About The Programming Languages?'
last_modified_at: 2020-01-25T05:46:00+00:00
categories:
  - Blog
tags:
  - Post Formats
  - readability
  - standard
---
Computer programs, known as software, are instructions that tell a computer what to do. Computers do not understand human languages, so programs must be written in a language that the computer can use. There are hundreds of programming languages, and they were developed to make the programming process easier for people. However, all programs must be converted into instructions that the computer can execute.

#### **What is** Machine Language**?**

A computer’s native language, which differs among different types of computers, is its **machine language** &#8211; a set of built-in primitive instructions. These instructions are in the form of binary code, so if you want to give a computer an instruction in its native language, you have to enter the instruction as binary code. For example, to add two numbers, you might have to write an  
instruction in binary code as follows: 

##### 1101101010011010 



#### Assembly Language

Programming in machine language is a tedious process. Moreover, programs written in machine language are very difficult to read and modify. For this reason, assembly language was created in the early days of computing as an alternative to machine languages. Assembly language uses a short descriptive word, known as a **mnemonic**, to represent each of the machine-language instructions. For example, the mnemonic _&#8216;add&#8217;_ typically means to add numbers, and _&#8216;sub&#8217;_ means to subtract numbers. To add the numbers 2 and 3 and get the result, you might write an instruction in assembly code as follows:

##### add 2, 3, result



Assembly languages were developed to make programming easier. However, because the  
the computer cannot execute assembly language, another program &#8211; called an **assembler** &#8211; is used to translate assembly-language programs into machine code.

<div class="wp-block-image">
  <figure class="aligncenter size-large is-resized"><a href="https://www.dev-guide.org/wp-content/uploads/2020/03/what-dont-you-know-about-the-programming-languages-1.png" target="_blank" rel="noreferrer noopener"><img loading="lazy" src="https://dev-guide.org/wp-content/uploads/2020/03/what-dont-you-know-about-the-programming-languages-1.png" alt="" class="wp-image-297" width="630" height="152" srcset="https://www.dev-guide.org/wp-content/uploads/2020/03/what-dont-you-know-about-the-programming-languages-1.png 874w, https://www.dev-guide.org/wp-content/uploads/2020/03/what-dont-you-know-about-the-programming-languages-1-300x73.png 300w, https://www.dev-guide.org/wp-content/uploads/2020/03/what-dont-you-know-about-the-programming-languages-1-768x186.png 768w" sizes="(max-width: 630px) 100vw, 630px" /></a><figcaption>An assembler translates assembly-language instructions into machine code.</figcaption></figure>
</div>

Writing code in assembly language is easier than in machine language. However, it is still tedious to write code in assembly language. An instruction in assembly language essentially corresponds to an instruction in machine code. Writing in assembly language requires that you know how the CPU works. Assembly language is referred to as a low-level language because assembly language is close in nature to machine language and is machine-dependent.



#### High-Level Language

In the 1950s, a new generation of programming languages known as high-level languages emerged. They are platform-independent, which means that you can write a program in a high-  
level language and run it in different types of machines. High-level languages are similar to English and easy to learn and use. The instructions in a high-level programming language are called statements. Here, for example, is a high-level language statement that computes the area of a circle with a radius of 5:

##### area = 5 \* 5 \* 3.14159;

There are many high-level programming languages, and each was designed for a specific purpose. 

  * **Ada**  
    Named for **Ada** Lovelace, who worked on mechanical general-purpose computers. Developed for the Department of Defense and used mainly in defense projects.

  * **BASIC**  
    **B**eginner’s **A**ll-purpose **S**ymbolic **I**nstruction **C**ode. Designed to be learned and used easily by beginners.

  * **C**  
    Developed at Bell Laboratories. Combines the power of an assembly language with the ease of use and portability of a high-level language.

  * **C++**  
    An object-oriented language, based on C.

  * **C#**  
    Pronounced “C Sharp.” An object-oriented programming language developed by Microsoft.

  * **COBOL**  
    **CO**mmon **B**usiness **O**riented **L**anguage. Used for business applications.

  * **FORTRAN**  
    **FOR**mula **TRAN**slation. Popular for scientific and mathematical applications.

  * **Java**  
    Developed by Sun Microsystems, now part of Oracle. An object-oriented programming language, widely used for developing platform-independent Internet applications.

  * **JavaScript**  
    A Web programming language developed by Netscape.

  * **Pascal**  
    Named for **Blaise Pascal,** who pioneered calculating machines in the seventeenth century. A simple, structured, general-purpose language primarily for teaching programming.

  * **Python**  
    A simple general-purpose scripting language good for writing short programs.

  * **Visual Basic**  
    It was developed by Microsoft. Enables the programmers to rapidly develop Windows-based applications.

A program written in a high-level language is called a **source program** or **source code**. Because a computer cannot execute a source program, a source program must be translated into machine code for execution. The translation can be done using another programming tool called an **interpreter** or a **compiler**.

An interpreter reads one statement from the source code, translates it to the machine code or virtual machine code, then executes it right away, as shown in figure **(a)**.  
Note a statement from the source code may be translated into several machine instructions. A compiler translates the entire source code into a machine-code file, and the machine-code file is then executed, as shown in figure **(b)**.<figure class="wp-block-image size-large">

<a href="https://www.dev-guide.org/wp-content/uploads/2020/03/what-dont-you-know-about-the-programming-languages-2.png" target="_blank" rel="noreferrer noopener"><img loading="lazy" width="1024" height="408" src="https://dev-guide.org/wp-content/uploads/2020/03/what-dont-you-know-about-the-programming-languages-2-1024x408.png" alt="" class="wp-image-306" srcset="https://www.dev-guide.org/wp-content/uploads/2020/03/what-dont-you-know-about-the-programming-languages-2-1024x408.png 1024w, https://www.dev-guide.org/wp-content/uploads/2020/03/what-dont-you-know-about-the-programming-languages-2-300x120.png 300w, https://www.dev-guide.org/wp-content/uploads/2020/03/what-dont-you-know-about-the-programming-languages-2-768x306.png 768w, https://www.dev-guide.org/wp-content/uploads/2020/03/what-dont-you-know-about-the-programming-languages-2.png 1224w" sizes="(max-width: 1024px) 100vw, 1024px" /></a><figcaption>(a) An interpreter translates and executes a program one statement at a time. (b) A compiler translates the entire source program into a machine-language file for execution.</figcaption></figure>
