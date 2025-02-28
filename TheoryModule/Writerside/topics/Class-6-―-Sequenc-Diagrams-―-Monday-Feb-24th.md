# Class #6 ― Sequence Diagrams ― Monday Feb 24th 

> The content off this file will engulf information about sequence diagrams. These diagrams will be presented in 
> theoretical and graphical notions.

## Sequence Diagrams
<p>Sequence diagrams model interactions between objects during the execution time of our system. These 
<b><code>append the with whom and the how to the use case what definition</code></b>. In this sense, activity 
diagrams make use of our use case definition to expand and explain the way objects within our 
system interacts with its components to execute the task that permits the use case.</p>
<p>These diagrams have a rectangular box notation for <b>objects</b>, and a dropping dash line represents the 
<b><code>lifetime of an object.</code></b></p>
<p>While the previous definition went over some of the internal structure, the following 
sections will delve deeper into the content of Sequence Diagrams, their parts, uniqueness, 
examples, etc</p>

### Sequence Diagrams ― Definition
<p>A sequence diagram is part of the group known as <b><code>Interaction Diagrams</code></b>, 
these are the transition from use cases (the what), robustness diagrams (the relatively simple 
how) and the concrete sequence of events that lead to the real how of your application, sequence 
diagrams.
</p>
<p>The idea of using these, is that they allow us <b><code>to model important runtime 
interactions between the parts that make up our system, defining the logical view of 
our domain model</code></b></p>
<note><p>From our friend Amazon Q, <i>A sequence diagram is a type of interaction diagram that 
illustrates how different objects or components in a system communicate with each other over 
time. It shows the chronological flow of messages and interactions between participants, 
represented as parallel vertical lines (lifelines) extending down the page. The diagram depicts 
the sequence of method calls, responses, and signals exchanged between objects during the 
execution of a specific scenario or use case. Messages between objects are shown as horizontal 
arrows connecting the lifelines, with time progressing downward on the diagram. The diagram 
captures both synchronous and asynchronous communication patterns while maintaining temporal 
ordering of events.</i></p></note>
<p>One thing to note both from our definition, and the one provided by Amazon Q, is the emphasis 
that is placed on <strong>capturing the order of interactions between parts of our 
system</strong>. This is often seen in our class through trace analysis and can even be seen as 
we move through calls and method invocation(horizontally), and time frames lines or Activation Bars
(vertically). In later sections we will take a look at how to read these diagrams, but for now 
lets head on to the ten most important rules to remember about these daigrams</p>

### Sequence Diagrams ― Top 10 Sequence Diagramming Guidelines
<p>As with robustness diagrams (I am sure these must exist for activity diagrams too, I just 
haven't gotten around to write them), there are a series of guidelines that we can think of, or 
follow, when we are diagramming our sequence diagrams</p>
<note><p>All sequence diagrams must be made after having refined all use cases, and after having 
defined robustness and activity diagrams as these will flesh out any missing <b>entity</b> 
within our domain model.
</p></note>
<procedure title="Top 10 Sequence Diagramming Guidelines" type="steps">
<step>
<deflist collapsible="true" type="full"> 
<def title="Understand why you’re drawing a sequence diagram to get the most out of it">
<p>When drawing a sequenced diagram, <b><code>explore all the ins and outs of your 
design, not just the sunny day scenario</code></b>. Many errors can be caught at this stage, 
incoherencies in design too, that can be refactored easily now more than during the</p>
<p>Consider these pointers as to the use of sequence diagrams within the ICONIX process</p>
<list>
<li>Classes identified during robustness analysis are refined during  sequence diagramming, 
where controllers are transformed into operations on classes</li>
<li>Controllers don't always have a 1:1 relationship with operations - one controller may become 
multiple operations or occasionally a controller class</li>
<li>Sequence diagrams show detailed runtime interactions between objects to fulfill use case 
behavior. Consider exploring the how the system will accomplish behavior.</li>
<li>Design follows a two-pass approach: first pass (preliminary) focuses on attributes while ignoring behavior allocation</li>
<li>Second pass (detailed design) focuses specifically on allocating behavior among classes</li>
<li>Behavior allocation is done during detailed design because that's when sufficient information is available to make correct decisions</li>
</list>
</def>
</deflist>
</step>
<step>
<deflist collapsible="true" type="full">
<def title="Draw a sequence diagram for every use case, all courses shown">
<p>By now, having defined both the use case and the robustness diagramns, the next step is to, 
<b><code>for every use case defined within the current project</code></b>, develop a series of 
sequence diagrams that tie together the domain model classes and the attributes they will 
receive.</p>
<note><p>Use cases should be simple to follow, follow the EBP rule and keep them grounded within 
your domain model such that all transactions and lines of action are clear and held within a 
single diagram.
</p></note>
</def>
</deflist>
</step>
<step>
<deflist collapsible="true" type="full">
<def title="Start your sequence diagram from the boundary, entity, actors and use case text resulting from robustness analysis">
<p>Our diagrams should map <b><code>all entity to objects within our domain model and diagram, 
and all screens and GUI elements as parts of the sequence
</code></b>. In terms of controllers, almost all will become methods or communication lines 
between objects, although some can become <b><code>Managerial Classes or Controller 
Classes</code></b></p>
<note>Considering including technical information when talking about these types of diagrams. 
Remember that these show <b><code>a much more grounded, accurate and realistic view of 
the application EBP processes.</code></b> As such, persistency information, databases, objects, 
etc. are allowed.
</note>
</def>
</deflist>
</step>
<step>
<deflist collapsible="true" type="full">
<def title="Use the sequence diagram to show how the behavior of the use case is accomplished by the objects">
<p>In general, as we write our sequence diagrams, the communication lines (synchronous or 
asynchronous) should show the methods that can be expeced to be mapped to objects within our 
domain model. As such, <b><code>a robustness diagram's controllers often map to 
"logical" software functions, that are realized by one or more messages between 
objects</code></b>. For this reason, <i><code>defining messages is all about 
allocating behavior to collaborating objects (like a getter and setter kind of style)</code></i></p>
</def>
</deflist>
</step>
<step>
<deflist collapsible="true" type="full">
<def title="Make sure your use case text maps to the messages being passed on the sequence diagram">
<p>Make sure that all your sequence diagrams match the textual description of the use case as 
close as possible. Recall that the use case definition is <b><code>close to a 
contract between programmers and clients, specifying runtime behavior requirements 
that satisfy customer's needs</code></b></p>
<p>To this end, we often want to, as with other diagrams, keep the use case text nearby to make 
sure we follow it closely</p>
</def>
</deflist>
</step>
<step>
<deflist collapsible="true" type="full">
<def title="Don't spend too much time worrying about focus of control">
<p>The <b><code>focus of control</code></b>, or also called <b><code>activation bar</code></b>, 
is a symbol used to define, <i><b><code>whhich object "has the focus" or is 
currently in control</code></b></i>. These are useful, yes, when we are working in use case 
diagrams to know when control goes from one object to another, but if they start pilling up, or 
if they are annoying to work with in visual tools, we can disable them without any problems.</p>
<p>The following warning reviews some of the information that is often associated with drawing 
sequence diagrams and their difficulty.</p>
<warning>
<list>
<li><strong>CASE tool difficulties</strong>: Often stems from unclear use cases and requirements rather than the 
tool itself. Complete and thorough behavior requirements should be established before detailed 
design</li>
<li><strong>Information density</strong>: Sequence diagrams require detailed information as they show 
implementation specifics. Complex diagrams can be split into multiple pages, though it's better 
to keep use cases concise through proper factoring</li>
<li><emphasis><strong>Unclear purpose</strong></emphasis>: Having a clear understanding of the diagram's purpose is 
essential - refer 
to guidelines about understanding why you're drawing a sequence diagram</li>
</list>
</warning>
</def>
</deflist>
</step>
<step>
<deflist collapsible="true" type="full">
<def title="Assign operations to classes while drawing messages">
<p>As with the previous point on this issue, <b><code>sequence diagrams are helpful 
to filter out, from use cases, behavior that can be attributed directly to objects</code></b>. 
Most enterprise level products for UML and requirement analysis offer tools to <i>directly 
append behavior</i> to classes from within the diagrams, use these if you want to quickly add 
behavior in.</p>
</def>
</deflist>
</step>
<step>
<deflist collapsible="true" type="full">
<def title="Review your class diagrams frequently while you're assigning operations to classes, 
make sure these are in the right classes">
<p>Consider always to take a pause or two as you define your sequence diagrams to 
<b><code>take a look back at your class diagrams for each object and review correct 
addition of methods</code></b>. Often errors here can lead to larger issues during production.</p>
</def>
</deflist>
</step>
<step>
<deflist collapsible="true" type="full">
<def title="Pre-factor your design on sequence diagrams before coding">
<p>When we are developing our classes and assigning behavior to these, we can often make 
mistakes like adding a behavioral method to a class <i>and then deciding</i> it goes into 
another. <b><code>Correctly designing sequence diagrams should be all you need to make 
allocations correctly before heading to coding</code></b>
</p>
<p>Doing this early removes the need to refactor when the code is written, changing methods from 
class to class or extracting new classes out of incorrectly associated methods.
</p>
</def>
</deflist>
</step>
<step>
<deflist collapsible="true" type="full">
<def title="Clean up the static model before proceeding to the CDR"><p>
Before we move onto CDR (Critical Design Review), a step that <b><code>represents a 
crucial milestone in the design process where the static model is reviewed and cleaned 
up</code></b>, we can do a similar thing even before we draw a sequence diagram. This is often 
useful as information and <b><code>pre-factoring</code></b> can help us clean up our code, and 
reduce the amount of incosistencies and holes that can be within it.
</p>
<note>While the preliminary static model should be somewhat complete at this stage, we 
can always add infrastructure or scaffolding classes, <b><code>determine 
design patterns to use</code></b>, grab onto <b><code>application frameworks to use
</code></b>, or we can also simply complete the parameter lists on operations, etc</note></def>
</deflist>
</step>
</procedure>
<p>The previous bullet points have cleared some questions for me and, as I see them, provide 
information that might not have been discussed in class and answer questions that might be too 
complicated to ask in a single class, but, we have yet to write a diagram of our own (or at 
least analyze it). For now, we must keep waiting for this part, as it is time to take a look at 
the extensive list of structures a sequence diagram can have.</p>

### Sequence Diagrams ― Basic Structures
<p>To understand its structures we are going to go ahead and follow the presentation provided in 
class (all 71 slides I have to go of it), and information from the book that I think would prove 
benefitial
</p>
<procedure title="Basic Structures of a Sequence Diagram" collapsible="true" type="choices"> 
<deflist type="full" collapsible="true">
<def title="Participants">
<p>The first slides took care of participants. Any sequence diagram is made up of a 
<b><code>collection of participants, i.e., the parts of our system that interact with each other 
within it
</code></b>. Participants can be represented in various formats, from simple rectangles with 
stereotypes to robustness diagram notation (i.e., the circles with their respective lines).</p>
<p>Participants, often align on the <b><code>top of the diagram, presenting a clear 
line that shows all actors involved</code></b>, however these can change the level of their 
apperance depending on who wrote the diagram. Moreover, the concept of a 
<i><b><code>lifeline is often associated with participants</code></b></i>, as this 
<b><code>dashed line represents the timeframe in which the object is alive</code></b></p>
<tip><img alt="ParticipantsandLifelines.png" src="ParticipantsandLifelines.png" thumbnail="true"/></tip>
<p>The naming conventions used to define these are various, but these often stem from a single 
descriptor line <i><b><code>name [selector] : class_name ref decomposition</code></b></i></p>
<tip><p>These components can be broken down into these notions</p>
<ul>
<li><strong>name</strong>: is the normal name that is assigned to the object, but this has 
<b><code>nothing to do with the class name</code></b></li>
<li><strong>[selector]</strong>: refers to a selector used to identify the object within a 
collection of objects of the same type</li>
<li><strong>class_name</strong>: refers to the domain-model-based class name used to 
define the class in the overall static model</li>
<li><strong>ref decomposition</strong>: is a way for us to tell the reader that there exists a 
reference material under the name <b><code>held within the decomposition parameter</code></b>, 
that explains how this <b><code>participant works internally</code></b></li>
</ul>
</tip>
</def>
<def title="Time"><p>Time is often showcased within this model as the 
<i><b><code>lifeline lines</code></b></i> that appear within an object. These are not to 
be confused with the time structure that can be found in other diagrams to represent 
actual timing of events or of the day, etc.</p>
<warning>Time does not flow horizontally as we have been used to reading in other diagrams. Time 
in sequence diagrams <b><code>starts at the top fo the daigram and progresses down the 
page, the order of operations also indicates an order in time</code></b>

Do also note that <b><code>time is not absolute when represented within a sequence 
diagram</code></b>, although timing is important in terms of ordering, the actual time an operation 
takes is never truly represented here
</warning>
</def>
<def title="Events, Signals and Messages">
<p>These three are grouped together as they often represent three parts that are involved within 
the same section, i.e., the arrows in a sequence diagram. Events can be defined 
as <b><code> the points in which some action within our diagram starts and ends, i.e., 
anywhere where something occurs</code></b>. On the other hand, signals and messages refer to the 
same concept, <b><code>the communication between two objects that is often represented 
through black arrows</code></b>
</p>
<tip><img alt="ActionsAndEvents.png" src="ActionsAndEvents.png" thumbnail="true"/></tip>
<p>As with participants, there is a format for the arguments, the way we declare something, or 
even if it's a variable or not. This format is the following <format style="bold" 
color="CornflowerBlue"><emphasis>attribute = signal_or_message_name 
(arguments): return_type</emphasis></format></p>
<tip><p>As before, these can be broken down into simple ideas</p>
<ul>
<li><strong>attribute</strong>: refers to an optional <b><code>attribute 
assignment within the message caller</code></b> that is done to the return of any method. This 
effectively says, <i>store the result of this method within one of my internal parameters</i>
</li>
<li><strong>signal_or_message_name</strong>: this refers to the mandatory name that defines the 
method that is invoked within the message
</li>
<li><strong>arguments</strong>: this refers to a list of parameters that can be passed into the 
method. These can be separated by commans into a list where all parameters follow the syntax 
<b><code>name: class</code></b>
</li>
<li><strong>return_type</strong>: refers to the return type of the method.</li>
</ul>
</tip>
<p>In addition to one-to-one communication between the caller and receiver, there are cases 
where there are, not only multiple callers and receivers, but also <b><code>multiple 
messages sent between a caller and receiver</code></b>. In this case, all messages that are held 
within a single activation bar or focus of control bar are said to be <b><code>nested 
messages</code></b>. Therir representation does not change at all aside from the fact that all 
event starting points should appear within the same activation bar.
</p>
<tip><img alt="nestedMessages.png" src="nestedMessages.png" thumbnail="true"/></tip>
</def>
<def title="Activation Bars (Focus of Control bars)">
<p>These are simple lines that we have reviwed before, they are meant to show that a sender and 
a receiver of a message are active when some action is being done, i.e., when a signal or 
message has been sent from a caller to a receiver. These are <b><code>not mandatory 
at all</code></b></p>
<tip><img alt="ActivationBars.png" src="ActivationBars.png" thumbnail="true"/></tip>
<p>On the concept of activation bars, not only do we not have to wrie them, if we do not write 
them then there is no need for us to say that these methods return right after being called. 
There is the concept of a <b><code>time-consuming message</code></b>, which is represented as a 
line that is not horizontal, but rather angled at 30 degrees to showcase that there is a 
distance of time between the call, and the return, or between the call and the object creation.</p>
<tip><img alt="TimeConsumingEvents.png" src="TimeConsumingEvents.png"/></tip>
</def>
<def title="Message Arrow Types">
<p>Within sequences diagrams, as we are going to show an almost software defined view of our 
appplication, we are allowed to introduce two types of communication style 
<b><code>synchronous and asynchronous</code></b>, these two have their own arrows. We can also 
introduce <b><code>return statements through return arrows</code></b>, as well as object 
<b><code>creation and destruction.</code></b></p>
<note>Object creation can be done either with a simple line connecting to the initial 
<b><code>lifeline, if we chose to define this object at the top of the page</code></b>, or it 
can connect to the box of a new object if we choose to represent this new object in line with 
its creation statement
</note>
<tip><img alt="arrowTypes.png" src="arrowTypes.png" thumbnail="true"/>
<list type="bullet">
<li><strong>Synchronous messages</strong>: are implemented when the caller 
<b><code>waits for the receiver</code></b> to <b>return</b> from its invocation. This operation 
of course can, but does not require to, have a return statement or type.
</li>
<li><strong>Asynchronous messages</strong>: are implemented when the caller invokes a message on 
the receiver, but the caller <b><code>does not wait for the processing of said action to 
finish</code></b>, rather the caller continues execution, and might even do more work outside 
from the space of that previous invocation while waiting for a return.
</li>
<li><strong>Return Message</strong>: is implemented as an <b><code>optional piece of information 
that can be used at the end of an activation bar
</code></b>, that shows the return to the caller of the method.
<note>A participant can have a method call to itself, showing a line that connects right into 
itself creating a small activation bar.
</note>
</li>
<li><strong>Participant creation and destruction methods</strong>: these two lines represent a 
way for the designer to manifest that an object was <b><code>created during the 
execution of the sequence, or that an object is destroyed at some point before the 
natural conclusion of the diagram</code></b>
<note>In Java we do not often have, or in other languages even, a way to manually 
destroy objects, as opposed to creating them. As such, in our programs we often skip or 
ignore the <i>destroy</i> stereotype </note></li>
</list>
</tip>
<p>A full example of these can be seen in these next diagrams
</p>
<tip>
<img alt="AsynchIO.png" src="AsynchIO.png" thumbnail="true"/>
<img alt="SynchIO.png" src="SynchIO.png" thumbnail="true"/>
</tip>
</def>
<def title="Iteration Order">
<p>This is perhaps the most confusing, and often non mentioned (within the books at least) part 
of understanding sequence diagrams. In general, we know that <b><code>we do read a 
sequence diagram horizontally</code></b>, to this end then, one or more messages might appear on 
the same line if they are executed at the same time, for example. But <b><code>we do read these 
diagrams from top to bottom, i.e.,  in such a way that the vertical level in which any message 
appears matters.
</code></b> For this reason, we can extrapolate the following rule
</p>
<warning><p>Horizontal positioning of message arrows do not matter, these can be at 
the same time (i.e., on the same level) on one or more paths bewteen objects. However, the 
<b><code>vertical spacing and order of appearance</code></b> does matter, as it determines the 
way messages have to be ordered with respect to one another.
</p></warning>
<p>From this notion, it is clear that we can get different <b>traces</b> (known as iteration 
orders from the diagram), as we take a look at the positioning of messages within the diagram. 
to understand this consider the following trace diagram</p>
<tip><img alt="TracesOne.png" src="TracesOne.png" thumbnail="true"/>
<note>The previous image showcases another structure within activity diagrams (the seq combined
fragment zone), which defines that all of these elements are executed in weak sequence. However it 
does not mean that one has to be done after the other, as shown by the traces. The 
presence of these only means that while there is a sequential order, it is not strict. 
Specifically <b><code>occurrence specifications on different lifelines from 
different operands may come in any order.</code></b></note></tip>
</def>
<def title="Combined Fragments">
<warning>This is probably the most extensive section of this review, so bare with me for a little 
over 
400 lines of text!
</warning>
<p>Combined (Sequence) fragments are a way for us to <b><code>represent complex 
entaglement between calls, return statements, etc. based on a grouping of segments within a 
sequence diagram.
</code></b>. This is always represented as a <i><code>box with a label, always 
enclosinbg a portion of the interaction within a sequence diagram</code></i></p>
<note>A combined fragment is an interaction fragment which <b><code>defines a 
combination (expression) of fragments. A combined fragment is defined by an 
interaction operator, and corresponding interaction operands. Through the use of 
combined fragments the user will be able to describe a number of traces in a 
compact and concise manner.</code></b></note>
<p>Within our course material, we did not see specifically what any of these fragments meant, we 
saw examples on how to define them but not their meaning. As such, this next sectin is devoted 
entirely to defining these
</p>
<tip>
<deflist type="full" collapsible="true">
<def title="[alt] Combined Fragment">
<p>Alt is a fragment for <b><code>alternatives</code></b>. This operator means that <b>code 
the combined fragment represents a choice or alternatives of behavior.</b></p>
<p>Some pointers to take from this one are</p>
<list columns="2" type="bullet">
<li>It represents a choice of alternatives</li> <li>At most one of the operands will be chosen</li>
<li>Requires defining a guard condition for each block (implicit or explicit that evaluaes to 
true)</li> <li>An [else] condition follows the programming else concept</li>
</list>
<note>
<img alt="altCF.png" src="altCF.png" thumbnail="true"/>
</note>
</def>
<def title="[opt] Combined Fragment">
<p>The [opt] fragment represents the <b><code>option combined fragment</code></b>. This fragment 
states that <b><code>the combined fragment represents a choice of behavior where either 
the (sole) operand happens or nothing happens</code></b>. 
</p>
<note>

<img alt="optCF.png" src="optCF.png"/>
</note>
</def>
<def title="[assert] Combined Fragment">
<p>This combined fragment means that <b><code>the combined fragment represents the 
assertion that the sequence of the assert operand are the only valid continuations (i.e., all 
other continuations result in an invalid trace
</code></b></p>
<note>
<img alt="assertCf.png" src="assertCf.png"/>
</note>
</def>
<def title="[neg] Combined Fragment">
<p>These are defined as being <b><code>negative (invalid)</code>. These traces occur when 
the system has failed</b></p>
<note>
<img alt="negCF.png" src="negCF.png"/>
</note>
</def>
<def title="[ignore] Combined Fragment">
<p>The ignore combined fragment is obscue, as it is defined as <b><code>there are 
some message types that are not shown within this combined fragment. These message 
types can be considered insignificant and are impliclitly ignored if they appear in a 
correspoding execution
</code></b></p>
<note>Think of this ignore combined fragment as a way for us to define a set of messages that 
although can appear within the trace of a diagram, the position in which they come up, and their 
order does not matter, <b><code>as it also does not matter if they show upor not in a 
trace</code></b>
</note>
<p>To define these we use curly bracers and wrap around the messages that we simply don’t care 
about.</p>
<tip>
<img alt="ignoreCF.png" src="ignoreCF.png"/>
</tip>
</def>
<def title="[consider] Combined Fragment">
<p>This combined fragment states that <b><code>only those messages that are defined 
wtihin the curly braces around the name are to be considered, any other message will 
be ignored</code></b></p>
<tip>
<img alt="considerCF.png" src="considerCF.png"/>
</tip>
</def>
<def title="[ref] Combined Fragment">
<p>Ref can be used to <b><code>define that some section of our sequence diagram is 
done in another sequence diagram where its implementation is expanded upon. It can be though of 
as a continuation mark but as its own combined fragment.
</code></b></p>
<note>A combined fragment with the operator "ref" is used to represent one or more processing 
sequences enclosed in a frame and executed under specific named conditions. It can refer to 
an interaction defined on another diagram4.</note>
<tip>
<p>Sequence diagram showing the definition of a ref combined fragment</p>
<img alt="refCF.png" src="refCF.png" thumbnail="true"/>
<p>Sequence diagram showing the expanded view of the ref combined fragment</p>
<img alt="refCF2.png" src="refCF2.png" thumbnail="true"/>
</tip>
</def>
<def title="[loop] Combined Fragment">
<p>Loop can be used to <b><code>represent a repetitive sequence of interactions in a sequence 
diagram. It allows for the specification of iterative behavior with optional bounds and 
conditions. </code></b> The loop operand represents a recursive application of  he sequence 
operator where 
each iteration follows the previous one.</p>

<note>A combined fragment with the operator "loop" can be controlled by iteration bounds and/or guards. The syntax follows:
<code>loop-operand ::= loop '(' min-int ',' max-int ')'</code>
where:
<list>
<li>No bounds specified: Potentially infinite loop (0 to ∞)</li>
<li>Only min-int specified: Executes exactly that number of times</li>
<li>Both min-int and max-int specified: Executes between min and max times</li>
<li>Guard condition boolean expression: loop continuation regardless of bounds</li>
</list>
</note>

<tip>
<p>Loop variations include:</p>
<list>
<li>loop : Potentially infinite loop</li>
<li>loop(10) : Executes exactly 10 times</li>
<li>loop(5,10) : Executes minimum 5, maximum 10 times</li>
<li>loop(5,10)condition : Executes between 5-10 times unless condition becomes false</li>
</list>
</tip>
</def>
<def title="[break] Combined Fragment">
<p>The operator [break] represents a <b><code>breaking operation or exceptional 
scenario that is performed instead of the remainder of the enclosing interaction 
fragment</code></b>. A break condition always requires a guard, and it has to wrap around all 
lifelines held within a combined fragment. It breaks only when its guard condition becomes true.</p>
<tip>
<img src="https://www.uml-diagrams.org/notation/sequence-operator-break.png" thumbnail="true"/>
</tip>
</def>
<def title="[par] Combined Fragment">
<p>The operator [par] determines a potentially parallel execution of behaviors of the operands 
of the combined fragment. These operands can be interleaved in any way <b><code>so 
long as the order imposed by each operand is preserved</code></b></p>
<note>Think back to the traces example, when we looked at the parallel execution of these 
traces, we considered that a should come before b, but we never said anything about c having 
to come after a, or before it even. The idea is <b><code>within all parallel lines we should 
keep the relative order, but between parallel lines there is no need so long as the inner order 
is preserved
</code></b>
<img alt="TracesTwo.png" src="TracesTwo.png" thumbnail="true"/>
</note>

</def>
<def title="[strict] Combined Fragment">
<p>Basically this is the opposite of the seq operator where all operations within the strict 
have to happen in a <b><code>strict sequencing order</code></b>, i.e., the order of execution 
cannot be altered</p>
<tip>
<img alt="StrictCF.png" src="StrictCF.png"/>
</tip>
</def>
<def title="[seq] Combined Fragment">
<p>The seq operator represents <b><code>weak sequencing between behaviors of operands, which 
means that while order is maintained within each operand, interactions between different 
lifelines can occur in any order, </code></b> unless they are on the same lifeline where 
ordering must be 
preserved.</p>

<note>Weak sequencing is characterized by:
<list>
<li>Order of specifications within each operand remains maintained</li>
<li>Specifications on different lifelines from different operands can occur in any order</li>
<li>Specifications on the same lifeline from different operands must maintain first operand before second operand ordering</li>
</list>
</note>

<tip>
<p>Important behaviors:</p>
<list>
<li>When operands are on different participants: Reduces to parallel merge</li>
<li>When operands work on same participant: Reduces to strict sequencing</li>
</list>
</tip>
<tip>

<img alt="seqCF.png" src="seqCF.png"/>
</tip>
</def>
<def title="[critical] Combined Fragment">
<p>A critical region defines one in which <b><code>traces cannot be interleaved by 
other ocurrence specifications (on the lifelines covered by the region). </code></b> This then 
means that this region is treated <b><code>atomically</code></b>.</p>
<tip>
<img src="https://www.uml-diagrams.org/notation/sequence-operator-critical.png" thumbnail="true"/>
</tip>
</def>
</deflist>
</tip>
</def>
<def title="Continuation Marks"><p>
Within traces, and specifically within combind fragments, there are continuation marks. 
Continuation marks are used to <b><code>define continuations of different branches of an 
alternative Combined Fragment. Continuations are intuitively similar to labels 
representing intermediate points in a flow of control.</code></b>
</p>
<warning>The positioning of the label used in the Continuation marks affects the idea of 
the continuation mark as a whole. If <b><code>the label is placed underneath</code></b> all the 
operands for said alternative flow, this means that <i><code>the continuation sequence 
is defined externally</code></i>.
If this part is defined above the operands for the combined fragment, this means that all 
operands <b><code>are part of the continuation sequence that resolves said alterantive.</code></b>
</warning>
<tip>
<img src="https://flylib.com/books/4/282/1/html/2/images/umlnut2_1034.jpg" thumbnail="true"/>
<img src="https://flylib.com/books/4/282/1/html/2/images/umlnut2_1035.jpg" thumbnail="true"/>
</tip>
</def>
<def title="Gates">
<p>Gates are a sequence diagram construct that allows the diagram to 
<b><code>communicate with external sequence diagrams</code></b>, this communication is done 
<b>towards another sequence diagram</b> using a mesage that goes from a lifeline to the edge of 
the sequence diagram’s border. And <b>from another sequence diagram</b>, where the communication 
line comes from the border and into a lifeline.
</p>
<tip>
<p>Outbound communication and inboud in the same graph (origin sequence diagram)</p>
<img alt="GatesOne.png" src="GatesOne.png"/>
<p>Outbutnd communication and inbound in the same graph (receiver sequence diagram)</p>
<img alt="GatesTwo.png" src="GatesTwo.png"/>
</tip>
</def>
<def title="Lost and Found Messages">
<note>These two are important concepts as they, often define, the beginning and some end 
point of our diagrams. For example, a found message can be used to define the start of a 
sequence diagram, while a lost message can be used to define the output</note>
<p>A <b><code>Found Message</code></b> is defined as one <b><code>where the receiving event is known</code></b> 
(this could be the start of our sequence diagram), but where the is no (known) sending event. 
This might be useful to separate concerns for actors that we do not want to mention in the 
sequence diagram</p>
<tip>
<img src="https://www.uml-diagrams.org/notation/sequence-message-found.png" thumbnail="true"/>
</tip>
<p>A <b><code>Lost Message</code></b> is defined as one where the sending event is known (maybe 
the end of our sequence diagram) is known, but there is no receiving event. This is interpret 
<b><code>as if the message never reached its destination.</code></b></p>
<tip>
<img src="https://www.uml-diagrams.org/notation/sequence-message-lost.png" thumbnail="true"/>
</tip>
</def> 
<def title="State Invariants">
<p>A state invariant <b><code>is an interaction fragment which represents a runtime 
cosntraint on the participants of the interaction</code></b>. It can be used to specify variable 
values, internal or external states, etc.
</p>
<p>This is often used to convey the meaning that <b><code>for the remainder of the 
interaction to complete successfully, the condition must be true.</code></b> we can think of it 
as being evaluated <i><code>immediately prior to the execution of the next occurrence 
specification, such that all actions that are explicitly modeled have been executed.
</code></i></p>
<tip>
<img alt="stateInvariants.png" src="stateInvariants.png"/>
</tip>
<note>State invariants can also be modeled through state diagrams (i.e. state nodes) within 
the sequence diagram</note>
</def>
<def title="Corregions">
<p>Corregions are used to represent a set of events where <b><code>the sequence of 
them does not matter, they can occur safely in any order</code></b></p>
<tip>
<img src="https://support.unicomsi.com/manuals/systemarchitect/114100/Architecting_and_designing/images/coregion.png"/>
</tip>
</def>
</deflist>
</procedure>
<p>Having defined all the parameters above, it is time for us to follow an example diagram from 
the book. I have no real mind after all of that to simply write my own diagram, so I will use 
the books example to follow the procedure they do.</p>

### Sequence Diagrams ― Defining Our First Diagram
<p>The following example is about the submit book review use case example. What we will do is 
follow the four steps that they showcase in the book for writing a sequence diagram</p>
<procedure title="Four Steps To Define A Sequence Diagram" type="steps">
<step>
<note>For the first step, <b><code>always copy the use case text from the finalized robustness 
diagrams 
</code></b> to the sequence diagram’s canvas.</note>
<p>Given that we have refined our use case a ton in the previous design artifacts, the process 
now boils down to gathering the text that we already refined and transform it into the sequence 
diagram. </p>
<tip>

<img alt="sequenceDiagramStepOne.png" src="sequenceDiagramStepOne.png" thumbnail="true"/>
</tip>
</step>
<step>
<note>Having modified the static model of our application throughout the entirety of the 
analysis before, we should by now have an updated static model and an updated set of classes 
and entities to use within our sequence diagram. From this static model, 
<b><code>be sure to copy all required entity objects to the diagram's canvas</code></b></note>
<p>Up until this point, modifications to the static model should be pretty much finalized (to a 
certain extent of course), and have they not been finalized, they should be finalized as soon as 
possible. This is because this last step is not about discovering more classes or more 
attributes, is about discovering methods and behavior that can be connected to these classes. 
</p>
<p>Nevertheless, it is important to <b><code>not forget about nouns (boundary objects and actors)
</code></b>, that can also be placed within the diagram. For example all boundary views in a GUI 
app have to be visible within the activity diagram. Moreover, since we can add 
technology-dependent information, we can also add supporting architectural and technical 
information.
</p>
<tip>
<img alt="sequenceDiagramStepTwo.png" src="sequenceDiagramStepTwo.png" thumbnail="true"/>
</tip>
</step>
<step>
<note>After copying over the entity objects of our robustness diagram, <b><code>it is time to 
copy all nouns (boundar objects) into our canvas.
</code></b></note>
<p>Generally, the boundary objects and actors remain "nouns" within our logical view of the 
application. However, at this point they take a larger role as they present the entry points 
(actors) to our sequence diagram, and boundary objects the places with which the actor interacts 
with to produce some behavior that is communicated with the rest of the application</p>
<p>It is important to note that these boundaries and actors <b><code>never came from 
the static model, as these cannot be included within it</code></b>. What can be included, 
however, is the set of technology-dependent helper classes and structurally required classes 
that aid in the communication and transfer of information within your diagram.</p>
<tip>
<img alt="sequenceDiagramPartThree.png" src="sequenceDiagramPartThree.png" thumbnail="true"/>
</tip>
</step>
<step>
<note>This is the most complicated step of them all, it is no longer about copying content, 
it is about translating some content into another (mainly controllers into messages and 
behavior) that can be assigned to classes within your static model. The guidelines shown here 
will help us through this
</note>
<code>Guidelines For Correct Behavior Allocation</code>
<list type="alpha-lower">
<li><b><format color="CornFlowerBlue">Converting Controllers from Our Robustness 
Diagram</format></b>: One thing we can do is convert each controller into a communication 
message or behavior that can be then added into a class. To do this we can 
<b><code>step through our robustness diagram, and translate all controllers into 
one or more communication line</code></b>. 
<warning>We should regularly check the information we are 
putting out into our diagram. Although the robustness diagram provides a clear and concise use 
case text, it is always a good idea to check constantly and compare class diagrams with 
robustness diagrams
</warning>
Sometimes, it is more recommendable to <b><code>translate a controller into a controller 
class rather than into methods</code></b>
<note>Keep your design patterns close, as they can guide you through the design process 
effectively</note>
</li> 
<li><b><format color="CornFlowerBlue">Deciding Which Controllers to Assign to Which 
Classes</format></b>: 
To decide which controller is assigned to what class, we have to think about the level of 
responsibility we want the class to have. <b><code>Often times, we try to put everything within 
a single object and that is a problem.
</code></b> This means that we have to decide between <i><code>doing all the work within 
a class, collaborating, or delegating all work to another class</code></i>
<warning>If you think of your objects (or classes) as people, then the set of behaviors 
(operations) that they are responsible for gives them a sort of personality. We want to 
<b><code>watch out for schizophrenic objects</code></b>, because an object should be 
focused on a cohesive, related set of behaviors</warning>
</li> 
</list>
<tip>
<img alt="sequenceDiagramPartFourOne.png" src="sequenceDiagramPartFourOne.png" thumbnail="true"/>
<img alt="sequenceDiagramPartFourTwo.png" src="sequenceDiagramPartFourTwo.png" thumbnail="true"/>
</tip>
</step>
</procedure>