---
title: A Short History of Java
last_modified_at: 2020-02-01T07:38:00+00:00
categories:
  - Blog
tags:
  - Post Formats
  - readability
  - standard
---
If you are interested in Java and you opened this post maybe you want to learn something more about Java history. Let me present to you the timeline of events and how Java evolved to its current state. This blog post is based on various published sources (most importantly an interview with Java’s creators in the July 1995 issue of SunWorld’s online magazine). 

# 1991

Java goes back to 1991, when a group of Sun engineers, led by Patrick Naughton and James Gosling (a Sun Fellow and an all-around computer wizard), wanted to design a small computer language that could be used for consumer devices like cable TV switchboxes. Since these devices do not have a lot of power or memory, the language had to be small and generate very tight code. Also, as different manufacturers may choose different central processing units (CPUs), it was important that the language not be tied to any single architecture. The project was code-named “Green.” 

The requirements for small, tight, and platform-neutral code led the team to design a portable language that generated intermediate code for a virtual machine. The Sun people came from a UNIX background, so they based their language on C++ rather than Lisp, Smalltalk, or Pascal. But, as Gosling says in an interview, “All along, the language was a tool, not the end.” Gosling decided to call his language “Oak” (presumably because he liked the look of an oak tree that was right outside his window at Sun). The people at Sun later realized that Oak was the name of an existing computer language, so they changed the name to Java. This turned out to be an inspired choice. In fact, Java is the name of an island in Indonesia where the first coffee (called Java coffee) was produced. James Gosling chose the name while drinking coffee near his office. It is important to say that Java is not a shorthand for anything, it is just a name.

# 1992

In 1992, the Green project delivered its first product, called “*7.” It was an extremely intelligent remote control. Unfortunately, no one was interested in producing this at Sun, and the Green people had to find other ways to market their technology. However, none of the standard consumer electronics companies were interested either. The group then bid on a project to design a cable TV box that could deal with emerging cable services such as video-ondemand. They did not get the contract. (Amusingly, the company that did was led by the same Jim Clark who started Netscape—a company that did much to make Java successful. 

# 1993 &#8211; 1994

The Green project (with a new name of “First Person, Inc.”) spent all of 1993 and half of 1994 looking for people to buy its technology. No one was found. (Patrick Naughton, one of the founders of the group and the person who ended up doing most of the marketing, claims to have accumulated 300,000 air miles in trying to sell the technology.) First Person was dissolved in 1994. While all of this was going on at Sun, the World Wide Web part of the Internet was growing bigger and bigger. The key to the World Wide Web was the browser translating hypertext pages to the screen. In 1994, most people were using Mosaic, a noncommercial web browser that came out of the supercomputing center at the University of Illinois in 1993. (Mosaic was partially written by Marc Andreessen as an undergraduate student on a workstudy project, for $6.85 an hour. He moved on to fame and fortune as one of the cofounders and the chief of technology at Netscape.) In the SunWorld interview, Gosling says that in mid-1994, the language developers realized that “We could build a real cool browser. It was one of the few things in the client/server mainstream that needed some of the weird things we’d done: architecture-neutral, real-time, reliable, secure—issues that weren’t terribly important in the workstation world. So we built a browser.” 

# 1995

The actual browser was built by Patrick Naughton and Jonathan Payne and evolved into the HotJava browser, which was designed to show off the power of Java. The browser was capable of executing Java code inside web pages. This “proof of technology” was shown at SunWorld ’95 on May 23, 1995, and inspired the Java craze that continues today 

# 1996 &#8211; 1997

Sun released the first version of Java in early 1996. People quickly realized that Java 1.0 was not going to cut it for serious application development. Sure, you could use Java 1.0 to make a nervous text applet that moved text randomly around in a canvas. But you couldn’t even print in Java 1.0. To be blunt, Java 1.0 was not ready for prime time. Its successor, version 1.1, filled in the most obvious gaps, greatly improved the reflection capability, and added a new event model for GUI programming. It was still rather limited, though. 

# 1998 &#8211; 1999

The big news of the 1998 JavaOne conference was the upcoming release of Java 1.2, which replaced the early toylike GUI and graphics toolkits with sophisticated scalable versions. Three days after its release in December 1998, Sun’s marketing department changed the name to the catchy Java 2 Standard Edition Software Development Kit Version 1.2. 

Besides the **Standard Edition**, two other editions were introduced: the Micro Edition for embedded devices such as cell phones, and the **Enterprise Edition** for server-side processing. 

# 2000 &#8211; 2005

Versions **1.3** and **1.4** of the Standard Edition were incremental improvements over the initial Java 2 release, with an ever-growing standard library, increased performance, and, of course, quite a few bug fixes. 

Version **5.0** was the first release since version 1.1 that updated the Java language in significant ways. (This version was originally numbered 1.5, but the version number jumped to 5.0 at the 2004 JavaOne conference.) After many years of research, generic types (roughly comparable to C++ templates) have been added —the challenge was to add this feature without requiring changes in the virtual machine. Several other useful language features were inspired by C#: a “for each” loop, autoboxing, and annotations. 

# 2006 &#8211; 2013

Version **6** (without the .0 suffix) was released at the end of 2006. Again, there were no language changes but additional performance improvements and library enhancements. 

As datacenters increasingly relied on commodity hardware instead of specialized servers, Sun Microsystems fell on hard times and was purchased by Oracle in 2009. The development of Java stalled for a long time. In 2011, Oracle released a new version, with simple enhancements, as **Java 7**. 

# 2014

In 2014, the release of **Java 8** followed, with the most significant changes to the Java language in almost two decades. Java 8 embraces a “functional” style of programming that makes it easy to express computations that can be executed concurrently. All programming languages must evolve to stay relevant, and Java has shown a remarkable capacity to do so. 

# 2017

The main feature of **Java 9** goes all the way back to 2008. At that time, Mark Reinhold, the chief engineer of the Java platform, started an effort to break up the huge, monolithic Java platform. This was to be achieved by introducing modules, self-contained units of code that provide a specific functionality. It took eleven years to design and implement a module system that is a good fit for the Java platform, and it remains to be seen whether it is also a good fit for Java applications and libraries. 

# 2018 &#8211; till now

Starting in 2018, Java versions are released every six months, to enable faster introduction of features. Certain versions, such as **Java 11**, are designated as long-term support versions. At this moment (February 1, 2020) the newest version of Java is **Java 14**.
