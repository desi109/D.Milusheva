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

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/ufdjrpv462htl0gvn2xt.jpg) 
 
---

# Pipe and Filter
#### Definition

Pipe and Filter is architectural pattern, which has independent entities:
- filters ***(components)*** - which perform transformations on data and process the input they receive
- pipes ***(connectors)*** - which serve as connectors for the stream of data being transformed, each connected to the next component in the pipeline.

#### Description
The pattern of interaction in the pipe-and-filter pattern is haracterized by successive transformations of streams of data. As you can see in the diagram, the data flows in one direction. It starts at a data source, arrives at a filter’s input port(s) where processing is done at the component, and then, is passed via its output port(s) through a pipe to the next filter, and then eventually ends at the data target.

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/djkrhs2ml21aqulr6fsk.jpg)

#### When used
Commonly used in data-processing applications (both batch and transaction-based) where inputs are processed in separate stages to generate related outputs.

#### Examples 
The architectural pattern is very popular and used in many systems, such as the text-based utilities in the UNIX operating system. Whenever different data sets need to be manipulated in different ways, you should consider using the pipe and filter architecture. 
  - ***Compilers***: They perform language transformation. Input is in language e.g. Java and output is in machine language. In order to do that the input goes through various stages inside the compiler — these stages form the pipeline. The most commonly used division consists of 3 stages: front-end, middle-end, and back-end. The front-end is responsible for parsing the input language and performing syntax and semantic and then transforms it into an intermediate language. The middle-end takes the intermediate representation and usually performs several optimization steps on it, the resulting transformed program in is passed to the back-end which transforms it into language B.
Each level consists of several steps as well, and everything together forms the pipeline of the compiler.
![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/n1fdzvuomikukhawzgku.png)
  - ***UNIX Shell***: The Pipeline is one of the defining features of the UNIX shell, and obviously, the same goes for Linux, MacOS, and any other Unix-based or inspired systems.
In a nutshell, it allows you to tie the output of one program to the input of another. The benefit it brings is that you don’t have to save the results of one program before you can start processing it with another. The long-term and even more important benefit is that it encourages programs to be small and simple. There is no need for every program to include a word-counter if they can all be piped into wc. Similarly, no program needs to offer its own built-in pattern matching facilities, as it can be piped into grep. In the provided example, the input.txt is read and the output is then provided to grep as input which searches for the pattern “text” and then passes the results to sort, which sorts the results and outputs into the file, output.txt. 
```bash
cat input.txt | grep "text" | sort > output.txt
```
input.txt ➜ grep ➜ sort ➜ output.txt
  - ***ATM system***
    ![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/4h52uzbzqd0myxmh640s.png)

#### Advantages
- Easy and simple for composition and evolution
- Intuitive and easy to understand
- The filters are discrete: reusability and low coupling between components (modifiability)
- Concurrency support

#### Disadvantages
- Each filter must analyze its data
- Difficult to share global data
- Problems with reuse - e.g. functional
transformations with incompatible data
- The data transmission format must be
agreed
- Does not provide a way for filters to interact
together to solve a problem 

---
                   
# Data-centered 
#### Definition
The Data-Centered architecture consists of various components that communicate through a shared data warehouse. The data is centralized and all components can access/modify it. Shared data can be considered as a ***connector*** between ***components***.

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/7nyacdw74i00sj4ydfq0.png)

#### Description
In this style we have:
- Central data structure or data warehouse, which is responsible for ensuring permanent storage data. It represents the current state.
- Many independent components that work with the central data warehouse, perform calculations, and can return results.
Interactions or communication between components are carried out only through the data warehouse (can be considered as a connector). Data is the only means of communication between
customers. The flow of control differentiates architecture into two categories: ***Repository*** and ***Blackboard***.

Repository:
- The central data structure is passive and customers (components) of the data warehouse are active.
- Participating components check the repository of data for changes.
- No notifications are sent to the components.

Blackboard:
- The central data structure is active and the customers
and are passive.
- The logic flow is determined by the current state of data in the data warehouse.
- All components must be informed about changes in the data.

#### Examples 
- ***Databases*** - The most well-known examples of the data-centered architecture is a database architecture, in which the common database schema is created with data definition protocol – for example, a set of related tables with fields and data types in an RDBMS.
- ***Airline CRM System*** - CRM is a software system that manages personalized relationships with a company’s clients. Marketing campaigns, customer service, and cross-selling campaigns are usually managed with a CRM system.
- ***Web-based data services*** - Another example of data-centered architectures is the web architecture which has a common data schema (i.e. meta-structure of the Web) and follows hypermedia data model and processes communicate through the use of shared web-based data services.
- ***IDE***
![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/fsjop0q5om8aeu1njkjj.png)

#### Advantages
- Scalability - new components can be added
- Concurrency - all components can work in parallel
- Reuse - components are not direct communication with each other
- Centralized data management
- Better conditions for security, archiving, etc.
- The components are independent of the manufacturer data

#### Disadvantages
- High dependence between the data structure of storage and components
- Storage - single point of failure (single point of failure)
- Changes in data structure strongly affect customers
- Multiple sync issues components

---- 

# Layered 
#### Definition
Organizes the system into layers with related functionality
between each layer. Each layer offers services through an interface, but only for the layer which is directly above it and uses the services of the layer that is directly below it.
Thus, each layer represents:
• Server - for the top layer
• Client - for the bottom layer

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/zdgr748q1lnmk1iw6g19.png)

#### Description
Organizes the system into layers, with related functionality associated with each layer. A layer provides services to the layer above it, so the lowest level layers represent core services that are likely to be used throughout the system.

#### Examples 
- ***iLearn system*** - iLearn digital learning system has a four-layer architecture that follows this pattern.
![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/wsn71x1wzmizqn93jyrk.png)
- ***Open System Interconnection model*** - OSI model is a reference model and used for communicating with systems that are open for communication with other systems.
![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/yg99ms0z0zddmrjgktrq.png)
- ***Other 4-layered systems*** - The presentation layer contains all categories related to the presentation layer. The business layer contains business logic. The persistence layer is used for handling functions like object-relational mapping. The database layer is where all the data is stored.
![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/v8mm05axvr1ylf5e1ena.png)
- ***[Layered architecture - example app](https://github.com/zachgoll/layered-architecture-example-app)***

#### When used
Used when building new facilities on top of existing systems, when the development is spread across several teams with each team responsibility for a layer of functionality or when 
there is a requirement for multilevel security.

#### Advantages
- Each layer supports similar tasks (better cohesion)
- Abstraction - the internal structure of the layers is hidden
- Allows replacement of entire layers
- Additional services (e.g. authentication) can be provided in each layer to increase system reliability

#### Disadvantages
- Providing a clear separation between layers is often difficult - a high-level layer has to interact directly with a lower level
- Productivity can be a problem due to multiple levels of interpretation of service request as it is processed by everyone layer
 
---- 

# Client-Server
#### Definition
At Client-Server the functionality of the system is organized in services provided by servers. Customers are users of these services and access servers to take advantage of them. It is not necessary for a server to have information about its
customers.

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/ob31tcdia857stupot0o.png)

#### Description
In a client–server architecture, the system is presented as a set of services, with each service delivered by a separate server. Clients are users of these services and access servers to make
use of them.

#### Examples
- ***E-commerce shop***
- ***Client-Server Architecture for a film library***
![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/ned8a79zjd0xtz3vkmcj.png)
- ***Other common systems***
![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/y6ck97v4z1rd283069re.png)

#### When used
Used when data in a shared database has to be accessed from a range of locations. Because servers can be replicated, may also be used when the load on a system is variable.

#### Advantages
- Its centralized architecture facilitates the protection of
the data
- Servers can be distributed over a network
- Data is transferred through protocols that are not of interest from the platforms
- General functionality (e.g. printer) can be available to all customers
- The capacity of the Client and the Servers may change
separately

#### Disadvantages
- Productivity depends on the network as well as the system
- If too many customers simultaneously request data from the server may be overloaded
- Data packets can be changed during transmission.
- There may be management problems if the servers are
owned by various organizations

---- 

# Model-View-Controller
#### Definition
The system is structured in three logical components that interact with each other. The Model component manages system data and related data operations. View The View component defines and controls how data is presented to the user. The Controller component controls user interaction (e.g. keystrokes, etc.) and transmits these interactions to
the View or Model component.

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/uko1mbffg102gn9vrhqh.png)

#### Description
Separates presentation and interaction from the system data. The system is structured into three logical components that interact with each other. The Model component manages the system data and associated operations on that data. The View component defines and manages how the data is presented to the user. The Controller component manages user interaction (e.g., key presses, mouse clicks, etc.) and passes these interactions to the View and the Model.

#### Examples 
- Web frameworks such as: ***AngularJS*** and ***Ember.js*** all implement an MVC architecture, albeit in slightly different ways
- ***Web-based application system organized using the MVC pattern***
![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/jlmpcp65j4ogo7ebuw1t.png)

#### When used
Used when there are multiple ways to view and interact with data. Also used when the future requirements for interaction and presentation of data are unknown.

#### Advantages
- Great flexibility
- Easy to maintain and implement future improvements
- Clear separation between presentation logic and business logic
- Allows data to change independently their performance and vice versa
- Multiple views for one model

#### Disadvantages
- Even if the data model and interactions are simple,
this style can introduce complexity and require a lot of code
- Not suitable for small applications
- Performance issue with frequent updates in model
- Software developers using MVC must be skilled in many technologies

---- 

# Implicit Invocation
#### Definition
In the implicit call, instead of calling a procedure directly, the component can announce one or more events.
Other components in the system may register interest in
event by associating a procedure with the event. When the event is announced, the system calls everyone procedures that have been registered for the event. In this way the event calls procedures in other modules.

Explicit Invocation:
![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/sb4q32k0oahsw1fuehci.png)

Implicit Invocation:
![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/f9gcgb73b81g27n4r05m.png)

#### Description
The components in the system interact with each other through
broadcast events. Components work simultaneously and communicate through receiving or broadcasting events. The event bus can be considered as a connector - All components interact only through it. Events can also contain data.

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/9pp1e943to6hy523j8st.png)

<!-- #### Examples -->

#### Advantages
- Loose coupling 
- The components can be very heterogeneous
- Components are easy to replace/add/use again
- High efficiency for distributed systems - events are independent and can travel through the network
- Security - events are easily tracked and logged

#### Disadvantages
- The sequence of execution of components is difficult to be controlled
- It is not certain if there is a component that responds to a given event
- Large amounts of data are difficult to transfer from events
 Event bus - a single point of failure point of failure

---- 

# Microservices
#### Definition
Fowler & Lewis [1](http://martinfowler.com/articles/microservices.html) define the architectural style of micro-services (micro-services) as a “development approach of an application as a set of small services, each of who works in his own process and communicates with the light mechanisms. "

Microservices are targeted to applications where the connection loose coupling is possible and cohesion is possible strongest cohesion - (smart endpoints and dumb
pipes). Two ways are used (mainly) for communication - direct communication via light protocols (e.g. REST) ​​or messages/events (via the message/event bus).

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/d7mp4hjr8rb9dfjkikap.png)

#### Description
Microservices is an architectural style that structures an application as a collection of small autonomous services, modeled around a business domain.

#### [Examples](https://blog.dreamfactory.com/microservices-examples/)
- ***Amazon***
- ***Netflix*** 
- ***Uber***
![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/325ueil6h36gxylnvyw1.png)
- ***Etsy***

<!-- #### When used -->

#### Advantages
- Low coupling
- Improves modularity
- Promotes parallel development
- Promotes scalability 

#### Disadvantages
- Infrastructure costs are usually higher
- Integration testing complexity
- Service management and deployment
- Nanoservices anti pattern

---

##### Recommended Books/Links:
- Software Engineering Design: Theory and Practice by Carlos E. Otero
- Software Engineering by Ian Sommerville
- https://people.utm.my/noraini/files/2016/09/Chapter-4-Pattern-and-Styles.pdf
- http://www.softwareengineeringdesign.com/book-resources/chapter4/Chapter%204%20-%20Styles%20and%20Patterns%20in%20Architecture%20-%20Session%20II.pdf
