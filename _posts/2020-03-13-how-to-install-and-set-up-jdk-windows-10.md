---
title: 'How to Install and Set up JDK (on Windows 10)'
last_modified_at: 2020-03-13T09:03:43+00:00
categories:
  - Blog
tags:
  - Post Formats
  - readability
  - standard
---
In this tutorial, I will show you how to install and set up the Java Development Kit (JDK) on Windows 10. You can find a <a href="https://www.youtube.com/watch?v=epRyzvnndIo" target="_blank" rel="noreferrer noopener" aria-label="video (opens in a new tab)">video</a> of the whole process, step-by-step, on my YouTube channel. If you are new in programming and you don&#8217;t know what is JDK, read <a rel="noreferrer noopener" aria-label="this blog post (opens in a new tab)" href="https://www.dev-guide.org/the-java-language-specification-api-ide-jdk-jre-and-jvm/?preview=true&_thumbnail_id=415" target="_blank">this blog post</a> first.

## Step 1: 

### Downloading the JDK 

The most complete and up-to-date versions of the Java Development Kit are available from Oracle for Linux, Mac OS, Solaris, and Windows. To download the Java Development Kit (JDK) are available from Oracle for Linux, Mac OS, Solaris, and Windows. Versions in various states of development exist for many other platforms, but those versions are licensed and distributed by the vendors of those platforms. 

Somewhat confusingly, versions 1.2 through 1.4 of the kit were known as the Java SDK (Software Development Kit). You will still find occasional references to the old term.  
Up to Java 10, there is also a Java Runtime Environment (JRE) that contains only the virtual machine. That is not what you want as a developer. It is intended for end users who have no need for the compiler.

Next, you’ll see the term Java SE everywhere. That is the Java Standard Edition, in contrast to Java EE (Enterprise Edition) and Java ME (Micro Edition). You might run into the term Java 2 that was coined in 1998 when the marketing folks at Sun felt that a fractional version number increment did not properly communicate the momentous advances of JDK 1.2. However, since they had that insight only after the release, they decided to keep the version number 1.2 for the development kit. Subsequent releases were numbered 1.3, 1.4, and 5.0. The platform, however, was renamed from Java to Java 2. The next version of the Java Standard Edition was called Java SE 6, followed by Java SE 7 and Java SE 8. However, the “internal” version numbers are 1.6.0, 1.7.0, and 1.8.0. In Java 9, there were 32-bit and 64-bit versions of the Java Development Kit. The 32-bit versions are no longer developed by Oracle. You need to have a 64-bit operating system to use the Oracle JDK. 

  *  **Visit the web site at <a rel="noreferrer noopener" href="http://www.oracle.com/technetwork/java/javase/downloads" target="_blank">www.oracle.com/technetwork/java/javase/downloads</a> and download the JDK for Windows.**  
  
    **_NOTE:_** You want the JDK (Java SE Development Kit), not the JRE. Accept the license agreement and download the file.  
    

<div class="wp-block-image">
  <figure class="aligncenter size-large is-resized"><a href="https://www.dev-guide.org/wp-content/uploads/2020/03/how-to-install-and-set-up-jdk-windows-10-1-1.png" target="_blank" rel="noreferrer noopener"><img loading="lazy" src="https://www.dev-guide.org/wp-content/uploads/2020/03/how-to-install-and-set-up-jdk-windows-10-1-1-1024x554.png" alt="" class="wp-image-450" width="768" height="416" srcset="https://www.dev-guide.org/wp-content/uploads/2020/03/how-to-install-and-set-up-jdk-windows-10-1-1-1024x554.png 1024w, https://www.dev-guide.org/wp-content/uploads/2020/03/how-to-install-and-set-up-jdk-windows-10-1-1-300x162.png 300w, https://www.dev-guide.org/wp-content/uploads/2020/03/how-to-install-and-set-up-jdk-windows-10-1-1-768x416.png 768w, https://www.dev-guide.org/wp-content/uploads/2020/03/how-to-install-and-set-up-jdk-windows-10-1-1-1536x831.png 1536w, https://www.dev-guide.org/wp-content/uploads/2020/03/how-to-install-and-set-up-jdk-windows-10-1-1.png 1696w" sizes="(max-width: 768px) 100vw, 768px" /></a></figure>
</div>

## 

## Step 2: 

### Installing the JDK 

After downloading the JDK, you need to install it and figure out where it was installed &#8211; you’ll need that information later. 

  * Launch the setup program. You will be asked where to install the JDK. The default location will be a path name, such as **C:\Program Files\Java\jdk-x.0.x** (where **x.0.x** is the current version of JDK).

<div class="wp-block-image">
  <figure class="aligncenter size-large is-resized"><a href="https://www.dev-guide.org/wp-content/uploads/2020/03/how-to-install-and-set-up-jdk-windows-10-2.png" target="_blank" rel="noreferrer noopener"><img loading="lazy" src="https://www.dev-guide.org/wp-content/uploads/2020/03/how-to-install-and-set-up-jdk-windows-10-2-1024x722.png" alt="" class="wp-image-466" width="447" height="314" srcset="https://www.dev-guide.org/wp-content/uploads/2020/03/how-to-install-and-set-up-jdk-windows-10-2-1024x722.png 1024w, https://www.dev-guide.org/wp-content/uploads/2020/03/how-to-install-and-set-up-jdk-windows-10-2-300x211.png 300w, https://www.dev-guide.org/wp-content/uploads/2020/03/how-to-install-and-set-up-jdk-windows-10-2-768x541.png 768w, https://www.dev-guide.org/wp-content/uploads/2020/03/how-to-install-and-set-up-jdk-windows-10-2.png 1064w" sizes="(max-width: 447px) 100vw, 447px" /></a></figure>
</div>

## 

## Step 3: 

### Setting up the JDK 

The installation directory is denoted as **jdk**. For example, when referring to the **jdk/bin** directory, I mean the directory with a name such as  
**C:\Program Files\Java\jdk-x.0.x\bin** . 

When you install the JDK, you need to carry out one additional step: Add the **jdk/bin** directory to the executable path &#8211; the list of directories that the operating system traverses to locate executable files.

  * Type “**environment**” into the search bar of the Windows Settings, and select “**Edit environment variables**”. 
  * Then in the newly opened windows, select the **Advanced tab** and click the **Environment Variables** button. 
  * Locate and select a variable named **Path** in the **System Variables** list. 
  * Click the **Edit** button, then the **New** button, and add an entry with the **jdk\bin** directory. (As in the previous example, it will be **C:\Program Files**\**Java\jdk-11.0.4\bin** .)<figure class="wp-block-image size-large">

<a href="https://www.dev-guide.org/wp-content/uploads/2020/03/how-to-install-and-set-up-jdk-windows-10-3.png" target="_blank" rel="noreferrer noopener"><img loading="lazy" width="1024" height="516" src="https://www.dev-guide.org/wp-content/uploads/2020/03/how-to-install-and-set-up-jdk-windows-10-3-1024x516.png" alt="" class="wp-image-452" srcset="https://www.dev-guide.org/wp-content/uploads/2020/03/how-to-install-and-set-up-jdk-windows-10-3-1024x516.png 1024w, https://www.dev-guide.org/wp-content/uploads/2020/03/how-to-install-and-set-up-jdk-windows-10-3-300x151.png 300w, https://www.dev-guide.org/wp-content/uploads/2020/03/how-to-install-and-set-up-jdk-windows-10-3-768x387.png 768w, https://www.dev-guide.org/wp-content/uploads/2020/03/how-to-install-and-set-up-jdk-windows-10-3-1536x774.png 1536w, https://www.dev-guide.org/wp-content/uploads/2020/03/how-to-install-and-set-up-jdk-windows-10-3.png 1572w" sizes="(max-width: 1024px) 100vw, 1024px" /></a></figure> 

## 

## Step 4: 

### Check the Installation 

Last, to be sure that your JDK was set up and configurated, open Command Prompt windows and type this command:

<pre class="wp-block-code"><code lang="bash" class="language-bash">java -version</code></pre>



If there is outputted your version of JDK, everything is ready.

<div class="wp-block-image">
  <figure class="aligncenter size-large is-resized"><a href="https://www.dev-guide.org/wp-content/uploads/2020/03/how-to-install-and-set-up-jdk-windows-10-4.png" target="_blank" rel="noreferrer noopener"><img loading="lazy" src="https://www.dev-guide.org/wp-content/uploads/2020/03/how-to-install-and-set-up-jdk-windows-10-4.png" alt="" class="wp-image-469" width="480" height="265" srcset="https://www.dev-guide.org/wp-content/uploads/2020/03/how-to-install-and-set-up-jdk-windows-10-4.png 824w, https://www.dev-guide.org/wp-content/uploads/2020/03/how-to-install-and-set-up-jdk-windows-10-4-300x166.png 300w, https://www.dev-guide.org/wp-content/uploads/2020/03/how-to-install-and-set-up-jdk-windows-10-4-768x425.png 768w" sizes="(max-width: 480px) 100vw, 480px" /></a></figure>
</div>
