# Class #7 ― State Machines ― Monday Mar 10th

> The present file will contain information regarding the implementation of state machine diagrams for all of our 
> use cases. The goal of this section is to define the main characteristics, implementation details, etc., about 
> this type of artifact. Additionally, Project One, part Three has been described and presented.


## Introduction to State Machines 

### Introduction to State Machines: Definitions
<p>Stat machines are representations of the internal state that an object through an interaction has. Thea idea of 
these diagrams is to represent, in various fields, the way that the state of an object changes through a business 
process.</p>
<tldr>Behavioral state machine is specialization of <b><code>Behavior diagrams</code></b>, used to specify discrete 
behavior 
of a part of 
designed systems through finite state transitions.</tldr>
<p>The idea then of this type of diagram is to show, represent, or display the way the state of an object or the 
internal state of our app responds to various changes through <b><code>transitions that represent events</code></b>, 
these events can lead to changes in state that are represented with nodes in the diagram.
</p>

### Introduction to State Machines: Components
<p>A state machine diagram, also known as <b><code>state diagram or statechart diagram</code></b>, contains several 
key components that will be listed in no particular order in the next section</p>
<procedure title="Components of a State machine diagram" collapsible="true">
<deflist type="full" collapsible="false">
<def title="States">
<p>In any state diagrams, there are three different components that are key, and are all held within the State label.
These are <b><code>common States, Initial PseudoState, and Final State</code></b>. These three form the basis of the 
overarching process represented within a state diagram. These can be defined as points in the story that is shown 
over the diagram, these points in the story can be though as changes in the state of an object of our system.
</p>
<p>Consider the case of a light switch, although complete software-agnostic, it shows three different states. Often 
it starts in the <i>initial pseudo state, as off</i>, and different transitions or changes like flipping it on and off,
can either keep it in the same state or progress to the <i>on or off state</i>, after getting to this state we have 
a <i>final pseudo state</i>
</p>
<p>This is not the best way to explain this information, this is because this has nothign to do with software and 
has little to no states that would allow us to visualize the interaction, even mentally (!), as such I think we 
should take a look at an example from the book</p>

<img alt="AccountApplicationStateDiagram.png" src="AccountApplicationStateDiagram.png" thumbnail="true"/>
<note>In the above picture we can see all three of the nodes that I was talking about
<list>
<li><b><format color="WhiteSmoke">Initial Pseudo state</format></b>: often used to indicate the start of the diagram.
It is represented by a filled circle.
</li> 
<li><b><format color="WhiteSmoke">States</format></b>: The tiny rectangles with rounded corners are the state nodes. 
These state nodes are defined  as <b><code>condition of being at a certain time. [These] can be passive (being 
something)
qualities or active qualities (doing something)</code></b>. It is interesting to note that there exists an even 
deeper organization than the one presented here for these diagrams, to be presented in an inner section. 
</li>
<li><b><format color="WhiteSmoke">Final Pseudostate</format></b>:Tiny concentric circles defining the end of an 
interaction, it is the last node from which no other state transitions can appear. </li> 
</list>
</note>
</def>
<def title="Transitions"> 
<p>Transitions are defined as arrows that represent changes that can arise within our system and move us from state 
to state, this can be external, like changes in an API status, client input or status, etc. or internal, like 
considerations taken by our app to handle incorrect states or faulty components, as well as transitions defined to 
move the application process or control it</p>
<p>In general, these transitions represent a change of state, indicating <b><code>(right above the 
directed arrow that represents them)</code></b> the reason or circumstances that caused the state change to occur.</p>
<note>Transition labels follow this pattern <i><code>[triggers][guard]/ behavior</code></i>, where each 
element is 
an optional.
<tip>
<p>The components of a behavioral transition can be defined as follows.</p>
<list>
<li><b><format color="WhiteSmoke">Trigger or [Triggers]</format></b>: both of these represent the same thing, 
<b><code>the event(s) that can induce a state transition.</code></b> However the semantics are different, as in 
the first case it is a single event, however the second label is a series of events that can fire. 
<b><code>Do mind that although an event might match with an event required for a transition, we require the guard to 
pass too to make the transition
</code></b></li> 
<li><b><format color="WhiteSmoke">Guard Constraint</format></b>: defined as a boolean expression written in terms 
of parameters of the triggering events, and links to the <b><code>context object</code></b>. Since there can be 
more than one guard in any expression, we define that if there is more than one, all guards must pass before the 
transition fires.</li>
<li><b><format color="WhiteSmoke">Behavior Expression(s)</format></b>: Operation(s) that are executed if and when 
the transition fires. <b><code>These can be written in terms of operations, attributes, and links of 
the context objct and the parameters of the triggering event, or any other features visible in its 
scope.</code></b></li>
</list>
<tip>
<p>A Context Object is a specialized instance of a Behaviored Classifier that maintains the current state of a state machine and manages state transitions based on events and conditions. As a Behaviored Classifier, it encapsulates both structural features (attributes and associations) and behavioral features (operations and signals) that can be referenced within the state machine's transitions and states. The Context Object provides the execution environment for the state machine, making its properties and methods available to guard conditions and behavior expressions during transitions. Within the state machine, transitions can access and modify the Context Object's attributes, invoke its operations, and evaluate its associations to determine if guard conditions are met or to execute behavior expressions. This tight integration between the Context Object and its state machine ensures that the state-dependent behavior remains cohesive and properly encapsulated within the broader system architecture.</p>
</tip>
</tip>
</note>
</def>
</deflist>
</procedure>