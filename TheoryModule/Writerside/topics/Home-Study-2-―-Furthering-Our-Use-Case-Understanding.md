# Home Study #2 ― Furthering Our Use Case Understanding 

<note><p>The following content is an expansion upon the base knowledge imparted in multiple classes about Use Cases in 
OO. For an exact definition and an explanation on how to define them check <a 
href="Class-1-Software-Design-Monday-Jan-13th.md">on the section Requirements, a closer look</a>. While for use case 
modeling through UML and how to define them to a certain extent check<a href="Class-2-Software-Design-Monday-20th.md"> 
on the section about Use cases </a>.
<br/>
If you require any other information, like further definitions on actors, and on the representations for use cases, 
check this file! </p>
</note>

## Glossary of Terms 
<procedure title="Glossary of Terms" collapsible="true">
<deflist type="wide">
<def title="System Actors">
<p>Entitity of the real world that interacts with the system through a use case. These might have roles like 
<code>customers, publishers, sellers, etc.</code>, while they could ask be software components like databases.</p>
</def>
</deflist>
</procedure>

## Use Cases ― Going Further ― Complementary Definitions
<p>While the definitions for actor, scenario and and goals have been given, and while we have also checked what use 
case instances are, we have yet to tread deeper into some content related to these actors. Specifically, we 
shall take a closer look at actors, then scenarios and finally use cases (in another section), such that we are 
capable of understanding fully use case</p>

### Complementary Definitions ― Actors
<note><p>Actors are generally defined as <b><code>something with behavior</code></b>, that can be a person, 
computer system or organization. These have some interaction with our system and often expect 
<b><code>some result from their interactions</code></b></p></note>
<p>The idea is that actors have some kind of relationships with our system, these can be both internal or externals, 
just like stake-holders in a company. There is little to no 
</p>
<p>Generally, information is sent from and to our software, independently of the type of actor that we have (human 
or machine). The difference is that in some cases, external and internal communication may <code>vary in 
terms of the communication protocol, environment , and even medium.</code>For example, external <code>human 
actors</code> might receive and consume content through a screen or mobile device with a keyboard (useful for input 
too!). However, a machine external actor might receive content through networks and different protocols for 
transferring information (XML-based communication, TCP/IP, etc)</p>
<p>The main idea here is that we ought to be able to differentiate between then to produce correct and grounded use 
cases. These use cases shouldn't just be <code>measurable</code>, but they should also be <code>grounded and 
based on one or more requirements</code>, as well as <code>centered on the user's (actor's perspective)</code>. 
Through this shift from focusing on what to do and rather on how the user will carry out a process, help us optimize 
our use cases and even our own code!
</p>
<p>There are some key terms here that we must understand like before, but these will be posted in the glossary for 
this study session. However, in an effort to keep these sessions informative, I've asked my friend Amazon Q to 
provide us some pointers to study on these two's differences</p>
<procedure type="choices" title="Difference Between Machine and Human Actors" collapsible="false">
<tabs>
<tab title="Human Actors — Characteristics">
<p>The following are the main characteristics of human actors in OOAD:</p>
<br/>
<list type="bullet">
<li><b><format color="CornFlowerBlue">Role & Context</format></b>: Human actors represent external users who interact with the system, such as administrators, customers, or operators.</li>
<li><b><format color="CornFlowerBlue">Interactions</format></b>: They actively initiate use cases, typically via UI interactions such as filling in forms, clicking on buttons, or requesting specific functionalities. </li> 
<li><b><format color="CornFlowerBlue">Goals</format></b>: Each type of human actor has specific goals they need the system to achieve (e.g., creating an account, retrieving data, submitting forms). </li><li><b><format color="CornFlowerBlue">Decision-Making</format></b>: Human actors often make decisions or provide unique inputs that influence the system's behavior or workflow.</li>
<li><b><format color="CornFlowerBlue">Feedback Dependency</format></b>: They rely on clear feedback from the system to complete tasks or validate their interactions.</li>
<li><b><format color="CornFlowerBlue">Domain Expertise</format></b>: Sometimes, they operate the system with knowledge of specific workflows or domains (e.g., system administrators may possess advanced knowledge of system requirements or configurations).</li>
<li><b><format color="CornFlowerBlue">Precondition Sensitivity</format></b>: Human actors depend on the system fulfilling preconditions like interface availability or correct initial states for certain use cases to begin.</li>
</list>
</tab>
<tab title="Machine Actors — Characteristics">
<p>The following are the main characteristics of machine actors in OOAD:</p>
<list type="bullet">

<li><b><format color="CornFlowerBlue">External Systems</format></b>: Machine actors may represent other software systems, databases, APIs, or automated services interacting with the system.</li>
<li><b><format color="CornFlowerBlue">Automation</format></b>: Unlike humans, machine actors operate autonomously based on predefined protocols, requiring no manual intervention.</li>
<li><b><format color="CornFlowerBlue">Reliability</format></b>: Machine actors are expected to function consistently and reliably according to specifications.</li>
<li><b><format color="CornFlowerBlue">Integration</format></b>: They usually interact with the system via machine-readable interfaces like APIs, data streams, or shared resources.</li>
<li><b><format color="CornFlowerBlue">Role in Dependencies</format></b>: Machine actors handle system dependencies such as third-party services (e.g., author credential databases, payment gateways).</li>
<li><b><format color="CornFlowerBlue">Event-Driven Behavior</format></b>: Their interaction is often triggered by internal or external events (e.g., data requests, scheduled tasks, or system actions).</li>
<li><b><format color="CornFlowerBlue">Data Handling</format></b>: Machine actors process input and output data in structured formats, such as JSON, XML, or standardized protocols.</li>
<li><b><format color="CornFlowerBlue">Isolated Blackbox Behavior</format></b>: Design-wise, they are treated as components with limited visibility into their internal workings beyond their interfaces.</li>
</list>
</tab>
</tabs>
</procedure>
<p>Additionally, there are three types of actors we will discuss here, only in terms of simple definitions (not 
placed in the glossary of terms as they are only important in this context</p>
<deflist type="wide" collapsible="true">
<def title="Primary Actor"><p>These drive forward use cases and user interaction with the app, they help us 
analyze user interaction deeply as these <b><code>have user goals fulfilled through using services 
of our program</code></b></p></def>
<def title="Supporting Actor (Secondary Actor)"><p>These can be seen as more closely related to secondary 
actors, and even machine actors, as these are defined as those that <b><code>provide a service 
(information, for example) to our application</code></b></p></def>
<def title="Offstage actor"><p>These are defined as those actors that <code>have an interest in the 
behavior of the use case, but do not support it directly</code>, these can be government agencies, regulator 
bodies, etc.</p></def>
</deflist>


### Complementary Definitions ― Scenarios
<p>As before, scenarios are a series of steps, decisions, or any other condition that must be taken such that a 
requirement is satisfied in some sense. For example, a company might have a system that is in charge of arranging 
deliveries during business hours, while another might be in charge of delivering outside business hours (maybe these 
can be the same system but with different configurations). Here is where scenarios come into play, suppose we give 
this software to an untrained recently hired employee. 
</p>
<p>Unless it is a hugely simplified software, with clear messages and with a human-center design all around, then 
the operator will inevitably run into some challenges. They might forget their company credentials, or misconfigure 
something. Indubitably, then, scenarios can help us prevent these, forcing the user to follow a certain path in 
testing and optimizing to lead them through it, while also checking those that can happen.
</p>
<note><p><b>Scenarios</b>, are defined as a specific sequence of actions and interactions between actors and 
the system; it is also called use case instance. It can be seen as a path or story through the system, where 
we have the common <i><b>"sunny-day path (flow)"</b></i>, commonly associated with the program and the user 
behaving beautifully and synchronized, while we also those extensions, that are divergences of this path.</p></note>
<p>Scenarios often record three relevant types of steps <i><b><code>an 
interaction between actors, a validation, or a state change by the system</code></b></i></p>

### Complementary Definitions ― Extensions

<p>Extensions are all those paths that might execute if the main <code>"sunny-day path"</code>, 
fails, receives incorrect input, or at any point fails to maintain its state. These are known as 
branches that represent possible paths of execution and their <code>outcomes (both positive 
and negative)</code> within a system.</p>
<note><p>It is often recommended, to write both a combination of the sunny-day path, as 
well as the alternative (extension) branches to produce and satisfy almost all 
stake-holder requirements independently of failure or success.</p></note>
<p>Additionally, it is often the case that, in contrast to the main flow of execution definition,
alternative paths are always more in depth and show more information that, going deep into 
recursive listing of possible scenarios and their execution paths, as well as points of return 
and no return for a system </p>
<note><p>An extension always has two parts, <b><code>the condition and the 
handling</code></b></p></note>
<p>The condition, is often known as something that can be detected by the system 
(<code>in fact, it is recommended you write them like this)</code>, while the handling 
represents the way the system should handle said condition to produce either an output, to 
restore itself, or to terminate if needed. Interestingly, most of the time by default <code>a 
extension handling block merges back with the main success scenario (not always)
</code>
</p>


## Use Cases ― Going Further ― Three Common Use Case Formats 

<p>Through these last two classes, I have grown a bit worrisome about the syntaxes and the way in which we write use 
cases. For example, in some presentations we have defined requirements through paragraphs (one or two at most) that 
indicate that a software product should do (functionality then, in most cases).
</p>
<p>On the other hand, we have used the same kind of format to define use cases (and on top of that we have assigned 
them requirements in the same format). This has had me confused as I do not really see the difference between a use 
case and a requirement. Take these two paragraphs as an example</p>
<compare type="top-bottom" first-title="Requirement Definition" 
second-title="Use Case Definition">
<code-block lang="plain text">
Requerimiento en lenguaje tradicional:
- Nombre: Requerimiento A.1
- El sistema de manejo de contenido 
tiene que permitir que un 
administrador cree una cuenta de 
blog si todos los detalles del nuevo 
blogger están verificados usando 
la base de datos de credenciales de autores
</code-block>
<code-block lang="Plain Text">
- Documentación relacionada: A.1, etc.
- Flujo normal (principal): 
  El administrador le pide al sistema 
  crear una nueva cuenta de blog 
  entrando  los detalles del autor. 
  El  sistema valida los detalles del 
  autor con la “Base de Datos de 
  Credenciales de Autores”.  
  El sistema crea una nueva cuenta de blog 
  y le manda al autor un email 
  con todos los detalles de la cuenta.
</code-block>
</compare>
<p>These two are practically the same thing, the only thing that changes is that the second (bottom) version appends 
more information and paths that is added. But had I not added titles, these two could very well pass for one 
simple requirement and a complex requirement overly defined.
</p>
<p>The truth is that this is no mistake, this happens because there are three ways to represent use cases, and one 
fo them just happens to match the style in which requirements are established. These are 
<i><b><code>brief, casual, and fully dressed use case definitions</code></b></i>, and we will be studying them soon</p>


### Three Common Use Case Formats ― Brief Format
<p>The brief format is specifically what its name says, there is no other way to explain it, no wordy sentences, it 
is simply a paragraph.</p>
<note><p>Brief-formatted use cases often define only a <code>one paragraph summary of the main success scenario.
</code></p></note>
<p>Additionally, thanks to our newest friend Deepseek we are going to get some characteristics, fact checked by our 
friend Amazon Q</p>
<procedure>
<list type="bullet" columns="4">
  <li><b><format color="CornFlowerBlue">Concise and Focused</format></b>: A brief use case is typically one 
paragraph (2–5 sentences or 3-10 steps) and avoids unnecessary details, focusing on the core purpose.</li>
  <li><b><format color="CornFlowerBlue">Clear Goal</format></b>: It describes the specific goal the use case aims to achieve, answering what the user wants to accomplish.</li>
  <li><b><format color="CornFlowerBlue">Actor-Centric</format></b>: It identifies the primary actor (user or system) and may mention secondary actors if relevant.</li>
  <li><b><format color="CornFlowerBlue">System Interaction</format></b>: It describes the high-level interaction between the actor and the system to achieve the goal.</li>
  <li><b><format color="CornFlowerBlue">Outcome-Oriented</format></b>: It clearly states the result or outcome of the use case, specifying what the system delivers.</li>
  <li><b><format color="CornFlowerBlue">Scope and Context</format></b>: It defines the boundaries of the use case 
(albeit not so formally detailed), including what’s included and excluded, and provides context for its execution.</li>
  <li><b><format color="CornFlowerBlue">Assumptions and Preconditions</format></b>: It briefly mentions conditions that must be true before the use case starts (e.g., the user must be logged in).</li>
  <li><b><format color="CornFlowerBlue">Avoids Implementation Details</format></b>: It focuses on what the system does, not how it does it, leaving technical details for later stages.</li>
</list>
</procedure>
<p>Lastly, here is an example of what we mean by a short (brief) use case format</p>
<deflist>
<def title="Brief Use Case Example">
<p>
<b>Purchase Item from Online Store</b>
<br/><br/>
A registered customer browses the online store and selects an item to purchase. After adding the 
item to their shopping cart, they proceed to check out where they confirm their shipping address 
and select their preferred payment method. The system validates the payment information and 
processes the transaction. Upon successful payment, the system generates an order confirmation, 
sends a confirmation email to the customer, and updates the inventory. The customer can now view 
their order details in their account history.
</p>
</def>
</deflist>

### Three Common Use Case Formats ― Casual Format
<p>A casual format, as defined by Alistair Cockburn (2001), who is the author of the 
aforedmentioned format. Defines this format as follows</p>
<note><p><b>A casually formatted use case</b>, consists of multiple paragraphs, which 
cover the main success scenario, and the alternative success and failure scenarios. It is 
written in a narrative form without numbered steps.</p></note>
<p>This then means that we are going ahead and expanding upon our original use case, our 
original idea of how the system should interact and behave with the user. Rather than thinking 
about only the correct path of execution, we are effectively considering the good and the ugly 
paths of execution that can happen, maybe not all of them but that is better than none.</p>
<p>The effect that this has is that, in terms of formats we are in a middle ground between fully 
dressed and brief, we are going towards detailing the real issues, actors, paths of execution 
(flows), etc.
</p>
<p>As before, we can consider some of the characteristics of this style using our best friend 
Claude</p>
<procedure> <list type="bullet" columns="4"> <li><b><format color="CornFlowerBlue">Goal-Level 
Hierarchy</format></b>: Organizes use cases into three levels - Summary (high-level), User-Goal 
(main functionality), and Subfunctions (supporting details).</li> <li><b><format 
color="CornFlowerBlue">Fully Dressed Format</format></b>: Contains comprehensive sections 
including primary actor, stakeholders, preconditions, triggers, main success scenario, 
extensions, and variations.</li> <li><b><format color="CornFlowerBlue">Stakeholder 
Interests</format></b>: Lists all parties with a vested interest in the use case, their needs, 
and what they expect from the system.</li> <li><b><format color="CornFlowerBlue">Main Success 
Scenario</format></b>: Details the primary flow of events that leads to goal achievement, 
written as numbered steps in present tense.</li> <li><b><format 
color="CornFlowerBlue">Extensions/Alternative Flows</format></b>: Documents what happens when 
things go wrong, including error conditions and alternative paths to success.</li> 
<li><b><format color="CornFlowerBlue">Scope Levels</format></b>: Distinguishes between system 
scope (black-box) and design scope (white-box) to clarify system boundaries.</li> <li><b><format 
color="CornFlowerBlue">Guarantees</format></b>: Specifies minimal and success guarantees that 
the system provides, regardless of scenario outcome.</li> <li><b><format 
color="CornFlowerBlue">Technology-Free Content</format></b>: Describes business processes and 
user intentions without referencing specific technical solutions or implementations.</li> 
</list> </procedure>
<p>Now, while this is not something that anyone would expect me to know, nor that was taught at 
all in class. I shall expand upon the use case levels for the casual format.</p>
<deflist> <def title="Use Case Levels">
<b>1. Summary Level (Cloud/Strategic)</b>

<b>Summary level use cases operate at the highest level of business processes, typically spanning 
hours, days, or even months to complete</b>. These use cases <code>encompass multiple user goals and 
business processes</code>, making them particularly valuable for executives and project managers.
They provide a strategic view of the system's capabilities. For instance, <i><code>"Manage Entire Sales 
Process"</code></i> would be a summary level use case that includes numerous lower-level 
activities. This level helps stakeholders understand the broad scope of system functionality 
without delving into 
operational details.

<b>2. User Goal Level (Sea Level/Primary)</b>

The user goal level <b>represents the most common and practical use cases, taking minutes to hours
to complete</b>. These use cases capture complete, <i><code>meaningful tasks from a user's 
perspective - the 
kind of work that provides direct value and can be accomplished in a single sitting</code></i>. For example,
"Process Customer Order" is a user goal level use case. This is considered the most important 
level for system design as it directly reflects how users interact with the system to 
accomplish their primary objectives. Most use cases should be written at this level.

<b>3. Subfunction Level (Fish/Supporting)</b>

Subfunction level use cases <b>describe the lowest level of granularity, typically taking seconds 
to minutes to complete</b>. These are <i><code>supporting tasks that are necessary to achieve user 
goals but 
don't represent complete user objectives on their own</code></i>. For example, "Select Payment Method" 
would be a subfunction level use case. These use cases are often triggered from within user goal 
level use cases and represent the detailed steps needed to complete higher-level objectives. 
While important for implementation, they should not be the primary focus of use case analysis.

</def> 
</deflist>
<p>Lastly, thanks to our little friend Amazon Q, we are going to get a singular example on how 
to define one of these kinds of use cases, specifically a <code>user goal level casual format use 
case</code></p>
<deflist>
<def title="Casual format, user goal level use case example">
<p>
<b>Use Case: Purchase Item from Online Store</b>
<br/>
<b>Primary Actor: </b> Customer
<br/><br/>
<b>Main Success Scenario:</b><br/>
Customer starts with items in their shopping cart and proceeds to checkout. They confirm their 
shipping address and select a delivery method. The system calculates total cost including 
shipping. Customer provides payment information and confirms the order. The system processes the 
payment, generates an order confirmation, updates inventory, and sends a confirmation email to 
the customer. The order is now ready for fulfillment.
<br/><br/>
<b>Alternative Paths:</b><br/>
</p>
<list>
<li>If payment fails, a customer can try another payment method</li>
<li>If items become unavailable during checkout, a customer is notified and returns to the cart</li>
<li>If a shipping address is invalid, the customer must provide a correct address</li>
</list>
</def>
</deflist>

### Three Common use Case Formats ― Fully Dressed Format
<p>The last use case format that we are going to study is the fully dressed type. This type of 
use case defines a <code>ton more points</code> than the others, and it goes in depth about 
almost all possible correct, and extension paths that can happen for almost all combination of 
user input. This is the top of the food chain in use case definition, as it includes everything 
from the others and dares to add more. Formally, it can be defined as follows 
</p>
<note><p><i>A fully dressed use case</i> describes the main success scenario, alternative 
scenarios, and failure scenarios in full detail. They typically use numbered steps to adi 
readability of alternative scenarios that branch from the main.
</p></note>
<p>This use case, as can be noted with the previous definition, suffers from a complexity issue 
unlike any other. It is basically a nightmare of bullet points and organization, and it most 
likely will force you think deeply about your code and the user's interactions with it. However, 
I must point out that there is a template that comes with this, to be presented in this file now.
</p>
<procedure type="choices" title="Template for Fully Dressed Use Cases" collapsible="true">
<table>
<tr><td>Use Case Section</td><td>Definition</td></tr>
<tr><td>Use Case Name</td><td>Serves as the initial identifier, and immediate deswcriptor 
of the use case's purpose. <b><code>It should be carefully crafted,</code></b>, 
<code>begin with a strong verb action, clear object action, and reflect the actor's goals
</code>, Most often contains business language and is between 2-5 words in length</td></tr>
<tr><td>Scope</td><td>Defines the 
boundaries and context of the system being described in the use case. <b><code>It clarifies what 
system is being specified</code></b>, <code>whether it's describing the entire organization, a 
specific software system, or a single component</code>. The scope helps stakeholders understand 
where the use case fits within the larger system hierarchy and typically indicates whether it's 
a black-box (system scope) or white-box (design scope) description.</td></tr>
<tr><td>Level</td>
<td>Indicates the hierarchical position of the use case within the business process structure. 
<b><code>It categorizes the use case into one of three levels</code></b>, <code>Summary 
(strategic/cloud), User Goal (sea level), or Subfunction (fish level)</code>. The level helps 
determine the use case's granularity and its relationship to other use cases, typically 
specified with a single word or phrase that matches one of these three categories.</td></tr> 
<tr><td>Primary Actor</td><td>Identifies the main stakeholder who initiates the use case and 
receives its primary value. <b><code>It specifies the role rather than an individual</code></b>, 
<code>describes who triggers the use case, and has goals that the system must fulfill</code>. 
The primary actor can be a human user, another system, or a time-triggered event, and should be 
described using a clear role name that reflects their organizational or system function.</td></tr>
<tr><td>Stakeholders and Interests</td><td>Lists all parties who have a vested interest in the 
outcome of the use case. <b><code>It identifies both direct and indirect participants</code></b>,
<code>specifies what each stakeholder expects from the system, and describes their specific 
interests or concerns that must be protected or addressed</code>. This section ensures that all 
relevant perspectives are considered in the use case design and implementation.</td></tr> 
<tr><td>Preconditions</td><td>States what must be true before the use case can begin. 
<b><code>It defines the required system state and conditions</code></b>, <code>lists assumptions 
that must be valid, and specifies any mandatory prerequisites that must be met</code>. These 
conditions are not tested within the use case itself but must be established before the use case 
can execute successfully.</td></tr> <tr><td>Success Guarantee</td><td>Describes what must be 
true after the use case successfully completes. <b><code>It specifies the post-conditions and 
outcomes</code></b>, <code>defines the minimal acceptable results that must be achieved, and 
outlines the promises the system makes to all stakeholders</code>. This section ensures that all 
stakeholder interests are satisfied when the use case completes normally.</td></tr>
<tr><td>Main Success 
Scenario</td><td>Describes the most common successful path that satisfies stakeholder interests. 
<b><code>It presents a numbered sequence of steps</code></b>, <code>shows interactions between 
actors and system, and describes a complete flow from trigger to goal delivery</code>. Written 
in present tense, each step represents one actor-system interaction without branching conditions.
</td></tr> <tr><td>Extensions</td><td>Documents alternative flows and error conditions that can 
occur during execution. <b><code>It captures variations from the main scenario</code></b>, 
<code>describes how the system handles failures, and specifies recovery paths or alternative 
successful outcomes</code>. Each extension is linked to a specific step in the main success 
scenario.</td></tr> <tr><td>Special Requirements</td><td>Lists non-functional requirements 
specific to the use case. <b><code>It specifies quality attributes</code></b>, <code>defines 
performance requirements, security needs, usability requirements, and other constraints that 
affect this particular use case</code>. These requirements are distinct from general system 
requirements.</td></tr> <tr><td>Technology and Data Variations</td><td>Identifies different ways 
the same goal can be achieved. <b><code>It lists alternative technologies or data 
formats</code></b>, <code>describes different implementation options, and specifies variations 
in how information can be handled or presented</code>. This section maintains technology 
independence while acknowledging implementation flexibility.</td></tr> <tr><td>Frequency of 
Occurrence</td><td>Indicates how often the use case is expected to be executed. <b><code>It 
specifies the anticipated volume</code></b>, <code>defines timing patterns of use, and provides 
metrics useful for system sizing and performance requirements</code>. This information helps in 
resource planning and system optimization.</td></tr>
</table>
</procedure>
<p>Now, since the table in and of itself is long, I will not be adding an example here, however 
I do recommend reading the <i><b><code>Use Case UC1: Process Sale on page 127 of the Craig 
Larman Applying UML and Patterns book
</code></b></i>. On the other hand, from this writing an interesting topic came about, 
specifically regarding whitebox and blackbox scopes </p>

#### Fully Dressed Format ― Black-box scope (System Scope)
<p>These are the most common and recommended kind of use cases, as they <b><code>do 
not describe the internal workings of the system, its components, or design. </code></b>. 
Rather, <i><b><code>they define and describe the system as having 
responsibilities</code></b></i>. Generally, in the books that we have covered, this is the 
longest they take in describing the way it should work. However, we must note that.</p>
<note><p>Black-box scope (system scope) use case definition, are always those that are 
related to responsibilities of the system, not the implementation details, it handles 
what the system must do to achieve some goal, not how it should do it</p></note>
<p>Given that there is not a lot of content around for this (in the books, I am sure online 
there is plenty more), I asked my friend Claude to devise a listing of characteristics for us.</p>
<procedure> <list type="bullet" columns="4"> <li><b><format color="CornFlowerBlue">External 
Perspective</format></b>: Views the system as a complete unit from the outside, focusing on what 
the system does rather than how it accomplishes tasks.</li> 
<li><b><format color="CornFlowerBlue">Input-Output Focus</format></b>: Emphasizes the 
interactions between actors and system, describing inputs provided and outputs received without 
internal details.</li> 
<li><b><format color="CornFlowerBlue">System Boundaries</format></b>: Clearly defines where the 
system's responsibility begins and ends, treating internal operations as opaque.</li> 
<li><b><format color="CornFlowerBlue">Actor Interactions</format></b>: Describes all exchanges 
between external actors and the system, including both human users and other systems.</li> 
<li><b><format color="CornFlowerBlue">Observable Behavior</format></b>: Documents only behaviors 
and results that can be observed from outside the system, excluding internal processes.</li> 
<li><b><format color="CornFlowerBlue">Interface-Level Description</format></b>: Focuses on the 
system's interfaces and external communication points without revealing implementation details.</li> 
<li><b><format color="CornFlowerBlue">Functional Requirements</format></b>: Specifies what 
functions the system must perform without constraining how these functions are implemented.</li> 
<li><b><format color="CornFlowerBlue">Technology Independence</format></b>: Maintains neutrality 
regarding technical implementation, focusing on business requirements and user needs.</li> 
</list> </procedure>

#### Fully Dressed Format ― White-box scope (Design Scope) 
<p>White-box use cases, provide a <b><code>detailed view of the internals of a 
systems functionality and implementation</code></b>.Unlike their counterparts, these use cases 
expose the inner workings, mechanisms, and component operations that make the system function, 
making them <i><code>particularly useful during the design and implementation phases 
of software development</code></i></p>
<note><p>Usually, white-box testing focus on delving into the <b>technical 
architecture and implementationd etails</b> of an application, describing how different 
components and subsystems collaborate to achieve desired functionality.</p></note>
<p>These are some of the most important characteristics of white-box scope, provided by yours 
truly Claude</p>
<procedure> <list type="bullet" columns="4"> <li><b><format color="CornFlowerBlue">Internal 
Structure</format></b>: Reveals the system's internal components, subsystems, and their 
relationships, showing how functionality is distributed.</li> <li><b><format 
color="CornFlowerBlue">Component Interaction</format></b>: Details how different parts of the 
system communicate and collaborate to achieve the desired functionality.</li> <li><b><format 
color="CornFlowerBlue">Implementation Details</format></b>: Includes specific technical 
approaches, algorithms, and methods used to accomplish system functions.</li> <li><b><format 
color="CornFlowerBlue">Data Flow</format></b>: Describes how information moves between internal 
components and how data transformations occur within the system.</li> <li><b><format 
color="CornFlowerBlue">Technical Architecture</format></b>: Specifies the technical framework, 
patterns, and architectural decisions that shape the system's implementation.</li> 
<li><b><format color="CornFlowerBlue">Internal Processing</format></b>: Shows step-by-step 
processing details, including internal validations, calculations, and business logic 
implementation.</li> <li><b><format color="CornFlowerBlue">System Dependencies</format></b>: 
Identifies internal dependencies between components, modules, and services within the system 
boundary.</li> <li><b><format color="CornFlowerBlue">Technical Constraints</format></b>: 
Acknowledges technical limitations and requirements that influence the internal design and 
implementation choices.</li> </list> </procedure>




