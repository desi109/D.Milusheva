---
title: "Architectural Styles"
excerpt_separator: "<!--more-->"
last_modified_at: 2021-03-29
categories:
  - Blog
tags:
  - Post Formats
  - readability
  - standard
---

The architecture of a system describes its major components, their relationships (structures), and how they interact with each other. Software architecture serves as a blueprint for a system. It provides an abstraction to manage the system complexity. Now we will look at the main architecural styles:
- Pipe and Filter
- Data-Centered
- Layered
- Client-Server
- Model-View-Controller
- Implicit Invocation
- Microservices

First let's give a description of:
- Components - calculation elements and elements for
data storage. Communication with other elements is
implemented through their interfaces ***(ports)***.
- Connectors - the architectural elements for communication.
Like the components communicate with other elements through
their interfaces ***(roles)***.
- Topology - Successful communication between 2 architectural
the element occurs when a role is attached to a port
and their interfaces are compatible. The architectural
elements, their interrelationships and limitations, represent
the ***topology***. 

[![architectural-styles-1](https://github.com/desi109/D.Milusheva/tree/gh-pages/assets/images/2021/03/2021-03-29-architectural-styles-1.jpg)]

<br>  

---- 

# Pipe and Filter
### Definition

Pipe and Filter is architectural pattern, which has independent entities:
- filters ***(components)*** - which perform transformations on data and process the input they receive
- pipes ***(connectors)*** - which serve as connectors for the stream of data being transformed, each connected to the next component in the pipeline.

### Description
The pattern of interaction in the pipe-and-filter pattern is haracterized by successive transformations of streams of data. As you can see in the diagram, the data flows in one direction. It starts at a data source, arrives at a filter’s input port(s) where processing is done at the component, and then, is passed via its output port(s) through a pipe to the next filter, and then eventually ends at the data target.

[![architectural-styles-2](https://github.com/desi109/D.Milusheva/tree/gh-pages/assets/images/2021/03/2021-03-29-architectural-styles-2.jpg)]

### Advantages

### Disadvantages

### Examples 
The architectural pattern is very popular and used in many systems, such as the text-based utilities in the UNIX operating system.Whenever different data sets need to be manipulated in different ways,, you should consider using the pipe and filter architecture. 
  - Compilers
  - UNIX Shell

<br>  

---- 
                   
# • Data–Centered 
### Definition
### Description
### Advantages
### Disadvantages
### Examples 

<br>  

---- 

# • Layered: 
https://medium.com/java-vault/layered-architecture-b2f4ebe8d587
### Definition
### Description
### Advantages
### Disadvantages
### Examples

<br>  

---- 

# • Client–Server
### Definition
### Description
### Advantages
### Disadvantages
### Examples

<br>  

---- 

# • Model–View–Controller
### Definition
### Description
### Advantages
### Disadvantages
### Examples 

<br>  

---- 

# • Implicit Invocation
### Definition
### Description
### Advantages
### Disadvantages
### Examples

<br>  

---- 

# • Microservices
### Definition
### Description
### Advantages
### Disadvantages
### Examples



```yaml
excerpt_separator: "<!--more-->"
```


### Recomended Books:
- Software Engineering Design: Theory and Practice by Carlos E. Otero
- Software Engineering by Ian Sommerville
