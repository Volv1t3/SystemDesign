# Class #5 ― Robustness and Activity Diagrams  

> The following will contain information about <b>a practical application of domain modeling, domain models, and use 
> case analysis to create an architectural view of a to-be-implemented application.</b> The content will be broken 
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

## Wednesday 5h Class & Monday 17th ― Robustness Diagrams
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
<p>Despite the class presentation showing only three parts, in theory (based on the agile 
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
screen, a report, HTML pages, or a system interface that actors interact with. On the 
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

### Robustness Diagrams ― Designing Our First Diagrams
<p>To design a Robustness diagram, there is a whole process that should be followed, and there is a whole set of 
considerations (guidelines) that we must follow to ensure that we do robustness analysis correctly.</p>
<p>In the broadest sense of the word, robustness analysis is alla bout designing these graphs and using them to 
improve our domain model, use cases, altogether, and in the end produce a middle ground step between the what domain 
model, and the how design analysis.
</p>
<img alt="TheHowMiddleGround.png" src="TheHowMiddleGround.png" thumbnail="true"/>
<p>In the following sections, we will use the base concepts reviewed in previous sections to improve our 
understanding of <i><b><code>Robustness Analysis, and Robustness Diagram Design</code></b></i></p>

#### Robustness Diagrams ― Robustness Analysis
<p>Before we delve into the ten considerations (or guidelines) for designing good robust 
diagrams and applying those in the context of our design modeling. We need to take a step back 
and discuss the topic at hand, Robustness Analysis, since these ten guidelines are meant to 
facilitate this process</p>
<note><p><i>Robustness Analysis <b><code>is a technique that bridges the gap between analysis and design 
in software development by validating and refining use cases through visual modeling</code></b>. It employs 
specialized diagrams that use three main types of objects—boundary objects (interfaces), 
control objects (processing), and entity objects (data)—,to <i><code>represent system interactions and 
behaviors</code></i>. The analysis <i><b><code>helps 
identify missing requirements, clarify system responsibilities, 
and expose potential design flaws early in the development process</code></b></i> by forcing developers to 
think through how use cases will be implemented. Robustness Analysis serves as an intermediate 
step between use cases and sequence diagrams, providing a way to verify that use cases are 
complete and technically possible before moving into detailed design. This technique, originally 
developed as part of the ICONIX process, helps teams create more robust and maintainable 
software systems by ensuring that the design supports all required capabilities.</i></p></note>

<p>From this little sidenote we can then extrapolate two things, one the <b>ICONIX process</b> 
which would be a great home study session, as well as the use of robustness analysis. We can 
think of this type of analysis as a means to and end through which we validate the use cases 
we've written, a means to and en through which we further ground our design into more feasible, 
implementable, and overall correct use cases and requirements.</p>
<p>For this reason, this crucial design step is taken after the use case modeling phase has 
passed (since we are in an iterative environment, this never really stops, but we 
cannot just go back to this all the time). The idea then is to bridge this gap that might exist 
between the design analysis phase (i.e, when we take care of designing conceptual classes and 
defining further interactions), to this diagramming, and more abstract, wishful, to some extent, 
phase of OOAD.
</p>
<p>Having analyzed its implications, it becomes important to write about the pros, cons and key 
points about Robustness Analysis, such that our information is complete at least for this 
section.</p>
<procedure title="Robustness Analysis in Software Development ― Key Notes, Pros, and Cons" collapsible="true">
<tabs>
<tab title="Robustness Analysis | Key Points">
<list>
<li><b><format color="CornFlowerBlue">Definition and Purpose</format></b>: A bridging technique between analysis and design phases that validates and refines use cases through visual modeling</li>
<li><b><format color="CornFlowerBlue">Core Components</format></b>: Three main object types:
- Boundary objects (interfaces)
- Control objects (processing)
- Entity objects (data)</li>
<li><b><format color="CornFlowerBlue">Design Role</format></b>: Acts as an intermediate step between use cases and sequence diagrams</li>
<li><b><format color="CornFlowerBlue">Analysis Level</format></b>: Focuses on validating use case completeness and technical feasibility</li>
<li><b><format color="CornFlowerBlue">Origin</format></b>: Developed as part of the ICONIX process for software development</li>
</list>
</tab>

<tab title="Robustness Analysis | Pros">
<list>
<li><b><format color="CornFlowerBlue">Requirements Validation</format></b>: Helps identify missing requirements early in the development process</li>
<li><b><format color="CornFlowerBlue">Design Verification</format></b>: Ensures use cases are technically feasible before detailed design</li>
<li><b><format color="CornFlowerBlue">System Clarity</format></b>: Clarifies system responsibilities and interactions</li>
<li><b><format color="CornFlowerBlue">Early Problem Detection</format></b>: Exposes potential design flaws at an early stage</li>
<li><b><format color="CornFlowerBlue">Implementation Guidance</format></b>: Forces developers to think through practical implementation details</li>
</list>
</tab>

<tab title="Robustness Analysis | Cons">
<list>
<li><b><format color="CornFlowerBlue">Additional Step</format></b>: Introduces an extra phase between analysis and design</li>
<li><b><format color="CornFlowerBlue">Learning Requirements</format></b>: Teams need to understand specialized diagram notation and concepts</li>
<li><b><format color="CornFlowerBlue">Process Integration</format></b>: Must be effectively incorporated into existing development workflows</li>
<li><b><format color="CornFlowerBlue">Time Investment</format></b>: Requires dedicated effort for visual modeling and analysis</li>
<li><b><format color="CornFlowerBlue">Methodology Specific</format></b>: Originally tied to ICONIX process, may need adaptation for other methodologies</li>
</list>
</tab>
</tabs>
</procedure>
<p>Having defined these considerations, it is time for us to take a look at the ten key 
guidelines about Robustness Analysis</p>

##### Robustness Analysis ― Ten Guidelines
<p>These ten guidelines are ten principles that can be applied when designing, iterating, and 
even implementing a robustness diagram or analysis. The ideas that they present involve 
all aspects of the analysis process, from use case analysis, robustness diagram preparation and 
design, as well as the iterative process that holds the two together and takes our conceptual 
understanding of our system further</p>
<procedure>
<deflist type="full" collapsible="true">
<def title="1. Paste the Use Case Text Directly onto your Robustness Diagram.">
<p>Since we are painting a picture of the use case, <b><code>line by line and action 
by action</code></b>, it is generally advisable to keep the whole text of the use case nearby. 
Some prefer to keep it on another window, others to include it within the diagram as a comment. 
Whichever the selected option, this straightforward rule follows <i><b><code>you'll work through 
the use case a sentence at a time as you draw diagram [effectively] making them two 
different views of the same thing. Therefore you should be able to walk through the 
text, and trace it on the diagram</code></b></i>
</p>
<p>An example of this would be. </p>

<img alt="Ex1.png" src="IncludingUseCaseText.png" thumbnail="true"/>
</def>
<def title="2. Take Your Entity Classes From the Domain model and Add Any That Are Missing.">
<p>In general, it is a good practice to <b><code>base your entity objects from your 
domain model, i.e., they should come from it</code></b>. However, it is not uncommon for a 
domain model to be lacking in some areas and excel in others, meaning that you 
<b><code> might have to add some classes onto it later on</code></b>. If at any point in your 
robustness analysis does a single class come about, and it is not in your domain model, add it!</p>
<note>As a little sidenote, a robustness diagrams, typically represents GUI elements as 
boundary objects, software functions using controllers, and domain objects using entities.</note>
</def>
<def title="3. Expect to Rewrite Your Use Case While Drawing the Robustness Diagram.">
<p>Just like with any other project, essay, or even our own domain model analysis, rewriting is 
key and being open to doing so is a must in this world. More often than not, first drafts show 
<b><code>vague, ambiguous text; incomplete or incorrect information</code></b>. As such, it is 
not uncommon to find cases where we will have to rewrite, shorten or lengthen our use case 
definitions by having to iterate over it line by line, this because it  
<b><code>brings errors to the surface.</code></b></p>
</def>
<def title="4. Make a Boundary Object For Each Screen">
<p>This is one rule that we must never forget, <b><code>all user facing boundary 
objects should have a name, an unambiguous one at that</code></b>. Moreover, we should always 
include these boundary objects as they help us structure the flow of information that goes into 
the diagram.</p>
</def>
<def title="5. Remember that Controllers Are Typically Logical Software Functions.">
<p>This one might be harder to wrap our heads around, given that we have been talking mostly 
about non-software related topics just yet. We often think about robustness diagrams as only 
showing actions and hiding away from software constructs, but this is actually the opposite.</p>
<note>Always consider that not all controllers become controller classes in the end, some of 
then represent logical software functions that will become communication paths (methods for 
example). Only in the case where a series of controllers are clustering do we talk about 
<b><code>manager classes*</code></b></note>
</def>
<def title="6. Dont Worry About the Direction of the Arrows on a Robustness Diagram.">
<p>This is another one of those rules that Daniel told us during class. While sometimes they can 
help make a diagram less ambiguous, they are not required. <b><code>Given that these 
diagrams are meant to disambiguate our use case text, and help us discover missing 
domain model objects</code>, any line’s direction might not be required, or useful 
<code>however, if we are trying to show data flow or control flow, they might!</code></b></p>
</def>
<def title="7. Show invoked Use Cases In Your Robustness Diagram.">
<p>As the title of this rule states, if we were to find ourselves within a use case that holds 
within it multiple invocations, or that to some extent requires us to call other use cases to 
perform its main business logic. Then we have to include them. The way to do so is through the 
keyword <b><code>invokes</code>, placed right above or in the middle of the communication 
line</b> from an <b><code>object to the use case</code></b></p>
<p>An example of this would be.</p>

<img alt="InvokinguseCases.png" src="InvokingUseCases.png" thumbnail="true"/>
</def>
<def title="8. The Robustness Diagram Represents a Preliminary Conceptual Design of a Use Case.">
<p>One key benefit of preparing robustness diagrams before trying to build code is that, as 
these are conceptual design artifacts for our system, we can <b><code>validate 
behavior without doing the real design, before of it even!</code></b></p>
<note><p>While this process might appear to be complicated at first, given that it is a 
different process altogether from a development perspective, working with it allows for 
detachment of our thinking from the idea->code->debug->refactor cycle, and focus on what we are 
doing and 
the abstract how, not the language-dependent how.
</p></note>
</def>
<def title="9. Objects on your Robustness Diagram will 'Morph' into the Detailed Design.">
<p>In our implementation, we generally separate <i><code>nouns to be entity and 
boundary objects, and verbs to be controllers</code></i>. While this might give way to the idea 
that every little diagram entity done has to become a class later on, the truth is that only 
boundary and entity objects will become an object.</p>
<note><b><code>More often than not, 
controllers will end up as messages or methods in boundary or entity classes, while 
the latter will become classes or active entities in our system</code></b></note>
</def>
<def title="10. Remember that a Robustness Diagram is an 'Object Picture' of a Use Case">
<p>This guideline goes back to our main ideas, since we are doing this process of robustness 
analysis in order to improve our use case definitions and ground them in relation to the domain 
model that’s been defined for the system, it is important that we think of these diagrams as 
pictures of how the use case is supposed to play out in steps.
</p>
<p>Always remember that <b><code>a robustness diagrams ties use cases to objects and 
the application's GUI. For this reason, it must not show just the basic course, but 
all the alternative courses as well</code></b></p>

<img alt="image.png" src="AllPathsDiagram.png" thumbnail="true"/>
</def>
</deflist>
</procedure>
<note><p>As a reminder, entity objects (nouns) are capable of talking to 
<b><code>controllers only</code></b>. On the other hand, <b>controller entities</b>, can 
only communicate with <b><code>other controllers or entities</code></b>. Lastly, 
<b>boundary objects</b> can only talk to <b><code>controller objects</code></b></p>
<img alt="image.png" src="AllValidrelationships.png" thumbnail="true"/>

> As a sidenote to the sidenote, the previously shown tool is called EA, which is an enterprise 
> tool developed, actively used, and updated, by Sparx Systems.
</note>
<p>With this information, let’s first take a look at a simple diagram example, and attempt to 
identify the issues that are held within it</p>

#### Robustness Diagrams ― Analysis Example

<procedure title="Side-by-side comparison for a set of diagrams from the Internet Book Store example" type="choices" collapsible="true">
<code>Before Refinements</code>
<list columns="1" type="none">
<li>
<deflist type="full" collapsible="true">
<def title="Diagram">
<img alt="clipboard-image-1739827257.png" src="JSPFirstAttemptDiagram.png" thumbnail="true"/>
</def>
</deflist>
</li>
<li>
<deflist collapsible="true">
<def title="Analysis">
<p>The previous diagram shows a first attempt at formulating a robustness diagram for the basic 
course of the <b><code>Show Book Details use case</code></b>, while it in theory captures the 
sequential logic of the use case, and traversing this diagram with ease is possible as we follow 
the use case definition, there are various points of contention where we can improve our 
analysis and in general our diagram definition. </p>
<p>For starters, one of the main complications is the lack of arros (<i>yes in this case it 
is an issue)</i>, in most cases a simple diagram is traversible without knowing the direction of 
the arrows, but in this case, without knowing the use case definition it is hard to figure out 
if flow goes to the home page and to the View Book Details in parallel, or sequentially, or if 
one depends on the other. The idea of a robustness diagram is to add more depth, but keep the 
interaction readable, to a use case.
</p>
<p>Moreover, some components mix names that can be though of as actions, nouns, and a mixture 
of both. For example, the <b>View Book Details</b> boundary object can be simplified to <b>Book 
Details</b>, to isolate the fact that it handles an entity object, and it is meant to handle its 
details. Lastly, there are issues on the naming conventions of other boundary objects. 
<b><code>Never add technology-dependent naming into a robustness diagram</code></b>, their use 
is not to indicate what technology will be used, rather their use is to show the flow of 
actions within a use case.
</p>
</def>
</deflist>
</li>
</list>
<code>After Refinements</code>
<list type="none">
<li>
<deflist collapsible="true" type="full"> 
<def title="Diagram">
<img alt="clipboard-image-1739827815.png" src="ImprovedRobustDiagram.png" thumbnail="true"/>
</def>
</deflist>
</li>
<li>
<deflist type="full" collapsible="true">
<def title="Analysis">
<p>As can be noted in the robustness diagram, many of the issues highlighted before have been 
fixed, and the use case definition has been improved with more information and concept 
separation. For starters, even if there are no line directions in the diagram, the way it is 
structured now provides for an easy way to distinguish steps in the use case. First the user 
interacts with the home page, where the system calls internal controller actions to retrieve 
information (possibly from a database, and in the form of Book Lists and Catalogs), and proceeds to 
display them. <i>This on its own</i> already organizes the use case much better, showing  
that first loading happens, and then the user can click on any book and be taken to the Books 
Details page, where the system populates the information of another query only about the 
selected book.
</p>
<p>Moreover. the technical jargon has been removed and allows for a clearer diagram to be 
presented where the path of information now clearly follows the use case, and showcases the 
process to great detail.</p>

</def>
</deflist>    
</li>
</list>
</procedure>
<p>Within the book, there is a singular example that showcases the process in its entirety. 
While the goal of this section is not to copy the example completely, we will take from it, both 
images and information to create our own narrative here.
</p>

#### Robustness Diagrams ― Design Process
<p>One of the first things to do when starting a new robustness diagram is to first pull up the 
use case definition text, and as we defined earlier, bring it over as a comment or on a 
second monitor close to you so you can iterate over it line by line.</p>
<p>From here our goal is to, aside from <b>not panicking</b>, to handle the first line of our 
use case. In practice this first line should <i><code>include the actor (primary, 
secondary or supporting), that is involved with the use case</code></i>, with this primary 
component identified, we should move to put it on the screen directly.</p>
<note>In some cases, our use case definitions might go as deep as to specify what UI 
component is used for which action and at which moment in the interaction. While this 
can be useful to contextualize the app, <b><code>it is generally not 
recommended to add UI components individually into a robustness diagram</code></b>, rather they 
should be wrapped within screens, pages, or any other UI-holding component.
</note>
<p>Now, as the use case continues, we might find mentions to UI elements, or actions done to 
them (consider a button and a mention to "being pressed"). In these cases, it is better to 
define those actions in terms of <b><code>comments above communication lines</code></b></p>
<procedure>
<img alt="clipboard-image-1739828715.png" src="DiagramUpToThisPoint.png" thumbnail="true"/>
</procedure>
<p>From the communication image clearly there is still a series of ambiguous 
statements, and communication lines. For example, while the use case refers to the write review 
button being pressed, <i>we do not know from where</i>, is the state of where the user pressed 
the button important to us?</p>
<p>Moreover, there is ambiguity in the definition for both click and enter, and enter review and 
click send, which one is supposed to come first, which one calls to what part of the system. All 
of these inconsistencies are present in our <b>use case definition too</b>, since we based the 
diagram from it, we can start to see the fallacies in our model. All in all, while the main 
ideas of the use case are present in the diagram, they need further clarification before we can 
say that this diagram is completed.
</p>
<p>Based on the domain model for this example, we can notice that for the customer to even press 
the review button, they must be located within a book page (!). This then means that the action 
of pressing the button is not registered directly by the Write Review Page, but by the 
<b>Book Details Page</b>, where the options for such a task would be present. In addition, we 
can see that the enter review and click send action can only be carried out within the <i>Write 
Review Page</i>, separating both concerns from each other in terms of the GUI.
</p>
<p>Furthermore, looking at the controllers that extend from the singular boundary object of our 
model, clearly these can be expanded and refined further, as the moderation aspect of 
the use case is clearer and well-defined in the text. The moderation activity in the end of the 
use case diagram can too be included, but this time, since it involves another actor, it can be 
added as a <b><code>use case invocation</code></b>
</p>
<procedure>
<img alt="clipboard-image-1739829658.png" src="ImprovedDiagramWithUseCaseinvocation.png" thumbnail="true"/>
</procedure>
<p>One key feature of the previous diagram is that it shows clearly the <b><code>main flow
</code></b> of our use case. It can be easily understood as a representation of all steps that 
have to be true for the use case to finish successfully. However, this means that the diagram 
ignores all <b><code>alternative flows</code></b>, that in this case extend far from the user 
space (log in or not logged in), but also towards the moderation and content verification 
concerns.</p>
<p>In this section, it is important to note that while we can leave conditions implicitly 
defined, <i>like the version of the diagram shown in figure 5.15</i>, it is often recommended 
not to do this as we can add information on the alternative flows. For example, in the case the 
book review length is not okay (i.e., &lt; 10 characters), a separate, alternative flow, can be 
presented in the diagram to show how information flows if any, or both, conditions are not 
correct.</p>
<p>As for the user case, clearly, the diagram requires more than just a simple corrective step. 
First, we need to think about our domain model. Is there any object (as entities have to come 
from there), that can handle the task of managing and verifying user sessions and passwords? If 
this part exists, then it can be used directly in the graph, if it does not, we must create a 
new domain conceptual class, and add it to the diagram. In the case of this use case, and this 
domain model, said class does not exist and it must be added. Moreover, through this analysis, a 
point can be raised that the Log In use case can be brought here, as we do not need to showcase 
all the steps the log in use case shows, only call it and manage its results.
</p>

<procedure>
<img alt="ImprovedUseCaseWithAlternativeFlows.png" src="ImprovedUseCaseWithAlternativeFlows.png" thumbnail="true"/>
</procedure>
<p>To conclude this series on the design process for a robustness diagram, the following diagram 
showcases the full output of the entire process. Including the concept mentioned before of 
appending further information to alternative paths in regards to UI and responses to faults.
</p>

<procedure>
<img alt="FinalizedRobustnessDiagramForBookReviewUseCase.png" src="FinalizedRobustnessDiagramForBookReviewUseCase.png" thumbnail="true"/>
</procedure>


## Monday 10th Class ― Activity Diagrams
<p>An activity diagram can be thought of as a flow diagram with added information. The idea is that 
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


