# Class #7 ― State Machines ― Monday Mar 10th

> The present file will contain information regarding the implementation of state machine diagrams for all of our 
> use cases. The goal of this section is to define the main characteristics, implementation details, etc., about 
> this type of artifact. Additionally, Project One, part Three has been described and presented.


## Introduction to State Machines 

### Introduction to State Machines : Types
<p>Accordingly, given that we can represent not only running conditions but simple actions and states, these 
diagrams branch into two separate state machine types, useful for <b><code>modeling space particulars 
such as business rules</code></b></p>
<procedure title="State Machine Types" id="smt" collapsible="true" type="choices">
<step><b><format color="CornFlowerBlue">Behavioral State Machines</format></b>: most state machines are 
specializations of the Behavioral diagram type. A <b><code>behavioral state machine</code></b>are those that 
<i><code>have internal actions in some of their states</code></i></step>
<step><b><format color="CornflowerBlue">Protocol State Machines</format></b>: this is a specialization of 
behavioral state machines, characterized by <b><code>having actions whose actions occur in 
transitions, not in internal states</code></b>. Ergo, there are no internal states in these machines</step>
</procedure>

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
<deflist type="full" collapsible="true">
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
<def title="Events">
<p>Any event that is represented within a state diagram should be <b><code>atomic, i.e., a final action 
that cannot be decomposed.</code></b> Conceptually, we think that these events are meant to be immediate, although 
this is not a requirement. Events often respond to two different changes, <i><code>external stimuli, as 
these can be caused by changes on the outer layer of the application</code> Or  <code>internal, as these 
can also be brought about internal state changes</code></i></p>
<p>An event, then, can be though as different from a state, as <b><code>an event is something that triggers a change 
from state to state</code></b>, these are often represented as text above a transition arrow. However, as we have 
seen within the transition block, we know that these might or might not occur depending on certain context 
condtitions and boolean <i>guards</i></p>
<note>The relationship between transitions and events is direct. Transitions come about from an event (internal 
or external) that modifies the internal state of the context of the state machine. Despite this, however, there 
is still the possibility of an event not triggering a transition (depending on the boolean guard condition it has 
attached to it).</note>
<p>The structure of an event is similar to that of the Transitions, in fact, <b><code>the transition 
syntaxis is often the same as the event sintaxis as the event leads to the transition, not the other way 
around.</code></b></p>
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
<p>A Context Object is a specialized instance of a Behaviored Classifier that maintains the 
current state of a state machine and manages state transitions based on events and conditions. 
As a Behaviored Classifier, it encapsulates both structural features (attributes and 
associations) and behavioral features (operations and signals) that can be referenced within the 
state machine's transitions and states. The Context Object provides the execution environment 
for the state machine, making its properties and methods available to guard conditions and 
behavior expressions during transitions. Within the state machine, transitions can access and 
modify the Context Object’s attributes, invoke its operations, and evaluate its associations to 
determine if guard conditions are met or to execute behavior expressions. This tight integration 
between the Context Object and its state machine ensures that the state-dependent behavior 
remains cohesive and properly encapsulated within the broader system architecture.</p>
</tip>
</tip>
</note>
<p>Transitions may have one, two or <b><code>none of the attributes listed above</code></b>. In the case when this 
is not present, then we say the following.</p>
<tip>A transition that is <b><code>unnamed, unguarded, and has no side effects</code></b> is a very simple and 
straightward transition in UML. It means,
<list>
<li>Transition does not have a specific name or label</li>
<li>Transition does not have any guard conditions</li>
<li>Transition does not trigger any additional actions or side effects</li>
</list>
<p>This transition type can be divided into three subtypes <b><code> unnamed transitions</code></b> (used when the 
transition is self-explanatory), <b><code>unguarded transitions</code></b>(a transition that will happen regardless 
of the context object's state as it does not require a guard check to execute), and <b><code>transitions 
with no side effects</code></b> (transitions where the only relevant action is the state change itself, not any 
internal side effects.</p>
</tip>
<p>In addition,, we have another type of transitions known as the <b><code>Completion States</code></b>, which are 
defined as <b><code>transitions that take place when everything to be done in the current state is 
completed</code></b>, these are often represented as transitions whose endpoint has no connection.</p>
</def>
</deflist>
</procedure>


#### Components: Deeper look into States
<p>When it comes to states, the idea of them is simple to understand, these represent either a condition of a 
machine, or a system, or even an object during the lifecycle of an application. This, however, can be expanded to 
represent conditions like being, or doing. As such we have <b><code>Simple States, Composite State, Doing state, and 
Submachine States
</code></b></p>
<p>These states allow us to model complex internal behaviors, running conditions, internal timings, or even running 
conditions that a state might have. This means that these states are quite different, and more complex, than those 
presented in <b><code>finite state machines, and although they are modelled similarly, they tend to 
differ slightly.</code></b></p>
<tldr><p>A state models a specific moment in the behavior, subsystem or application, taken a sa condition of being 
for the state machine in a specific moment. These of course, can also represent <b><code>waiting, doing, receiving, 
etc. as well as static conditions.</code></b></p></tldr>
<p>The following listing provides a series of definitions </p>

<note>States can be of two types <b><code>static states or dynamic states </code></b>. The 
difference that comes from them is.
<list>
<li>A state that is blocking, or an action that requires awaiting for some external change, or internal change. 
(<b><code>Static State</code></b>)</li>
<li>A state that requires some kind of internal change, or a combination of events to transpire for an outcome to 
be produced (<b><code>dynamic states</code></b>)</li>
</list>
</note>
<p>In contrast to transitions, <b><code>a state can be active for a period of time</code></b>, this is because an 
action that takes from state to state should be immediate, on the other hand, active states can be blocking too.</p>
<p>In addition to the state types presented so far, all of which have been linear and singular, a total of two more 
types can be 
mentioned, <b><code>Composite States, and Orthogonal Composite States</code></b>, whose separating detail is the 
presence of inner states within a single state, and multiple regions of mutually exclusive disjoint states, 
respectively</p>

<procedure title="Types of State Machine's States" id="types_of_state_machine_s_states" collapsible="false">
<deflist type="full" collapsible="true">
<def title="Simple States">
<p>Simple events are the <b><code>most basic form of states, often with no internal structure</code></b>. These are 
the simple events that have a name and forward and backward arrows emanating from it. The following is a listing of 
its characteristics.</p>
<procedure title="UML State Machine Simple States ― Key Points" collapsible="true">
<tabs>
<tab title="Simple States | Key Points">
<list>
<li><b><format color="CornFlowerBlue">Definition and Purpose</format></b>: A <code>basic unit of state behavior</code> representing a condition or situation during which an object satisfies some condition, performs some activity, or waits for an event</li>
<li><b><format color="CornFlowerBlue">Structure</format></b>: Contains a name, internal actions (entry, exit, do), and transitions to other states</li>
<li><b><format color="CornFlowerBlue">Behavior Types</format></b>: Can include entry actions, exit actions, and do-activities that execute while in the state</li>
<li><b><format color="CornFlowerBlue">Transition Rules</format></b>: States can have multiple incoming transitions but typically have clear conditions for outgoing transitions</li>
<li><b><format color="CornFlowerBlue">Visual Representation</format></b>: Depicted as rectangles with rounded corners containing the state name</li>
</list>
</tab>
</tabs>
</procedure>
<img src="https://www.uml-diagrams.org/notation/state-simple.png"/>
</def>
<def title="Static States">
<p>These are defined as those that <b><code>represent a situation where the system is waiting for some 
extenral (or internal) event to occur.</code></b> The following are some characteristics of this model</p>
<procedure title="UML State Machine Static States ― Key Points" collapsible="true">
<tabs>
<tab title="Static States | Key Points">
<list>
<li><b><format color="CornFlowerBlue">Definition and Purpose</format></b>: A <code>passive state type</code> representing a situation where the system is idle and waiting for an external or internal event to trigger a transition</li>
<li><b><format color="CornFlowerBlue">Structure</format></b>: Contains a name, event triggers, and guard conditions that determine when the state can transition</li>
<li><b><format color="CornFlowerBlue">Behavior Types</format></b>: Primarily focused on event handling and condition monitoring, with no ongoing internal activities</li>
<li><b><format color="CornFlowerBlue">Transition Rules</format></b>: Transitions occur only in response to specific events or when guard conditions are met, maintaining a wait-and-react pattern</li>
<li><b><format color="CornFlowerBlue">Visual Representation</format></b>: Typically shown as rectangles with rounded corners, often with an event trigger notation on outgoing transitions</li>
</list>
</tab>
</tabs>
</procedure>
</def>
<def title="Dynamic States">
<p>This third type of states, represent those states that have some <b><code>internal activity, like a 
compound state</code></b>.</p>
<procedure title="UML State Machine Dynamic States ― Key Points" collapsible="true">
<tabs>
<tab title="Dynamic States | Key Points">
<list>
<li><b><format color="CornFlowerBlue">Definition and Purpose</format></b>: An <code>active state type</code> representing a situation where the system is performing ongoing activities or contains nested substates while maintaining its current state</li>
<li><b><format color="CornFlowerBlue">Structure</format></b>: Contains a name, internal activities (do-activities), possible substates, and concurrent regions for parallel behavior</li>
<li><b><format color="CornFlowerBlue">Behavior Types</format></b>: Features continuous or long-running activities, often including composite states and orthogonal regions for complex behaviors</li>
<li><b><format color="CornFlowerBlue">Transition Rules</format></b>: Can transition based on both internal activity completion and external events, supporting hierarchical state nesting</li>
<li><b><format color="CornFlowerBlue">Visual Representation</format></b>: Depicted as rounded rectangles that may contain other states (substates) or parallel regions separated by dashed lines</li>
</list>
</tab>
</tabs>
</procedure>

<img alt="DynamicStateExample.png" src="DynamicStateExample.png" thumbnail="true"/>
</def>
<def title="Composite States">
<p>
Compound states contain <b>code internal subtates and transitions</b>. These might have a series of underlying 
states that can in many ways be connected to outer states, or even run on their own as an internal specification of 
the state. For example, an ATM state machine might have a <i><b>longer, more detailed composite state of PIN 
validation for a credit card transaction due to the need to validate the PIN entered by a user</b></i>
</p>
<img alt="CompositeStateWithOneRegion.png" src="CompositeStateWithOneRegion.png" thumbnail="true"/>
<p>The following are some characteristics of this state type.</p>
<procedure title="UML State Machine Composite States ― Key Points" collapsible="true">
<tabs>
<tab title="Composite States | Key Points">
<list>
<li><b><format color="CornFlowerBlue">Definition and Purpose</format></b>: A <code>hierarchical state type</code> that encapsulates a single region containing one or more substates, providing a way to organize complex state behavior into manageable hierarchies</li>
<li><b><format color="CornFlowerBlue">Structure</format></b>: Contains an outer state that encapsulates inner substates, entry/exit points, internal transitions, and a single region of state behavior</li>
<li><b><format color="CornFlowerBlue">Behavior Types</format></b>: Supports sequential substate execution, default entry states, entry/exit actions at both composite and substate levels, and history mechanisms for state memory</li>
<li><b><format color="CornFlowerBlue">Transition Rules</format></b>: Events are first processed by the innermost active substate; if not handled, they propagate up to the parent composite state following the state hierarchy</li>
<li><b><format color="CornFlowerBlue">Visual Representation</format></b>: Depicted as a larger rounded rectangle containing smaller rounded rectangles (substates), with a single continuous region and optional entry/exit points on the border</li>
</list>
</tab>
</tabs>
</procedure>
</def>
<def title="Orthogonal States (Composites With More than One Region">
<p>An <b><code>orthogonal composite state (just a parallel composite state)</code></b>, includes more than one 
region. Each region that is held within it is a set of mutually exclusive states and a set of transitions.</p>
<p>Within these regions (including the composite states), we can break down inner states into two groups, 
<b><code>direct substates</code></b>, those not contained by other substates, and <b><code>indirect 
substates</code></b>, those that are not.</p>
<note>When using this state type, or simple composites, <b><code>all incoming arrows are thought as 
being redirected to the initial state of the inner substates</code></b></note>
<p>Additionally, a composite state may have <b><code> one or more entry and exit points on its outside 
border</code></b></p>
<procedure title="UML State Machine Orthogonal States ― Key Points" collapsible="true">
<tabs>
<tab title="Orthogonal States | Key Points">
<list>
<li><b><format color="CornFlowerBlue">Definition and Purpose</format></b>: A <code>parallel composite state type</code> that contains multiple regions operating concurrently, enabling the modeling of independent but simultaneous behaviors within a single state</li>
<li><b><format color="CornFlowerBlue">Structure</format></b>: Contains multiple regions separated by dashed lines, where each region has its own set of mutually exclusive substates and transitions, operating independently of other regions</li>
<li><b><format color="CornFlowerBlue">Behavior Types</format></b>: Supports concurrent execution of multiple state configurations, synchronized activities across regions, and complex parallel processing patterns with independent entry/exit actions for each region</li>
<li><b><format color="CornFlowerBlue">Transition Rules</format></b>: Each region can transition independently, but the composite state itself can only exit when all regions complete their execution or when an external transition forces exit from all regions simultaneously</li>
<li><b><format color="CornFlowerBlue">Visual Representation</format></b>: Depicted as a large rounded rectangle divided into multiple regions by dashed lines, with each region containing its own set of substates and transitions</li>
</list>
</tab>
</tabs>
</procedure>
<note>In addition, note that transitions going out of an <b><code>initial pseudo state, do not have 
guards or triggers</code></b>, these are thought subsequent of the entry point and they can only have some 
<b><code>side effect</code></b></note>

<img alt="OrthogonalCompositeState.png" src="OrthogonalCompositeState.png" thumbnail="true"/>
</def>
</deflist>
</procedure>
<p>Within a state we can also have <b><code>internal activities</code></b></p>

##### States: Internal Activities Within a State
<p>Teh set of activities that are presented in the <b><code>internal activities compartment</code></b>, are a series 
of activities only executed when the state is active, i.e., when we are in said state. This is a compartment that 
hodls a list of internal actions or state (do) or activities (behaviors) that are perform while in the state
</p>
<p>The internal activities we defined are defined like this: <b><code>label / activity expression</code></b>, in 
addition, the labels entry, do and exit are reserved.</p>
<p>The labels defined beforehand are part of what is known as the <b><code> internal behavior of a state</code></b></p>
<note>The internal behavior of a state is behavior that happens while an object is in a state. These use the same 
model as defined before, <b><code>and entry, do and exit are reserved</code></b>
<list>
<li>Entry is used to define an activity done once entered the state
<img alt="ExFive.png" src="ExFive.png" thumbnail="true"/>
<tip><p>Using entry actions depends on the context of our diagram, but it can be often used when <b><code> there is 
more than one transition into a state, or when an action is performed on every transition, or when something is done 
on entry and not on exit
</code></b></p></tip>
<img alt="ExSix.png" src="ExSix.png" thumbnail="true"/>
<img alt="ExSeven.png" src="ExSeven.png" thumbnail="true"/>
</li>
<li>Do defines activities that are executed while we are in the state
</li>
<li>Exit performs an activity when we leave the state
<tip>As usual, there are some considerations when we will use exit actions. Specifically we should consider 
<b><code>a) if there is more tha one transition out of the state and one action is performed one every 
one of these. Or b) if the action is only done on the exit from the original state and is superfluous to the 
receiving state.
</code></b></tip>
<img alt="ExEight.png" src="ExEight.png" thumbnail="true"/>
<img alt="ExNine.png" src="ExNine.png" thumbnail="true"/>
</li>
</list>
</note>
<p>In addition to this compartment, however, there is also the <b><code>internal transition compartment</code></b>, 
hat is defined as <i><b><code>a list of internal transitions, where each item has the form of a 
trigger (a trigger is an event)</code></b></i></p>

<img alt="InternalBehaviorAndTransitions.png" src="InternalBehaviorAndTransitions.png" thumbnail="true"/>

##### States: Demistifying Composite States
<p>Earlier in class, we were presented with a series of graphs that were complex, hard to understand and most 
importantly had little to no text descriptions along with them. For this section, I will attempt to demystify  
these through the information we have acquired. in this section </p>

<procedure title="Demystifying Composite States" id="demystifying_composite_states" collapsible="true">
<code>Composite States Example One</code>
<list columns="2">
<li>
<img alt="ExampleOneCompState.png" src="ExampleOneCompState.png" thumbnail="true"/>
</li>
<li><p>The state shown on the left has a series of overlapping connections, but we can begin analyzing it by taking a 
looking at the bounding boxes. The inner rectangle indicates that this diagram has two state machines, one 
higher-level and another inner state machine made up of states S1.1 and S1.2</p>
<p>In addition, we can see several lines going into the same set of states in the composited state S1. Nevertheless 
we can break this down into two groups, <b><code>group (a) made up of the transition e2 and unnamed from 
e4's final state to S2</code></b>, and <b><code>group (b) made up by e1 and e3</code></b>. The first group is the 
main continuation line, the unnamed event and e2 are both transitions (denoted by their events like e2) that can be 
though of as the <i>correct flow per se</i>. These move the use case from the start pseudo state to the end pseudo 
state and continue out to finish the state machine flow</p>
<p>On the other hand, the second group represents alternative paths, these can be though of as, maybe in the case of 
e1 an alternative access param, or e3 an alternativa exit param (we can see these by virtue of the arrowhead)
</p>
</li>
</list>
<code>Composite States Example Two</code>
<list columns="2">
<li><img alt="ExampleTwoCompositeStates.png" src="ExampleTwoCompositeStates.png" thumbnail="true"/></li>
<li>This second example si the application of the <b><code>single entry and single exit nodes that are 
defined as pseudo states</code></b>. These two allow us to represent those access points more clearly while keeping 
the same logic as before. In general, these are simple representations of the same thing that make the diagram 
easier to understand.
<note>Do recall that as far as this diagram is concerned, we cannot add any more entry or exit pseudo states into 
the inner compound state.
</note>
</li>
</list>
<code>Composite States Example 3</code>
<list columns="2">
<li>
<img alt="CompositeExampleThree.png" src="CompositeExampleThree.png" thumbnail="true"/>
</li>
<li>This next diagram is a bit more complicated, it presents us with everything that we must know to understand and 
practice these diagrams. First, we can see that we have two states that supposedly lead us to the composited state 
S1. These do not have any arrows pointing into them (I do not know what these are meant to be in this example). 
Nevertheless, when we take a look at the inner regions of the S1 composited state, we can see that we have two 
submachines that have a series of internal states that execute in parallel
It is interesting to note that these also have exit and entry lines coming in and out to different nodes, which 
could be simplified into a simpler diagram.
</li>
</list>
</procedure>

### Components: Deeper look into Transitions
<p>In addition to the content that we have reviewed in terms of transitions, there are a set of 
<b><code>four transition types</code></b>, these are better defined in the following picture</p>
<procedure title="Transition Types" id="transitionTypes" collapsible="false">
<img alt="TransitionTypes.png" src="TransitionTypes.png" thumbnail="true"/>
</procedure>
<p>These are specifications of what we can find when we are working with transitions. For instance, in general terms 
when we are working with composit transitions, or even those that have transitions in their inner transition 
compartments, we will most likely find an entry transition (which is executed when a state is entered), an exit 
transition (a transition executed only when exiting a state), and a series of internal transitions (which are not 
the same as the do <i>internal activities</i>)
</p>
<p>As such, in an example, we can see both entry, exit and do transitions, as well as internal transitions. In this 
sense there are four transition variations available</p>
<procedure title="Transition Variations" id="Variations" collapsible="true">
<step><p><i>Transition occurs when the trigger occurs</i></p>
<img alt="ExOne.png" src="ExOne.png" thumbnail="true"/>
</step>
<step><p><i>Transition occurs if the guard evaluates to true</i></p>
<img alt="ExTwo.png" src="ExTwo.png" thumbnail="true"/>
</step>
<step><p><i>Transition occurs after the completion of internal behavior</i></p>
<img alt="ExThree.png" src="ExThree.png" thumbnail="true"/>
</step>
<step><p><i>Transition includes transition behavior if guard evaluates to false</i></p>
<img alt="ExFour.png" src="ExFour.png" thumbnail="true"/>
</step>
</procedure>

#### Deeper look into Transitions: How do Internal Transitions execute?
<p><b>Internal transitions</b> represent behavioral responses within a state that execute without causing the state itself to exit and re-enter. This concept allows for efficient handling of events by maintaining the current state context and avoiding the overhead of exit/entry actions, effectively encapsulating localized behaviors while preserving the state's ongoing activities and hierarchical position in the state machine.</p>
<note>The use of internal transitions is to handle variation of behavior within the state. These can model error 
handling, communication logic, logging logic, validation logic, etc. The idea is to model these behaviors using 
internal transitions such that we do not disturb the overarching flow adn state of the state</note>
<p>As such, internal transitions are particularly useful for modeling several common scenarios:</p>
<procedure>
<list columns="2">
<li>Event Handling Within States</li>
<li>Error handling or Recovery Actions</li>
<li>Status updates or progress monitoring</li>
<li>Logging or diagnostic operations</li>
<li>Data validation checks</li>
<li>Resource Management</li>
<li>UI State Management</li>
<li>System Monitoring</li>
<li>Incremental Processing</li>
</list>
</procedure>
<p>For this reason, these internal transitions, as they define some kind of behavior associated with them, it is 
more useful to have them as controllers for a state that has a do activity. FOr instante, if we have an input field 
in a state, we might be able to handle validation of the data through internal transitions.</p>

<procedure title="Some Examples on Internal Transitions" id="some_examples_on_internal_transitions" collapsible="true">
<list>
<li><b><format color="CornFlowerBlue">Validation State Management</format></b>:
<p><b>Form Validation State Management</b> represents a common UI pattern where internal transitions handle input validation, formatting, and error display without disrupting the form's overall state. This concept allows for efficient user feedback and data validation while maintaining the form's active state, effectively managing the user interaction flow without requiring complete state changes for every input event.</p>

```PlantUML
@startuml
state "DisplayingForm" as DF {
    state "ValidInput" as VI
    state "InvalidInput" as II
    
    [*] -> VI
    
    DF : validateField / showFieldError()
    DF : formatInput / reformatField()
    DF : updateValue / refreshDisplay()
    
    VI -> II : validateField [isInvalid] / showFieldError()
    II -> VI : formatInput [isValid] / reformatField()
}
@enduml
```
</li> 
<li><b><format color="CornFlowerBlue">System Monitoring State Management</format></b>: 
<p><b>System Monitoring State Management</b> demonstrates how internal transitions can handle continuous system health checks and resource management within an active system state. This pattern enables real-time monitoring and adjustment of system resources while maintaining system operation, effectively implementing self-healing and adaptive behaviors without transitioning between different operational states.</p>

```plantuml
@startuml
state "SystemRunning" as SR {
    state "NormalOperation" as NO
    state "ResourceOptimization" as RO
    
    [*] -> NO
    
    SR : healthCheck / updateStatus()
    SR : performanceAlert / adjustResources()
    SR : heartbeat / updateTimestamp()
    
    NO -> RO : performanceAlert / adjustResources()
    RO -> NO : healthCheck / updateStatus()
}
@enduml

```
</li> 
</list>
</procedure>
<tip>The previous examples, provided by our friend Amazon Q involve many details that are important to both note, 
understand and apply in demystifying internal transitions</tip>
<p>The examples above, showcase a single state which not only handles internal transitions, but also inner states, 
<b><code>transforming these states into composite states </code></b>, where what we have is not just a singular 
state (in case of the first example <i>DisplayingForm</i>), rather we have a complex state that demonstrates the 
inner workings of te composite state</p>
<p>We begin the first example by taking a look at the information presented in the upper level compartment, while 
this is not the correct place to put them, as above would be an empty compartment with either some do activities or 
entry or exit, it shows three inner transitions</p>
<p>These <b><code>internal transitions: validateField / showFIeldError(), formatInput / reformatField(), 
padteValue / refreshDisplay()</code></b>, are all internal transitions that showcase some of the transitions that 
are handled <b><code>internally within ovearching state</code></b>. These transitions are then further used within 
the composite states compartment that illustrates how these are used to transition between inner state ValidInput 
and InvalidInput</p>

### Introduction To State Machines: Submachines
<p>One additional component, which often ties in with the idea of composited states and orthogonal states is the 
idea of <b><code>submachines</code></b>.</p>
<tldr><p><b>Submachines</b>, represent a state within a higher-level state machine that itself contains its own 
complete state machine. This concept allows for hierarchical organization of complex state behaviors by 
encapsulating detailed state transitions within a single state at a higher level</p></tldr>
<procedure title="UML State Machine Submachines ― Key Points" collapsible="true">
<tabs>
<tab title="Submachines | Key Points">
<list>
<li><b><format color="CornFlowerBlue">Definition and Purpose</format></b>: A <code>reusable state machine</code> that encapsulates complex behavior and can be referenced by multiple state machine diagrams, functioning as a modular and reusable component</li>
<li><b><format color="CornFlowerBlue">Structure</format></b>: Contains its own complete state machine with entry/exit points, internal states, and transitions that can be referenced from other state machines</li>
<li><b><format color="CornFlowerBlue">Behavior Types</format></b>: Supports hierarchical decomposition, state reuse, and encapsulation of complex behaviors while maintaining its own context and state configuration</li>
<li><b><format color="CornFlowerBlue">Transition Rules</format></b>: Entry and exit points serve as interfaces between the submachine and its parent state machine, allowing controlled flow of execution across machine boundaries</li>
<li><b><format color="CornFlowerBlue">Visual Representation</format></b>: Depicted as a state with a special submachine indicator (often shown as a fork or small state machine icon), with explicit entry and exit points</li>
</list>
</tab>

<tab title="Pros">
<list>
<li><b><format color="Green">Reusability</format></b>: Can be referenced and reused across multiple state machines, reducing redundancy and promoting code reuse</li>
<li><b><format color="Green">Maintainability</format></b>: Changes to the submachine are automatically reflected in all places where it's used</li>
<li><b><format color="Green">Complexity Management</format></b>: Helps manage complex systems by breaking them down into smaller, more manageable units</li>
<li><b><format color="Green">Encapsulation</format></b>: Internal details are hidden from the parent state machine, promoting better separation of concerns</li>
<li><b><format color="Green">Scalability</format></b>: Enables creation of large, complex state machines through composition of smaller, well-defined units</li>
</list>
</tab>

<tab title="Cons">
<list>
<li><b><format color="Red">Overhead</format></b>: Additional complexity in managing entry/exit points and interfaces between machines</li>
<li><b><format color="Red">Debugging Complexity</format></b>: Can make debugging more challenging due to the need to track state across multiple levels</li>
<li><b><format color="Red">Communication Overhead</format></b>: May require additional mechanism to handle data sharing between parent and submachine</li>
<li><b><format color="Red">Learning Curve</format></b>: More complex to understand and implement compared to simple states</li>
<li><b><format color="Red">Potential Coupling</format></b>: If not carefully designed, can lead to tight coupling between parent and submachine states</li>
</list>
</tab>
</tabs>
</procedure>
<p>One concept that might come about when reading about this secion is the concept of regions.</p>
<note><p>Regions are defined orthogonal part of either a composite state or a state machine, which contains 
inner states and transitions.</p>. In essence, all regions within composited states may execute at different 
rates (but in parallel), whose execution must wait for all branches to finish <b><code>before invoken a completion 
event to init a completion transition
</code></b></note>
<p>Submachining is useful to group some content that we do not want to put in the main diagram (because it is too 
large perhaps), but we still want a reference to in the main content. To do this we have a variety of options, each 
showing more or less detail to the reader.</p>
<procedure title="Submachine Usage Model" id="submachine_usage_model" type="choices">
<step><p>The first, and often simplest, way to use it is by defining the entire machine within the 
overarching state diagram. This then implicates <b><code>adding the entirety of the inner state 
diagram to the higher-level one, this being the lowest level of encapsulation possible</code></b></p>
<img alt="LowestAbstractionSubMachine.png" src="LowestAbstractionSubMachine.png" thumbnail="true"/>
</step>
<step><p>The second level of abstraction is to mention the state by only. This can be done by simply replacing the 
original inner state machine with its name. While this is useful, it is not the most recommended approach</p>
<img alt="LevelTwoAbstractionSubMachines.png" src="LevelTwoAbstractionSubMachines.png" thumbnail="true"/>
</step>
<step><p>A higher level abstraction would be to show the name with a decomposition icon, which looks like a 
pair of glasses, and it indicates to the reader that there is a underlying state machine that is involved in 
the higher-level machine in the most abstracted and clear way that UML allows for</p>

<img alt="HighAbstraction.png" src="HighAbstraction.png" thumbnail="true"/>
</step>
</procedure>

### Introduction to State Machines: Activity Diagram Constructs
<p>In addition to the normal components of a state machine diagram, there are some components that appear to be 
ported from activity diagrams, which might be the reason why people often neglect these when we already have 
activity diagrams. The components in question are <b><code>initial and terminal pseudo states, choice 
(decision nodes), fork and join node, junction, and four new ones, shallow history pseudo state, deep 
history pseudo state, and entry and exit points</code></b></p>
<p>In class we have not covered all of these, but for the sake of completeness,  shall present at least the ones we 
have seen in class up to this moment</p>

<procedure title="Pseudo States in State Machines" id="pseudo_states_in_state_machines" type="choices">
<tabs>
<tab title="Initial Pseudo State">
<p>This marks the starting point of state machine, compound state or orthogonal region in a compound state. It is 
represented by a <b><code>small solid circle</code></b>. The idea of this seudo state is <i><code>it 
transitions to the first active state when the system starts</code></i></p>
<img src="https://sparxsystems.com/images/screenshots/uml2_tutorial/sm09.GIF" thumbnail="true"/>
</tab>
<tab title="Terminal Pseudo State">
<p>This marks that the execution of this state machine by means of its context object is terminated. This indicates 
that the state machine will not perform any more transitions or state changes. This is represented by a 
<b><code>line with one end as a cross</code></b></p>

<img src="https://sparxsystems.com/images/screenshots/uml2_tutorial/sm14.GIF" thumbnail="true"/>
</tab>
<tab title="Entry Point"><p>This marks the entry point into a state machine or a composite state. The idea of 
this section is that each state machine or composite state should have at most a single transition into the 
same region. This symbol is shown as a <b><code>small circle on the border of the state machine 
diagram or composite state, with a name associated to it.</code></b></p>
<img src="https://sparxsystems.com/images/screenshots/uml2_tutorial/sm10.GIF" thumbnail="true"/>
</tab>
<tab title="Exit Point">This marks the exit point of a state machine or a composite state. This indicates that the 
machine or submachine or composite state will immediately exit and head to the transition defined coming out of the 
symbol for this state, which is <b><code>a circle with a cross within</code></b>
<img src="https://sparxsystems.com/images/screenshots/uml2_tutorial/sm11.GIF" thumbnail="true"/>
</tab>
</tabs>
<!-- Separation for Choice, Fork, Join and Junction -->
<tabs>
<tab title="Choice">This represents a decision point in the state machine where multiple transitions branch out. The choice pseudostate evaluates guard conditions on its outgoing transitions to select which path to take. It is depicted as a <b><code>diamond-shaped symbol</code></b> on the diagram.
<img src="https://sparxsystems.com/images/screenshots/uml2_tutorial/sm12.GIF" thumbnail="true"/>
</tab>
<tab title="Fork">This splits an incoming transition into two or more parallel transitions that target vertices in different regions. The fork pseudostate allows the state machine to enter multiple states simultaneously. It is shown as a <b><code>short heavy bar</code></b> with multiple outgoing transitions.
<note>
<p>Do note that as far as fork outgoing lines are concerned, <b><code>these cannot have any kind of 
triggers or guards, only side effects</code></b></p>
</note>
<img src="https://sparxsystems.com/images/screenshots/uml2_tutorial/sm16.GIF" thumbnail="true"/>
</tab>
<tab title="Join">This combines multiple incoming transitions from different regions into a single outgoing transition. The join pseudostate waits for all parallel activities to complete before proceeding. It is represented by a <b><code>short heavy bar</code></b> with multiple incoming transitions.

<img alt="ForkAndJoin.png" src="ForkAndJoin.png" thumbnail="true"/>
</tab>
<tab title="Junction">This chains together multiple transitions, allowing for more complex path 
constructions. The junction pseudostate can merge multiple incoming transitions or split an 
incoming transition into multiple outgoing ones with different conditions. It appears as a 
<b><code>small black circle</code></b> on the diagram.
<img src="https://sparxsystems.com/images/screenshots/uml2_tutorial/sm13.GIF" thumbnail="true"/>
</tab>
</tabs>
<tabs>
<tab title="Deep History Pseudo State">
<p>As with a shallow history state, the idea of this node is to represent a state that 
<b><code>when present within a composite state machine</code></b>, will <b><code>call the most 
recent state immediately before the most recent exit state
</code></b>. In contrast to a shallow history state, this last exit state can be 
<i><code>nested at any depth</code></i></p>
<p>The idea is that these pseudo states represent the <b><code>most recent active 
configuration of the composite state that directly contains this pseudostate</code></b>. As per 
the docs from the official UML</p>
<tip>
<p>A composite can have <b><code>at most</code></b> one deep history node, and at most 
<b><code>one transition</code></b> may originate from the history connector to the default deep 
history state</p>
</tip>
<p>This state is often represented as a <b><code>capital H with a start next to it : 
H*</code></b></p>

<img alt="DeepHistoryStates.png" src="DeepHistoryStates.png" thumbnail="true"/>
<p>The following would be an example of how this diagram could be read</p>
<tip>
<ol class=" "><li class=" ">    <p>The composite state 'Composite state 1' is entered and becomes active 
(via the transition emanating from the <a href="">initial pseudostate</a>).    </p>
</li><li class=" ">    <p>Composite states 'Composite state 2' and 'Composite state 3' are also 
entered and become active (via the transitions emanating from the initial pseudostates).    </p>
</li><li class=" ">    <p><a href="">Simple state</a> 'Simple state 1' is entered and becomes 
active (via the transition emanating from the initial pseudostate).    </p>
</li><li class=" ">    <p><a href="">Events</a> 'E1' is fired. The simple state 'Simple state 3' 
is entered and becomes active.    </p>
</li><li class=" ">    <p>Then the event 'E2' is fired. The simple states 'Simple state 2' and 
'Simple state 4' are entered and become active.    </p>
</li><li class=" ">    <p>After event 'E2' is fired, composite state 'Composite state 1' is 
exited and simple state 'Simple state 5' is entered and becomes active.    </p>
</li><li class=" ">    <p>Now the automatic transition leaving simple state 'Simple state 5' is 
processed.    </p>
</li><li class=" ">    <p>This leads to the composite state 'Composite state 1' being entered 
again by its deep history. Now 'Simple state 2' and 'Simple state 4' are reactivated because the 
state 'Composite state 1' was active before.    </p>
</li></ol>
</tip>
<p>Lastly this would be the set of characteristics that matter when working with this diagram</p>
<warning>
<ul class=" "><li class=" ">    <p>Deep history works/functions recursively. That means that all 
child states of the regions of the containing composite state that were active before, are 
reactivated recursively (remember that the <a href="">shallow history</a> doesn't reactivate the children).    </p>
</li><li class=" ">    <p>If the target of one of the default transitions is a composite state, 
than it proceeds with the default entry of the composite state.    </p>
</li><li class=" ">    <p>Composite states can contain at most one deep history.    </p>
</li><li class=" ">    <p>The state machine is considered ill-formed if the containing composite 
state has never been active before and it has no default transitions.    </p>
</li></ul>
</warning>
</tab>
<tab title="Shallow History Pseudo State">
<p>In contrast to the deep history pseudo state, while this state does the exact same thing 
(<b><code>recall the state before an exit</code></b>), the way it does it is much simpler. In 
general, the shallow history state is allowed only to <b><code>return to states 
in the same depth</code></b>. It is important to note that, as well as for the deep history 
state, these states belong to <b><code>composite states not to a region within a 
composite state</code></b></p>
<note>
A composite state can have <b><code>at most one</code></b> shallow history state. The state can 
have at most <b><code>one transition coming from the history connector</code></b>. In all cases, 
if the composite state was not active before the shallow history is reached (in the first time), 
the default transitions are taken until we arrive back at the shallow history node
</note>
<img src="https://yasmine.seadex.de/images/download/attachments/2785317/shallow_history_context_1.png" thumbnail="true"/>
<p>The above graph can be explained as follows</p>
<tip>
<ol class=" "><li class=" ">    <p>The composite state <i>Composite state 1</i> is entered and 
becomes active (via the transition emanating from the initial pseudostate).</p>
</li><li class=" ">    <p>Composite states <i>Composite state 2</i> and <i>Composite state 3</i> are also entered and 
become active (via the transitions emanating from the initial pseudostates).</p>
</li><li class=" ">    <p>Simple state <i>Simple state 1</i> is entered and becomes active (via the transition 
emanating from the initial pseudostate.</p>
</li><li class=" ">    <p>Event <i>E1</i> is fired. The state simple state <i>Simple state 3</i> is 
entered and becomes active.</p>
</li><li class=" ">    <p>Then the event <i>E2</i> is fired. The simple states <i>Simple state 2</i> and 
<i>Simple state 4</i> are entered and become active.</p>
</li><li class=" ">    <p>After event <i>E2</i> is fired, composite state <i>Composite state 1</i> is exited 
and simple state 'Simple state 5' is entered and becomes active.    </p>
</li><li class=" ">    <p>Now the automatic transition leaving the simple state <i>Simple state 5</i> is processed.   
</p>
</li><li class=" ">    <p>This leads to the composite state <i>Composite state 1</i> being entered again by its shallow 
history. Now, because the composite state <i>Composite state 1</i> was active before, simple 
states <i>Simple state 2</i> and <i>Simple state 4</i> are reactivated.    </p>
</li></ol>
</tip>
<warning>
<ul class=" "><li class=" ">    <p>Shallow history does not work recursively. This means that 
all child states of the regions of the containing composite state that were active before, are 
reactivated - but not their children (As opposed to deep history, where children are also reactivated).    </p>
</li><li class=" ">    <p>If the target of one of the default transitions is a composite state, 
than it proceeds with the default entry of the composite state.    </p>
</li><li class=" ">    <p>Composite states can contain at most one shallow history.    </p>
</li><li class=" ">    <p>The state machine is considered ill-formed if a shallow history is 
reached while the containing composite state has never been active before and it has no default 
transitions.    </p>
</li></ul>
</warning>
</tab>
</tabs>
</procedure>

### Introduction to State Machines: State Transition Tables
<p>
Often, state machines can be represented as state transition tables which show all states in a table, repeating them 
as an adjacency matrix showing which transition takes which state to another. The idea is to have a matrix 
representation of <b><code>states and the transitions that take the execution from one to another</code></b>. Using 
the information that is provided in this table one can follow the state machine diagram, to some extent, in the same 
way as if we were reading them directly.
</p>
<note>Even if we have internal composited states and transitions have to present in the table showing what state 
we have to go to when these transitions arrive.</note>
<p>In general, the table structured in a dissimilar way to the simpler state diagrams from finite state automata. 
<b><code>Rather, these tables show the current state, incoming trigger, guard, action, an the next state</code></b>, 
like a database table, not like a true matrix. Nevertheless, if we take a look at the current state and next state 
columns we can still see the original matrix representation
</p>

<procedure title="Representation of a State Transition Table" id="representation_of_a_state_transition_table">

<deflist type="full">
<def title="State Diagram">

<img alt="InfoExampleStateOne.png" src="InfoExampleStateOne.png" thumbnail="true"/>
</def>
<def title="State Transition Table">

<img alt="InfoExampleStateTwo.png" src="InfoExampleStateTwo.png" thumbnail="true"/>
</def>
</deflist>
</procedure>
<p>As can be noted through the graphs, the concepts of these tables is to give us a view of the 
transitions, why they happen, what made them happen, and what guard had to be true for us to 
transition. They can be used to understand a model in terms of changes in states rather than a 
complex graph of lines and symbols. Clearly, both the graphical and tabular view showcase the same 
information, thought I would posit that the second version is much cleaner, specially if we have 
a deep hierarchy of nested states.
</p>

### Introduction to State Machines: State Naming
<p>
The concept of naming a state, although not directly related to building a state machine, is an 
important aspect that is often used and explored when we are working on defining the states in 
our machine. In general, <b><code>these often change with the type of machine we are 
using</code></b>, for instance the language we use might change in protocol state machines 
compared to behavioral state machines.</p>
<p>In general, the main rule for state naming is that we should name it after the 
<b><code>criteria for defining the state</code></b>, like for a Person, behavior context, we 
would have states that maybe come across as <i><code>isTeenager, isADult, 
isSeniorCitizen</code></i>, which might be tied to a condition (guard) statement</p>
<p>However this can also be changed and the name could be based on the last operation handled by 
the context object.
</p>

#### State Naming: Mapping Parts of Speech to Text
<p>Despite the information present on the slides being somewhat helpful in determining the way 
we should name transitions, states, etc., there are still other rules that we might find useful 
when going down from a high level use case towards a lower level state machine description of 
each actor, action, state and transition. </p>
<note>Naming always comes down to semantics, <b><code>specially about the way we 
use state machines and how expressive we want our diagrams to be</code></b></note>

<procedure title="Mapping Parts of Speech to State Machines" 
id="mapping_parts_of_speech_to_state_machines" collapsible="true">

<deflist type="wide">
<def title="States">
<p>States are typically handled using <b><code>nouns or adjetives</code></b>. As these represent 
different conditions of being, they are often named with nouns or adjectives that 
<b><code>describe the status or quality of the system</code></b>
</p>
<note>A state can also be named after a long-performing actiivty that running while in the 
state, like <b><code>Idle, Cruising, etc.</code></b>. For this reason, if the operaion is 
ongoing, we often want gerund verbs that end in <b>ing</b>, to represent the name of an 
ongoing activity.</note>
<p>Examples can be: <b><code>idle, loading, authenticated or error</code></b></p>
</def>
<def title="Event/Transitions">
<p>Events and or transitions are usually named with verbs. Since these <b><code>cause state 
transitions
</code></b>, they are actions or occurrences, so they best be named with verbs.</p>
<p>Examples can be <b><code>submit, cancel, fail, load, sign in, or clear form data</code></b></p>
</def>
<def title="Actions">
<p>Actions are operations <b><code>executed in response to events or state 
transitions (like behavior specifications in a transition definition)</code></b>. To name these, 
we use <i>verb phrases</i> that describe the action that is being taken.
</p>
<p>Exaxmples can be <b><code>sendRequest, displayError or updateData</code></b></p>
</def>
<def title="Guards">
<p>
Given that guards are conditional guards that determine if a transition should occur, they can 
<b><code>be named with adjectives or past participles describing the condition being met</code></b>
</p>
<p>Examples can be <b><code>isLoggedIn, hasValidData or isExpired</code></b></p>
</def>
<def title="Parent States">
<p>Parent states are the higher level holder states that within themselves hold various smaller 
state machines or states. In this sense, a parent state is one that holds within it substates 
much like a composite state would hold within it more states and even whole state machines.
</p>
<p>In this case, these can be named using compound nouns like <b><code>Viewing 
Shopping Cart</code></b> where child states could be <b><code>Empty or Populated</code></b></p>
</def>
<def title="Invoked Actors">
<p>Often, a state machine might invoke an APi or some kind of service, if this is the case we 
call them <b><code>invoked actors</code></b>, and as such the labels should use nouns or gerunds,
like <b><code>fetchingData, or userAuthentication</code></b>
</p>
</def>
</deflist>

<img alt="CompleteExampleForStateMachineDiagram.png" src="CompleteExampleForStateMachineDiagram.png" thumbnail="true"/>
</procedure>

## Introduction to State Machines: Transition-Oriented View
<p>This last concept is simple, it involves handling signals (receiving and sending) to represent the process of the 
state diagram, it is about <b><code>integrating both signals nd states</code></b>
</p>
<p>In this diagramming flavour, what we have is that transitions are handled through <b><code>an activity diagram's 
signal blocks
</code></b>, for example, we can have a signal receiver node or signal outputting line to emphasize transitions and 
the inputs of transitions.</p>
<procedure title="Example of Transition-Oriented View">

<img alt="ExampleTransitionOrientedView.png" 
src="ExampleTransitionOrientedView.png" thumbnail="true"/>
</procedure>

### Transition-Oriented View: Protocol State Machines
<p>Protocol state machines are simplifications of the behavioral state machines. As such, these 
do not show various components in their states, like <b><code>entry, exit or do 
activities</code></b>. They, however, do show the legal sequence of events and resulting states. 
</p>
<note>They tend to represent an external view of a server class, as seen by a client using 
that server class. For this reason, <b><code>they are useful to model and depict 
communication protocols like TCP, or database connections</code></b></note>