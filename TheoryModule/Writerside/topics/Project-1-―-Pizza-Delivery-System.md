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
            <td>Customer Registration Allows Prefference Storage</td>
            <td>The system should allow a registered user to input prefferences on shipping, billing, and payment methods, such that the information is not re-entered again.</td>
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
            -To this end it must maintain secure practices, including token amangement and access validation, ensuring reliable and real-time connectivity to these services securely</td>
        </tr>
        <tr>
            <td>AISMA02</td>
            <td>AI Service Connection—Delivery Route Prediction</td>
            <td>The system must provide, in combination with the data it produces from deliveries, drivers, and GPS 
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
<def title="Design Artifact: 'Pizza Delivery Service | Domain Model`">

<img alt="DesignArtifactFive.png" src="DesignArtifactFive.png" thumbnail="true"/>
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
provides information for a delivery zone in a given day, for example, as opssoed to DeliveryMetricRecord providing 
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
<p>An item that is used during the making of a pizza as a topping placed on top of a piece of dough. This is the main definition used through this program</p>
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

