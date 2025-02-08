# Class #1,2,3 — Software Design — 13,16,20th Jan

<p>In order for us to tackle learning software development design patterns, we have to understand the backbone of 
this topic, the language used in this area, factors that come into view when we are working with design patterns, 
etc.
<br/><br/>
Often, it is recommended to have a <code>glossary of terms</code> related to this topic, to design patterns such that when 
reviewing information outside this class, or when following course materials, that we are able to understand the 
ideals and principles behind this field.
</p>

## Glossary of Terms

<procedure title="Glossary of Terms" collapsible="true">
<deflist>
<def title="System">
A <code>set of modules, components</code> that are related to each other in such a way that they attempt to <code>provide functionality</code> and solve a problem.
</def>

<def title="Requirement Acquisition">
The process of gathering information about the problems requirements, <code>what is to be solved, what is to be allowed in the codebase, what the user wants, expects, desires, and how this can be implemented down into code</code>
</def>

<def title="Object-Oriented Design">
The solution to the problem at hand. This aspect of our work has various levels: backend level (hardware, connectivity, etc), business logic (business requirements were we can apply design patterns)
</def>

<def title="Software Design Patterns">
Solutions to a problem in software development that have been proven over time to solve similar issues in various fields and under different constraints. <code>These are solutions that the community of developers over the years have found, and have pruned to be adaptable in various fields.</code>
</def>

<def title="Version Control Systems">
Systems that allow us to manage versions of our projects, communication, error management, branching, etc.
</def>

<def title="Build Management Systems">
Systems that allow us to work collaboratively, manage dependencies, build configurations, deployment configurations, etc.
</def>

<def title="Testing Frameworks">
Programs that allow us to handle testing patterns, like unit testing, etc.
</def>

<def title="Concept">
General idea, conceived in the mind, abstracted away from reality
</def>

<def title="Abstract">
Expressing a property, characteristic, attribute, or relationships, seen separately from other characteristics in an object.
</def>

<def title="Abstraction">
Simplification of an object or concept, focusing on attributes relevant to the problem at hand.
</def>

<def title="Artifact">
A tangible product generated during the system development process, such as UML diagrams, project plans, error lists, etc.
</def>

<def title="UML (Unified Modeling Language)">
A graphical language used to specify, construct, and document the artifacts of software systems, as well as to model business processes and other non-software systems.
</def>

<def title="Functional Requirements">
Describes what the system should do.
</def>

<def title="Non-Functional Requirements">
Describes how the system should deliver certain features, such as response times, system load, fault tolerance, security, usability, graphical interface aesthetics, reliability, etc. – think quality of service.
</def>
</deflist>
</procedure>


## Introduction to System Development

<p>When we are in the process of designing software, be it for our purposes or for an external company, one key question to ask 
ourselves, or the team we are working with is <code>What do we want this system to do for us?</code>. That is the 
job of the development team to figure out, the task at hand is <code>identify what the client wants, the ways the 
development team can achieve these goals, etc.
</code><br/><br/>
Inherently then, analysis and design of systems boils down to a couple of important characteristics and points to 
keep in mind
</p>
<procedure>
<list columns="2">
<li><b><format color="CornFlowerBlue">Analysis done in the problem-space of our case</format></b>:</li>
<li><b><format color="CornFlowerBlue">Design done in the solution-space of our case</format></b></li> 
<li><b><format color="CornFlowerBlue">Always define the way we will implement certain system 
functionality</format></b></li> 
<li><b><format color="CornFlowerBlue">Always define hardware and software components needed</format></b>: </li>
<li><b><format color="CornFlowerBlue">What do we need to program?*</format></b></li>
</list>
</procedure>

### Software Design Patterns


<p>Software design patterns are like step by step solutions that you can get in Math textbooks or for physics 
problems. These are tested, tried and true, correct and useful solutions, software solutions that can be applied 
with minimal changes into any scenario where they fit, and make our code more robust, simpler to read, elegant, 
reusable, and extensible. Specifically, they are defined as</p>
<procedure>
<p>" Software design patterns are <code>fragments of design that solve common, and recurring problems</code>, with 
well defined and clear rules in OOP contexts and more, that are based on the software development's communities work 
on the field. "</p>
</procedure>
<p>Software Patterns have three main constituent parts <code>Name(Handler/Identifier), Problem, Solution, and 
Consequences
</code>
<br/><br/>
The ideas behind these parts are explained beneath.
</p>
<procedure>
<list>
<li><b><format color="CornFlowerBlue">Name(Handler)</format></b>: Identifier used to classify design patterns, its solutions, consequences, and the problem it solves rather quickly.</li> 
<li><b><format color="CornFlowerBlue">Problem</format></b>: Describes when to apply the pattern. It explains the 
problem and its context. Sometimes, these also include some <code>conditions that must be met before it makes sense 
to apply these. 
</code></li> 
<li><b><format color="CornFlowerBlue">Solution</format></b>: describes the elements that make up the solution to a 
problem (Relationships, responsibilities, and collaborations). The solution <code>provides an abstract 
description of a design problem and how an arrangement of these items solve it</code></li>
<li><b><format color="CornFlowerBlue">Consequences</format></b>: present the results, tradeoffs, and possible 
consequences of applying a design pattern. These are <code>useful for deciding and evaluating between 
alternative design patterns</code>, as well as <code>knowing the costs and benefits of their application</code></li> 
</list>
</procedure>
<p>Following this introduction, I present three examples of these structures (only in words for now)</p>
<procedure>
<tabs>
<tab title="Information Expert">
  <list>
    <li><b>Purpose:</b> Assign the responsibility of handling certain logic or behavior to the class that has the necessary information to perform it.</li>
    <li><b>Problem:</b> How do you decide which class should take responsibility for a specific behavior?</li>
    <li><b>Solution:</b> Assign the responsibility to the class that has the information required to fulfill it, reducing dependency and improving cohesion.</li>
  </list>
</tab>
<tab title="Singleton">
  <list>
    <li><b>Purpose:</b> Ensure that a class has only one instance and provide a global point of access to it.</li>
    <li><b>Problem:</b> You need to manage shared resources, configurations, or instances that should not be duplicated.</li>
    <li><b>Solution:</b> Create a single instance of the class and provide a way to access it globally, often implemented with private constructors and static methods.</li>
  </list>
</tab>
<tab title="Factory Method">
  <list>
    <li><b>Purpose:</b> Define an interface for creating objects, but allow subclasses to alter the type of objects that will be created.</li>
    <li><b>Problem:</b> You need to delegate the instantiation logic of specific objects to subclasses without tightly coupling the code to a single concrete class.</li>
    <li><b>Solution:</b> Create a factory method that subclasses override to specify the class of the object being created.</li>
  </list>
</tab>
<tab title="Observer">
  <list>
    <li><b>Purpose:</b> Define a one-to-many dependency between objects so that when one object changes state, all its dependents are notified and updated automatically.</li>
    <li><b>Problem:</b> You need to maintain consistency and communication between related objects, but they should remain loosely coupled.</li>
    <li><b>Solution:</b> Establish a subject class that maintains a list of observers and notifies them of any changes to its state.</li>
  </list>
</tab>
</tabs>
</procedure>

### Version Control and Source Code Building
<p>Both of these tasks often take tremendous amounts of time to get right. On the one hand, setting up and 
controlling our software, its components, and the entirety of the system, architecting it around various developers, 
or even across different systems without overlap is <code>hard</code>. On the other hand, controlling our source 
code, the way its built in one system and the way it should be built in any other, sharing dependencies, managing 
versions and distributions, versioning, etc.
<br/><br/>
While these are concepts closely related with the DevOps field, even for simple projects it is imperative that we 
know and work on these, as they will be tools we use throughout our careers, as well as in day to day side-project 
work, as these show competence in development
</p>

### Introduction to System-level, Module-Level and Class-Level Testing
<p>In our areas, testing is a base that is always talked about and used in the development cycle and the life cycle 
of a project or product. Additionally, There are different types of development that are based on either testing as 
we develop <code>(Test-Driven-Development TDD)</code>, or testing as we design <code>(Design-Driven-Testing). At the 
moment I will not go deep into each of them, however I will list some of the types of tests and testing 
methodologies that exist in software.
</code></p>
<procedure>
<list columns="2">
<li><b><format color="CornFlowerBlue">Unit Testing</format></b>: Involves reviewing and testing individual components or units of the software in isolation. The primary purpose is to ensure that each small portion of the code functions correctly. Typically performed by developers during development, it tests methods, functions, or small logical pieces.</li>

<li><b><format color="CornFlowerBlue">Requirement-Implementation Testing | Acceptance Testing</format></b>: Involves reviewing and testing the entirety of the finished product to assess whether it meets the agreed-upon requirements, functionality, and goals. The focus is on verifying that the product matches the expectations of end-users or stakeholders, ensuring it satisfies business needs and use cases.</li>

<li><b><format color="CornFlowerBlue">Black-box Testing</format></b>: Focuses on testing the functionality of an application without knowing the internal code structure or design. Testers interact with the application based on its inputs and expected outputs, verifying if it behaves as intended. This type is suitable for acceptance and system testing stages as it validates the product from the user’s perspective.</li>

<li><b><format color="CornFlowerBlue">White-box Testing</format></b>: Involves testing the internal logic and structure of the code. Testers need knowledge of the implementation and can test paths, data flows, and control logic at the class or integration level. Primarily used for unit or integration testing, it focuses on testing internal functions and ensures code coverage.</li>

<li><b><format color="CornFlowerBlue">Integration Testing</format></b>: Tests the interactions between multiple components or modules within a system to ensure they function as intended when combined. It evaluates how data is passed and processed among units, detecting any defects in the interfaces between modules.</li>

<li><b><format color="CornFlowerBlue">System Testing</format></b>: Validates the software system as a whole by testing all integrated modules and components. This testing type ensures that the complete solution works as expected in its intended environment, covering functional and non-functional testing.</li>

<li><b><format color="CornFlowerBlue">Regression Testing</format></b>: Focuses on re-running tests after changes (e.g., bug fixes, updates) to ensure the newly introduced code has not broken or negatively affected existing functionality. It ensures system reliability throughout development iterations.</li>

<li><b><format color="CornFlowerBlue">Smoke Testing</format></b>: A preliminary test to verify that the core functionalities of a system work as expected. Typically conducted after a new build, it ensures that the most critical features are performing before deeper testing processes begin.</li>

<li><b><format color="CornFlowerBlue">Exploratory Testing</format></b>: A manual testing approach where testers 
interact with the application dynamically without predefined scripts. It focuses on uncovering edge cases, 
discovering unidentified issues, and exploring the application intuitively as a user would.</li>

<li><b><format color="CornFlowerBlue">Performance Testing</format></b>: Measures how well the system performs under 
different load conditions or stress levels. Subtypes include Load Testing (validating application behavior under 
expected load), Stress Testing (pushing the system beyond its capacity), and Scalability Testing (measuring the 
software's ability to handle growth).</li>

<li><b><format color="CornFlowerBlue">Usability Testing</format></b>: Ensures that the application is intuitive, 
user-friendly, and meets the expectations of its intended audience. This kind of testing emphasizes the user 
experience and interface design, based on the end-user's interaction.</li>

<li><b><format color="CornFlowerBlue">Security Testing</format></b>: Focuses on identifying vulnerabilities, 
weaknesses, and potential threats in the software to prevent unauthorized access, data breaches, or functionality 
disruption. It often involves penetration testing or ethical hacking approaches.</li>
</list>
</procedure>

<procedure>
<tabs>
<tab title="Design-Driven Testing">
<list>
<li><b>Purpose:</b> Ensure software design quality by deriving tests from design specifications and architectural decisions before implementation.</li>
<li><b>Problem:</b> How to validate that the implementation adheres to the intended design and architectural constraints?</li>
<li><b>Solution:</b> Create tests based on design artifacts, interfaces, and architectural patterns, focusing on validating design decisions and component interactions rather than just functionality.</li>
<li><b>Steps:</b> 
  <ul>
    <li>Analyze design artifacts such as UML diagrams, architecture documentation, and technical specifications.</li>
    <li>Write tests covering design specifications like relationships, interfaces, and expected workflows.</li>
    <li>Iteratively validate the implementation to ensure compliance with the design.</li>
  </ul>
</li>
<li><b>Example:</b> Test the interaction between modules in a banking application, ensuring the payment module adheres to sequence diagrams with accurate transfer flows.</li>
<li><b>Use Cases:</b> 
  <ul>
    <li>Enterprise systems demanding alignment with rigid architectural frameworks.</li>
    <li>Microservice architectures where validating service dependencies is critical.</li>
    <li>Mission-critical systems in healthcare, aerospace, or finance where regulatory compliance is required.</li>
  </ul>
</li>
</list>
</tab>
<tab title="Test-Driven Development">
<list>
<li><b>Purpose:</b> Drive software development through short, iterative cycles where tests are written before the actual code implementation.</li>
<li><b>Problem:</b> How to ensure code correctness, maintainability, and design quality while developing new features?</li>
<li><b>Solution:</b> Follow the Red-Green-Refactor cycle: write a failing test first (Red), implement the minimum code to make it pass (Green), then improve the code without changing its behavior (Refactor).</li>
<li><b>Steps:</b> 
  <ul>
    <li>Define a test based on expected functionality or user requirements.</li>
    <li>Write the minimum code required to pass the test.</li>
    <li>Refactor the code and remove duplications where necessary.</li>
  </ul>
</li>
<li><b>Example:</b> While building a shopping cart application, the `calculateTotal()` function is developed iteratively using failing tests for various cases (e.g., empty cart, discounts).</li>
<li><b>Use Cases:</b> 
  <ul>
    <li>Agile development environments requiring fast, error-free iterations.</li>
    <li>Startups that need to ensure rapid quality delivery of new features.</li>
    <li>Open-source projects where test cases serve as both verification and implicit documentation.</li>
    <li>Bug fixing, where tests are created for known issues to prevent regression.</li>
  </ul>
</li>
</list>
</tab>
</tabs>
</procedure>

### Agile-Framework Software Development
<p>Agile is a widely adopted software development framework that emphasizes iterative progress, collaboration, and 
adaptability. Its foundation lies in delivering small, valuable increments of work while accommodating changing 
requirements throughout the lifecycle of a project. Agile focuses on customer satisfaction, flexibility, and 
fostering close communication between developers and stakeholders.</p>

<procedure>
  <list columns="2">
    <li><b>Iterative Progress</b>: Agile breaks down projects into smaller, manageable sprints with a time-boxed duration, allowing teams to consistently deliver functional increments of the product.</li>
    <li><b><format color="CornFlowerBlue">Customer Collaboration</format></b>: Agile prioritizes regular communication 
with stakeholders to align deliverables with evolving customer needs.</li>
    <li><b><format color="CornFlowerBlue">Flexibility</format></b>: The framework is designed to adapt to changes and 
new requirements, even in the later stages of development.</li>
    <li><b>Focus on Communication</b>: Agile promotes cross-functional teamwork and continuous feedback to improve efficiency and quality.</li>
    <li><b>Emphasis on Quality</b>: Testing is integrated into each iteration, ensuring that quality checks occur frequently to meet high standards.</li>
    <li><b><format color="CornFlowerBlue">Lightweight Documentation</format></b>: Agile minimizes excessive 
documentation, focusing instead on working software and collaborative interaction.</li>
  </list>
</procedure>

## Object-Oriented Software analysis and Design
<p>Object-Oriented design in software is the same process as above, only that the software solutions that are trying 
to solve come in the way of Object-Oriented programs, implementations, etc. This means that while we still look to 
analyze deeply each system requirement based on the field we are working in, and while we also attempt to design a 
conceptual solution for the problem, we do so differently here, now we think in terms of <code>hierarchies, 
abstractions, generalizations, etc.</code>
<br/><br/>
In general, these are some of the key points to keep in mind for both <code>analysis and design in terms of OO</code>
</p>
<procedure>
<tabs>
<tab title="Analysis in OO Software Design">
<list>
<li><b>Purpose:</b> The analysis phase focuses on understanding the problem domain and gathering system requirements from stakeholders.</li>
<li><b>Key Actions:</b>
  <ul>
    <li>Identify user and stakeholder needs by analyzing real-world scenarios.</li>
    <li>Define the required functionality of the system in specific and measurable terms.</li>
    <li>Break down the problem domain into logical components and relationships.</li>
    <li>Ensure requirements are free of ambiguity and are complete to guide design and implementation.</li>
  </ul>
</li>
<li><b>Challenges:</b> 
  <ul>
    <li>Requirements often change as business needs evolve, impacting design and implementation.</li>
    <li>Stakeholders may have difficulty articulating their needs precisely.</li>
  </ul>
</li>
<li><b>Outcome:</b> A clear, detailed requirements specification that forms the foundation for effective design and implementation.</li>
</list>
</tab>

<tab title="Design in OO Software Design">
<list>
<li><b>Purpose:</b> Create a conceptual framework for solving the problem, typically expressed as high-level abstractions and designs.</li>
<li><b>Characteristics:</b>
  <ul>
    <li>Design is abstraction-based and focuses on structuring the solution without diving into implementation details.</li>
    <li>Addresses system architecture, including component relationships and their interactions.</li>
    <li>Prioritizes user-facing requirements aligned with stakeholder needs over technical constraints.</li>
    <li>Documents design artifacts, such as UML diagrams, that provide a blueprint for implementation.</li>
  </ul>
</li>
<li><b>Challenges:</b>
  <ul>
    <li>Design artifacts operate at an abstract level but may fail to account for real-world implementation complexities.</li>
    <li>It often assumes ideal performance, infrastructure, and technical flexibility, which may not align with practical constraints.</li>
  </ul>
</li>
<li><b>Addressing Design vs. Implementation Gap:</b>
  <ul>
    <li>Use iterative designs with developer feedback to ensure feasibility.</li>
    <li>Create prototypes to validate design assumptions and detect potential challenges early.</li>
    <li>Involve developers and implementers during the design phase to surface technical constraints.</li>
    <li>Document assumptions, constraints, and non-functional requirements (e.g., security and performance).</li>
  </ul>
</li>
<li><b>Outcome:</b> A robust design blueprint that serves as the basis for implementation while accounting for practical challenges.</li>
</list>
</tab>

<tab title="Implementation in OO Software Design">
<list>
<li><b>Purpose:</b> Translate design blueprints into working software by implementing the detailed, technical features and functionality.</li>
<li><b>Characteristics:</b>
  <ul>
    <li>Deals with concrete technical details, such as frameworks, libraries, and APIs.</li>
    <li>Focuses on ensuring adherence to the high-level design while managing technical and performance constraints.</li>
    <li>Requires handling edge cases and technical complexities (e.g., error handling, security, scalability).</li>
    <li>Emphasizes code quality, maintainability, and alignment with design intent.</li>
  </ul>
</li>
<li><b>Challenges:</b>
  <ul>
    <li>Abstraction gaps between design and implementation can lead to misalignment.</li>
    <li>Implementation must account for unforeseen constraints like legacy systems, infrastructure limitations, and technical debt.</li>
    <li>Design assumptions (e.g., ideal conditions) may not be practical when realized in the implementation phase.</li>
  </ul>
</li>
<li><b>Strategies for Success:</b>
  <ul>
    <li>Adopt iterative coding approaches to continuously validate and refine the implementation.</li>
    <li>Use design patterns that accommodate flexibility and real-world scenarios.</li>
    <li>Include technical spikes or proof-of-concept tasks to address uncertainties early in the project cycle.</li>
    <li>Maintain open collaboration and feedback loops between designers and implementers.</li>
  </ul>
</li>
<li><b>Outcome:</b> Fully functioning software that adheres to design specifications, meets user needs, and operates effectively within technical constraints.</li>
</list>
</tab>
</tabs>
</procedure>

### Objects in OO Software Design
#### What is an object?
<p>An object can be defined as <code>"an entity that has state [properties and their values during the lifetime of 
an object],behaviour [refers to the way an object acts and interacts in terms of state changes and method 
invocations],and identity [properties of an object that distinguish it from others]</code></p>

#### How to Create an Object?
<p>The process of creating an object is not as simple as creating a class or abstracting a section of our code to 
this style of implementation. Rather, the process involves a series of steps or key points to think about</p>
<procedure>
<list style="decimal">
<li><b><format color="CornFlowerBlue">Discovering essential domain concepts</format></b> [these can be found in the 
requirements that were initially derived from meetings and conversations with stake-holders.] 
</li>
<li><b><format color="CornFlowerBlue">Creating apropiate objects based on domain concepts</format></b>: </li>
<li><b><format color="CornFlowerBlue">Ensuring object cohesion (degree to which elements belong 
together)</format></b> [We should take a look at high cohesion and low coupling between classes and modules in our 
projects]
</li> 
<li><b><format color="CornFlowerBlue">Maintaining low coupling between objects</format></b> [there should be low 
interconnection and interdependence between objects]</li>
<li><b><format color="CornFlowerBlue">Understanding the field of study (domain) of our requirements</format></b></li>
</list>
</procedure>

#### Detail Extraction
<p>For us to do as such and follow these steps, then, we also have to think about <b>detail extraction</b>. Sometimes our 
projects do not require a class model every component of the environment, but it does require some 
<code>important, or rather, essential, concepts to be modelled</code>. For this reason we have to then think about 
<code>extracting terms, concepts and parts of the field of study (those directly related to our project), and then 
use those to inspire classes in software
</code></p>
<p>This also involves <code>defining a glossary of terms for our project</code>, such that <b>all of our 
stake-holders are on the same page about the terms used in all phases of software development</b></p>

#### Characteristics of an Object
<p>An object in any OO project, has both static and dynamic properties, fields, or parameters internally that alter 
its behavior and define its identity. In essence, these properties, specifically <code>static properties</code>, 
are those that give way for all the dynamic parts of an object.</p>

#### Responsibilities of an Object
<p>An object ion an OO environment has a set of defined responsibilities, sort of like a contract that it has to 
abide to, such that it couples well with the rest of our codebase</p>
<procedure>
<list columns="1">
<li><b><format color="CornFlowerBlue">Services that an object provides to another object</format></b></li> 
<li><b><format color="CornFlowerBlue">The Protocol of an object, defining the order in which methods 
within it are called</format></b></li> 
<li><b><format color="CornFlowerBlue">The rol it plays within the entire project (Client Object, 
Server Object, Proxy Object, etc.)</format></b></li> 
</list>
</procedure>

#### Interfaces and Implementation
<p>A class provides, in a way, a view of the methods, like a contract, that it can have with other classes and 
clients. That is, <code>"it provides, or acts, as a contract between abstraction and clients"</code>. Interfaces on 
the other hand <code>capture the contract, and divide them through forward facing and inward facing visibillity of 
parts in our class
</code>
<br/><br/>
In this sense, interfaces control visibility through access modifiers (including package-private modifiers).
<br/><br/>
The main idea behind having interfaces, and access modifiers is to reduce the avenues of error, possible external 
affectations both coming in and going out, by changes in our class.
</p>

#### Relationships Between Classes and Visibility Rules in UML
<p>When it comes to UML diagrams, there are some rules that are important to define when it comes to class 
hierarchies and class member distinctions. While wrappers like what we know from online creators and even the 
IntelliJ UML viewer does not present these symbols directly; we should, either way, be familiar with them</p>
<procedure>
<tabs>
  <tab title="Relationships between classes and their symbols">
    <img alt="RelationshipsBetweenClasses.png" src="RelationshipsBetweenClasses.png"/>
  </tab>
  <tab title="Access Modifiers and visibility symbols">
    <img alt="AccessModifiersSymbology.png" src="AccessModifiersSymbology.png"/>
  </tab>
</tabs>
</procedure>

## Requirements — A Closer Look

<p>Understanding requirements is one of the fundamental steps in software design. By defining what is needed from the system and its behavior, developers can shape the solution effectively. Alongside requirements, identifying use cases helps clarify specific interactions between the system and its users or other systems. Below, we explore these concepts further.</p>

<procedure>
<tabs>
<tab title="Requirements">
  <list>
    <li><b>Definition:</b> Requirements describe the functions and constraints of a system. They detail what the system should do, the conditions it needs to fulfill, and the limitations it must adhere to.</li>
    <li><b>Types:</b>
      <ul>
        <li><b>Functional Requirements:</b> Specify the actions the system must be able to perform, such as calculations, data processing, and user interactions.</li>
        <li><b>Non-Functional Requirements:</b> Define constraints and qualities the system should have, such as performance, scalability, security, and usability.</li>
      </ul>
    </li>
    <li><b>Purpose:</b> To provide a clear and concise guideline for developers and stakeholders to ensure the final product meets expectations and solves the intended problems.</li>
    <li><b>Examples:</b>
      <ul>
        <li><b>Functional:</b> The system must allow users to log in using their email and a password.</li>
        <li><b>Non-Functional:</b> The system must handle up to 10,000 concurrent user logins without significant performance degradation.</li>
      </ul>
    </li>
  </list>
</tab>
<tab title="Use Cases">
  <list>
    <li><b>Definition:</b> Use cases are detailed descriptions of how users or other systems interact with the software to achieve specific goals. Each use case represents a single scenario of interaction.</li>
    <li><b>Components:</b>
      <ul>
        <li><b>Actors:</b> The users or external systems that interact with the software.</li>
        <li><b>Goals:</b> The objectives or outcomes the actors aim to accomplish by interacting with the software.</li>
        <li><b>Scenario:</b> The steps or sequence of interactions between the actor and the system to achieve the goal.</li>
      </ul>
    </li>
    <li><b>Purpose:</b> Use cases help to clarify requirements by illustrating specific interactions. They provide better understanding for developers, testers, and all involved stakeholders.</li>
    <li><b>Examples:</b>
      <ul>
        <li><b>Login Use Case:</b> The user enters their credentials, the system validates them, and the user is granted access if the login is successful.</li>
        <li><b>Shopping Cart Use Case:</b> The user adds items to their cart, reviews them, and proceeds to checkout for purchase.</li>
      </ul>
    </li>
  </list>
</tab>
</tabs>
</procedure>

<p>Based on the previous definition, it is clear that both complement each other, and while some might consider use 
cases as requirements just more verbose, they are two different topics. Requirements, inform the developer 
of functionality, of specific classes or behaviors that their program should handle. On the other hand, Use cases 
give the developer information about how the company expects the user to behave in their program, allowing the 
developer to optimize for correct use and foresee incorrect one.</p>
<p>While we might be tempted to move forward and into domain models(a topic that we will be 
covering later on), it is important for us to take a look at another core component 
<i><code>Use Case Analysis</code></i></p>

### Use Case Analysis
<p>Use case analysis consist on finding the environment where our program will be used, effectively analyzing the 
<code>actors that will be related to our software but cannot control directly</code>, these can be <b>users, 
databases, time, etc.</b>
<br/><br/>
Having gotten our actors, we should <code>find and define use cases</code>, which means finding and deciding, and 
effectively modeling <b>the interaction that each user would have with our system</b>, starting from the human 
component, all the way down to software components both company-wise or external. Each of these use cases should 
be thoroughly described, <code>creating a set of descriptions, both in desired outcomes and testing methodology 
information
</code>, through which to base our expectations for the results in these use case testing that we can 
architect from use case definitions.
</p>
<note>
As we have established both for OOD, and for normal design analysis, we should always keep a 
<i><b><code>glossary of terms</code></b>, where we define general context-based words for the project</i> such that 
everyone is capable of understanding the project at any moment.
</note>
<p>
Besides the importance that we are giving to use cases, the core background task that had to be done before is 
<code>domain analysis</code>, making sure that we have defined everything required in here (processes, actors, 
information, terms, relationships, etc), such that we <i><code>articulate correctly a set of use cases</code></i>
</p>

#### Finding Use Cases
<p>
There are some questions that are useful for us to identify actors within a domain model.</p>

<procedure title="Use Case Analysis | Key Questions to Determine Actors" collapsible="true">
<list>
<li><b><format color="CornFlowerBlue">Who is interested in the system?</format></b>
    <list columns="2">
        <li>Direct stakeholders (users, operators, administrators)</li>
        <li>Indirect stakeholders (management, investors)</li>
        <li>Third-party integrators</li>
        <li>Competitors and market analysts</li>
        <li>Business process owners</li>
        <li>Quality assurance teams</li>
        <li>Regulatory compliance officers</li>
        <li>External auditors</li>
    </list>
</li>

<li><b><format color="CornFlowerBlue">Who is likely to use the system?</format></b>
    <list columns="2">
        <li>Primary users (daily interaction)</li>
        <li>Secondary users (occasional interaction)</li>
        <li>System administrators</li>
        <li>Support staff</li>
        <li>Emergency response personnel</li>
        <li>Help desk operators</li>
    </list>
</li>

<li><b><format color="CornFlowerBlue">Who will benefit from the system?</format></b>
    <list columns="2">
        <li>End users gaining functionality</li>
        <li>Organizations improving efficiency</li>
        <li>Customers receiving services</li>
        <li>Partners leveraging capabilities</li>
        <li>Society (if applicable)</li>
        <li>Business stakeholders</li>
    </list>
</li>

<li><b><format color="CornFlowerBlue">Who will supply information to the system?</format></b>
    <list columns="2">
        <li>Manual data entry personnel</li>
        <li>Automated data feeds</li>
        <li>IoT devices and sensors</li>
        <li>External APIs and services</li>
        <li>Legacy system integrations</li>
        <li>Real-time data streams</li>
    </list>
</li>

<li><b><format color="CornFlowerBlue">Who will maintain information in the system?</format></b>
    <list columns="2">
        <li>Database administrators</li>
        <li>Content managers</li>
        <li>System operators</li>
        <li>Automated maintenance processes</li>
        <li>Data stewards</li>
        <li>Compliance officers</li>
    </list>
</li>

<li><b><format color="CornFlowerBlue">Where in the organization is the system to be used?</format></b>
    <list columns="2">
        <li>Physical locations</li>
        <li>Departments and divisions</li>
        <li>Remote access requirements</li>
        <li>Geographic distribution</li>
        <li>Security zones</li>
        <li>Disaster recovery sites</li>
    </list>
</li>

<li><b><format color="CornFlowerBlue">Who manages system security?</format></b>
    <list columns="2">
        <li>Security administrators</li>
        <li>Compliance teams</li>
        <li>Access control managers</li>
        <li>Audit personnel</li>
        <li>Security operations center</li>
        <li>Risk management teams</li>
    </list>
</li>

<li><b><format color="CornFlowerBlue">Who handles system failures?</format></b>
    <list columns="2">
        <li>Technical support teams</li>
        <li>Operations teams</li>
        <li>Emergency response teams</li>
        <li>Backup administrators</li>
        <li>Service desk personnel</li>
        <li>System reliability engineers</li>
    </list>
</li>

<li><b><format color="CornFlowerBlue">Who provides training and documentation?</format></b>
    <list columns="2">
        <li>Training department</li>
        <li>Technical writers</li>
        <li>Subject matter experts</li>
        <li>Knowledge base maintainers</li>
        <li>User experience teams</li>
        <li>Documentation specialists</li>
    </list>
</li>

</list>
</procedure>


<warning><p>It is important, of course, to understand the core foundational technological knowledge 
that someone will have, and to address their needs if they are to be in touch with our product.
</p></warning>

<p>Despite how simple the use case definition might be, finding these, and describing them can be hard.
<br/><br/>
For example, a use case should <i><code>specify a sequence of actions, communications to one or more 
actors, etc.</code></i>. Additionally, we should take a look at what comes out of a use case application, the 
outcomes that we expect. This is defined as <b><code>a use case should yield an observable result to a 
particular actor</code>, while also, <code>maintaining funcitonality from the point of view of entities 
from outside the system</code></b>
<br/><br/>
Now, there will be other sections in this document that take a look at use case analysis in 
depth, with examples and how to model them in UML. For now this brief introduction as to how to 
find these definitions and the questions our use cases should keep in mind, lead us to domain 
modeling, that <code>as we defined earlier</code> <i><b><code>is the step that had to be done 
prior to even deciding on use cases
</code></b></i>
</p>


### Domain Models

<p>In object-oriented analysis, domain models are an essential tool for representing the underlying concepts and relationships in a particular problem space. They help in breaking down the domain into manageable parts, focusing on its key elements to create a clear and shared understanding among stakeholders. Below, we expand on the definition, characteristics, and examples of domain models.</p>

<procedure>
<list>
<li><b>Definition:</b> A domain model is a conceptual representation of the real-world entities, attributes, and relationships within a specific domain. It forms the foundation for understanding a problem and acts as a blueprint for creating the system's structure.</li>
<li><b>Purpose:</b> Domain models provide clarity on the essential aspects of a problem, ensuring that software solutions are aligned closely with real-world requirements. They guide the development team in capturing the business logic accurately.</li>
<li><b>Characteristics:</b>
  <ul>
    <li>Comprised of <b>concepts</b>, <b>attributes</b>, and <b>associations</b> that are relevant to the domain.</li>
    <li>Aimed at representing real-world ideas rather than software objects or code structures.</li>
    <li>Fosters communication between technical and non-technical stakeholders by using a shared vocabulary.</li>
    <li>Dynamic and adaptable, as it evolves with better understanding of the problem space.</li>
  </ul>
</li>
<li><b>Process:</b> 
  <ul>
    <li>Analyze the problem domain and identify key concepts (e.g., roles, entities, or processes).</li>
    <li>Define the attributes that describe each concept.</li>
    <li>Establish meaningful associations between concepts to describe their interactions and dependencies.</li>
    <li>Create diagrams or models that visually represent these elements.</li>
  </ul>
</li>
<li><b>Examples:</b>
  <ul>
    <li>A shopping domain model may include concepts like <b>"Customer"</b>, <b>"Product"</b>, and <b>"Order"</b>. Attributes would include things like "Customer Name," "Product ID," and "Order Date," while associations could show that a Customer places an Order which contains Products.</li>
    <li>A library management domain may model <b>"Books"</b>, <b>"Members"</b>, and <b>"Borrowing Transactions."</b></li>
  </ul>
</li>
</list>
</procedure>
<p>Additionally, below we present to ways to represent these concepts. The first of these is Domain Models</p>
<procedure>
<p>A simple UML representation of the shopping domain model, including key concepts, attributes, and associations:</p>
<code-block lang="PLANTUML">
@startuml
class Customer {
  - customerID: int
  - name: String
  - email: String
}

class Order {
- orderID: int
- orderDate: Date
- totalAmount: float
  }

class Product {
- productID: int
- productName: String
- price: float
  }

Customer "1" -left- "many" Order : places
Order "1" -left- "many" Product : contains
@enduml
</code-block>
<p><b>Description:</b></p>
<list>
<li><b>Customer:</b> Represents a person placing an order. Each customer has a unique ID, name, and email.</li>
<li><b>Order:</b> Represents a single purchase attempt. An order is placed by one customer and can contain multiple products. Orders have attributes such as order ID, date, and total amount.</li>
<li><b>Product:</b> Represents an item in the shopping system. Products are associated with multiple orders and contain attributes like ID, name, and price.</li>
<li><b>Relationships:</b>
  <ul>
    <li><b>Customer places Order:</b> A customer can place multiple orders (1-to-many relationship).</li>
    <li><b>Order contains Product:</b> An order can contain several products (many-to-many relationship).</li>
  </ul>
</li>
</list>
</procedure>
<p>Moreover, another interesting representation is Partial Interaction Diagrams, which are defined and designed as 
follows</p>
<procedure>
<code-block lang="MERMAID">
sequenceDiagram
    Customer->>Order: Places an Order
    Order->>Product: Adds Products to the Order
    Product-->>Order: Confirms Product Details
    Order-->>Customer: Sends Order Confirmation
</code-block>
<p><b>Description:</b></p>
<list>
<li><b>Customer Places Order:</b> The customer initiates the process by placing an order in the system.</li>
<li><b>Order Adds Products:</b> After the order is created, it interacts with the product catalog to add products to the order.</li>
<li><b>Product Confirms Details:</b> The product entity responds by confirming details like availability, price, and other specifics.</li>
<li><b>Order Sends Confirmation:</b> Finally, after products are added successfully, the system sends an order confirmation back to the customer.</li>
</list>
</procedure>

#### Domain Modeling
<note><p>While the concept of a domain model was introduced first (by virtue of it having 
been the 
first 
part of a previous presentation given out in class), it is not purely in this order, that things 
happen. Rather, domain modeling comes first, and a domain model is an outcome of it
</p></note>
<p>Domain modeling is an activity, or the process through which we 
<i><b><code>obtain a domain model to be used in our software design and analysis</code></b></i>. 
On its own, domain modeling is an activity that focuses on <i>creating conceptual 
representations of a specific problem domain. </i> Effectively, it focuses on finding 
<i><b>key entities, their attributes, actions, behaviors, relationships, and constraints</b></i> 
within a system.
<br/><br/>
The following definition list will shine a bit more light on these definitions
</p>
<deflist>
<def title="Domain Modeling">
<i>Domain modeling refers to the process of identifying key actors, entities, attributes, 
actions, behaviors, relationships, and constraints within a system.</i> It is the process 
through which we obtain a <i><b><code>domain model</code></b></i></def>
<def title="Domain Model">
<i>A Domain model is a conceptualization of our real world, focusing on real world entities 
(classes), their attributes, and relationships within a domain, that attempts to explain a domain 
space.
</i>
</def>
</deflist>
<p>There are some key characteristics that I would like to list out for domain modeling, as 
these were not fully described through our domain model section in this document</p>
<procedure title="Domain Modeling | Keynotes" collapsible="false">
<list>
<li><b><format color="CornFlowerBlue">What does it focus on?</format></b>: on 
<b><code>real-world classes and how these relate to each other</code></b></li>
<li><b><format color="CornFlowerBlue">How does it organize these classes? </format></b>: around 
key abstractions.</li>
<li><b><format color="CornFlowerBlue">Does it keep a glossary of terms?</format></b>: it uses 
the domain model as a project glossary.</li>
<li><b><format color="CornFlowerBlue">How does it relate to use cases?</format></b>: the idea 
of domain modeling is to <i><b>use the domain model obtained</b></i> as a base for creating 
use cases, linking the objects and classes within the domain model to use cases (behavioral 
requirements)</li> 
</list>
</procedure>
<p>As can be noted through our paragraph above, we have noticed how it is important to focus on 
<code>using the domain model to</code><b><code>organize a glossary of terms, 
effectively creating a common vocabulary for people in the project</code></b>. As we talked 
about in the general characteristics of a domain model, it represents <i>basic conceptos or 
mental models of the problem domain, using simplified class diagrams with associations
</i>
<br/><br/>
It is here were we need to think about high cohesion, loose coupling</p>
<deflist type="full">
<def title="High Cohesion vs. Loose Coupling">
<p>The idea of high cohesion and loose coupling is a software design and analysis motto that 
effectively means that we should write classes, in a broader sense, that are related to each 
other. However, we should <b>not write classes that are too dependent on each other</b>. This then 
means that we should architect our system such that classes are cohesive, related, but not 
coupled, dependent.</p>
<p>The balance between these principles creates systems that are:</p>

- More maintainable: Changes in one part have minimal impact on others
- More reusable: Components can be easily repurposed
- More testable: Components can be tested in isolation
- More scalable: Components can be modified or replaced without system-wide changes
<p>In practice, this means:</p>

- Using interfaces and abstract classes to define contracts
- Implementing dependency injection
- Following the Single Responsibility Principle
- Avoiding direct object creation within classes
- Minimizing shared state between components

</def>
<def title="High Cohesion">
<p><b>High Cohesion</b> refers to the degree to which elements within a class or module belong 
together. A highly cohesive class:</p>

- Has a single, well-defined responsibility
- Contains methods that are strongly related to each other
- Manages a specific aspect of the system
- Is easier to maintain and understand

<p>For example, a 'UserAuthentication' class that only handles user authentication tasks exhibits
high cohesion.
</p>
</def>
<def title="Loose Coupling">
<p><b>Loose Coupling</b> describes the degree of dependency between different classes or modules. 
Loosely coupled classes:</p>

- Interact through well-defined interfaces
- Can be modified independently of each other
- Are easier to test and maintain
- Can be replaced with alternative implementations
- 
<p>
For example, using interfaces to define communication between services rather than direct class 
dependencies demonstrates loose coupling.
</p>

</def>
</deflist>

<p>Lastly, it is important for us to know that through <b><code>domain modeling</code></b>, and 
its outcome, domain models, we should be <b><code>always thinking about nouns and 
noun phrases</code></b>, extracting these from high level requirements to create use cases</p>

### Design Classes

<p>Design classes statically represent the blueprint and structure of a system's classes, often visualized 
through diagrams. They act as a bridge between the concept of a system's dynamic behavior and its static components, 
helping us capture the higher-level architecture of the software.</p>

<p>Design classes typically encapsulate a variety of aspects necessary for defining an object-oriented system. They 
include critical properties, such as attributes (data the class holds), methods (operations on the data), visibility 
(public, private, or protected entities), and the relationships (dependencies, associations, inheritances) between 
the classes.</p>

<p><b>Characteristics of Design Classes:</b></p>
<list>
<li><b><format color="CornFlowerBlue">Encapsulation:</format></b> Design classes are built around the principle of encapsulating data and its related behavior into a single entity, enabling a modular and organized system structure.</li>
<li><b><format color="CornFlowerBlue">Abstraction:</format></b> They simplify the representation of the real-world entities within the context of the problem being solved, focusing only on the most relevant properties and behaviors.</li>
<li><b><format color="CornFlowerBlue">Reusability:</format></b> Properly defined design classes can be reused across multiple parts of the system or even across different systems.</li>
<li><b><format color="CornFlowerBlue">Relationships:</format></b> They often capture the interactions and relationships between entities, identifying aspects such as composition, aggregation, inheritance, and dependencies.</li>
<li><b><format color="CornFlowerBlue">Static by Nature:</format></b> Design classes depict structural aspects that do not change over time, in contrast to dynamic models like sequence diagrams or state diagrams.</li>
</list>

<p><b>Methodologies for Implementing Design Classes:</b></p>
<list>
<li><b><format color="CornFlowerBlue">Class Diagram Creation:</format></b> The most common methodology involves using UML (Unified Modeling Language) diagrams to visualize and organize the design classes. These include their attributes, methods, and relationships, ensuring clarity in representation.</li>
<li><b><format color="CornFlowerBlue">Refinement Through Interaction Diagrams:</format></b> Often, interaction diagrams like sequence or collaboration diagrams can provide crucial insights into dynamic behaviors, which are subsequently translated into the static views of design classes.</li>
<li><b><format color="CornFlowerBlue">Focus on Responsibility Assignment:</format></b> Each design class is assigned specific responsibilities to ensure separation of concerns, a key principle in object-oriented design. This ensures the system remains modular and easier to maintain.</li>
<li><b><format color="CornFlowerBlue">Alignment with Requirements:</format></b> Design classes are mapped directly to system requirements, ensuring that each system feature or module is adequately addressed in the design.</li>
<li><b><format color="CornFlowerBlue">Iterative Refinement:</format></b> Design classes are not static throughout the development lifecycle. They are refined iteratively as new requirements are introduced or as gaps in initial designs are closed.</li>
</list>

<p><b>Benefits of Design Classes:</b></p>
<list>
<li><b><format color="CornFlowerBlue">Systematic Development:</format></b> They provide a formalized approach to defining how various system components will interact, leading to a more systematic and predictable development process.</li>
<li><b><format color="CornFlowerBlue">Improved Communication:</format></b> By using tools like UML diagrams, teams can more effectively communicate the system's design to stakeholders, from developers to non-technical clients.</li>
<li><b><format color="CornFlowerBlue">Maintainability:</format></b> Clear and modular class design makes it easier to maintain the codebase, implement changes, and find defects.</li>
<li><b><format color="CornFlowerBlue">Supports Testing:</format></b> The modular structure of design classes simplifies testing by defining independent units that can be analyzed in isolation.</li>
</list>

<p>Design classes are an essential foundation of well-structured software systems. They allow us to concretely 
define and visualize the components and their interrelations, ensuring the system aligns with requirements while 
adhering to object-oriented principles. These diagrams are not merely static entities but evolve as the system 
requirements are re-analyzed, improving their practicability and relevance in real-world applications.</p>

## UML Diagrams - A closer Look
<p>UML diagrams are products of UML, the unified modeling language, that allows both software and non-software teams 
to develop artifacts (diagrams, state diagrams, actions, project plans, etc), related to their business in such a 
way that they are visibly appealing and allow technical and non-technical users to understand the goals, 
requirements, and state of a project.
<br/><br/>
Generally, UML is used to <code>conceptually design key concepts about the domain of the problem we are trying to solve
</code>. Moreover, these diagrams are often seen from <code>the specification vantage point</code>, hence these often 
represent abstractions of software and components with specifications and interfaces. 
<br/><br/>
On the other hand, these do present also, views from the implementor point of view, as they also can be used to describe
software models, classes, or interfaces, and abstractions, through a technology like a language.
<br/><br/>
In UML, and in OO software design, there are <code>three basic types of classes</code> <b>that we must keep in 
mind</b> when we are developing an OO software project, and when we are going to use UML diagrams for their design 
and modeling. These are.
</p>
<procedure>
<tabs>
<tab title="Conceptual Class">
  <list>
    <li><b>Definition:</b> A conceptual class represents key real-world concepts within the problem domain. These are abstractions focused on modeling real-world entities and their relationships as they pertain to the specific problem.</li>
    <li><b>Key Concepts:</b>
      <ul>
        <li>Conceptual classes represent <b>real-world concepts</b> relevant to the problem space.</li>
        <li>These classes are <b>abstractions</b>, with no implementation or system-specific details.</li>
        <li>They are identified during the <b>analysis phase</b> of development and help refine the understanding of the problem domain.</li>
        <li>They often include relationships and roles between entities but exclude methods or attributes.</li>
      </ul>
    </li>
    <li><b>Purpose:</b> To provide a high-level understanding of the problem space and facilitate communication between developers and stakeholders.</li>
    <li><b>Examples:</b>
      <ul>
        <li>In a library system: Book, Member, Librarian.</li>
        <li>In an e-commerce system: Customer, Product, Order.</li>
      </ul>
    </li>
    <li><b>Possible UML Representation:</b> Use Class Diagrams to represent conceptual classes without attributes or methods. Focus on relationships between entities.</li>
  </list>
</tab>
<tab title="Software Class">
  <list>
    <li><b>Definition:</b> A software class is a specification of a software component that defines its attributes, operations (methods), and relationships. It is a structured translation of conceptual classes into software representations.</li>
    <li><b>Key Concepts:</b>
      <ul>
        <li>Software classes include <b>attributes</b> and <b>methods</b> that define the behavior of the class.</li>
        <li>They typically describe <b>relationships</b> such as inheritance, composition, aggregation, or dependencies.</li>
        <li>Software classes act as a bridge between conceptual classes and implementation classes, maintaining some level of abstraction.</li>
        <li>They serve as reusable blueprints for implementation in object-oriented design.</li>
      </ul>
    </li>
    <li><b>Purpose:</b> To define the structural and behavioral aspects of a class for software development while ensuring modularity, scalability, and reusability.</li>
    <li><b>Examples:</b>
      <ul>
        <li>A "Customer" class with attributes (name, email) and methods (placeOrder, updateDetails).</li>
        <li>A "Product" class with attributes (name, price) and methods (checkAvailability, calculateDiscount).</li>
      </ul>
    </li>
    <li><b>Possible UML Representation:</b> Represent software classes in detailed Class Diagrams that include attributes and methods while showing their relationships with other classes.</li>
  </list>
</tab>
<tab title="Implementation Class">
  <list>
    <li><b>Definition:</b> An implementation class is a class written in a specific programming language (e.g., Java, Python, C++) that contains the real, executable implementation of the software class. These classes include method definitions, data storage details, and access controls.</li>
    <li><b>Key Concepts:</b>
      <ul>
        <li>Implementation classes are <b>language-specific</b> and use syntax and constructs of the respective programming language.</li>
        <li>They include <b>access modifiers</b> (e.g., public, private) to control which parts of the code can access attributes and methods.</li>
        <li>These classes hold the <b>actual implementation</b> of methods and data structures needed for execution.</li>
        <li>Interactions, external library usage, and specific business logic are defined here.</li>
      </ul>
    </li>
    <li><b>Purpose:</b> To provide the functional and executable implementation of a software class in the system using the chosen programming language and environment.</li>
    <li><b>Examples:</b>
      <ul>
        <li>A "Customer" Java class with private variables such as name and email and public methods like "placeOrder()" or "updateDetails()."</li>
        <li>A "Product" Python class with attributes like price and methods like "get_discounted_price()".</li>
      </ul>
    </li>
    <li><b>Possible UML Representation:</b> Implementation classes may still use Class Diagrams, but these are often supplemented by actual source code instead of purely visual representations.</li>
  </list>
</tab>
</tabs>
</procedure>

## Iterative Development VS Cascade Development

<p>Software projects can be approached using a variety of development methodologies, each catering to different types of projects, requirements, or team dynamics. Two widely discussed approaches are cascade and iterative development. They differ fundamentally in philosophy, implementation, and adaptability to changes during development. Below we take a more in-depth look at each methodology, their characteristics, and what to do before and during the early stages of a project.</p>

<procedure>
<tabs>
<tab title="Cascade Development">
  <list>
    <li><b>Definition:</b> Cascade development, also known as the Waterfall model, is a sequential software development process where each phase is completed before moving on to the next one. It is linear and rigid with little room for iteration or flexibility.</li>
    <li><b>Key Characteristics:</b>
      <ul>
        <li><b>Sequential Process:</b> Phases like requirements, design, implementation, and testing are completed one after the other.</li>
        <li><b>Fixed Requirements:</b> The requirements are determined, documented, and agreed upon before development begins. Changes are typically not supported after this phase.</li>
        <li><b>Predictable:</b> The systematic, step-by-step approach creates a predictable timeline and deliverables.</li>
        <li><b>Documentation Heavy:</b> Emphasis is placed on documenting every stage to track progress and keep the project organized.</li>
        <li><b>Longer Feedback Loop:</b> User feedback generally happens late in the process, typically after the implementation phase.</li>
      </ul>
    </li>
    <li><b>Before Starting the Project:</b>
      <ul>
        <li>Perform a <b>feasibility analysis</b> of the project to determine its viability.</li>
        <li>Identify <b>fixed requirements</b> and ensure they are complete and agreed upon by stakeholders.</li>
        <li>Estimate the <b>time</b> and <b>cost</b> required for development.</li>
        <li>Define the <b>scope of the project</b> and any constraints.</li>
        <li>Create detailed <b>project documentation</b> for each phase.</li>
      </ul>
    </li>
    <li><b>First Steps in Development:</b>
      <ul>
        <li>Design the <b>overall system architecture</b> based on agreed requirements.</li>
        <li>Break down the process into clearly defined phases (e.g., requirements, design, implementation, testing).</li>
        <li>Focus entirely on a single phase at any given time. For example, do not begin coding until the design phase is complete.</li>
      </ul>
    </li>
  </list>
</tab>
<tab title="Iterative Development">
  <list>
    <li><b>Definition:</b> Iterative development is a cyclical approach where the overall project development is divided into multiple small iterations. Each iteration encompasses all phases—requirements, design, implementation, and testing—and delivers a functional subset of the total system.</li>
    <li><b>Key Characteristics:</b>
      <ul>
        <li><b>Focus on Cycles:</b> Development is conducted in short, iterative cycles that allow regular evaluation and adjustments.</li>
        <li><b>Flexible Requirements:</b> The system is not required to have complete specifications at the start, and new requirements can emerge during development.</li>
        <li><b>Risk Management:</b> High-risk and high-value aspects are prioritized and tackled during the initial iterations.</li>
        <li><b>User Feedback:</b> Users are continuously involved to provide feedback after each iteration.</li>
        <li><b>Incremental Delivery:</b> Deliverables are presented progressively after each cycle, building on top of previous functional components.</li>
      </ul>
    </li>
    <li><b>Before Starting the Project:</b>
      <ul>
        <li>Identify <b>high-priority system requirements</b> and risks to address first.</li>
        <li>Define the <b>scope of each iteration</b>.</li>
        <li>Estimate <b>time and resources</b> required for the entire project, but treat each iteration as a mini-project.</li>
        <li>Prepare for <b>continuous collaboration</b> with users and stakeholders.</li>
      </ul>
    </li>
    <li><b>First Iterations:</b>
      <ul>
        <li>Tackle the <b>highest-risk and highest-value components</b> of the system first.</li>
        <li>Focus on creating a strong <b>core architecture</b> that will sustain later iterations.</li>
        <li>Deliver functional subsets of the system for <b>user feedback and evaluation.</b></li>
        <li>Incorporate user input to refine designs and address potential issues early.</li>
        <li>Document progress after each cycle to maintain project clarity.</li>
      </ul>
    </li>
  </list>
</tab>
<tab title="Incremental Development">
  <list>
    <li><b>Definition:</b> Incremental development is a process where the functionality of the system is divided into smaller, independent pieces, called increments, each of which adds functionality to the system with every completed step. It overlaps with iterative development but focuses more on adding completed features to the system.</li>
    <li><b>Key Characteristics:</b>
      <ul>
        <li><b>Feature-Based Increments:</b> Each increment builds and improves the system by delivering completely functional units (features or modules).</li>
        <li><b>Modularity:</b> Divides the system into independent components, making it easier to manage and test each piece.</li>
        <li><b>Frequent Delivery:</b> Deliver usable parts of the system at regular intervals, increasing stakeholder satisfaction and providing early value.</li>
        <li><b>Integration Focus:</b> Emphasizes integrating increments seamlessly into the existing system architecture.</li>
        <li><b>Continuous Testing:</b> Each increment is tested and evaluated before integrating it into the complete system.</li>
      </ul>
    </li>
    <li><b>Before Starting the Project:</b>
      <ul>
        <li>Identify independent, <b>modular functionality</b> that can be developed and delivered incrementally.</li>
        <li>Estimate <b>time and resources</b> for each increment.</li>
        <li>Ensure the system's <b>architecture supports incremental integration</b>.</li>
        <li>Prepare to <b>prioritize functionality</b>, focusing first on the most important or foundational modules.</li>
      </ul>
    </li>
    <li><b>First Steps in Development:</b>
      <ul>
        <li>Deliver fully working <b>core modules or features</b> before advancing to less critical functionality.</li>
        <li>Focus on testing and <b>stable integration</b> of every delivered increment.</li>
        <li>Solicit <b>feedback from users</b> on each increment to refine future iterations.</li>
      </ul>
    </li>
  </list>
</tab>
</tabs>
</procedure>

<p>In conclusion, cascade development is suitable for projects where requirements are fixed and changes are unlikely, while iterative and incremental development provide more adaptability, flexibility, and collaboration, making them better suited for dynamic and evolving projects.</p>


