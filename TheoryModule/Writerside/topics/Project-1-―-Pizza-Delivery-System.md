# Project #1 ― Pizza Delivery System 

> This file contains all information requested within the specification for homework #1 (project #1) for System 
> Design NRC ().
> It includes all information regarding the domain model analysis done, and use-case definition and 
> diagramming.
> It is separated into various sections detailing all content related to the project specification and 
> realization.

<note><p>The following is information related to te project, group names and identifiers, etc.
</p>
<list>
<li><b><format color="Orange">Assignment Name</format></b>: 
 [Project One: Pizza Delivery System],
</li> 
<li><b><format color="Orange">Group Members</format></b>: [
<list type="none">
<li><b><format color="Orange">Marcos Lopez Pazmiño</format></b> [00332617],</li> 
<li><b><format color="Orange"> Carlos Flores Villacis</format></b> [00329746], </li> 
<li><b><format color="Orange">Santiago Arellano Jaramillo</format></b> [00328370],</li> 
</list>
]
</li></list>
</note>

## Domain Modeling Process
<p>The following subsections contain the information produced, analyzed, and iterated over to define a domain model 
that reduces into a single graph all the interactions inside our system. From <code>User Management, down to 
Authentication and AI Analysis</code>, all relevant <i>business-level and user-level
</i> requirements have been analyzed and filtered to produce a domain model that is extensive, yet extensible enough 
to be incrementally built upon to produce more features where the specification is to grow, or to reduce features where 
the specification to be adjusted.
</p>
<p>The original specification was expanded thoroughly to accommodate for design decisions like authentication, 
content management, payment processing, among other requirements that were fleshed out based on previous experiences 
with systems like the specified one. Internally, our application mirrors functionality that is included in 
applications such as <b><code>Uber Eats or Pedidos Ya</code></b>, attempting to build upon the extensive knowledge base that these 
applications can offer, reducing their reach and refocusing them towards a pizza delivery system.</p>
<p>Requirements defined in the new refined requirements table, such as account management, verification, storage, or 
experiences with applications that operate within a similar market. <i>Through careful analysis of their domain models 
even delivery and tracking options, we were expanded upon based on the team's collective knowledge and shared 
(or at least the domain model that is perceivable through their application's user facing functionality), we were 
able to improve our application</i>, and our understanding of this system.</p>
<p>Internally, this section will present the key steps done to procure a correct, functional, and accurate domain 
model through an iterative approach that started with a keyword and <b><code>noun phrase</code></b> keyword 
selection of the original specification. In parallel to this, our team analyzed <i>all base <b>requirements</b></i> 
that could be extracted from the original specification to piece together our basic understanding of the development 
process at hand.</p>
<p>Once this analysis was done, we bifurcated again into two development branches done in parallel. The first 
development line focused solely on defining potential classes and refining them for the last stage, 
<i><code>the domain model diagram</code></i>, while the second development line attempted to piece out a more 
refined requirements listing to procure correct use cases.
</p>

### Development Steps ― Keyword Mapping and Base Requirements
<p>Once the specification had been revised, and the project idea selected, we focused on, as we mentioned earlier, 
producing two software design artifacts key to our domain model assessment.</p>

#### Development Steps ― Keyword Mapping
<tldr>Keyword mapping served as a pivotal point in our design iterations, as through these keywords we defined 
possible classes and mapped them towards the domain model design effectively. Without these keywords, the project 
only consisted o requirements, and we were unsure on how to implement them.
</tldr>
<p>One fundamental step that our team took was to decide what parts of the specification made sense, which ones 
needed more work, and which ones were a design element that we should include in our next iterations. To do 
this, we first began with a process of <i><code>keyword extraction</code></i> from the specification using the 
<i><b>noun phrases</b></i> approach with a hybrid of sentence analysis and <i><b>conceptual class categories</b></i>,
through which we defined both specification-related keywords and added keywords our experiences told us we required
</p>
<p>From this hybrid approach we produced five categories, <i><b><code>AI-driven Delivery Forecast, 
Delivery Management and Optimization, Inventory Prediction and Management, Customer Registration && 
Profile Management, and Pizza Ordering Process</code></b></i>. Within each of these we defined actors, nouns, verbs, 
and even possible classes that in any way supported our concept model of the application and added onto, or came 
from, the specification supplied for this project. The following image showcases the entire graph that was 
produced as a design artifact</p>

<deflist collapsible="false">
<def title="Design Artifact: 'Pizza Delivery Service | Keyword Mapping' ">
<img alt="DesignArtifactOne.png" src="DesignArtifactOne.png" style="block" thumbnail="true"/>
</def>
</deflist>
<note>If the image appears to small, this is an issue on our end as it is a large image that we are trying to 
present in a small frame. In addition to this view, this image can be found within the GitHub files for this 
repository for better visualization. Moreover, the website allows for its storage as for any other image presented here.
</note>
<p>One of the key aspects done here was to distribute these keywords into five sections. While there is some 
overlap between the analysis and AI forecasting sections, we believed in the separation of concerns as a good thing 
for our design analysis and the iterative process that we were trying to implement. For instance, while we worked on 
classes for the Pizza Order, we could go back and append information into the Pizza Ordering Process bubble as we 
found more keywords or details that we had missed in our original revision.
</p>
<p>The same can be said about the reverse process. We often came back to the keywords mapping both in the domain 
model definition, and the class definition process to orient ourselves and keep in touch with our original design 
ideas.</p>

#### Development Steps ― Base Requirements
<p>In parallel to that line of development, our team focused on defining and collecting all requirements defined 
within the base specification. While at this phase in development, it is quite early to define requirements head on, 
since most of the work happens in the class definition, we decided to define these as a guideline to, in another 
iteration, increment on top of them before we defined the complete domain model.
</p>
<p>For this reason, our team produced the following requirements table</p>

<procedure title="Design Artifact: 'BaseSpecification Requirements'" collapsible="true">
<table>
    <thead>
        <tr>
            <th><format style="bold" color="CornflowerBlue">ID</format></th>
            <th><format style="bold" color="CornflowerBlue">Title</format></th>
            <th><format style="bold" color="CornflowerBlue">Description</format></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>ACCMA01</td>
            <td>Customer Registration Process</td>
            <td>The system should be capable of providing an option for customers to register an account with the pizza shop</td>
        </tr>
        <tr>
            <td>ACCMA02</td>
            <td>Customer Registration Allows Preference Storage</td>
            <td>The system should allow a registered user to input preferences on shipping, billing, and payment methods, such that the information is not re-entered again.</td>
        </tr>
        <tr>
            <td>ACCMA03</td>
            <td>Customer Registration Control Panel</td>
            <td>The system should provide registered users with the ability to change their stored information through account settings</td>
        </tr>
        <tr>
            <td>ADFMA01</td>
            <td>AI Integration For Delivery Analysis</td>
            <td>The system should leverage and connect with AI services to perform analysis and forecasting of information</td>
        </tr>
        <tr>
            <td>ADFMA01-01</td>
            <td>AI Integration With Delivery Schedules</td>
            <td>The AI Integration of this system should allow it to analyze and forecast optimal delivery schedules.</td>
        </tr>
        <tr>
            <td>DELMA01</td>
            <td>Delivery Optimization</td>
            <td>The system should be capable of analyzing and modifying delivery routes.</td>
        </tr>
        <tr>
            <td>DELMA01-01</td>
            <td>Delivery Optimization With Allowed Radius</td>
            <td>To improve delivery efficiency, the system should allow managerial accounts to modify a delivery 
radius for drivers</td>
        </tr>
        <tr>
            <td>DELMA01-02</td>
            <td>Delivery Optimization With Data Collection</td>
            <td>To perform such an optimization, the system should be capable of interfacing with a GPS system to collect longitude and latitude data from each driver.</td>
        </tr>
        <tr>
            <td>DELMA01-02-01</td>
            <td>Data Collection Frequency</td>
            <td>The system should allow for monitoring and modification of the frequency in which GPS data is collected from drivers</td>
        </tr>
        <tr>
            <td>ORDMA01</td>
            <td>Placing An Order Through Website</td>
            <td>The system should allow for the user to create, modify and finalize an order through a web browser. 
Allowing the user to search for Pizzas, add them to their cart, and then fulfill their order</td>
        </tr>
        <tr>
            <td>ORDMA02</td>
            <td>Check-out Requires An Address</td>
            <td>The system should validate that to proceed to check-out, the user must provide a delivery address.</td>
        </tr>
        <tr>
            <td>ORDMA03</td>
            <td>Check-out Requires Valid Payment Method</td>
            <td>The system should validate a payment method and depending on which is used, request more information to accurately perform a monetary transaction</td>
        </tr>
        <tr>
            <td>ORDMA03-01</td>
            <td>Check-out Requires Valid Payment Method—Credit Card</td>
            <td>The system should validate that if the user selects to pay with a credit card, the information should be submitted in its totality for a payment process</td>
        </tr>
        <tr>
            <td>POSMA01</td>
            <td>AI Integration For Predictive Inventory Analysis</td>
            <td>The system should be capable of gathering sales data and ingredient usage data to predict quantities required to meet demand</td>
        </tr>
        <tr>
            <td>POSMA02</td>
            <td>AI Integration Through Predictive Algorithms</td>
            <td>The system should leverage AI and predictive algorithms to optimize inventory management, reducing 
waste,and minimizing stock shortages</td>
        </tr>
    </tbody>
</table>
</procedure>
<p>The process carried out here details our original chain of though about the specification, and in tandem, about 
the system as a whole. The requirements, ordered based on their IDS revolve around the five sections described both 
in the specification document and in the keyword mapping section of this documentation webpage. <i><code>All of the 
information was either expanded upon slightly, or taken in their entirety from the original specification.
</code></i>, all in an effort to produce a coherent set of goals and functions that the user must allow, but without 
thinking too much on the implementation of said features just yet.
</p>
<p>With these two steps done, but with our mind still placed upon the idea of continuous refactoring and improvement,
we set our sights on a second development iteration process, our second sprint to produce both the possible classes, 
and the actors of our system
</p>

### Development Steps ― Possible Classes and Actors
<p>Based on the specification's requirements, and the content produced in our original sprint when it came to 
keyword mapping, our team worked on defining all possible classes in our system, keeping them light (i.e., not many 
parameters were defined, nor the relationships between them), but also concise and grouped by the same categories 
that we had used to organize our keyword ideas.</p>

#### Development Steps ― Possible Classes
<p>With the keywords defined, and the specification written out, our team figured out a series of classes, relating 
to all points of contention in the documentation, our analysis, and within the five overarching groups we defined 
earlier. The design artifact produced here is the following</p>

<deflist type="full">
<def title="Design Artifact: 'Pizza Delivery Service | Possible Classes'">
<img alt="DesignArtifactThree.png" src="DesignArtifactThree.png" thumbnail="true"/>
</def>
</deflist>
<p>As can be noted through the previous image, we denoted all classes within the same categories, and in addition, 
we defined with a green border color those classes that passed all of our requirements and our notions for the 
application and were directly placed within the final domain model.</p>
<p>Inherently, though, we can also notice a series of connections and aggregations of classes represented by various 
hierarchical levels in the lines or bubbles used in the diagram. Take as an example the <code>ShoppingCart</code> 
class, where there are lines connecting it to <code>Order, Pizza, and Ingredient</code>, all classes that are 
aggregated on top of each other to produce a customer shopping cart and populate it with information.
</p>
<p>Notions like these came in handy when we defined the domain model, as our common understanding of composition, 
inheritance and aggregation helped us achieve a high-cohesion model where classes and objects are not specifically 
attached to each other forming dependency cycles, rather they know about each other, and only in specific 
circumstances are they composed of each other.
</p>

#### Development Steps ― Possible Actors 
<p>Despite the size of our possible class definition, we reduced the scope of our system's actors when we viewed 
them not just from a software perspective, but as books on the matter recommend, we saw them both from the business 
stake-holder perspective, and the programming and design model. When viewed from both angles we managed to identify 
a series of possible actors <b><code>separated into primary and supporting actors</code>, each with their own 
<code>external and internal categories</code></b>. These classifications helped us understand what points of our 
system would be in touch with which actors, and in later stages, these helped us optimize our use case analysis. For 
now, however, we simply present the design artifact as is, it will be expanded upon later.
</p>

<deflist>
<def title="Design Artifact: 'Pizza Delivery Service | Actors'">
<img alt="DesignArtifactFour.png" src="DesignArtifactFour.png" thumbnail="true"/>
</def>
</deflist>

### Development Steps ― Refined Requirements
<p>Once these design elements were produced, we began work on a new requirements table that expanded upon all the 
ideas presented both in our discussions, and in the base specification for the project. The idea of this section was 
not to just repeat what has been said before in the base requirements, rather, we used it as a point to expand our 
original goals and functional requirements for the system, keeping in mind that we must be declarative and 
expressive in our documentation. In this sense, we produced the following listing that is collapsible for visibility 
purposes.
</p>
<procedure title="Design Artifact: 'Refined Requirements'" collapsible="true">
<table>
    <thead>
        <tr>
            <th>ID</th>
            <th>Title</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>ACCMA01</td>
            <td>Customer Registration Process</td>
            <td>The system should be capable of providing an option for customers to register an account with the pizza shop</td>
        </tr>
        <tr>
            <td>ACCMA02</td>
            <td>Customer Registration Allows Preference Storage</td>
            <td>The system should allow a registered user to input preferences on shipping, billing, and payment methods, such that the information is not re-entered again.</td>
        </tr>
        <tr>
            <td>ACCMA03</td>
            <td>Customer Registration Control Panel</td>
            <td>The system should provide registered users with the ability to change their stored information through account settings</td>
        </tr>
        <tr>
            <td>ACCMA04</td>
            <td>Registration Generalization—Account Type Differentiation</td>
            <td>The system shall be capable of supporting different, specialized, account types for various access rights and functionalities, separated from the aggregate of the program (Customer, Delivery Drivers, Administrators, Managers)</td>
        </tr>
        <tr>
            <td>ACCMA05</td>
            <td>Registration Generalization—Account Differentiation</td>
            <td>The system shall guarantee that certain fields within each of the created Account Types follow validation procedures. Moreover, certain fields shall remain unique internally as to differentiate between Account Types and users.</td>
        </tr>
        <tr>
            <td>ACCMA05-01</td>
            <td>Account Differentiation - Input Parameters And Unique Validation</td>
            <td>The system shall be capable of storing log-in information pertaining to the user (independently of their access rights). Moreover, it shall guarantee that the individual username stored internally per Account is unique to that Account. 
            <br/>
            - Additionally, contact information supplied at any access right level should be validated to ensure proper communication channels can be established</td>
        </tr>
        <tr>
            <td>ACCMA06</td>
            <td>Customer Management—Profile Management and information</td>
            <td>The system should store detailed information about a Customer profile, including order history, 
rating history (specifically related to Pizzas),
and any support tickets that the user might open during the existence of their accounts in our systems.</td>
        </tr>
        <tr>
            <td>ACCMA07</td>
            <td>Driver Management - Profile Management</td>
            <td>The system shall be able to collect, validate, and report various driver-specific parameters such as license details and validity, performance metrics, and delivery zone management</td>
        </tr>
        <tr>
            <td>ACCMA08</td>
            <td>Administrative Management</td>
            <td>The system must allow various access rights levels to modify fields in their respective areas to improve the functioning of those and the system as a whole. To this end, it should keep logging information for any administrative accounts.</td>
        </tr>
        <tr>
            <td>ACCMA09</td>
            <td>Account Management—Account Security</td>
            <td>The system shall implement a series of security features to authenticate registered users and deter malicious actors. For this reason, the system should implement methods like login attempt tracking, session management, and password authentication supplied by a subsystem.</td>
        </tr>
        <tr>
            <td>AISMA01</td>
            <td>AI Service Authentication And Connection</td>
            <td>To leverage the data the system will produce from drivers, deliveries, and inventories, it must include and maintain a connection to various AI service providers. 
            <br/>
            -To this end it must maintain secure practices, including token management and access validation, ensuring reliable and real-time connectivity to these services securely</td>
        </tr>
        <tr>
            <td>AISMA02</td>
            <td>AI Service Connection—Delivery Route Prediction</td>
            <td>The system must provide, in combination with the data it produces from deliveries, 
            drivers, and GPS 
systems, and the connection with AI services it must have,
a series of AI-driven delivery route optimization algorithms and models</td>
        </tr>
        <tr>
            <td>AISMA02-01</td>
            <td>Delivery Route Prediction—Optimization And Results</td>
            <td>The AI-driven optimization in the system shall produce impactful results that help optimize decision-making in terms of routes, delivery radius, zone management, etc. 
             <br/>   
            - For this reason, the system shall produce Records of information where new routes and parameters are held for the Delivery Manager to handle and make impactful decisions on route optimization</td>
        </tr>
        <tr>
            <td>AISMA03</td>
            <td>AI Service Connection—Inventory Prediction</td>
            <td>The system must be capable of providing, based on the AI-driven services it handles, and data 
produced in warehouses where ingredients are stored, AI-driven solutions for inventory management to improve 
efficiency, 
reduce wastage, and maximize resource utilization.</td>
        </tr>
        <tr>
            <td>AISMA03-01</td>
            <td>Inventory Prediction—Stock Level Prediction</td>
            <td>With the information provided by warehouse managers and warehouse IoT data gathering tooling, the system must be capable of providing Ai-based optimizations to predict shortages and overflows in stock level for various products used in the pizza shop.</td>
        </tr>
        <tr>
            <td>AISMA03-02</td>
            <td>Inventory Prediction—Ingredient Usage Analysis</td>
            <td>The system must be capable of analyzing, through data collected from sales and warehouses, ingredient usage patterns to identify trends in usage and optimize product rotation intervals.</td>
        </tr>
        <tr>
            <td>DELMA01</td>
            <td>Delivery Optimization</td>
            <td>The system shall be capable of analyzing and modifying delivery routes through two coupled systems.</td>
        </tr>
        <tr>
            <td>DELMA01-01</td>
            <td>Delivery Optimization With Allowed Radius</td>
            <td>To improve delivery efficiency, the system should allow managerial accounts to modify a delivery radius 
for drivers</td>
        </tr>
        <tr>
            <td>DELMA01-02</td>
            <td>Delivery Optimization With Data Collection</td>
            <td>To perform such an optimization, the system should be capable of interfacing with a GPS system to collect longitude and latitude data from each driver.</td>
        </tr>
        <tr>
            <td>DELMA02</td>
            <td>Real-Time Delivery Status updates</td>
            <td>The system shall provide real-time tracking and status updates for all active deliveries. For this reason, the system must also be compliant with all of these two sub-requirements</td>
        </tr>
        <tr>
            <td>DELMA02-01</td>
            <td>Delivery Status Updates—Status Notification System</td>
            <td>The system shall notify relevant stakeholders (customers, managers, drivers) of delivery status changes</td>
        </tr>
        <tr>
            <td>DELMA02-02</td>
            <td>Delivery Status Updates—Delivery Milestone Tracking</td>
            <td>The system shall track and record key delivery milestones (ORDER PICKED UP, IN TRANSIT, APPROACHING DESTINATION, DELIVERED)</td>
        </tr>
        <tr>
            <td>DELMA03</td>
            <td>Delivery Zone Analytics</td>
            <td>The system must be capable of analyzing and reporting on the conditions of deliveries done to a certain zone. To this end, the system should analyze average delivery times, average speed, completed deliveries to the zone, etc. All in an effort to optimize delivery routes</td>
        </tr>
        <tr>
            <td>ORDMA01</td>
            <td>Placing An Order Through Website</td>
            <td>The system should allow the user to create, modify and finalize an order through a web browser. Allowing 
the user is to search for Pizzas, add them to their car, and then fulfill their order 
<br/>
- In addition, the system shall 
allow guests to place an order through the same website</td>
        </tr>
        <tr>
            <td>ORDMA02</td>
            <td>Check-out Requires An Address</td>
            <td>The system should validate that to proceed to check-out, the user must provide a delivery address.
            <br/>
    - In the case that the user is a guest, then the delivery address must be at all times present and verified for the process to continue</td>
        </tr>
        <tr>
            <td>ORDMA03</td>
            <td>Check-out Requires Valid Payment Method</td>
            <td>The system should validate a payment method and depending on which is used, request more information to accurately perform a monetary transaction</td>
        </tr>
        <tr>
            <td>ORDMA04</td>
            <td>Shopping Cart Management</td>
            <td>The system shall allow for users to manipulate, reorder, remove, or otherwise change their Pizza orders through an internal construct called Shopping Cart.</td>
        </tr>
        <tr>
            <td>ORDMA04-01</td>
            <td>Shopping Cart Management - Cart Item Management</td>
            <td>The system shall allow users to modify at most one order at a time within their cart. This includes 
modifications on Pizza orders, amounts, ingredients, sizes, etc.</td>
        </tr>
        <tr>
            <td>ORDMA04-02</td>
            <td>Shopping Cart Management—Cart Price Calculation</td>
            <td>The system must be able to calculate and constantly update a running total for the items held within the order wrapped around the Shopping cart, this may or may not include fee details, taxes, etc.</td>
        </tr>
        <tr>
            <td>ORDMA05</td>
            <td>Pizza Configuration</td>
            <td>The system shall allow any users (registered or guests) to customize, configure, add or remove ingredients, change sizing, or any combination of zero, one or more of these operations on the items held within their Order. 
            <br/>
        - To do this, the system must allow for three specific configuration or selection options.</td>
        </tr>
        <tr>
            <td>ORDMA05-01</td>
            <td>Pizza Configuration - Pizza Definition And Ingredient Management</td>
            <td>The system must allow the user to select various aspects of a Pizza to configure it to their liking. These include crust sizes, diameter options, as well as the selection of one or more ingredients for their Pizza.</td>
        </tr>
        <tr>
            <td>ORDMA05-02</td>
            <td>Pizza Configuration - Popular Combinations</td>
            <td>The system must allow the user to see and select one or more Pizzas from a popular combination section, where repeated customization orders or prebuilt configurations are displayed for quick selection. These options might come from Content Managers, repeated orders within the system, or from Pizza Menus.</td>
        </tr>
        <tr>
            <td>ORDMA05-03</td>
            <td>Pizza Configuration - Pizza Menu</td>
            <td>The system must show the users, in addition to the option of creating and configuring their own specialized Pizza, a prebuilt menu of common combinations for the user to quickly select from.</td>
        </tr>
        <tr>
            <td>ORDMA06</td>
            <td>Order Processing</td>
            <td>The system must be capable of validating all information associated with an Account in the process of Ordering from the pizza shop. This includes validating items, ingredient availability, as well as the creation of a connection between the delivery driver and the customer for them to identify the location of their parcel.</td>
        </tr>
        <tr>
            <td>ORDMA07</td>
            <td>Payment Processing</td>
            <td>The system must support various payment methods (subjected to their own rules as defined in requirements ORDMA02 and ORDMA03), for the user to select through which to pay their order. These include cash payment and credit/debit card payments 
            <br/>
            - The system will review the information supplied and validate their accuracy with a corresponding third-party service to confirm payment before delivery can begin.</td>
        </tr>
    </tbody>
</table>

</procedure>

### Development Outcome ― Domain Model
<p>The outcome of this sprint was the domain model diagram, separated into subsystems and their interconnection that 
defines the whole system and our proposed implementation of it. The domain model presented here includes 
notions to all parameters, classes, and their interconnections as defined in all sections prior to this one.
</p>

<deflist>
<def title="Design Artifact: 'Pizza Delivery Service | Domain Model'">

<img alt="DeliveryAritfactFiveCorrected.png" src="DesignArtifactFive.png" thumbnail="true"/>
</def>
</deflist>
<note>All class parameters are explained in a separated listing provided in the Appendix of this webpage, where a 
glossary of terms is also included
</note>



## Use Case Diagrams
<p>As per the project's requirements, the next sprint we did was solely focused on iterating over our domain model, 
actors, and requirements to find use cases and implement them through diagrams and casually formatted use case 
definitions. These are presented here in incremental steps</p>

### Use Cases ― Listing
<p>For this section, the team split work between two sections of the main actors for the program.
The first leg of the design process focused on planning, defining, and iterating over the design 
and definition of most use cases related to both external users of the application, and 
admnistrative level actors. The idea was to produce most of the content that is required to make 
these use cases both correct in terms of the domain model, and the general specification 
and requirements of the application.
</p>
<p>The second leg of the use case definition sprint focused on defining use cases for the 
internal system actors like the GPSSystem, AIServiceProvider, etc. Those actors that while not 
external in their entirety, are modeled within the domain model as outside entities that offer 
their services to the system, but are not held within a central system. In this sense, this 
chapter will focus on providing all documentation related to the use cases defined within these 
two sprints</p>

#### Use Cases ― Listing ― First Leg 
<p>As per the previous discussion, the first leg of this chapter will present all use cases 
defined for the external actors (Customer, Guest Customer, and Delivery Driver), as well as all 
administrative actors (Content Manager, Delivery Manager, Customer Manager, and Warehouse 
Manager). It is at this point that we must point out a key design choice taken within the system 
architecture and the use case definitions presented here.
</p>
<note><p>In all administrative use cases, there will be times when the reader might 
encounter both <i><b><code>ContentManagerSubSystem and Content Manager</code></b></i>, in terms of 
the 
<b>domain model</b>, these two refer to the same component within our architecture. However, the 
distinction between the names is done to emphasize the distinction between 
<b><code>ContentManagerSubSystem (the internal content management system programmatically defined 
and only modified indirectly), with Content Manager (a real human manager in charge of 
supervising the content management operations and modify the system to produce valuable 
business outcomes)</code></b>. This distinction can be found in almost all administrative level 
use cases. 
</p></note>
<p>As can be noted with the definition above, the use of these two terms is entirely meant to be 
a tool for us to define both the internal components and the external entity that in some cases 
initiates a use case (Content Manager), and the other that receives changes from said use case 
(ContentManager). With this out of the way, we begin now with the presentation of all use cases 
defined for this system, each with their own tabs.
</p>

<procedure title="Use Cases Listing ― External and Administrative Actors" 
collapsible="false">
<deflist collapsible="true">
<def title="Customer/Guest Use Cases">
<p>The following are use cases defined for both the Customer (Registered Account user), and the 
Guest (Non-registered Account user).</p>
<deflist type="full" collapsible="true">
<def title="Update Shopping Cart Items">
<list>
<li><b><format color="CornFlowerBlue">Related Requirement Definition</format></b>: <i>ORDMA04, 
ORDMA04-01, ORDMA04-02, ORDMA05, ORDMA05-01, ORDMA05-02, ORDMA05-03</i></li> 
<li><b><format color="CornFlowerBlue">Main Flow</format></b>: <p>
A customer accesses the system's web interface and views available pizza menus (popular 
combinations, preconfigured options, and <i><code>"Create your Own Pizza"</code></i> menu) 
in the <i><code>"My Shopping Cart"</code></i> tab, selects one, and proceeds to 
the <i><code>"Configure Your Order"</code></i> tab to specify details like crust and size.  The 
system confirms the 
order, updates the total in the <i><code>"Shopping Cart Contents"</code></i> tab, and allows the 
customer to 
continue or cancel.
</p></li> 
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>: <p>
During the customer’s shopping cart modification, if the system detects that one or more 
ingredients are unavailable or low on stock, it will alert the customer through an <b>on-screen 
popup</b> and suggest 
alternative ingredients to use based on the available ones in the customer’s pizza. If the client attempts 
to make more than one pizza modification concurrently, the system will inform the customer and 
block additional modifications until the opened modifications are done. 
</p></li> 
</list>

<img alt="UpdateShoppingCartItemsCorrected.png" src="UpdateShoppingCartItemsCorrected.png" thumbnail="true"/>
</def>
<def title="Place Pizza Order">
<list>
<li><b><format color="CornFlowerBlue">Related Requirement Definition</format></b>: <i>ORDMA01,
ORDMA02, ORDMA03, ORDMA04, ORDMA05, ORDMA06, ORDMA07, DELMA02</i></li>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>: <p>
After modifying their shopping cart, the customer proceeds to the <i><code>"Review Your Order"</code></i> tab to 
review, modify, or cancel their order.  Choosing to continue, the system moves the user to a 
<i><code>"Checkout"</code></i> tab, and the customer provides a delivery address, which is internally verified.  
Next, they select a payment method, which is also validated internally. Upon successful payment 
validation, the system processes the payment, sends an order confirmation notification, and 
internally notifies stakeholders to begin order tracking.  The system then tracks the order and 
provides live map updates to the customer.
</p></li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>: <p>
During checkout, the customer's delivery address might be outside a delivery radius for the pizza
delivery system, at which point the system informs the customer of the issue and requests a different
delivery address. During payment processing, if the payment service fails to validate the customer's
payment information, the system will inform the customer of this error and request another payment
method to be used. Once the order is confirmed, the delivery drivers in a customer's area might all be
busy, at which point the system informs the user of this issue and provides a temporary GPS tracking
map page.
</p></li>
</list>

<img alt="PlacePizzaOrder.png" src="PlacePizzaOrder.png" thumbnail="true"/>
</def>
<def title="Track Active Order Status">
<list>
<li><b><format color="CornFlowerBlue">Related Requirement Definitions</format></b>: <i>DELMA02, DELMA02-01, DELMA02-02</i></li>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>: 
<p>
If the customer has an active order in the system, the customer can accesses their active 
order details through the <i><code>"Track My Order"</code></i> tab in the system's web interface. 
The system displays the status of 
their order, displaying an internal flag to the user if the order is still in the kitchen. Once 
the order enters the delivery phase, the system’s web interface will begin to display a live GPS 
feed through a <b>live map</b>, showing the location of the driver, the customer and an ETA for 
the delivery. The system automatically updates the map and displays new milestones as they are 
reached.
</p></li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>: 
<p>
In the off chance the GPS tracking system becomes temporarily unavailable, the system will fall 
back to a milestone status update, without the real-time location tracking ability it normally 
displays. The system then will roll back to a simple interface, showing the ETA and current 
milestone. Based on delivery driver route changes, the system recalculates the ETA information 
and presents it to the user. If the system at any point loses connection from the user, it will 
queue changes such that synchronization is never lost until the user reconnects to a suitable 
network.
</p></li>
</list>
<img alt="TrackActiveOrderStatus.png" src="TrackActiveOrderStatus.png" thumbnail="true"/>
</def>
</deflist>
</def>
<def title="Customer Only Use Cases">
<p>The following are use cases defined solely for the Customer (Registered Account user).</p>
<deflist collapsible="true" type="full">
<def title="Reorder From History">
<list>
<li><b><format color="CornFlowerBlue">Related Requirement Definitions</format></b>: <i>ORDMA01, ORDMA02, ORDMA03, ACCMA02, ACCMA06</i></li>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>: 
<p>
The customer accesses their <i><code>"Order History"</code></i> record through the 
<i><code>"My account information"</code></i> tab, 
where the system displays a list of the previous orders registered to the customer’s account, 
showing price,items, delivery location, and payment method used. From this listing, the user 
can select one previous order, Selecting an order repopulates the shopping cart. The customer 
can accept or modify the prefilled information, including payment method and order items.  
After modification or acceptance, the system validates ingredient availability, payment method, 
and delivery location.  If valid, the system proceeds to the Place Pizza Order use case.
</p></li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>: 
<p>
If any ingredients from the original order are unavailable, the system notifies the customer and 
suggests alternatives or modifications. If the delivery address from the original order is no 
longer within the service area, the system prompts the customer to provide a new valid address. 
If the previously used payment method is expired or invalid, the system requests the customer to 
select or provide a new payment method. In cases where the price of items has changed since the 
original order, the system displays the updated pricing and requires customer acknowledgment 
before proceeding with the order.
</p></li>
</list>

<img alt="ReorderFromHistory.png" src="ReorderFromHistory.png" thumbnail="true"/>
</def>
<def title="Manage Payment Methods">
<list>
<li><b><format color="CornFlowerBlue">Related Requirement Definitions</format></b>: <i>ACCMA02, ACCMA03</i></li>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>: 
<p>
The customer can accesses their account settings in the <i><code>"My account 
information"</code></i> tab within the 
system’s web interface and selects the <i><code>"Stored Payment Methods"</code></i> tab, where 
the system displays stored payment methods. The customer can modify, remove, update, or add 
methods. When removing a payment method, the system requests confirmation from the customer 
before removing it. On any other case, the system requests the new information, internally 
reviews and validates the information, and asks the customer to confirm the changes. 
</p></li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>: 
<p>
If the internal payment method validation fails, the system informs the customer of the specific 
error, including the information that caused the error, and requests correction. When attempting 
to remove a payment method that is set as default, the system requires the customer to select a 
new default method first. If a payment method is currently associated with an active order, the 
system prevents its removal and notifies the customer of the significance of this payment method 
in the system at that moment. In cases where the customer attempts to add a payment method that 
already exists, the system prompts them to update the existing entry instead.
</p></li>
</list>

<img alt="ManagePaymentMethods.png" src="ManagePaymentMethods.png" thumbnail="true"/>
</def>
<def title="Manage User Defined information">
<list>
<li><b><format color="CornFlowerBlue">Related Requirement Definitions</format></b>: <i>ACCMA02, ACCMA03, ACCMA06</i></li>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>: 
<p>
The user accesses their online account setting through the <i><code>"My account 
information"</code></i> tab in the system's web interfaces, then the customer access the 
<i><code>"Manage my Preferences"</code></i> tab. the system displays account information 
(excluding payment methods), such as billing details, delivery addresses, purchase history, and preferences. 
. The customer can add, modify, or remove information. The customer 
then selects an option and follows the indicated steps on the screen. Changes are validated (for 
addresses and billing) or directly stored (for personal information).
</p></li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>: 
<p>
If any validation fails (invalid address, incorrect phone format, etc.), the system highlights 
the specific fields needing correction and provides guidance on proper format. When attempting 
to remove a primary delivery address, the system requires the customer to designate a new 
primary address first. If the customer tries to update information that is currently being used 
for an active order, the system warns that changes will not affect the current order.
</p></li>
</list>

<img alt="ManageUserDefinedInformation.png" src="ManageUserDefinedInformation.png" thumbnail="true"/>
</def>
</deflist>
</def>
<def title="Delivery Driver Use Cases">
<p>The following are use cases defined solely for the Delivery Driver (Account Specialization) 
actor</p>
<deflist collapsible="true">
<def title="Accept Delivery Assignment">
<list>
<li><b><format color="CornFlowerBlue">Related Requirement Definitions</format></b>: <i>DELMA01, DELMA02, DELMA02-01, DELMA02-02</i></li>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>: 
<p>
The delivery driver receives a notification to the <i><code>"Available Deliveries Near 
You"</code></i> tab in the system’s web interface about a 
new 
delivery assignment in their delivery radius. The system displays the 
details including the customer's location, order contents, and delivery payment amount. After 
reviewing, the driver accepts via the system interface, changing their status to "On Delivery," 
showing this milestone to the customer on their interface too. 
The system will use the AI-driven delivery forecast service to 
calculate the optimal route based on current location and destination. Finally, the system 
notifies both the customer and delivery management about the assignment acceptance.
</p></li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>: 
<p>
If the driver is unable to accept the delivery (vehicle issues, personal emergency), they can 
reject the assignment through the system’s web interface silently, allowing the system to look 
for other available drivers. The system then reassigns the delivery to another available driver 
and updates the estimated delivery time. If the driver accidentally accepts a delivery, they 
have a brief window to cancel the acceptance before the order is locked in. In cases where the 
system cannot establish a connection to update the driver's GPS location, it queues the status 
update and continues to retry while allowing the driver to proceed with the delivery.
</p></li>
</list>
<img alt="AcceptDeliveryAssignment.png" src="AcceptDeliveryAssignment.png" thumbnail="true"/>
</def>
<def title="Update Delivery Status">
<list>
<li><b><format color="CornFlowerBlue">Related Requirement Definitions</format></b>: <i>DELMA01, DELMA02, DELMA02-01, DELMA02-02</i></li>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>: 
<p>
The driver accesses the delivery status update interface, <i><code>"Manage My 
Deliveries"</code></i> dashboard in the 
system’s web interface and 
selects their current delivery, the driver updates the delivery status at key milestones (picked 
up, in transit, approaching, delivered). The system timestamps updates, recalculates ETAs, and 
notifies the customer.  The delivery map is also updated to reflect the driver's location and 
status.
</p></li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>: 
<p>
If the system loses GPS connectivity, it stores status updates locally until connection is 
restored. If a driver forgets to update a status, the system can prompt them 
based on GPS location data. In cases where the wrong status is selected, the driver can correct 
it within a limited timeframe, with the system logging both the original and corrected entries.
</p></li>
</list>
<img alt="UpdateDeliveryStatus.png" src="UpdateDeliveryStatus.png" thumbnail="true"/>
</def>
<def title="Complete Delivery Route">
<list>
<li><b><format color="CornFlowerBlue">Related Requirement Definitions</format></b>: <i>DELMA01, DELMA02, DELMA02-01, DELMA02-02</i></li>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>: 
<p>
The driver accesses their delivery status update interface <i><code>"manage My 
Deliveries</code></i> through the system’s web interface and marks completed deliveries as 
finished, confirming successful handovers. The system processes these completions, updates 
delivery records, and adjusts driver availability, storing the driver and delivery metrics 
internally. Once all assigned 
deliveries are complete, the driver manager is updated on the freeing of this driver.
</p></li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>: 
<p>
If a delivery cannot be completed (customer not present, incorrect address, etc.), the driver 
records the issue and contacts the delivery manager through the system for instructions. The 
system may suggest returning to the restaurant or attempting delivery to another customer in the 
area. If multiple deliveries are part of a route, the system helps reorganize remaining 
deliveries when one cannot be completed. In cases where the system cannot process the completion 
immediately, it queues the updates and allows the driver to continue with their next task.
</p></li>
</list>

<img alt="CompleteDeliveryRoute.png" src="CompleteDeliveryRoute.png" thumbnail="true"/>
</def>
</deflist>
</def>
<def title="Content Manager Use Cases">
<p>The following are use cases defined solely for the Content Manager (Administrator 
Specialization) actor</p>
<deflist type="full" collapsible="true">
<def title="Manage Promotional Campaigns">
<list>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>: 
<p>
A content manager accesses the <i><code>"Manage 
Restaurant Content"</code></i> dashboard through the 
system’s web interface, which displays promotional information, pricing, product listings, and 
campaign data. The system additionally displays an AI-driven report for orders in a given period 
of time. The content manager 
then accesses a section within this dashboard to manage, create, or schedule promotional 
campaigns for specific pizza combinations, performing bulk or single modifications. After 
providing necessary information, the system validates inputs for conflicts and pricing accuracy. 
Upon validation, the content manager confirms the campaign setup. Following confirmation, the 
system updates all relevant platform sections.
</p></li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>: 
<p>
If the system detects any irregularities during the validation process, inconsistent pricing, 
conflicts with other campaigns, etc., an alert will be shown to the content manager, and the 
system will suggest 
alternative dates or modifications. 
</p></li>
</list>
<img alt="ManagePromotionalCampaigns.png" src="ManagePromotionalCampaigns.png" thumbnail="true"/>
</def>
<def title="Update Ingredient Information">
<list>
<li><b><format color="CornFlowerBlue">Related Requirement Definitions</format></b>: <i>ORDMA05-01</i></li>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>: 
<p>
The content manager accesses the <i><code>"Manage Pizza Offerings"</code></i> dashboard through the 
system’s web interface, which displays existing pizza combinations, ingredients, and menus. The 
manager can then update ingredient descriptions, allergen warnings, and nutritional data. Once 
the data is registered, the system asks for confirmation.  After confirmation, the system 
automatically updates all relevant user-facing and internal systems.
</p></li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>: 
<p>
If the data was left unchanged then the system informs the user that no changes have been made 
and prompts for either exiting without any changes or continuing editing ingredient information. 
If at any moment the system loses interconnection between the main servers and the content 
manager’s dashboard, the system will back up and log all relevant information that was unsaved 
for picking up later.
</p></li>
</list>

<img alt="UpdaeIngredientInformation.png" src="UpdaeIngredientInformation.png" thumbnail="true"/>
</def>
<def title="Manage Menu Categories">
<list>
<li><b><format color="CornFlowerBlue">Related Requirement Definitions</format></b>: <i>ORDMA05, ORDMA05-03</i></li>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>: 
<p>
The content manager accesses the <i><code>"Manage Menu Structures</code></i> dashboard through the 
system’s web interface, the content manager selects categories for modification, creating new 
sections, reorganizing items, and updating descriptions.  The system logs all changes for review.
Once the system registers all changes, the system makes a call to 
action to the content manager to confirm the changes, after which the system implements all 
changes, while also keeping a log of the confirmation from the content manager.
</p></li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>: 
<p>
If the reorganization breaks existing promotional or pricing relationships, the system alerts 
the content manager and requires resolution.
</p></li>
</list>

<img alt="ManageMenuCategories.png" src="ManageMenuCategories.png" thumbnail="true"/>
</def>
</deflist>
</def>
<def title="Warehouse Manager Use Cases">
<p>The following are use cases defined solely for the Warehouse Manager (Administrator 
Specialization) actor</p>
<deflist type="full" collapsible="true">
<def title="Process Bulk Orders">
<list>
<li><b><format color="CornFlowerBlue">Related Requirement Definitions</format></b>: <i>AISMA03, AISMA03-01</i></li>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>: 
<p>
The warehouse manager accesses the <i><code>"Inventory Management"</code></i> dashboard through the 
system’s web interface, and reviews current inventory levels across all ingredients. 
They analyze the inventory data, and AI-driven reports provided by the 
<b>StorageForecastService</b> subsystem creating bulk purchase orders based on current stock 
levels and usage patterns. The manager coordinates with suppliers by selecting quantities, 
delivery dates, and special requirements. Once orders are created, the system updates inventory 
forecasts and notifies relevant stakeholders.
</p></li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>: 
<p>
If suppliers cannot fulfill the order quantities or delivery dates, the manager must adjust 
orders or find alternative suppliers. When inventory forecasts show discrepancies with actual 
needs, the system alerts the manager to review and modify orders. If budget constraints affect 
ordering, the system requires additional approval levels before proceeding.
</p></li>
</list>

<img alt="ProcessBulkOrders.png" src="ProcessBulkOrders.png" thumbnail="true"/>
</def>
<def title="Configure Storage Alerts">
<list>
<li><b><format color="CornFlowerBlue">Related Requirement Definitions</format></b>: <i>AISMA03-01</i></li>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>: 
<p>
The warehouse manager accesses the <i><code>"Inventory Management</code></i> dashboard through the 
system’s web interface. Once inside, the warehouse manager defines alert thresholds for different 
storage conditions, configuring parameters like temperature ranges, humidity levels, and 
expiration date notifications. The system caches this information within its internal change log 
for warehouse managers, and asks for confirmation from the manager. Once confirmed, the system 
applies and stores all changes in the main system storage.
</p></li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>: 
<p>
If at any point the system loses communication with the warehouse manager’s interface (e.g., 
wireless or wired network damage or loss), the system will back up all information that was last 
stored, periodically storing data as the user registers information to keep in an internal 
storage, there to be restated into the program once connection is back up. If the changes 
introduced for the storage alerts are invalid, or override other configurations, the user will 
be informed of these changes.
</p></li>
</list>

<img alt="ConfigureStorageAlerts.png" src="ConfigureStorageAlerts.png" thumbnail="true"/>
</def>
<def title="Process AI Ingredient Usage Report">
<list>
<li><b><format color="CornFlowerBlue">Related Requirement Definitions</format></b>: <i>AISMA03-02</i></li>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>: 
<p> The warehouse manager accesses the <i><code>"Inventory Management"</code></i> dashboard 
through the system's web interface.
The warehouse manager reviews the AI-generated ingredient usage report from the 
IngredientUsageForecast service, analyzing usage trends, purchasing patterns, and AI 
recommendations.  Based on this, they update storage configurations, modify order quantities, 
and coordinate promotional activities with the Content manager.  After confirmation from the 
warehouse manager, the system logs the changes and implements them.
</p></li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>: 
<p>
If the AI recommendations conflict with current storage capabilities, the manager must develop 
alternative solutions. When usage patterns show unexpected changes, the system requires manual 
verification. If communication with the Content Manager is delayed, the system maintains current 
configurations while flagging items for review.
</p></li>
</list>

<img alt="ProcessAIIngredientUsageReport.png" src="ProcessAIIngredientUsageReport.png" 
thumbnail="true"/>
</def>
<def title="Process AI Inventory Forecast Report">
<list>
<li><b><format color="CornFlowerBlue">Related Requirement Definitions</format></b>: <i>AISMA03, AISMA03-01</i></li>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>: 
<p>The warehouse manager accesses the <i><code>"Inventory Management"</code></i> dashboard 
through the system's web interface. The warehouse manager retrieves the AI-generated inventory 
forecast report from the 
InventoryForecastService.  The warehouse manager analyzes this against real-time and historical 
data, 
adjusting 
storage allocations, order schedules, and inventory thresholds.  The system periodically saves 
this information; after the warehouse manager confirms the changes, the system logs and 
implements them.
</p></li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>: 
<p>
If the forecast indicates potential storage capacity issues, the system will warn the warehouse 
manager about these conflicts. If the system loses connection with the warehouse manager 
interface, it will store all information supplied up to that point to load back up when the 
connection is reestablished.
</p></li>
</list>

<img alt="ProcessAIInventoryForecastReport.png" src="ProcessAIInventoryForecastReport.png" thumbnail="true"/>
</def>
</deflist>
</def>
<def title="Delivery Manager Use Cases">
<p>The following are use cases defined solely for the Delivery Manager (Administrator 
Specialization) actor</p>
<deflist type="full" collapsible="true">
<def title="Configure Delivery Zones">
<list>
<li><b><format color="CornFlowerBlue">Related Requirement Definitions</format></b>: <i>DELMA01, DELMA01-01</i></li>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>: 
<p>
The delivery manager accesses <i><code>"Configure Delivery Zones"</code></i> dashboard through 
the system's web interface and views current delivery zone boundaries. They analyze coverage 
data and traffic patterns for each zone based on an <b>AI-driven report</b> provided by the 
DelliveryForecastService . Based on this 
analysis, they adjust zone boundaries, update delivery fees, and modify service areas.  The 
system validates the changes for gaps and overlaps. After manager confirmation, the system 
updates the zone configurations and logs all changes.
</p></li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>: 
<p>
If proposed changes create coverage gaps, the system alerts the manager and suggests boundary 
adjustments. When fee changes exceed predetermined thresholds, the system requires additional 
approval. If traffic pattern data is unavailable for certain areas, the system uses historical 
delivery data for recommendations. A delivery manager defines and updates delivery zone 
boundaries, setting service areas and delivery fees based on distance and traffic patterns, 
ensuring optimal coverage.
</p></li>
</list>

<img alt="ConfigureDeliveryZones.png" src="ConfigureDeliveryZones.png" thumbnail="true"/>
</def>
<def title="Handle Delivery Exceptions">
<list>
<li><b><format color="CornFlowerBlue">Related Requirement Definitions</format></b>: <i>DELMA02, DELMA02-01</i></li>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>: 
<p> The delivery manager accesses the <i><code>"Delivery Incident Reports"</code></i> dashboard 
through the system's web interface. The delivery manager receives alerts about delivery issues 
through the system. They assess the 
situation and access contingency planning tools. Based on the type of exception, they implement 
appropriate responses such as reassigning drivers, modifying routes, or adjusting delivery times.
The system updates affected orders and notifies relevant stakeholders of changes.
</p></li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>: 
<p>
If multiple exceptions occur simultaneously, the system helps prioritize responses based on 
urgency. When contingency plans affect multiple orders, the system provides impact analysis for 
review. If communication with affected drivers is disrupted, the system suggests alternative 
contact methods and temporary reassignments.
</p></li>
</list>

<img alt="HandleDeliveryExceptions.png" src="HandleDeliveryExceptions.png" thumbnail="true"/>
</def>
</deflist>
</def>
<def title="Customer Manager Use Cases">
<p>The following are use cases defined solely for the Customer Manager (Administrator 
Specialization) actor</p>
<deflist type="full" collapsible="true">
<def title="Process Customer Security Reports">
<list>
<li><b><format color="CornFlowerBlue">Related Requirement Definitions</format></b>: <i>ACCMA09, ACCMA05</i></li>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>: 
<p> The customer manager accesses the <i><code>"Security Reports"</code></i> dashboard through 
the system's web interface. The dashboard shows alerts from the SecurityManagerSubsystem about 
suspicious customer behavior. After reviewing the report (login patterns, transaction history, 
flagged behaviors), they contact the customer for verification or implement security measures, 
as needed. The system logs all actions and updates the account status.
</p></li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>: 
<p>
If customer contact cannot be achieved, then the system will lock down, or disable the 
account depending on the severity of the issue. If at any moment the system loses contact with 
the main servers for data storage and logging, the system will keep a redundant change log with 
the most up-to-date information, even if the customer manager did not save any changes.
</p></li>
</list>

<img alt="processCustomerSecurityReports.png" src="processCustomerSecurityReports.png" thumbnail="true"/>
</def>
<def title="Process Refund Requests">
<list>
<li><b><format color="CornFlowerBlue">Related Requirement Definitions</format></b>: <i>ACCMA06, ORDMA06</i></li>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>: 
<p>The customer manager accesses the <i><code>"Customer Support"</code></i> dashboard through the 
system's web interface.They review order 
details, delivery confirmation, and customer history. The manager validates the refund claim 
against established criteria and determines appropriate compensation. Upon approval, the system 
processes the refund through the original payment method and updates order records. The system 
then notifies the customer of the decision and refund status.
</p></li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>: 
<p>If the customer manager is unable to access the refund request dashboard through the system’s 
web interface, the system will inform the customer manager that there is an internal error and 
proceed to elevate the warning of an error up to an appropriate system administrator. If the 
customer manager is unable to view order details, delivery confirmations, or customer history, 
the system can offer a text (.txt) file version of this information provided through email or in 
the web interface. If the system is unable to process the refund, be it because of the payment 
method or system errors, it will notify the customer manager that appropriate actions are taken. 
If the system is unable to communicate with the customer, either because of account deletion or 
system errors, it will notify the customer manager for further action.
</p></li>
</list>

<img alt="ProcessRefundRequest.png" src="ProcessRefundRequest.png" thumbnail="true"/>
</def>
</deflist>
</def>
</deflist>
</procedure>
<p>Having defined all use cases for the first leg, there is another section I would like to 
cover here that the team identified while working on these. As can be seen above, some use cases 
have components, includes or requires, that are repeated throughout them. These are what we 
extracte as <b><code>subfunction-level use cases</code></b>. This type of subcases pass the 
Elementary Business Process test (barely), as they are components of higher user-level use cases.
The following defines the main flow (using the casual format) for each of these use cases
</p>
<procedure title="Use Case Listing ― Subfunction-level Use Cases">
<deflist type="full" collapsible="true">
<def title="Validate Payment Method">
<list>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>: 
<p>
The customer (registered/unregistered) inputs all details of their preferred payment method. The 
system takes those details and passes them through an API gateway to a validation service that 
validates expiration date, card number, and balance if applicable (debit cards, for example). If 
validation succeeds, the user is alerted to this in the check-out page, and the system logs all 
relevant order information along with information about the successful payment log. 

</p></li>
</list>
</def>
<def title="Validate Delivery Address">
<list>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>: 
<p>
The customer (registered/and most importantly if unregistered) inputs all details related to 
their preferred delivery location for their order. The system internally reviews the information 
provided to determine driver availability, zoning disposition, and other information relevant to 
the system and to the customer. If the information passed into the system is valid, then the 
program informs the user of the validity of this delivery location and proceeds with its process 
to check out and request a GPS tracking lock. 

</p></li>
</list>
</def>
<def title="Check Ingredient Availability">
<list>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>: 
<p>
The customer (registered/unregistered), throughout the modification of their pizza selections, 
or reordering from their history, can modify their pizza’s ingredients. The 
customer modifies the ingredients in their pizza, and the system follows these modifications 
with reviews on the availability of these ingredients. If no availability issues arise, the 
system informs the user of this and proceeds with order creation or checkout. 

</p></li>
</list>
</def>
<def title="Calculate Running Total">
<list>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>: 
<p>
The customer reviews their shopping cart, order, or simply attempts to reorder from their order 
history (if registered). The system, at this point, will attempt to repopulate the running total 
field of their shopping cart or order based on the items present in either. The system will 
update the running total information on the customer’s screen when all calculations have been 
completed. 

</p></li>
</list>
</def>
<def title="Acquire GPS Location Tracking lock">
<list>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>: 
<p>
The customer attempts to track, through the live map on the web interface live map, the location 
of the delivery driver assigned to the respective order. The system procures internally a GPS 
Location Tracking lock, assigning a direct channel of communication between the GPS system 
information relayed back to the system, to the user such that the information is updated 
periodically on the screen. 

</p></li>
</list>
</def>
<def title="Validate Billing Information">
<list>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>: 
<p>
The customer inputs their preferred billing information and associates it with their account. 
The system then proceeds to look at the information and validate it internally. After validation,
the system alerts the user that their information has been stored successfully and displays the 
information on the screen. 

</p></li>
</list>
</def>
<def title="Check For Duplicate Payment Methods">
<list>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>: 
<p>
The customer inputs an already existent payment method in their internal payment method holder. 
The system validates the information stored against the payment methods stored within the system 
and is associated with the account in question. Upon validation that the payment method is not a 
duplicate, it associates it with the customer’s account and reports the success of the operation 
to the method that called it such that it is updated in the payment information for a customer. 

</p></li>
</list>
</def>
<def title="Initialize GPS Tracking">
<list>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>: 
<p>
The customer places an order and pays for it, the system raises an alert to nearby drivers about 
the undelivered order for any driver to accept. A driver accepts the order and proceeds 
to pick up and begin delivery, the system internally communicates to the user that a delivery 
driver is en route to pick up their order. The system then initializes a GPS Tracking connection 
between the main system and the onboard equipment in the driver’s vehicle (or phone), through 
which it begins capturing both GPS information and delivery metrics.
</p></li>
</list>
</def>
<def title="Record Delivery Milestone">
<list>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>: 
<p>
The driver proceeds to deliver the order to the customer. As the driver proceeds with the 
delivery, the driver is prompted with various milestones that can be used to update the customer 
quickly without having to use the phone while en route. The system handles the communication of 
milestones to the customer and internally stores them as a progress record.

</p></li>
</list>
</def>
<def title="Submit Delivery Incident">
<list>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>: 
<p>
The delivery driver finalizes a delivery for a customer. The delivery driver experiences a 
series of issues with the package, order, customer, or any other issue that can arise through 
the delivery process. The delivery driver fills up a small form on the system’s web interface, 
and the system takes care of communicating this to a Delivery Manager for further action.

</p></li>
</list>
</def>
<def title="Log Administrative Action">
<list>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>: 
<p>
The administrator specialization performs sensible action within the system’s boundaries and in 
the boundary of their department. The system proceeds to record all prior states and the changes 
done to the system’s state, including confirmation to prompts by the system. The system saves 
the information in a log file corresponding to the administrative level and specialization of 
the manager that performed the changes.

</p></li>
</list>
</def>
<def title="Validate Administrative Credentials">
<list>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>: 
<p>
The administrator specialization attempts to log in to the system with their credentials through 
a specialized log-in form in the system’s web interface. The system proceeds to validate these 
credentials based on the information provided and the security rules of the internal Security 
Manager. Once validation is completed and successful, the system will alert the administrator’s 
specialization that their session will begin to be monitored for security purposes. Finally, the 
system allows the administrator in, to the respective dashboard of their division.
</p></li>
</list>
</def>

<def title="Process AI Forecast Report">
<list>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>: 
<p>
The administrator specialization, once logged in, attempts to review the information provided by 
the automated AI-driven forecast reports. The system provides all reports generated within a 
current timeframe and presents them as download, and viewable files within the interface of the 
system to the administrator specialization. The administrator specialization then uses this 
information to analyze, interpret, and validate predictions in their respective fields.
</p></li>
</list>
</def>

<def title="Review Customer Login Information">
<list>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>: 
<p>
The system registers that a user is attempting to log in to the system through their credentials.
The system registers these inputs and passes them into the internal security manager API system. 
The security manager validates the information provided against the information stored in the 
system’s storage, once validated the user is alerted of this and allowed into the application.
</p></li>
</list>
</def>

<def title="Log Administrative Content Change">
<p>
The administrator specialization accesses their respective portals. Once logged in, they attempt 
to perform changes on the internal system represented through their portals. The system logs all 
administrative content changes regardless of their access level in a separate internal storage. 
Once all changes have been performed by an administrator specialization, the system stops 
recording the log until further action is taken. 
</p>
</def>

</deflist>
</procedure>

## Annexes

### Annex A ― Domain Model Class Parameter Definitions
<p>The following contains a series of definitions for the usage, and the parameters held within all classes that are 
part of the domain model developed earlier.
</p>
<procedure title="Domain Model Class Parameter Definitions">
<tabs>
<tab title="Account Management Subsystem">
<deflist type="full" collapsible="true">
<def title="Account">
<p>The main hierarchical component that defines the users within our system, it is expanded with specialized 
implementations for different uses and concerns in the application, that is, it can be either an Administrator, a 
DeliveryDriver or a Customer</p>
<list type="bullet">
<li><b><format color="CornFlowerBlue">ID</format></b>:Defines the unique identifier internal to any Account</li> 
<li><b><format color="CornFlowerBlue">lastLogIn</format></b>: Defines the last login information for any account</li> 
<li><b><format color="CornFlowerBlue">accountType</format></b>: parameter that internally defines the type of 
account that the system is working with</li>
<li><b><format color="CornFlowerBlue">accountCreationDate</format></b>: parameter that defines the date of creation 
for an account 
</li> 
<li><b><format color="CornFlowerBlue">accountStatus</format></b>: parameter that defines the status of an account 
(i.e., ACTIVE, SUSPENDED, DELETED, UNDER_REVIEW, etc.)</li>
<li><b><format color="CornFlowerBlue">accountUniqueUsername</format></b>: internal parameter that holds a unique 
string formed from the information of the user, used to identify any account independently of overlaps with name 
or surname parameters</li>
<li><b><format color="CornFlowerBlue">accountRealFirstName/Surname</format></b>: parameters that define the real 
name and last name of an account.</li>
<li><b><format color="CornFlowerBlue">accountContactEmail and accountContactPhone</format></b>: parameters that 
define contact information for the account being created, applicable to all users in our account</li> 
</list>
</def>
<def title="DeliveryDriver">
<p>A specialized implementation of Account that represents delivery personnel within our system. This class contains 
all necessary information to track, manage, and optimize delivery operations for a specific driver.</p>
<note>This class is required in terms of LocationTracking services in the Delivery Tracking Subsystem, this 
because DeliveryMetricRecord, DeliveryZoneRecord, and LocationTracking classes require a DeliveryDriver to feed 
information about these concerns into it, to then further process this information in AI-based systems.</note>
<list type="bullet">
<li><b><format color="CornFlowerBlue">currentDeliveryStatus</format></b>: Enum parameter that defines the current 
status of a driver.</li>
<li><b><format color="CornFlowerBlue">currentActiveDeliveries</format></b>: Collection parameter that holds all 
current active delivery assignments for this driver, allowing multiple order deliveries to be optimized in a single route</li>
<li><b><format color="CornFlowerBlue">currentDeliveryLocation</format></b>: Parameter that holds the current GPS 
coordinates (latitude and longitude) of the driver, updated periodically for real-time tracking</li>
<li><b><format color="CornFlowerBlue">currentDeliveryRating</format></b>: Numerical parameter that represents the 
driver's performance rating based on delivery times, customer feedback, and successful deliveries</li>
<li><b><format color="CornFlowerBlue">currentVehicleInformation</format></b>: Composite parameter containing vehicle 
details including model, plate number, and vehicle type used for deliveries</li>
<li><b><format color="CornFlowerBlue">currentLicenseInformation</format></b>: Composite parameter containing 
driver's license details including license number, expiration date, and type of license</li>
<li><b><format color="CornFlowerBlue">currentMaxDeliveryRadius</format></b>: Numerical parameter defining the 
maximum allowed delivery radius for this driver, configurable by delivery managers for route optimization</li>
</list>
</def>
<def title="Customer">
<p>A specialized implementation of Account that represents the end users of our pizza ordering system. This class 
contains all necessary information to track customer orders, preferences, and payment methods. This class is the 
main access point available for users. This is the class assigned to all those customers that are registered 
in our system, and a simplified version of it is attached to those guests that wish to place orders in our system.</p>
<list type="bullet">
<li><b><format color="CornFlowerBlue">customerOrderHistory</format></b>: Collection parameter that maintains a 
record of all orders placed by this customer, including details of each order and its status</li>
<li><b><format color="CornFlowerBlue">customerRepeatedOrders</format></b>: Collection parameter that tracks 
frequently ordered items or combinations to provide quick reordering options and personalized recommendations</li>
<li><b><format color="CornFlowerBlue">customerOrderRating</format></b>: Collection parameter that stores the 
customer's ratings and feedback for previous orders, used for quality assurance and service improvement</li>
<li><b><format color="CornFlowerBlue">customerDefaultPaymentMethod</format></b>: Parameter that stores the 
customer's preferred payment method for faster checkout. This parameter can be updated through account settings</li>
</list>
</def>
<def title="Administrator">
<p>A specialized implementation of Account that represents system administrators with elevated access rights and 
management capabilities. This class contains all necessary information to track and manage system changes, access 
controls, and administrative operations.</p>
<list type="bullet">
<li><b><format color="CornFlowerBlue">administratorType</format></b>: Enum parameter that defines the level of 
administrator</li>
<li><b><format color="CornFlowerBlue">administratorDepartment</format></b>: Parameter that specifies which 
department this administrator belongs to, used for organizing administrative responsibilities</li>
<li><b><format color="CornFlowerBlue">administratorAccessRights</format></b>: Collection parameter containing the 
specific system permissions and access levels granted to this administrator</li>
<li><b><format color="CornFlowerBlue">administratorChangesLog</format></b>: Collection parameter that maintains a 
detailed record of all system changes and operations performed by this administrator for accountability and auditing 
purposes</li>
</list>
</def>
<def title="ContentManager">
<p>A specialized management class responsible for handling all content-related operations and modifications within 
the system. This class oversees the tracking and categorization of system content changes. Managers of this type are 
capable of modifying the content presented to the user both in the webpage and in pizza menus, offers, etc.
</p>
<list type="bullet">
<li><b><format color="CornFlowerBlue">contentChangesLog</format></b>: Collection parameter that maintains a detailed 
record of all content modifications made in the system</li>
<li><b><format color="CornFlowerBlue">contentModificationRights</format></b>: Parameter that defines the permission 
levels and access rights for content modification</li>
<li><b><format color="CornFlowerBlue">contentChangesCategories</format></b>: Collection parameter that organizes 
content changes into predefined categories for better tracking and management</li>
</list>
</def>
<def title="WarehouseManager">
<p>A specialized management class responsible for overseeing warehouse operations, inventory control, and stock 
management within the system. This class always talks to others in the AI optimization subsystem in order to 
maximize resource utilization and minimize wastage in the restaurant's operations.
</p>
<list type="bullet">
<li><b><format color="CornFlowerBlue">warehouseChangesLog</format></b>: Collection parameter that tracks all 
modifications and operations in the warehouse system</li>
<li><b><format color="CornFlowerBlue">warehousePurchaseOrdersLog</format></b>: Collection parameter that maintains 
records of all purchase orders and their status</li>
<li><b><format color="CornFlowerBlue">warehouseInventoryLevelsLog</format></b>: Parameter that tracks the historical 
and current inventory levels for all items</li>
<li><b><format color="CornFlowerBlue">warehouseStockLevelsThresholds</format></b>: Collection parameter that defines 
minimum and maximum stock levels for automatic reordering, these are updated based on AI optimizations done based on 
delivery and order information.</li>
</list>
</def>
<def title="CustomerManager">
<p>A specialized management class responsible for handling all customer-related operations, support, and analytics 
within the system. To do this, it is in contact both with customers and with verification and security systems,
being capable of administering users and helping them in tickets, as well as in security concerns.
</p>
<list type="bullet">
<li><b><format color="CornFlowerBlue">customerSupportTickersLogs</format></b>: Collection parameter that maintains 
records of all customer support interactions and their resolution</li>
<li><b><format color="CornFlowerBlue">customerPersonalizedMetrics</format></b>: Collection parameter that stores 
customer-specific data for personalization and analysis</li>
<li><b><format color="CornFlowerBlue">customerValidationLogs</format></b>: Collection parameter that tracks all 
customer validation and verification processes</li>
</list>
</def>
<def title="DeliveryManager">
<p>A specialized management class responsible for coordinating delivery operations, route optimization, and driver 
management within the system. It takes data from the classes internal to the AI optimization and delivery 
optimization subsystem and using it with the information provided by the GPS systems attached to drivers, optimizes 
routes and delivery radii to procure optimal delivery times and customer satisfaction.</p>
<list type="bullet">
<li><b><format color="CornFlowerBlue">deliveryActiveDriverPool</format></b>: Collection parameter that maintains the 
current status and information of all active delivery drivers</li>
<li><b><format color="CornFlowerBlue">deliveryActiveZoningRules</format></b>: Collection parameter that defines the 
current delivery zones and their associated rules</li>
<li><b><format color="CornFlowerBlue">deliveryActiveZonePerformanceLogs</format></b>: Collection parameter that 
tracks delivery performance metrics by zone</li>
<li><b><format color="CornFlowerBlue">deliveryActiveZoningRouteInformation</format></b>: Collection parameter that 
stores current delivery routes and their optimization data</li>
</list>
</def>
<def title="CustomerPreferences">
<p>A composite class within Customer that manages all user-defined preferences and customization options for the 
pizza ordering system. This class takes care of containing all information related to preferred payment methods, 
delivery locations, accessibility settings for the webpage, preferred name and surname for billing and delivery 
options, as well as a record of their preferred popular combinations for marketing purposes.</p>
<list type="bullet">
<li><b><format color="CornFlowerBlue">customerPreferredPaymentMethod</format></b>: Parameter that stores the 
customer's default payment method preference for faster checkout</li>
<li><b><format color="CornFlowerBlue">customerPreferredDeliveryLocation</format></b>: Parameter that stores the 
customer's preferred delivery address for quick order placement</li>
<li><b><format color="CornFlowerBlue">customerPreferredAccessibilityColor</format></b>: Parameter that defines the 
customer's preferred UI color scheme for accessibility purposes</li>
<li><b><format color="CornFlowerBlue">customerPreferredNameAndSurname</format></b>: Parameter that stores how the 
customer prefers to be addressed in communications</li>
<li><b><format color="CornFlowerBlue">customerPreferredPopularCombination</format></b>: Collection parameter that 
stores the customer's favorite pizza combinations for quick reordering</li>
</list>
</def>
<def title="DeliveryInformation">
<p>A composite class within Customer that manages all delivery-related location and address information for accurate 
order delivery. This class is used not only in the user settings, but also in order placing, validating (for guest 
users only), as well as in the Delivery Tracking Subsystem to update the user as the delivery comes closer to its 
location.</p>
<list type="bullet">
<li><b><format color="CornFlowerBlue">deliveryMainStreet</format></b>: Parameter that stores the primary street name 
for delivery address</li>
<li><b><format color="CornFlowerBlue">deliverySecondaryStreet</format></b>: Parameter that stores the secondary street 
information</li>
<li><b><format color="CornFlowerBlue">deliveryHouseApart</format></b>: Parameter that specifies whether the delivery 
location is a house or apartment</li>
<li><b><format color="CornFlowerBlue">deliveryBuildingNumber</format></b>: Parameter that stores the building or 
house number</li>
<li><b><format color="CornFlowerBlue">deliveryMapLocation</format></b>: Parameter that stores the GPS coordinates of 
the delivery location</li>
<li><b><format color="CornFlowerBlue">deliveryLocationRef</format></b>: Parameter that stores additional reference 
information to help locate the delivery address</li>
</list>
</def>
</deflist>    
</tab>
<tab title="Purchase Management Subsystem">
<deflist collapsible="true">
<def title="ShoppingCart">
<p>A class that manages the temporary storage and manipulation of items selected for purchase before creating an 
order. This class is composed of Orders, that is, the ShoppingCart class, which is unique to any Customer, is built 
upon orders that cannot exist without one ShoppingCart being present, this ensures that the user cannot define orders 
without having a ShoppingCart (an object given to logged-in or guest users)
</p>
<list type="bullet">
<li><b><format color="CornFlowerBlue">shoppingCartID</format></b>: Unique identifier for each shopping cart 
instance</li>
<li><b><format color="CornFlowerBlue">shoppingCartUserHandlerID</format></b>: Reference to the user who owns this 
shopping cart</li>
<li><b><format color="CornFlowerBlue">shoppingCartRunningTotal</format></b>: Current total price of all items in the 
cart</li>
<li><b><format color="CornFlowerBlue">shoppingCartDefinedDeliveryLocation</format></b>: Delivery location specified 
for this cart</li>
<li><b><format color="CornFlowerBlue">shoppingCartOrderDetails</format></b>: Collection of all items and their 
specifications in the cart</li>
</list>
</def>
<def title="Order">
<p>A class that represents a purchase order, stored within a ShoppingCart that is composed onto a shopping cart. In 
our model then, an Order cannot exist without a shopping cart present.</p>
<list type="bullet">
<li><b><format color="CornFlowerBlue">orderUniqueID</format></b>: Unique identifier for each order</li>
<li><b><format color="CornFlowerBlue">orderShopCartManagerID</format></b>: Reference to the shopping cart that manages 
this order</li>
<li><b><format color="CornFlowerBlue">orderDetails</format></b>: Detailed information about the items contained within 
the order</li>
<li><b><format color="CornFlowerBlue">orderRunningTotal</format></b>: Final total amount for the order</li>
</list>
</def>
<def title="Pizza">
<p>A class that represents a pizza product with its specifications and pricing. This is the core class of this 
subsystem as it aggregates, composes, and associates itself with many internal classes and systems required to make 
the payment and order processing overarching process smooth</p>
<list type="bullet">
<li><b><format color="CornFlowerBlue">pizzaIngredientsList</format></b>: Collection of ingredients used in the 
pizza</li>
<li><b><format color="CornFlowerBlue">pizzaServingsTotal</format></b>: Number of servings for this pizza</li>
<li><b><format color="CornFlowerBlue">pizzaDiameterSize</format></b>: Size of the pizza in diameter</li>
<li><b><format color="CornFlowerBlue">pizzaCrustStyle</format></b>: Style of the pizza crust</li>
<li><b><format color="CornFlowerBlue">pizzaRunningPrice</format></b>: Current price of the pizza</li>
</list>
</def>
<def title="PaymentProcessingSystem">
<p>A class that handles the processing of payments through external payment gateways.</p>
<list type="bullet">
<li><b><format color="CornFlowerBlue">paymentProcessingAPICredentials</format></b>: Secure credentials for payment 
gateway access</li>
<li><b><format color="CornFlowerBlue">paymentProcessingAPIHandler</format></b>: Handler for processing API requests 
and responses</li>
</list>
</def>
<def title="PaymentMethod">
<p>An abstract class that defines the base structure for different payment methods.</p>
<list type="bullet">
<li><b><format color="CornFlowerBlue">paymentMethodType</format></b>: Type of payment method (cash, card, etc.)</li>
<li><b><format color="CornFlowerBlue">paymentRequiredAmount</format></b>: Amount to be paid using this method</li>
</list>
</def>
<def title="CashPayment">
<p>A concrete implementation of PaymentMethod for cash transactions.</p>
<list type="bullet">
<li><b><format color="CornFlowerBlue">cashTotalOnUserSide</format></b>: Amount of cash provided by customer</li>
<li><b><format color="CornFlowerBlue">cashTotalOnSystemSide</format></b>: Amount registered in the system</li>
<li><b><format color="CornFlowerBlue">cashChangeToGive</format></b>: Change amount to be returned to the customer</li>
</list>
</def>
<def title="CardPayment">
<p>A concrete implementation of PaymentMethod for card transactions.</p>
<list type="bullet">
<li><b><format color="CornFlowerBlue">cardHolderInformation</format></b>: Name of the cardholder</li>
<li><b><format color="CornFlowerBlue">cardNumberInformation</format></b>: Encrypted card number</li>
<li><b><format color="CornFlowerBlue">cardSecCodeInformation</format></b>: Security code for the card</li>
<li><b><format color="CornFlowerBlue">cardExpirationInformation</format></b>: Card expiration date</li>
<li><b><format color="CornFlowerBlue">cardBankIssuerInformation</format></b>: Information about the issuing bank</li>
</list>
</def>
<def title="PizzaMenu">
<p>A class that manages the available pizza options and pricing.</p>
<list type="bullet">
<li><b><format color="CornFlowerBlue">menuPizzaListing</format></b>: Collection of available pizzas</li>
<li><b><format color="CornFlowerBlue">menuPizzaPricing</format></b>: Pricing information for regular pizzas</li>
<li><b><format color="CornFlowerBlue">menuPopularCombinationListing</format></b>: List of popular pizza combinations</li>
<li><b><format color="CornFlowerBlue">menuPopularCombinationPricing</format></b>: Pricing for popular combinations</li>
<li><b><format color="CornFlowerBlue">menuPromotionListing</format></b>: Current promotional offers</li>
<li><b><format color="CornFlowerBlue">menuPromotionPricing</format></b>: Pricing for promotional items</li>
</list>
</def>
<def title="Ingredients">
<p>A class that represents individual pizza ingredients and their properties.</p>
<list type="bullet">
<li><b><format color="CornFlowerBlue">ingredientUniqueID</format></b>: Unique identifier for each ingredient</li>
<li><b><format color="CornFlowerBlue">ingredientListingName</format></b>: Display name of the ingredient</li>
<li><b><format color="CornFlowerBlue">ingredientAllergiesInfo</format></b>: Allergy information related to the ingredient</li>
</list>
</def>
<def title="PopularCombination">
<p>A class that represents pre-defined popular pizza combinations.</p>
<list type="bullet">
<li><b><format color="CornFlowerBlue">popularCombinationDescription</format></b>: Detailed description of the combination</li>
<li><b><format color="CornFlowerBlue">popularCombinationPizzaIdentifier</format></b>: Unique identifier for the combination</li>
<li><b><format color="CornFlowerBlue">popularCombinationPizzaPricing</format></b>: Special pricing for the combination</li>
</list>
</def>
</deflist>
</tab>
<tab title="Delivery Tracking Subsystem">
<deflist collapsible="true">
<def title="DeliveryZoneRecord">
<p>A class that maintains statistical data and metrics for specific delivery zones to optimize delivery operations. 
This class is different from DeliveryMetricRecord as it handles the zone in its entirety, that is, this class 
provides information for a delivery zone in a given day, for example, as opposed to 
DeliveryMetricRecord providing 
information about a single delivery from a single driver</p>
<list type="bullet">
<li><b><format color="CornFlowerBlue">zoneCompletedDeliveries</format></b>: Counter tracking the total number of completed deliveries in this zone</li>
<li><b><format color="CornFlowerBlue">zoneAverageDeliveryTime</format></b>: Statistical measure of average delivery duration in this zone</li>
<li><b><format color="CornFlowerBlue">zoneAverageStops</format></b>: Average number of delivery stops made in this zone</li>
<li><b><format color="CornFlowerBlue">zoneAverageDeliverySpeed</format></b>: Average speed of deliveries in this zone</li>
<li><b><format color="CornFlowerBlue">zoneAverageNumClients</format></b>: Average number of clients served in this zone</li>
<li><b><format color="CornFlowerBlue">zoneMaxDeliveryRadius</format></b>: Maximum allowed delivery radius for this zone</li>
</list>
</def>
<def title="DeliveryTracking">
<p>A central class that manages real-time tracking and monitoring of active deliveries. This class is composited 
with a GPSSystem through which it grabs and listens to the location of the delivery driver as well as the customer 
to measure estimated time of arrival, locations, order status, etc. All in an effort to produce information that 
would benefit the AI-driven subsystem underneath.</p>
<list type="bullet">
<li><b><format color="CornFlowerBlue">deliveryCustomerLocation</format></b>: Destination coordinates for the delivery</li>
<li><b><format color="CornFlowerBlue">deliveryCurrentLocation</format></b>: Current real-time location of the delivery</li>
<li><b><format color="CornFlowerBlue">deliveryETA</format></b>: Estimated time of arrival for the delivery</li>
<li><b><format color="CornFlowerBlue">deliveryCurrentState</format></b>: Current status of the delivery (e.g., ORDER PICKED UP, IN TRANSIT, APPROACHING DESTINATION, DELIVERED)</li>
<li><b><format color="CornFlowerBlue">deliveryDriverInformation</format></b>: Reference to the assigned delivery driver's information</li>
</list>
</def>
<def title="DeliveryMetricRecord">
<p>A class that records and maintains actual delivery performance metrics for analysis and optimization. Both this 
class and DeliveryZoneRecord are used in the DeliveryAnalyzer class as part of th AI-driven suite of tools designed 
to improve the efficiency of the system by managing and monitoring delivery information in real time</p>
<list type="bullet">
<li><b><format color="CornFlowerBlue">deliveryRealArrivalTime</format></b>: Actual time when delivery arrived at destination</li>
<li><b><format color="CornFlowerBlue">deliveryRealDeliveryTime</format></b>: Actual total time taken for the delivery</li>
<li><b><format color="CornFlowerBlue">deliveryRealAverageStops</format></b>: Actual number of stops made during delivery</li>
<li><b><format color="CornFlowerBlue">deliveryRealAverageSpeed</format></b>: Actual average speed maintained during delivery</li>
</list>
</def>
<def title="GPSSystem">
<p>A class that manages GPS functionality and location tracking for delivery operations.</p>
<list type="bullet">
<li><b><format color="CornFlowerBlue">GPSLatitude</format></b>: Current latitude coordinate</li>
<li><b><format color="CornFlowerBlue">GPSLongitude</format></b>: Current longitude coordinate</li>
<li><b><format color="CornFlowerBlue">GPSAccessMethods</format></b>: Available methods for accessing GPS data</li>
<li><b><format color="CornFlowerBlue">GPSSynchronizationInterval</format></b>: Time interval for synchronizing GPS data</li>
<li><b><format color="CornFlowerBlue">GPSCaptureInterval</format></b>: Time interval for capturing new GPS coordinates</li>
</list>
</def>
</deflist>
</tab>
<tab title="Security Management Subsystem">
<deflist collapsible="true">
<def title="SecurityManager">
<p>A class responsible for managing and coordinating all security-related operations and authentication services 
within the system. Following the principle of Separation Of Concerns, the CustomerManager class, which initially was 
to perform security verifications too, was relieved of this concern and a new subsystem was proposed to amend this 
concern. Based on this, in later sprints, the team came up with the SecurityManager class, designed to handle 
security through an AuthenticatorService external to the system (APIs)
</p>
<list type="bullet">
<li><b><format color="CornFlowerBlue">securityAuthenticatorService</format></b>: Component that handles authentication requests and validates user credentials</li>
<li><b><format color="CornFlowerBlue">securityAuthenticatorPolicies</format></b>: Collection of security policies and rules that govern authentication processes</li>
</list>
</def>
<def title="AuthenticatorService">
<p>A service class that implements the core authentication logic and security validation processes. This class could 
be though of as a wrapper that holds within connections and tokens that allow the system to communicate with 
Authenticator services (APIs) required to validate user's information both for registration and logins.
</p>
<list type="bullet">
<li><b><format color="CornFlowerBlue">authenticatorSecurityParameters</format></b>: Configuration parameters for 
authentication processes including timeout limits, retry attempts, and security levels, all adjustable from the 
Adminstrator access level in our system.</li>
</list>
</def>
</deflist>
</tab>
<tab title="AI Service Provider Subsystem">
<deflist collapsible="true">
<def title="DataAnalyzer">
<p>A base class that provides core functionality for data analysis and prediction across the system. This is a base 
clase that is implemented in two concrete classes, The DeliveryAnalyzer and OrderAnalyzer, both used in regards to 
AI forecasting services to analyze our data and predict based on it as it is provided to the AI services.</p>
<list type="bullet">
<li><b><format color="CornFlowerBlue">analyzerUniqueID</format></b>: Unique identifier for each analyzer instance in the system</li>
<li><b><format color="CornFlowerBlue">analyzerName</format></b>: Human-readable name identifier for the analyzer instance</li>
</list>
</def>
<def title="DeliveryAnalyzer">
<p>A specialized analyzer class that processes and analyzes delivery-related data for optimization.</p>
<note>This class 
depends on the data produced by DeliveryDrivers both in the DeliveryZoneRecord and the DeliveryMetricRecord class, 
both of which produce delivery information based on drivers. This data is collected and filtered/analyzed before 
being sent to an AI service for a predictive algorithm to use it to output information about route and delivery 
radius modifications.
</note>
<list type="bullet">
<li><b><format color="CornFlowerBlue">analyzerPredictorModel</format></b>: The machine learning model used for delivery predictions</li>
<li><b><format color="CornFlowerBlue">analyzerPredictorIndicators</format></b>: Set of indicators used to make delivery predictions</li>
<li><b><format color="CornFlowerBlue">analyzerPredictorGuidelines</format></b>: Rules and guidelines that govern the prediction process</li>
</list>
</def>
<def title="RouteOptimizationRecord">
<p>A class that stores and manages optimization parameters for delivery routes.</p>
<note>This class returns the information that is supplied to the DeliveryManager class that is in charge of using it 
to adapt and manage delivery routes, radii, and other parameters to optimize deliveries and driving time.
</note>
<list type="bullet">
<li><b><format color="CornFlowerBlue">optimizationMaxOptimalDeliveryRadius</format></b>: Maximum optimal radius for delivery operations</li>
<li><b><format color="CornFlowerBlue">optimizationMaxDeliveryStops</format></b>: Maximum number of stops allowed in a delivery route</li>
<li><b><format color="CornFlowerBlue">optimizationAverageDeliverySpeed</format></b>: Average delivery speed used for route calculations</li>
</list>
</def>
<def title="AIServiceProvider">
<p>A base class for AI service integration and authentication management.</p>
<note>This class is meant to be a connector or gateway to an API service which provides the AI services used in 
the application, like cloud-based models. This system was not designed to keep AI models local, rather it was 
designed through a separation of concerns viewpoint, focusing on optimizing and making the whole design lean.</note>
<list type="bullet">
<li><b><format color="CornFlowerBlue">providerAPIAuthenticationInfo</format></b>: Authentication information for API access</li>
<li><b><format color="CornFlowerBlue">providerAPIAuthenticationToken</format></b>: Security token for API authentication</li>
<li><b><format color="CornFlowerBlue">providerAPIModelAccessInfo</format></b>: Access information for AI model usage</li>
</list>
</def>
<def title="DeliveryForecastService">
<p>A specialized service class for predicting and optimizing delivery routes. This class, as shown in the original 
domain model, produces a RouteOptimizationRecord which is passed onto Manager classes to adjust and optimize.</p>
<list type="bullet">
<li><b><format color="CornFlowerBlue">forecastServiceOptimalDeliveryRoutePredictor</format></b>: Component that predicts optimal delivery routes</li>
</list>
</def>
<def title="InventoryForecastService">
<p>A specialized service class for predicting inventory needs and managing stock levels. The information of this 
forecast service is passed onto a WarehouseManager such that the best decisions about potential inventory loss, or 
purchase patterns are taken based on predictive models</p>
<list type="bullet">
<li><b><format color="CornFlowerBlue">forecastServiceInventoryShortagePredictor</format></b>: Component that predicts potential inventory shortages</li>
<li><b><format color="CornFlowerBlue">forecastServiceInventoryLevelsNeedsPredictor</format></b>: Component that predicts required inventory levels</li>
</list>
</def>
<def title="IngredientUsageForecastService">
<p>A specialized service class for analyzing and predicting ingredient usage patterns. This class also appends 
information to the WarehouseManager class to make the best decisions about ingredient rotations, etc.</p>
<list type="bullet">
<li><b><format color="CornFlowerBlue">forecastServiceIngredientUsageTrendsData</format></b>: Historical data of ingredient usage patterns</li>
<li><b><format color="CornFlowerBlue">forecastServiceIngredientRotationData</format></b>: Data tracking ingredient rotation and freshness</li>
</list>
</def>
<def title="OrderAnalyzer">
<p>A specialized analyzer class for processing and analyzing order-related data. This class depends on information 
produced from Orders and purchase histories from Customers and Daily operations to handle an analysis on ingredient 
usage, pizza purchasing patterns, etc., all in an effort to increase productivity and optimize storage</p>
<list type="bullet">
<li><b><format color="CornFlowerBlue">analyzerPredictorModel</format></b>: The machine learning model used for order analysis</li>
<li><b><format color="CornFlowerBlue">analyzerPredictorIndicators</format></b>: Set of indicators used for order prediction</li>
<li><b><format color="CornFlowerBlue">analyzerPredictorGuidelines</format></b>: Rules and guidelines that govern the order analysis process</li>
</list>
</def>
</deflist>
</tab>
</tabs>
</procedure>

### Annex B ― Glossary of Terms
<p>The following is a small glossary of terms defined in the first and second sprints for this project.</p>
<deflist type="full">
<def title="AI Service Provider">
<p>Term used to describe the aggregate supplier of possible AI-based services to this system. It will be the basis of many optimization services within our application</p>
</def>
<def title="Ingredient">
<p>An item that is used during the making of a pizza as a topping placed on the pizza's top. This is the main definition used through this program</p>
</def>
<def title="Pizza">
<p>The fundamental building block of Orders, Shopping Carts and Customer Preferences. Pizzas are defined as collections of one or more ingredients (also known as Pizza Items) over a singular piece of flat dough.</p>
</def>
<def title="Pizza Item">
<p>A synonym used to refer to those ingredients that are put on top of the pizza dough during the making of a pizza. 
It is a crucial part of Storage Services and Customer Preferences</p>
</def>
</deflist>

### Annex C ― Out of Scope Features
<p>Due to the volumetric complexity of the task at hand, i.e., designing an entire system from 
the ground up, and the need to keep it both language agnostic and implementation agnostic, we 
have decided that some sections of information that, in a real world design would be required, 
outside of the original file.</p>
<p>One of the main considerations that we took here was that our system should focus on the 
original specification and only build upon it to a certain extent. Our idea is not to build an 
entire application from scratch and cover all possible avenues in user authentication for 
example. In our case we consider it and acknowledge that it is important as a use case and 
component of the system, but we are not focusing on it as the core of the program is the 
AI-driven forecasting services and the pizza delivery system. We decided against expanding our 
actors, use cases and requirements too much as this would lead to inconsistent work, and 
lengthy workflows that fall outside the time limit for this project</p>
<p>Rather, we chose to focus on the basics and make the application correct from its building 
blocks, while also allowing ourselves breathing room for future expansion and modification. As 
with everything in software, this architecture we have devised is not set in stone, rather we 
hope it keeps expanding and adapting to new ideas.</p>

