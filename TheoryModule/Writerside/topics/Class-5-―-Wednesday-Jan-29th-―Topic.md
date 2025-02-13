# Class #5 ― Monday 3rd, Wednesday 5th, Monday 10th Feb 2025  

> The following will contain information about <b>a practical application of domain modeling, domain models, and use 
> case analysis to create an architectural view of a to-be-implemented application. </b> The content will be broken 
> down into sections, taking great care to make it concise and robust, while maintaining flexibility and implementation 
> agnosticism. This document will contain some of the overview of my design process, and while we are at it, I will 
> use Eclipse's capella or Change Vision Astah to manage these projects.


## Monday 3rd Class ― Choosing the right tools
<p>Often work in groups not only comes down to project management and a balance of power within the group, or the 
affinity of each other within the boundaries of this group, but to the tooling that is used to keep everything afloat.
</p>
<p>In my case, I am used to using github, workflows, and I am a documentation centric individual, while some others 
might not be that documentation centric. Moreover, and honestly sadly, I do not have a group as of the time of 
writing this. Therefore, I will try to keep the work that I want to do simple and to some extent educational when it 
comes to this area of computer science, project management, design, etc.
</p>
<p>The main idea here is to use github to manage the program and to keep branches for working both in UML diagrams, 
etc. Since Astah or Capella do not have GitHub integration, etc.</p>
<note>This class was mostly spend working on the project found in the Project section, I will 
not be continuing this class record.
</note>

## Wednesday 5h Class ― Robustness Diagrams
<p>Robustness diagrams are one of the diagram models from UML that we are going to review in 
our upcoming classes.</p>

### Robustness Diagrams ― Definitions
<p>A robustness diagram is a type of UML diagram that comes about by analyzing each use case, 
<i><code>the idea is to analyze each use case and define a set of objects that it 
involves internally</code></i>. These diagrams then, serve as a detailed design of what we are 
defining in a use case, linking it with objects. Effectively, we can think of these as 
<i><b><code>pictures of a use case</code></b>, where once written, we ensure that a use case is 
contextualized within the domain model</i>
</p>
<note><p>Think of a robustness diagram as a picture, drawn from a use case definition that helps 
it become contextualized in the domain model.
</p></note>
<p>As with our other study sessions, before we move on to the elements of a robustness diagram, 
I would like to ask our friend Amazon Q to perform an analysis of relevant sources and list some 
pros, cons, and characteristics for this type of UML diagram.
</p>

<procedure title="Robustness Diagrams ― Key Notes, Pros, and Cons" collapsible="true">
<tabs>
<tab title="Robustness Diagrams | Key Points">
<list>
<li><b><format color="CornFlowerBlue">Definition and Purpose</format></b>: A UML analysis diagram that <code>bridges use cases and domain models</code>, visualizing how internal objects interact to fulfill use case requirements.</li>
<li><b><format color="CornFlowerBlue">Structure</format></b>: Consists of boundary, control, and entity objects that represent different aspects of system interaction</li>
<li><b><format color="CornFlowerBlue">Relationship Types</format></b>: Shows connections between different stereotyped objects and their interactions within a use case context</li>
<li><b><format color="CornFlowerBlue">Analysis Level</format></b>: Operates at an intermediate level between high-level use cases and detailed sequence diagrams</li>
<li><b><format color="CornFlowerBlue">Modeling Scope</format></b>: Focuses on analyzing and representing a single use case's internal object interactions</li>
</list>
</tab>

<tab title="Robustness Diagrams | Pros">
<list>
<li><b><format color="CornFlowerBlue">Early Validation</format></b>: Enables <code>early detection of design issues</code> and validation of use case completeness</li>
<li><b><format color="CornFlowerBlue">Gap Bridging</format></b>: Creates a smooth transition between analysis and design phases</li>
<li><b><format color="CornFlowerBlue">Domain Model Enhancement</format></b>: Helps identify missing elements and relationships in the domain model</li>
<li><b><format color="CornFlowerBlue">Responsibility Clarity</format></b>: Provides clear visualization of system responsibilities and object interactions</li>
<li><b><format color="CornFlowerBlue">Design Refinement</format></b>: Facilitates iterative refinement of system design before implementation</li>
</list>
</tab>

<tab title="Robustness Diagrams | Cons">
<list>
<li><b><format color="CornFlowerBlue">Non-Standard Nature</format></b>: Not part of standard UML specification, leading to <code>potential compatibility issues</code></li>
<li><b><format color="CornFlowerBlue">Complexity Management</format></b>: Can become difficult to maintain and understand in large-scale systems</li>
<li><b><format color="CornFlowerBlue">Resource Investment</format></b>: Requires additional time and effort in the design phase</li>
<li><b><format color="CornFlowerBlue">Documentation Overhead</format></b>: May create redundant documentation if not properly integrated into the development process</li>
<li><b><format color="CornFlowerBlue">Learning Curve</format></b>: Requires specific training and understanding of robustness analysis concepts</li>
</list>
</tab>
</tabs>
</procedure>

#### Robustness Diagrams ― Diagram Elements
<p>Despite the class presentation showing only three parts, in theory (basedc on the agile 
modeling webpage on the same topic), we have more than three, we have <b>four elements to a 
robustness diagram</b>. These will be discussed in the following procedure block</p>
<procedure title="Elements of a Robustness Diagram" type="choices">
<deflist type="full" collapsible="true">
<def title="Actors">
<p>Actors represent the same concept as in <b>use case diagrams</b>, that is, 
<i><code>in robustness diagrams, actors are still those that await an output from an 
action, and those external entities that initiated the use case</code></i></p>
</def>
<def title="Boundary Elements [Object]"><p>Defined as a software element, such as a 
screen, a report, HTML pages, or a system interfcae that actors interact with. On the 
other hand they can be defined as nouns (or objects)</p></def>
<def title="Control Elements [Controller]"><p>These can be defined as actions, as verbs, 
as they serve as <b><code>glue between boundary elements and entity elements, 
implementing the logic required to manage the various elements and their 
interactions.</code></b></p></def>
<def title="Entity Elements [Entity Object]"><p>Conceptual nouns (objects) like 
<b>Student or Seminar</b>, these in theory are objects that are represented within our 
domain model. For instance, in our project one of these might be a Customer, or Account, or 
even Pizza.</p>
</def>
</deflist>
</procedure>
<note>It is important to consider that use cases are the <i>what</i> the system is supposed to do, 
and the design phase of our implementation defines the how. But to go from the <i>what</i> to 
the <i>how</i>, we use robustness diagrams as the bridge.
</note>

<p>In general terms, robustness diagrams show all participating classes, within a use case, and 
software behavior as an overview. In this sense, <b>behavior is not yet linked to classes</b>, 
but we can see a flow of action represented by lines between entity objects.</p>

### Robustness Diagrams ― First Notions
<p>Having reviewed the basics of how to define these types of diagrams, we now can take a look at 
an example of this diagram type for a POS system. The idea of this example, is to show how this 
diagram is structured in general terms, while syntactically it might vary from the book's 
implementaiton, it is a web image I can present here quickly. 
</p>
<img src="https://online.visual-paradigm.com/repository/images/0fc03029-d912-40f0-bca3-be78a5e59b62/robustness-diagram-design/atm.png"/>

<p>As can be seen in the previous image, we have too considered the way these diagrams are often 
structured with respect to the design model used for each entity. Notice how the boundary 
objects, are effectively separation classes of our system from the outside world. It is 
effectively the point at which the user interacts with the use case and pushes the internal 
logic to execute. Notice how then in the second section we have a circular node with an arrow. 
This represent a Controller, which defines an action that the system will take during this use 
case. And finally, the circle with a little line underneath, represents an entity object, 
somethign with memory, an object in our domain model</p>
<p>We can see that this model showcases the steps our use case description indicated, but 
without words, now it shows the actions through connection lines (that can be annotated) between 
diagram objects.
</p>
<p>One key aspect to notice from this diagram is the use of arrows within our diagram. Usually, 
most use case diagrams connect the actor with the use case with a non-directed line, a line 
that simply shows connection (like an association line). The same can be done in robustness 
diagrams, like the following example, but do notice something 
<i><b><code>non-directed lines, really don't say anything about where to go.</code></b></i></p>
<img alt="ShowBookDetailsUndirected.png" src="ShowBookDetailsUndirected.png" thumbnail="true"/>
<p>As can be noted by the previous diagram, there is no way for a reader to know what is going 
o, or in what direction it should go. For example, after the Home Page boundary object, are we 
meant to biffurcate to both Display Book Details Page and Display Links (this highlights an issue 
of overcoupling of actions too), or are we meant to go first to the display links page and then 
to the display book details page. However, keep in mind that <b><code>object (entity) 
elements have undirected lines (most of the time) towards a given controller.</code></b>
</p>
<p>We can continue disecting this thing and when we take a look at it we can begin to see the 
execution pattern, but without the graph there is no way for us to quickly deduce how it 
communicates. For this reason, we add <b><code>directed lines to show where we have 
to go (maybe not at what moment and how), but we can show a direction now!</code></b></p>

<img alt="DirectedWriteCustomerReview.png" src="DirectedWriteCustomerReview.png" thumbnail="true"/>

<p>Given that this process is iterative, we can add or remove controllers, as well as rearrange 
communication lines to make the model easier to understand, showing clearly where each step 
takes afterward. The idea is not that a single robustness diagram should cover everything, we 
can have different robustness diagrams so long as they operate under the same use case and are 
connected to some extent within them.</p>

### Robustness Diagrams ― Considerations

<procedure title="Robustness Diagrams ― Design Considerations" collapsible="true">
<tabs>
<tab title="Design Considerations">
<list>
<li><b><format color="CornFlowerBlue">Object Stereotypes</format></b>: Clearly distinguish between <code>boundary, control, and entity objects</code> using proper notation</li>
<li><b><format color="CornFlowerBlue">Direction Flow</format></b>: Use directed lines to show clear flow of interactions and avoid ambiguity in process sequence</li>
<li><b><format color="CornFlowerBlue">Granularity</format></b>: Keep diagrams focused on single use cases to maintain clarity and prevent overcomplexity</li>
<li><b><format color="CornFlowerBlue">Object Naming</format></b>: Use meaningful and consistent naming conventions that reflect object responsibilities</li>
<li><b><format color="CornFlowerBlue">Visual Layout</format></b>: Arrange objects to minimize line crossings and maximize readability</li>
</list>
</tab>

<tab title="Implementation Guidelines">
<list>
<li><b><format color="CornFlowerBlue">Boundary Objects</format></b>: Should represent all system interfaces with external actors</li>
<li><b><format color="CornFlowerBlue">Control Objects</format></b>: Include only necessary processing steps and avoid overloading with multiple responsibilities</li>
<li><b><format color="CornFlowerBlue">Entity Objects</format></b>: Must align with domain model entities and maintain <code>undirected connections to controllers</code></li>
<li><b><format color="CornFlowerBlue">Connection Rules</format></b>: Ensure proper object communication patterns (boundary-to-control, control-to-entity)</li>
<li><b><format color="CornFlowerBlue">Validation</format></b>: Verify that all use case steps are properly represented in the diagram</li>
</list>
</tab>

<tab title="Iteration Strategies">
<list>
<li><b><format color="CornFlowerBlue">Refinement Process</format></b>: Continuously review and adjust diagrams as requirements evolve</li>
<li><b><format color="CornFlowerBlue">Decomposition</format></b>: Break down complex diagrams into smaller, more manageable sub-diagrams when needed</li>
<li><b><format color="CornFlowerBlue">Consistency Check</format></b>: Regularly verify alignment with use cases and domain model updates</li>
<li><b><format color="CornFlowerBlue">Stakeholder Review</format></b>: Include regular reviews with team members and stakeholders for validation</li>
<li><b><format color="CornFlowerBlue">Documentation</format></b>: Maintain clear documentation of changes and rationale for diagram modifications</li>
</list>
</tab>
</tabs>
</procedure>


## Monday 10th Class ― Activity Diagrams
<p>An activity diagram can be thought of as a flow diagram with added infomration. The idea is that 
<b><code>a use case shows what the system needs to do, but the activity diagram shows how</code></b>. It is meant to 
model processes and sequences of actions to complete a task within our system.
</p>
<p>Activity diagrams can be used to define both the main, and alternative, flows within our use case definitions. 
These diagrams can be used within software design or even business process analysis. </p>
<p>Activity diagrams often respond to either <b><code>external events that change the state or update 
some state within our application</code></b>, or they might respond to a method call, i.e., these two define ways in 
which an activity diagram can start.
</p>

### Activity Diagrams ― Basic Components Illustrated
<procedure>
<deflist type="full">
<def title="Initial Node, Activity Final Node">
<p>This pair of nodes is used to denote the start and end of an activity diagram respectively. 
From the initial node, lines with a direction (directed lines) will flow to other components 
(most likely a state). Meanwhile, an activity final node should only receive a single directed 
line entering it.</p>
</def>
<def title="Context of the activity diagram"><p>Can be defined as all parameters involved in 
the activity, be them process-relevant data, most of the time a class and/or objects. These are 
often defined in the top corner of an activity diagram bounding box.
</p>

![contextDiagrams.png](contextDiagrams.png)
</def>
<def title="Activity Pre- and Post-Conditions"><p>These are defined as activity-wide 
preconditions adn post conditions (i.e., start-up conditions, and after end conditions) 
that must be withheld during the activity diagram. These often related the system, anda re 
placed in the <b>top right corner of the activity diagram bounding box</b>
</p>

![ActivityPrePostConditions.png](ActivityPrePostConditions.png)
</def>
<def title="Object Nodes"><p>Often represented as squares (no rounded corners as those are the 
state diagram model), in this sense it represents simply <i><code>an object within an 
activity diagram, and despite it having output and input arrows, doesn't always represent output 
or input to another node.
</code></i>
</p>

![ObjectNodes.png](ObjectNodes.png)
</def>
<def title="Pins"><p>Pins can be used to model <b>where input and output happens 
within our graphs</b>. This is because there are both output and input pins, located 
after and before a state rounded rectangle respectively. These often have an 
<b><code>interconnection directed line between them</code>, that represents the flow 
from output to input on another node.</b></p>
<p>In general, if we want to represent an alternative path in an activity diagram, we can do so 
by putting a triangle above a communication line and in between pins.</p>

![ExceptionPins.png](ExceptionPins.png)

<p>If we want to <b>mark the possible value of a pin, we can define it with a label near it.
</b></p>

![ValuePin.png](ValuePin.png)
</def>
<def title="Object Flow Modifications"><p>Within a single process, we can add notes and 
comments to communication lines, while these can be informative comments, we can also do 
<b>transformations to the data</b>. These are annotations (think of them as stereotypes) 
that can be placed over a communication line to offer some context to the transformations 
done to data that entered an activity diagram.</p>

![ObjectFlowSelection.png](ObjectFlowSelection.png)

<p>The methods that we have are <b>selection: used to allow certain data to flow and not 
others</b>,<b>transformation: extracting information from an object.</b></p>
</def>
<def title="Parameter Sets">
<p>A parameter set can be defined as <b>A parameter set represents the inputs and outputs that 
are passed between activities, decisions, forks, joins, and other control structures within an 
activity diagram.
</b></p>
</def>
<def title="Connectors and Edges">
<p>Connectors can be defined in four ways: <b><code>single line connector, connector 
separated connector, object node connector, and input and output pin connector</code></b>
</p>

![ConnectorsAndEdges.png](ConnectorsAndEdges.png)
</def>
<def title="Decision and Merge Nodes">
<p>Decision nodes are characterized by <b><code>having an input line pointing into 
a rhombus from which two or more lines appear and point to states</code>. These lines can be 
further documented by <code>labels for the reason they happen</code>
</b>. Additionally, we can define the condition by defining a condition in a note.</p>

![DecisionAndMergeNodes.png](DecisionAndMergeNodes.png)

<p>Merge nodes are those that <b><code>receive two or more input lines into a rhombus and then 
output a single line to another state.
</code></b></p>

![DecisionWithMerge.png](DecisionWithMerge.png)
</def>
<def title="Time Events">
<p>Time signals are defined as <b>a specific point in time that triggers an action or 
transition. These are often used to represent scenarios where certain actions or processes 
need to occur after a specific period of time.</b>
</p>

![TimeEvents.png](TimeEvents.png)
</def>
<def title="Signals">
<p>There are two important symbols for signals that we have to check. <b><code>Accept Signal: 
which is represented as a rectangle with a pointy left inner end. And Send Signal: which is 
represented as a rectangle with a right exterior pointy edge.
</code></b> These often represent <i><b><code>interactions with external 
participants</code></b></i></p>

![SignalsSendReceive.png](SignalsSendReceive.png)
</def>
<def title="interruptible Activity Regions">
<p>Defined as regions (<b><code>represented through a dashed line, rounded corners 
rectangle</code></b>), where a set of interruptible actions are held, along with an 
<i><code>event that can cause the interruption</code></i>. To represent this interruptible 
activity region, this interruptible action has to have a Harry Potter lightning symbol</p>

![ActivityRegion.png](ActivityRegion.png)
</def>
<def title="Fork Node and Join Node">
<p>A fork node is a way for us to represent <b><code>activities that are run 
concurrently within an activity diagram</code></b>. This is represented by a 
<i><code>single thick black line where a single input directed line comes in and n 
directed lines come out pointing to all sequences of states that run 
concurrently</code></i><br/><br/>
Internally, since we are running concurrently, we have a new structure called an 
<b><code>flow final node</code>, that is not the same as <b>activity final node</b></b>. The 
flow final node is represented by a <b><code>circle with an x held within</code></b>, while the 
activity final node is the exact as we defined before.
</p>
<p>The thing between these two is that, if a concurrent line ends, that does not mean the use 
case ends, only the path that it took ends and the use case runs until it encounter the 
activity final node.</p>

![ForkWithFlowFinalNode.png](ForkWithFlowFinalNode.png)

<p>A join node is the opposite of a fork node, <b><code>as it takes n input lines and outputs a 
single one. Think of them as a merge node, but for concurrent task and not options. 
</code></b></p>

![JoinNode.png](JoinNode.png)

<note>As a sidenote, we can have a join specification, defined as a <b>condition that 
must be met for the flow to continue.</b></note>
</def>
<def title="Activity Partitions">
<p>Given that activities might involve different participants, such as different groups or 
roles within an organization or system, we must find a way to differentiate between them. The 
idea is to use <b><code>partitions to show which participant is responsible for which actions
</code></b></p>

![ActivityPartitions.png](ActivityPartitions.png)

<p>Another way of representing this is as a horizontal partition. The idea is to form a 
<b><code>table inwhich the lanes (swimlanes) represent subsystems in our organization</code></b>,
and the use case is distributed horizontally to separate states in terms of subsystems.
</p>

![HorizontalOrganizationSubsystems.png](HorizontalOrganizationSubsystems.png)

<note>As a sidenote, we can define the annotation <i><b><code>external</code></b></i> to 
define an activity that although represented as an state within an activity diagram, it is 
not handled internally by the system.</note>
<p>We can also separate responsibilities within an activity diagram based on object/class 
responsibilities, modelling <b>the actions that classes or objects are responsible for</b></p>

![ObjectBasedResponsibiltiesPartitioning.png](ObjectBasedResponsibiltiesPartitioning.png)
</def>
<def title="Exception handling">
<p>Exception handling within activity diagrams can be though of as 
<b><code>unstoppable action that is represented by the same symbol as the 
interruptible action, but that produces an output that can be passed into an state or node for 
it to perform an action based on the condition.
</code></b></p>


![HandlingExceptions.png](HandlingExceptions.png)
</def>
<def title="Expansion Regions"><p>often we want to show that <b>actions within a 
region are performed for each item in an input collection producing an output item 
collection from the collection input (something like a map function in Java where an 
operation (the expansion region) is applied to all values of an input collection)</b>.
<br/><br/>
Effectively then, we have multiple inputs, and or output tokens for or from activities or actions.
</p>

![ExpansionRegions.png](ExpansionRegions.png)
</def>
<def title="Streams"><p>The idea of streams is effectively the same as Java, the operations 
defined in an expansion region are defined once, but the execution happens on all input values 
from a collection of inputs as they become available. Meaning that <b><code>so long as 
there are data inputs becoming available from a state towards the input of a expansion 
region, the internal expansion region states will be applied to all input elements</code></b>. 
It is generally labeled within a expansion region, but with the keyword <b>stream</b>
</p>

![StreamExampleOne.png](StreamExampleOne.png)

<p>There is also the ability to put the stream in normal pin notation with each pin denoted with 
the <b>{stream}</b> mark.
</p>

![StreamExampleTwo.png](StreamExampleTwo.png)

<p>Or using a shorthand notation</p>

![StreamExampleThree.png](StreamExampleThree.png)
</def>
</deflist>
</procedure>


