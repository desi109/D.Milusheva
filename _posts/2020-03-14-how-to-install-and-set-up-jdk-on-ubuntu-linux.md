---
title: 'How to Install and Set up JDK (on Ubuntu/Linux)'
last_modified_at: 2020-03-14T11:07:00+00:00
categories:
  - Blog
tags:
  - Post Formats
  - readability
  - standard
---
In this tutorial, I will show you how to install and set up the Java Development Kit (JDK) on Ubuntu/Linux. You can find a <a href="https://youtu.be/UGR_qS1XHIQ" target="_blank" rel="noreferrer noopener" aria-label=" (opens in a new tab)">video</a> of the whole process, step-by-step, on my YouTube channel. If you are new in programming and you don&#8217;t know what is JDK, read <a rel="noreferrer noopener" href="https://www.dev-guide.org/the-java-language-specification-api-ide-jdk-jre-and-jvm/?preview=true&_thumbnail_id=415" target="_blank">this blog post</a> first. 

The most complete and up-to-date versions of the Java Development Kit are available from Oracle for Linux, Mac OS, Solaris, and Windows. To download the Java Development Kit (JDK) are available from Oracle for Linux, Mac OS, Solaris, and Windows. Versions in various states of development exist for many other platforms, but those versions are licensed and distributed by the vendors of those platforms. 

Somewhat confusingly, versions 1.2 through 1.4 of the kit were known as the Java SDK (Software Development Kit). You will still find occasional references to the old term.  
Up to Java 10, there is also a Java Runtime Environment (JRE) that contains only the virtual machine. That is not what you want as a developer. It is intended for end users who have no need for the compiler.

Next, you’ll see the term Java SE everywhere. That is the Java Standard Edition, in contrast to Java EE (Enterprise Edition) and Java ME (Micro Edition). You might run into the term Java 2 that was coined in 1998 when the marketing folks at Sun felt that a fractional version number increment did not properly communicate the momentous advances of JDK 1.2. However, since they had that insight only after the release, they decided to keep the version number 1.2 for the development kit. Subsequent releases were numbered 1.3, 1.4, and 5.0. The platform, however, was renamed from Java to Java 2. The next version of the Java Standard Edition was called Java SE 6, followed by Java SE 7 and Java SE 8. However, the “internal” version numbers are 1.6.0, 1.7.0, and 1.8.0. In Java 9, there were 32-bit and 64-bit versions of the Java Development Kit. The 32-bit versions are no longer developed by Oracle. You need to have a 64-bit operating system to use the Oracle JDK. 

## 

## Let&#8217;s Get Started!

  * **Open a new terminal. You can click the right button on your desktop screen.**  
    
  * **Now with the next command, we will add the PPA repository.**  
    PPA stands for Personal Package Archive and it is a repository in Linux or simply we can say that it is a collection of files that has information about various software.

<pre class="wp-block-code"><code lang="bash" class="language-bash">sudo add-apt-repository ppa:linuxuprising/java</code></pre>



  *  **Run the second command.**  
    `apt-get update`&nbsp;downloads the package lists from all repositories and PPAs, and &#8220;updates&#8221; them to get information on the newest versions.

<pre class="wp-block-code"><code lang="bash" class="language-bash">sudo apt-get update</code></pre>



  * **Install JDK with the next command.**

<pre class="wp-block-code"><code lang="bash" class="language-bash">sudo apt-get install oracle-java13-set-default</code></pre>

  * **Set installed JDK as default.**

<pre class="wp-block-code"><code lang="bash" class="language-bash">sudo apt install oracle-java13-set-default</code></pre>



  * **Check the installation.**  
    To be sure that your JDK was set up and configurated, open a new terminal and type this command: 

<pre class="wp-block-code"><code lang="bash" class="language-bash">java --version</code></pre>



If there is outputted your version of JDK, everything is ready.
