# Project #1 ― Part #2― Pizza Delivery System.

> This file contains all information requested within the specification for homework #2 (project 
> #1 part two) for System
> Design NRC (3003).
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

## Robustness Analysis
<p>A fundamental part of the analysis process held within an OOAD analysis mindset is the 
robustness analysis phase. This phase involves correcting, growing, and sometimes rewriting use 
cases to handle more in depth cases, to be specific and clearer, or in some cases, to add details 
that are missing but are crucial to an interaction.
</p>
<p>In general, details like these come up through conversations, through a second pass at the 
requirements and, more often than not, when re-reading use case definitions and comparing them 
to ideas previously held by the team, and represented in the static model (domain model). In our 
case, for this project about a Pizza Delivery System, it was no different, the team spent almost 
two weeks reviewing back to back all use cases, expanding upon their definitions, making sure to 
ground them with views manageable within the system, and connecting them to the domain model we 
had previously defined.
</p>
<p>From this process, a series of changes arose, from new use cases, better and complete 
definitions, to new classes that could be added to the domain model and add onto the model that 
we had devised for this system. Out of this fundamental part of our work, we worked out a series 
of use cases, and now additional architectural classes that aided in the refinement of our work, 
and in representing our model clearly.
</p>
<note>Of course this does not mean that all work done in the previous assignment was thrown 
out and redone (that would have been illogical), it means that we went back, analyzed the 
problem, classes and definitions again, and from these outputted better and more concise use 
cases and diagrams</note>

### Robustness Analysis ― The Get-Go
<p>At the beginning of our design phase, back when we had little experience with concepts like 
use case definition, grouding our applications, and most importantly, had zero concept of how to 
embark on a project like this, use cases came both from our requirements and from our past 
experiences with delivery applications, like Pedidos Ya. However, as we progressed to this next 
section we realized something important, we had been dreaming too much, and our use cases lacked 
seriousness and grounding.
</p>
<p>To remedy this issue, the first part of our analysis came by taking a look again at the 
domain model. While most of the classes defined within it were kept and used regularly 
throughout our robustness and activity diagrams, there were certain parts that were unclear, had 
little connection with each other unless explicitly defined in paper, and generally, there 
appeared to be some paths of communication missing.
</p>
<p>Seeing this large issue compounding over time was a nightmare scenario for us, so we tackled 
it directly before we even got to write revised definitions for our use cases. At least three 
pages of text were devoted to defining the core components of our systems clearly, 
<b><code>from the AI services and their forecast services, to the DeliveryTracking 
class and all of its components</code></b>, each of these documents included information that 
was of the upmost importance for us to write use cases clearly. These are presented here as 
evidence of our work</p>
<procedure title="The Get-Go ― Design Artifact One">
<img alt="canvas_meeting-ideas-250228_0240.png" src="canvas_meeting-ideas-250228_0240.png" thumbnail="true"/>
</procedure>
<p>As can be seen in the document above, a large effort of our time together as a team was spent 
on developing robust <i>descriptions of what certain domain model classes should be and their 
connection with others</i>. In addition, there is also documentation related to the sub-function 
level use cases that were employed within the user-level use cases we refined, as well as those 
that were added, all of which will be presented later on in this document
</p>
<p>Another key improvement here is our constant revision process were we worked to make sure 
that the use cases defined for the API and services actors matched those that were defined 
within the user and managerial account use cases. In this sense, what we worked on was defining 
a core set of business-logic-related use cases for all actors, where each use case, be it 
sub-function level or user level, correlated to some extent to the <b><code>domain 
model</code></b>, connecting classes within the static model to these use cases as needed, and 
as mentioned before, <b><code>adding more classes as needed</code></b>  </p>
<note>We not only meet up in class for these revisions, asynchronous revisions through 
messaging apps and synchronous revisions through zoom and in class were the key to making our 
use cases coordinated with each other and our descriptions robust
</note>
<p>With all of this information defined, and with the use cases we would tackle individually, we 
went ahead and defined a schedule for work. This schedule included meetings, revisions, and even 
deadlines that we attempted to follow as closely as possible even with the overbearing force of 
other university courses upon us. Nevertheless, as with the previous project, we decided to work 
in two phases, one phase focusing on the main actors and administrative actors use cases, in 
parallel with AI services and API use cases, while the second phase focused on refining further 
the secondary use cases we relied upon.
</p>

### Robustness Analysis ― First Phase
<p>This first phase of our work, as mentioned above, focused on the use cases related to all 
external actors, both directly related to the application inner workings (AI services for 
example), as well as those that would initiate contact with our application (customers, guests 
and managerial accounts). To do this, we worked on each of the use cases defined before, adding 
information to the domain model as required</p>
<p>Despite our work on these use cases, however, this section did not focus solely on rewriting 
old use cases into new more concrete implementations and leaving them at that. The main outcome of 
this section was a series of robustness and activity diagrams that were related to these use 
case definitions. As such, the following listing will show all use cases, like before, but with 
the diagrams appended underneath each definition</p>

<procedure title="Use Cases Listing ― External and Administrative Actors ― Robustness, and Activity Diagrams." 
id="use_cases_listing_external_and_administrative_actors">
<deflist collapsible="true">
<def title="Customer/Guest Use Cases">
<p>The following are use cases defined for both the Customer (Registered Account user), and the 
Guest (Non-registered Account user).</p>
<deflist type="full" collapsible="true">
<def title="Update Shopping Cart Items">
<list>

<li><b><format color="CornFlowerBlue">Related Requirement Definition</format></b>: <i>ORDMA04, 
ORDMA04-01, ORDMA04-02, ORDMA05, ORDMA05-01, ORDMA05-02, ORDMA05-03</i></li> 

<li><b><format color="CornFlowerBlue">Main Flow</format></b>:
<p>A customer clicks the <b><code>"View My Shopping Cart"</code></b> button on any number of 
pages, and is redirected to the <b><code>"My Shopping Cart"</code></b> view, within the 
system's web interface. The system then displays all information stored on the current 
customer's shopping cart. The customer presses the <b><code>"Update Shopping Cart Items 
Button"</code></b> and views the <b><code>"Available Pizza Options"</code></b> view (popular 
combinations, preconfigured options, and <b><code>"Create your Own Pizza"</code></b> menu). The 
customer selects one menu. Then the customer configures or selects a pizza, at which point the 
system checks for ingredient availability in storage. Upon successful ingredient validation, the 
user is redirected to the <b><code>"Finish Your Pizza"</code></b> tab to specify details like 
crust and size. Once all details are filled, the customer clicks on the <b><code>"Add To 
Shopping Cart"</code></b> button, at which point the system redirects the customer to the 
<b><code>"My Shopping Cart"</code></b> tab, showing the updated totals and contents.</p>
</li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>:
<p>After clicking the <b><code>"View My Shopping Cart"</code></b> button, the user might not 
have any information within their shopping cart, at which point the system shows the 
<b><code>"Shopping Cart Empty"</code></b> view. 
<br/><br/>
After clicking the <b><code>"Update Shopping 
Cart Items"</code></b> Button, if the system encounters an internal database error, the 
<b><code>"Failed To Communicate To Mainframe"</code></b> Banner will be shown, and the customer 
will be redirected to the <b><code>"My Shopping Cart"</code></b> View. 
<br/><br/>
After the system finished 
the Ingredient Availability Check, if any of the ingredients was not available to satisfy the 
customer's order, the system displays the <b><code>"Ingredient Unavailability"</code></b> banner 
and repopulates the <b><code>"Available Pizza Options View"</code></b>.</p>

</li>

</list>

<img alt="UpdateShoppingCartItems.png" src="UpdateShoppingCartItems.png" thumbnail="true"/>
<img alt="UpdateShoppingCartItemsRBD.png" src="UpdateShoppingCartItemsRBD.png" thumbnail="true"/>
<img alt="UpdateShoppingCartItemsACT.png" src="UpdateShoppingCartItemsACT.png" thumbnail="true"/>

</def>
<def title="Place Pizza Order">
<list>
<li><b><format color="CornFlowerBlue">Related Requirement Definition</format></b>: <i>ORDMA01, 
ORDMA02, ORDMA03, ORDMA04, ORDMA05, ORDMA06, ORDMA07, DELMA02</i></li>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>:
<p>After modifying their shopping cart, within the <b><code>"My Shopping Cart"</code></b> view, 
the customer presses the <b><code>"Review My Order"</code></b> button and is redirected to the 
<b><code>"My Order"</code></b> view to cancel or proceed with their order. Once in this view, 
the system displays updated totals and content. The customer presses the <b><code>"Continue to 
Checkout"</code></b> button, and the system redirects the user to a 
<b><code>"Checkout"</code></b> tab. The customer provides a delivery address, which is 
internally verified. Next, the system redirects them to a <b><code>"Select Payment 
Method"</code></b> view, where they select a payment method, which is also validated internally. 
Finally, after a redirection to the <b><code>"Provide Billing information"</code></b> they can 
opt to supply an optional billing information field. Upon successful billing information 
validation, the system processes the payment, and redirects the customer to the <b><code>"Order 
Confirmed"</code></b> view. The system then attempts to initialize a GPS Delivery Tracking 
connection with any driver that accepts the delivery.</p>
</li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>:
<p>After the user clicks the <b><code>"Review My Order "</code></b> button, if the customer's 
shopping cart is empty, then the system will inform the user through the <b><code>"No Content To 
Order"</code></b> banner and redirect them to the <b><code>"My Shopping Cart"</code></b> view. 
<br/><br/>
During checkout, if the customer's delivery address fails validation, the system 
communicates 
this through a <b><code>"Incorrect Address"</code></b> banner, and redirects to the 
<b><code>"Checkout"</code></b> view. 
<br/><br/>During payment processing, if the payment service fails to validate the customer's 
payment 
information, the system will inform the customer of this error through a <b><code>"Invalid 
Payment Method"</code></b> banner and redirect the customer to the <b><code>"Select Payment 
Method"</code></b> view. During the billing address processing, if the system fails to validate 
the customer's billing information, the system will inform the customer of this error through an 
<b><code>"Invalid Billing information"</code></b> banner, and redirect the customer to the 
<b><code>"Define Billing Information"</code></b> view.</p>
</li>
</list>

<img alt="PlacePizzaOrder.png" src="PlacePizzaOrder.png" thumbnail="true"/>
<img alt="PlacePizzaOrderRBD.png" src="PlacePizzaOrderRBD.png" thumbnail="true"/>
<img alt="PlacePizzaOrderACT.png" src="PlacePizzaOrderACT.png" thumbnail="true"/>
</def>
<def title="Track Active Order Status">
<list>

<li><b><format color="CornFlowerBlue">Related Requirement Definitions</format></b>: <i>DELMA02, 
DELMA02-01, DELMA02-02</i></li>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>:
<p>The customer accesses the <b><code>"Track My Order"</code></b> view from any number of pages. 
If the customer has an active order in the system, the customer can access their active order 
details through this view in the system's web interface. The system populates the view, with a 
live map showing both the order location and customer location, as well as any meaningful 
milestones. The system displays the status of their order, displaying an internal flag to the 
user if the order is still in the kitchen. Once the order enters the delivery phase, the 
system’s web interface will update the live map feed through a live GPS connection, showing the 
location of the driver, the customer and an ETA for the delivery. The system automatically 
updates the live map and displays new milestones as they are reached.</p>
</li> 

<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>:
<p>During the display of the <b><code>"Track My Order"</code></b> view, if the system detects 
that the customer does not have any current Orders associated with their shopping cart, the 
system notifies them through a <b><code>"No Current Order"</code></b> banner and redirects them 
to the <b><code>"My Shopping Cart"</code></b> view.</p>
<br/>
<p>During the <b><code>"Track My Order"</code></b> view displaying sequence, the system might lose 
connection to the DeliveryTracking instance with the GPS connection. The system will roll back 
to milestone-based delivery notifications until connection can be reestablished.</p>
<br/>
</li>

</list>

<img alt="TrackActiveOrderStatus.png" src="TrackActiveOrderStatus.png" thumbnail="true"/>
<img alt="TrackActiveOrderStatusRBD.png" src="TrackActiveOrderStatusRBD.png" thumbnail="true"/>
<img alt="TrackActiveORderACT.png" src="TrackActiveORderACT.png" thumbnail="true"/>
</def>
</deflist>
</def>
<def title="Customer Only Use Cases">
<p>The following are use cases defined solely for the Customer (Registered Account user).</p>
<deflist collapsible="true" type="full">
<def title="Reorder From History">
<list>

<li><b><format color="CornFlowerBlue">Related Requirement Definitions</format></b>: <i>ORDMA01, 
ORDMA02, ORDMA03, ACCMA02, ACCMA06</i></li>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>:
<p>The customer accesses the <b><code>"My Account Information"</code></b> view from any number 
of pages by clicking a link. The system validates that the customer has a proper Session Token 
assigned. Within this view, the customer accesses the <b><code>"My Order History"</code></b> 
view, by clicking on the <b><code>"View My Order History"</code></b> button, where the system 
displays a list of the previous orders registered to the customer’s account, showing price, 
items, delivery location, and payment method used. From this listing, the user can select one 
previous order, selecting an order repopulates the shopping cart. The system follows with the 
Update Shopping Cart Items use case.</p>
</li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>:
<p>During the Session Token validation, if the system detects that there is no session token 
assigned to the customer, it proceeds with the Customer Log In use case, i.e., having the user 
log in.</p>
<br/>
<p>If the customer’s information is empty, then the system displays the <b><code>"No Previous 
Orders"</code></b> banner and redirects the customer to the <b><code>"My Account 
Information"</code></b> view.</p>
</li>
</list>

<img alt="ReorderFromHistory.png" src="ReorderFromHistory.png" thumbnail="true"/>
<img alt="ReorderFromHistoryRBD.png" src="ReorderFromHistoryRBD.png" thumbnail="true"/>
<img alt="ReorderFromHistoryACT.png" src="ReorderFromHistoryACT.png" thumbnail="true"/>
</def>
<def title="Manage Payment Methods">
<list>

<li><b><format color="CornFlowerBlue">Related Requirement Definitions</format></b>: <i>ACCMA02, 
ACCMA03</i></li> 

<li><b><format color="CornFlowerBlue">Main Flow</format></b>: 

<p>The customer accesses the <b><code>"My Account Information"</code></b> view from any number 
of pages by clicking a link. The system validates that the customer has a proper Session Token 
assigned. Within this view, the customer presses the <b><code>"View My Payment 
Methods"</code></b> button that redirects to the <b><code>"Stored Payment Methods"</code></b> 
view. The system then polls the customer's records to populate the view with the stored payment 
information. From the list, the customer selects one payment method. The system prompts the user 
with a <b><code>"Modify"</code></b>, <b><code>"Remove"</code></b> or <b><code>"Add"</code></b> 
buttons, to modify a payment method, remove a payment method, or add a payment method 
respectively, The system, based on the input from the user handles invocation of internal 
methods specifically designed to handle these operations. After any operation is done, its 
result messages are handled internally and populated on the user's view.</p>
</li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>:
<p>If during the Session Token validation performed before accessing the <b><code>"My Account 
Information"</code></b> view, the system detects no token is assigned to the user (i.e., not 
logged in), it prompts the user to log in and initiates the Customer Log In use case.</p>
<br/>
<p>During the payment method retrieval operation, if the system detects that no stored payment 
methods exists for the customer, the system displays a <b><code>"No Stored Payment Methods 
Found"</code></b> banner and redirects the user to the <b><code>"Templated Stored Payment 
Methods"</code></b> view.</p>
</li>
</list>

<img alt="ManagePaymentMethods.png" src="ManagePaymentMethods.png" thumbnail="true"/>
<img alt="ManagePaymentMethodsRBD.png" src="ManagePaymentMethodsRBD.png" thumbnail="true"/>
<img alt="ManagePaymentMethodsACT.png" src="ManagePaymentMethodsACT.png" thumbnail="true"/>
</def>
<def title="Manage User Defined information">
<list>
<li><b><format color="CornFlowerBlue">Related Requirement Definitions</format></b>: <i>ACCMA02, 
ACCMA03, ACCMA06</i></li>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>:
<p>The customer attempts to access the <b><code>"My account information"</code></b> view within 
the system’s web interface by clicking a link in a number of pages. The system validates the 
existence of a session token for the customer. Once in the view, the customer clicks on the 
<b><code>"View My Preferences"</code></b> button, the system then redirects the customer to the 
<b><code>"My Preferences"</code></b> view. The system having requested information about the 
customer's preferences, displays account information (excluding payment methods), such as 
billing details, delivery addresses, purchase history, and preferences. The customer is 
presented with the <b><code>"Update Preferences"</code></b> button. The customer presses the 
button and is redirected to the <b><code>"Modifying My Preferences"</code></b> view containing 
all fields available for modification. The customer presses the <b><code>"Save 
Changes"</code></b> button when done. Once changes are received, the system proceeds to validate 
them in segments. The system begins validation of the Delivery Address changes (if any). Then 
the system validates the Billing information (if any). After validation the system returns to 
the <b><code>"My Account Information"</code></b> view.</p>
</li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>:
<p>As the customer attempts to access the <b><code>My Account Information</code></b>, if the 
system fails to identify an existent session toke for the customer (i.e., customer is not logged 
in), the system will redirect the customer to the <b><code>"Log In"</code></b> view, starting 
the Customer Log In use case.</p>
<br/>
<p>During validation, if the delivery address placed within the <b><code>"Modifying My 
Preferences"</code></b> view is invalid, the system will inform the customer of this fact 
through the <b><code>"Incorrect Address"</code></b> Banner, restoring previous customer 
preferences, and returning to <b><code>"My Account Information"</code></b> abruptly</p>
<br/>
<p>During validation, if the billing information placed within the <b><code>"Modifying My 
Preferences"</code></b> view is invalid, the system will inform the customer of this fact 
through the <b><code>"Invalid Billing Information"</code></b> Banner, restoring previous 
customer preferences and returning to <b><code>"My Account Information"</code></b> abruptly.</p> 
</li>
</list>
<img alt="ManageUserDefinedInformation.png" src="ManageUserDefinedInformation.png" thumbnail="true"/>
<img alt="ManageUserDefinedInformationRBD.png" src="ManageUserDefinedInformationRBD.png" thumbnail="true"/>
<img alt="ManageUserDefinedInformationACT.png" src="ManageUserDefinedInformationACT.png" thumbnail="true"/>
</def>
</deflist>
</def>
<def title="Delivery Driver Use Cases">
<p>The following are use cases defined solely for the Delivery Driver (Account Specialization) 
actor</p>
<deflist collapsible="true">
<def title="Accept Delivery Assignment">
<list>
<li><b><format color="CornFlowerBlue">Related Requirement Definitions</format></b>: <i>DELMA01, 
DELMA02, DELMA02-01, DELMA02-02</i></li>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>:
<p>The delivery driver, already logged in, accesses the <b><code>"Available Deliveries Near 
You"</code></b> view in the system’s web interface. The system, upon receiving an update about a 
new delivery assignment in the delivery driver's DeliveryRadius, populates a <b><code>"Available 
Delivery For You"</code></b> banner, and loads it into the screen, with the information about 
the order. The system displays the details including the customer’s location, order contents, 
and delivery payment amount. After reviewing, the driver accepts by clicking the 
<b><code>"Accept Delivery Challenge"</code></b> button in the system interface. The system 
internally handles accepting the interconnection of the Driver's GPS System with the Customer's 
Live Map (i.e., completing Place Pizza Order Use Case). The system changes the delivery driver's 
status to <b><code>"On Delivery"</code></b>, showing this milestone to the customer too. The 
system talks to the DeliveryForecastService and requests an ETA and optimized delivery route. 
Finally, the customer and delivery driver's live maps are updated to show the results of the 
AI-driven computation.</p>
</li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>:
<p>During the Listening for Newly Placed Orders phase, it is important to note that the use case 
defines itself as looping. The delivery Driver requires a Delivery Challenge to continue with 
the use case.</p>
<br/>
<p>During the Delivery Tracking Handshake synchronization, the system will attempt to 
synchronize the internal DeliveryTracking instance, and the Driver's on board systems at most 
three times. After these three attempts, the system will drop the connection, and revert to a 
Milestone-based tracking system.</p>
<br/>
<p>During the AI-driven delivery optimization request, the system will attempt to retrieve this 
information at most three times. After these three attempts, the system will drop the AI Service 
connection, and revert to a historical ETA. Then the system will report this issue automatically 
to the Delivery Manager for further escalation.</p>
</li>
</list>
<img alt="AcceptDeliveryAssignment.png" src="AcceptDeliveryAssignment.png" thumbnail="true"/>
<img alt="AcceptDeliveryAssignmentRBD.png" src="AcceptDeliveryAssignmentRBD.png" thumbnail="true"/>
<img alt="AcceptDeliveryAssignmentACT.png" src="AcceptDeliveryAssignmentACT.png" thumbnail="true"/>
</def>
<def title="Update Delivery Status">
<list>
<li><b><format color="CornFlowerBlue">Related Requirement Definitions</format></b>: <i>DELMA01, 
DELMA02, DELMA02-01, DELMA02-02</i></li>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>:
<p>The delivery driver, already logged in, clicks on the <b><code>"Manage My 
Deliveries"</code></b> button and is redirected to the <b><code>"Update Delivery 
Status"</code></b> view in the system’s web interface. The system polls the internal database to 
load all delivery information related to the delivery driver. The delivery driver selects their 
current delivery. The system prompts them to choose from a list of possible status updates 
(picked up, in transit, approaching, delivered).
Once selected, the driver saves their changes by clicking on the <b><code>"Save Status 
Update"</code></b> button. The system timestamps updates, recalculates ETAs, and notifies the 
customer. The system, finally, updates all live map instances with the current status for the 
delivery and driver location.
</p>
</li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>:
<p>During the accessing of the <b><code>"Update Delivery Status"</code></b> view, the system 
will attempt to poll information from the database about the driver's current deliveries. If no 
record is found, then the system informs the driver with the <b><code>"No Current 
Deliveries"</code></b> banner, and then redirects the driver to the templated (i.e., prefilled 
with dummy information) <b><code>"Update Delivery Status"</code></b> view.</p>
<br/>
<p>During the registering of the drivers’ status change, given that the system falls back to 
milestone-based tracking earlier on the Accept Deliver Assignment use case, this fallback is not 
mentioned here.</p>
</li>
</list>

<img alt="UpdateDeliveryStatus.png" src="UpdateDeliveryStatus.png" thumbnail="true"/>
<img alt="UpdateDeliveryStatusRBD.png" src="UpdateDeliveryStatusRBD.png" thumbnail="true"/>
<img alt="UpdateDeliveryStatusACT.png" src="UpdateDeliveryStatusACT.png" thumbnail="true"/>
</def>
<def title="Complete Delivery Route">
<list>
<li><b><format color="CornFlowerBlue">Related Requirement Definitions</format></b>: <i>DELMA01, 
DELMA02, DELMA02-01, DELMA02-02</i></li>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>:
<p>The delivery driver, already logged in, clicks on the <b><code>"Manage My 
Deliveries"</code></b> button and is redirected to the <b><code>"Update Delivery 
Status"</code></b> view in the system’s web interface. The system polls the internal database to 
load all delivery information related to the delivery driver. The delivery driver selects their 
current delivery. The delivery driver updates the status to <b><code>"Delivered"</code></b> 
confirming successful handover. The driver saves their changes by clicking on the <b><code>"Save 
Changes"</code></b> button. The system registers these changes, updating both the driver and 
customer's live map. The system finalizes the bridge connection (DeliveryTracking) between the 
customer and delivery driver. The system collects all relevant data. The data is first appended 
into the DeliveryZoneRecord for the driver's delivery zone, the system, then, creates a 
DeliveryMetricRecord instance and passes it to the AI-driven software for further analysis. The 
system, finally, returns the driver to the <b><code>"Update Delivery Status"</code></b> view.</p>
</li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>:
<p>During the accessing of the <b><code>"Update Delivery Status"</code></b> view, the system 
will attempt to poll information from the database about the driver's current deliveries. If no 
record is found, then the system informs the driver with the <b><code>"No Current 
Deliveries"</code></b> banner, and then redirects the driver to the templated (i.e., prefilled 
with dummy information) <b><code>"Update Delivery Status"</code></b> view.</p>
<br/>
<p>During the last synchronization and data collection steps, if the system's internal flag of 
'Milestone-based communication' is triggered, the system will avoid data collection steps as the 
system could not collect GPS data accurately. Rather the system finalizes the DeliveryTracking 
milestone-based communication bridge and redirects the driver to the <b><code>"Update Delivery 
Status"</code></b> view.</p> 
<br/>
</li>
</list>
<img alt="CompleteDeliveryRoute.png" src="CompleteDeliveryRoute.png" thumbnail="true"/>
<img alt="CompleteDeliveryRouteRBD.png" src="CompleteDeliveryRouteRBD.png" thumbnail="true"/>
<img alt="CompelteDeliveryRouteACT.png" src="CompelteDeliveryRouteACT.png" thumbnail="true"/>
</def>
</deflist>
</def>
<def title="Content Manager Use Cases">
<p>The following are use cases defined solely for the Content Manager (Administrator 
Specialization) actor</p>
<deflist type="full" collapsible="true">
<def title="Manage Promotional Campaign">
<list>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>:
<p>The content manager logs in with their credentials through the <b><code>"Log In"</code></b> 
view. The system validates their credentials. Once validated, the content manager is redirected 
to the <b><code>"Manage Restaurant Content"</code></b> dashboard through the system’s web 
interface. The system displays promotional information, pricing, product listings, and campaign 
data for various product campaigns. The content manager selects at most one promotional campaign 
to manage. Once selected, the manager clicks on the <b><code>"Manage Campaign"</code></b> button.
The system loads all previously listed information solely for this product campaign. The content 
manager clicks the <b><code>"Review AI-Driven Reports"</code></b> button. The system displays an 
AI-driven report for orders of the product campaign. The system shows the content manager the 
<b><code>"Modify Campaign"</code></b> and <b><code>"Delete Campaign"</code></b> buttons. The 
content manager clicks on either of these buttons. The system then proceeds to follow their 
respective use cases. After following the internal procedures for either process, the system 
reports all errors encountered to the dashboard through banners. Following this process, the 
system updates the information records for the selected product campaign.</p>
</li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>:
<p>During the log-in process, if the content manager introduces their information incorrectly 
more than three times, their account will be blocked, and a SecurityManager report will be 
stored within the ContentManagementSubsystem.</p>
<br/>
<p>During the polling of information from the DatabaseManagementSystem, if the system encounters 
that there is no information stored about promotional campaigns, the system will notify of this 
through a <b><code>"No Managed Campaigns"</code></b> banner, displaying a templated version of 
the <b><code>"Manage Restaurant Content"</code></b>.</p>
<br/>
<p>During the AI-driven report the system invokes the Process AI Forecast Report, if the system 
fails to receive an AI report after three attempts, the system will inform the manager with an 
<b><code>"Unable to Connect To Mainframe"</code></b> banner and log the information internally.</p> 
<br/>
</li>
</list>

<img alt="ManagePromotionalCampaigns.png" src="ManagePromotionalCampaigns.png" thumbnail="true"/>
<img alt="ManagePromotionalCampaign.png" src="ManagePromotionalCampaign.png" thumbnail="true"/>
<img alt="ManagePromotionalCampaignACT.png" src="ManagePromotionalCampaignACT.png" thumbnail="true"/>
</def>
<def title="Update Ingredient Information">
<list>
<li><b><format color="CornFlowerBlue">Related Requirement Definitions</format></b>: 
<i>ORDMA05-01</i></li>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>:
<p>The content manager logs in with their credentials through the <b><code>"Log In"</code></b> 
view. The system validates their credentials. Once validated, the content manager is redirected 
to the <b><code>"Manage Restaurant Content"</code></b> dashboard through the system’s web 
interface. The manager clicks on the <b><code>"Modify Existing Menu Offerings"</code></b> button,
and is redirected to a mockup view of the <b><code>"Menu Options"</code></b> view available to 
all users. Upon entry, the system displays existing pizza combinations, ingredients, and menus. 
The manager selects one of these categories, and the system loads the <b><code>"Expanded 
Offerings"</code></b> view, showcasing all details (ingredient, nutritional, price, etc.) 
information for all items within the collection. The manager selects at most one Pizza 
(PizzaCombination or Pizza). Once selected, the system presents all data points for that Pizza, 
in an editable <b><code>"Change Values"</code></b> view. Once the data is registered, the 
manager presses the <b><code>"Save Changes"</code></b> button to confirm and store their changes.
After storing, the system automatically updates all relevant user-facing and internal systems, 
creating an internal log in the ContentManagementSubsystem of all changes done.</p>
</li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>:
<p>During credential validation, if the system encounters any errors through the validation, 
the system will alert the manager through an <b><code>"Invalid Credentials"</code></b> banner. 
If the system receives the same error three times, the account will be locked and the underlying 
ContentManagementSubsystem will be notified through a log of the invalid log-in attempts.</p>
<br/>
<p>During all data retrieval points (i.e., Menu Options, and Expanded offerings data loading 
points), if the system encounters an internal database error, it will let the manager know 
through an <b><code>"Unable To Connect to Mainframe"</code></b> banner, redirecting them to the 
<b><code>"Manage Restaurant Content"</code></b> view.</p>
<br/>
<p>During data inputting in the <b><code>"Change Values"</code></b> view, if the data remains 
unchanged, the system alerts the user of this fact through a <b><code>"No Changes 
Registered"</code></b> Banner, saving previous state and redirecting the user to the 
<b><code>"Manage Restaurant Content"</code></b> view.</p>
<br/>
</li>
</list>

<img alt="UpdateIngredientInformation.png" src="UpdateIngredientInformation.png" thumbnail="true"/>
<img alt="UpdateIngredientInformationRBD.png" src="UpdateIngredientInformationRBD.png" thumbnail="true"/>
<img alt="UpdateIngredientInformationACT.png" src="UpdateIngredientInformationACT.png" thumbnail="true"/>
</def>
</deflist>
</def>
<def title="Warehouse Manager Use Cases">
<p>The following are use cases defined solely for the Warehouse Manager (Administrator 
Specialization) actor</p>
<deflist type="full" collapsible="true">
<def title="Configure Storage Alerts">
<list>

<li><b><format color="CornFlowerBlue">Related Requirement Definitions</format></b>: 
<i>AISMA03-01</i></li>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>: 

<p>The warehouse manager attempts to log in through the <b><code>"Log In"</code></b> view from a 
number of pages. The manager inputs their credentials and clicks the <b><code>"Log 
In"</code></b> button. The system validates those credentials internally. Upon validation, 
system redirects the manager to the <b><code>"Inventory Management"</code></b> dashboard through 
the system's web interface. The manager clicks on the <b><code>"Configure Storage Early Warning 
Alerts"</code></b> button, and the system displays the <b><code>"Early Warning Alerts 
List"</code></b> view. Once inside, the manager selects at most one product from the listing. 
The system then displays a <b><code>"Modify Early Warning Alert"</code></b> view. The warehouse 
manager defines alert thresholds for different storage conditions, configuring parameters like 
temperature ranges, humidity levels, and expiration date notifications. The system logs all 
changes internally. The manager presses the <b><code>"Save Changes"</code></b> button. Once 
pressed, the system applies all changes to the internal subsystem, and stores the log of all 
changes within it too.</p>
</li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>:
<p>During credential validation, if the system encounters any errors through the validation, 
the system will alert the manager through an <b><code>"Invalid Credentials"</code></b> banner. 
If the system receives the same error three times, the account will be locked and the underlying 
WarehouseManagementSubsystem will be notified through a log of the invalid log-in attempts.</p>
<br/>
<p>During the information polling from the main database, if the database fails to respond to a 
query, the system will retry at most three times, at which point it will warn the manager with 
the <b><code>"Unable to Connect to Mainframe"</code></b> Banner, before redirecting the manager 
to the <b><code>"Inventory Management"</code></b> dashboard. If the database fails to provide 
information, the system will poll at most three times before repeating the same warning process.
</p> 
<br/>
</li>
</list>

<img alt="ConfigureStorageAlerts.png" src="ConfigureStorageAlerts.png" thumbnail="true"/>
<img alt="ConfigureStorageAlertsRBD.png" src="ConfigureStorageAlertsRBD.png" thumbnail="true"/>
<img alt="ConfigureStorageAlertsACT.png" src="ConfigureStorageAlertsACT.png" thumbnail="true"/>
</def>
<def title="Process AI Ingredient Usage Report">
<list>

<li><b><format color="CornFlowerBlue">Related Requirement Definitions</format></b>: 
<i>AISMA03-02</i></li>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>:
<p>The warehouse manager attempts to log in through the <b><code>"Log In"</code></b> view from a 
number of pages. The manager inputs their credentials and clicks the <b><code>"Log 
In"</code></b> button. The system validates those credentials internally. Upon validation, 
system redirects the manager to the <b><code>"Inventory Management"</code></b> dashboard through 
the system's web interface. The warehouse manager clicks on the <b><code>"Review Ingredient 
Usage AI-Driven Reports"</code></b> button. The system loads all relevant AI-Driven reports 
produced over a period of time. The manager selects at most one report, and the system loads all 
information of said report into the <b><code>"Report In Detail"</code></b> view. The manager 
reviews the AI-generated ingredient usage report from the IngredientUsageForecast service, 
analyzing usage trends, purchasing patterns, and AI recommendations. After reviewing, the 
manager clicks the <b><code>"Download And Close"</code></b> or <b><code>"Close"</code></b> 
button. After executing the specified task, the system redirects the manager to the 
<b><code>"Inventory Management"</code></b> dashboard.</p>
</li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>:
<p>During credential validation, if the system encounters any errors through the validation, 
the system will alert the manager through an <b><code>"Invalid Credentials"</code></b> banner. 
If the system receives the same error three times, the account will be locked and the underlying 
WarehouseManagementSubsystem will be notified through a log of the invalid log-in attempts.</p>
<br/>
<p>During the AI-Driven report processing, if the system, after three attempts, fail to return 
any information to analyze, will proceed to notify the manager through an <b><code>"Unable to 
Connect To Mainframe"</code></b> banner, and report the issue to the underlying 
WarehouseManagementSubsystem of the error.</p> 
<br/>
</li>
</list>

<img alt="ProcessAIIngredientReport.png" src="ProcessAIIngredientReport.png" thumbnail="true"/>
<img alt="ProcessAIINgredientReportRBD.png" src="ProcessAIINgredientReportRBD.png" thumbnail="true"/>
<img alt="ProcessAIIngredientReportACT.png" src="ProcessAIIngredientReportACT.png" thumbnail="true"/>
</def>
<def title="Process AI Inventory Forecast Report">
<list>

<li><b><format color="CornFlowerBlue">Related Requirement Definitions</format></b>: <i>AISMA03, AISMA03-01</i></li> 

<li><b><format color="CornFlowerBlue">Main Flow</format></b>: 

<p>The warehouse manager attempts to log in through the <b><code>"Log In"</code></b> view from a 
number of pages. The manager inputs their credentials and clicks the <b><code>"Log 
In"</code></b> button. The system validates those credentials internally. Upon validation, 
system redirects the manager to the <b><code>"Inventory Management"</code></b> dashboard through 
the system's web interface. The warehouse manager clicks on the <b><code>"Review Inventory 
Forecast AI-Driven Reports"</code></b> button. The system loads all relevant AI-Driven reports 
produced over a period of time. The manager selects at most one report, and the system loads all 
information of said report into the <b><code>"Report In Detail"</code></b> view. The manager 
reviews the AI-generated report, done by the underlying InventoryForecastService, against 
real-time and historical data, adjusting storage allocations, order schedules, and inventory 
thresholds. After reviewing, the manager clicks the <b><code>"Download And Close"</code></b> or 
<b><code>"Close"</code></b> button. After executing the specified task, the system redirects the 
manager to the <b><code>"Inventory Management"</code></b> dashboard.</p>
</li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>:
<p>During credential validation, if the system encounters any errors through the validation, 
the system will alert the manager through an <b><code>"Invalid Credentials"</code></b> banner. 
If the system receives the same error three times, the account will be locked and the underlying 
WarehouseManagementSubsystem will be notified through a log of the invalid log-in attempts.</p>
<br/>
<p>During the AI-Driven report processing, if the system, after three attempts, fail to return 
any information to analyze, will proceed to notify the manager through an <b><code>"Unable to 
Connect To Mainframe"</code></b> banner, and report the issue to the underlying 
WarehouseManagementSubsystem of the error.</p> 
<br/>
</li>
</list>

<img alt="ProcessAIInventoryForecastReport.png" src="ProcessAIInventoryForecastReport.png" thumbnail="true"/>
<img alt="ProcessAIInventoryForecastReportRBD.png" src="ProcessAIInventoryForecastReportRBD.png" thumbnail="true"/>
<img alt="ProcessAIInventoryForecastReportACT.png" src="ProcessAIInventoryForecastReportACT.png" thumbnail="true"/>
</def>
</deflist>
</def>
<def title="Delivery Manager Use Cases">
<p>The following are use cases defined solely for the Delivery Manager (Administrator 
Specialization) actor</p>
<deflist type="full" collapsible="true">
<def title="Configure Delivery Zones">
<list>

<li><b><format color="CornFlowerBlue">Related Requirement Definitions</format></b>: <i>DELMA01, 
DELMA01-01</i></li>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>:
<p>The Delivery Manager attempts to log in through the <b><code>"Log In"</code></b> view from a 
number of pages. The manager inputs their credentials and clicks the <b><code>"Log 
In"</code></b> button. The system validates those credentials internally. Upon validation, 
system redirects the manager to the <b><code>"Delivery Management"</code></b> dashboard through 
the system's web interface. The manager clicks on the <b><code>"Configure Delivery 
Zones"</code></b> button, and the system redirects the manager to the <b><code>"Configure 
Delivery Zones"</code></b> view through the system's web interface. The system communicates 
internally with the database and polls all currently defined zoning rules for the program. The 
manager clicks on the <b><code>"Review AI-Driven Reports"</code></b> button. The system 
redirects the manager to the <b><code>"AI-Driven Reports"</code></b> view, where the system 
polls all stored RouteOptimizationRecord reports returned until that query by the 
DeliveryForecastService. Additionally, the system polls an up-to-date report from the underlying 
AI subsystem. The manager selects at most one report at-the-time. The system loads the 
respective report in a <b><code>"Viewing Report"</code></b> view. Using this report, the manager analyzes coverage 
data and traffic patterns for each zone based on this report. The system displays two options, 
<b><code>"Download and Close"</code></b> or <b><code>"Close"</code></b>. The manager clicks on 
either of these buttons and the system handles the required process. After review, the system 
redirects the manager to the <b><code>"Configure Delivery Zones"</code></b> view. The manager 
selects at most one zone to configure. The system loads all data associated with that zone into 
a <b><code>"Configure Zone Rules"</code></b> view. The manager modifies any and all fields 
within this view, the system validates each change internally against internal business logic. 
The manager clicks the <b><code>"Save Changes"</code></b> button, the system updates the zone 
configurations and stores a log of all changes into the underlying DeliveryManagementSubsystem.</p></li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>:
<p>During credential validation, if the system encounters any errors through the validation, 
the system will alert the manager through an <b><code>"Invalid Credentials"</code></b> banner. 
If the system receives the same error three times, the account will be locked, and the underlying 
DeliveryManagementSystem will be notified through a log of the invalid log-in attempts.</p>
<br/>
<p>During all database polling steps (<b><code>"Configure Delivery Zones"</code></b> view 
loading and <b><code>"Review AI-driven Reports"</code></b> loading), if the system is unable to 
establish a connection to the underlying mainframe, after three attempts, it will display an 
<b><code>"Unable To Connect to Mainframe"</code></b> banner, and redirect the manager to the 
<b><code>"Delivery Management"</code></b> dashboard.</p>
<br/>
<p>During the Configuration of a defined Delivery Zone, if the system encounters any incorrect 
state being introduced, the system will alert the manager through a <b><code>"Invalid 
Configuration Parameter"</code></b> banner, and request correction before proceeding.</p> 
<br/>
</li>
</list>

<img alt="ConfigureDeliveryZones.png" src="ConfigureDeliveryZones.png" thumbnail="true"/>
<img alt="ConfigureDeliveryZonesRBD.png" src="ConfigureDeliveryZonesRBD.png" thumbnail="true"/>
<img alt="ConfigureDeliveryZonesACT.png" src="ConfigureDeliveryZonesACT.png" thumbnail="true"/>
</def>
<def title="Handle Delivery Exceptions">
<list>
<li><b><format color="CornFlowerBlue">Related Requirement Definitions</format></b>: <i>DELMA02, DELMA02-01</i></li>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>:
<p>The Delivery Manager attempts to log in through the <b><code>"Log In"</code></b> view from a 
number of pages. The manager inputs their credentials and clicks the <b><code>"Log 
In"</code></b> button. The system validates those credentials internally. Upon validation, 
system redirects the manager to the <b><code>"Delivery Management"</code></b> dashboard through 
the system's web interface. The manager clicks on the <b><code>"Review Delivery 
Incidents"</code></b> button and is redirected to the <b><code>"Delivery Incident 
Reports"</code></b> dashboard through the system's web interface. The system loads all 
information about current delivery issues raised through DeliveryTracking driver-customer 
connections stored in the database. The delivery manager clicks on any of the open issues and an 
<b><code>"Issue Information"</code></b> view is populated. The system loads all information 
related to the current issue, including a live view of the driver-customer delivery map, and 
Order Details. The delivery manager assesses the situation and clicks on the <b><code>"Apply 
Corrective Measures"</code></b> button. The system redirects the manager to the 
<b><code>"Corrective Measures"</code></b> view, where previous conflict resolution information 
is populated from the database. Based on the type of exception, they implement appropriate 
responses, after applying a corrective measure the manager clicks on the <b><code>"Save 
Changes"</code></b> button. The system updates affected orders and notifies relevant 
stakeholders of changes. The system also stores internally, a log of all actions taken within 
the underlying 
DeliveryManagementSubsystem.</p>
</li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>:
<p>During credential validation, if the system encounters any errors through the validation, 
the system will alert the manager through an <b><code>"Invalid Credentials"</code></b> banner. 
If the system receives the same error three times, the account will be locked and the underlying 
DeliveryManagementSubsystem will be notified through a log of the invalid log-in attempts. </p> 
<br/>
<p>During all database polling steps (<b><code>"Delivery Incident Reports"</code></b> dashboard 
loading and <b><code>"Corrective Measures"</code></b> view loading), if the system is unable to 
establish a connection to the underlying mainframe, after three attempts, it will display an 
<b><code>"Unable To Connect to Mainframe"</code></b> banner, and redirect the manager to the 
<b><code>"Delivery Management"</code></b> dashboard.</p>
<br/>
<p>During the <b><code>"Issue information"</code></b> view population, if the system cannot 
access the DeliveryTracking instance connecting both driver and customer, or if the 
communication is milestone-based, the system will revert to a milestone-based list of all 
milestones achieved until the moment of review.</p> 
<br/>
</li>
</list>

<img alt="HandleDeliveryExceptions.png" src="HandleDeliveryExceptions.png" thumbnail="true"/>
<img alt="HandleDeliveryExceptionsRBD.png" src="HandleDeliveryExceptionsRBD.png" thumbnail="true"/>
<img alt="HandleDeliveryExceptionsACT.png" src="HandleDeliveryExceptionsACT.png" thumbnail="true"/>
</def>
</deflist>
</def>
<def title="Customer Manager Use Cases">
<p>The following are use cases defined solely for the Customer Manager (Administrator 
Specialization) actor</p>
<deflist type="full" collapsible="true">
<def title="Process Customer Security Reports">
<list>
<li><b><format color="CornFlowerBlue">Related Requirement Definitions</format></b>: <i>ACCMA09, 
ACCMA05</i></li>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>:
<p>The Customer Manager attempts to log in through the <b><code>"Log In"</code></b> view from a 
number of pages. The manager inputs their credentials and clicks the <b><code>"Log 
In"</code></b> button. The system validates those credentials internally. Upon validation, 
system redirects the manager to the <b><code>"Customer Experience Management"</code></b> 
dashboard through the system's web interface. The customer manager clicks on the <b><code>"View 
Security Reports"</code></b> button and accesses the <b><code>"Security Reports"</code></b> 
dashboard through the system's web interface. The system polls the internal database for all 
recent security alerts for customers, about suspicious customer behavior, loading them into the 
dashboard. The manager selects at most one of the displayed alerts. The system redirects the 
manager to the <b><code>"Review Alert"</code></b> view. The manager reviews the report (login 
patterns, transaction history, flagged behaviors). The manager then clicks on the 
<b><code>"Apply Corrective Measures"</code></b> button. The system loads all corrective measures 
applicable. The manager selects one option and clicks on the <b><code>"Save Changes"</code></b> 
button. The system internally implements these security measures. The system logs all actions
and updates the account status.</p>
</li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>:
<p>During credential validation, if the system encounters any errors through the validation, 
the system will alert the manager through an <b><code>"Invalid Credentials"</code></b> banner. 
If the system receives the same error three times, the account will be locked and the underlying 
CustomerManagementSubsystem will be notified through a log of the invalid log-in attempts. </p>
<br/>
<p>During the information polling from the main database, if the database fails to respond to a 
query, the system will retry at most three times, at which point it will warn the manager with 
the <b><code>"Unable to Connect to Mainframe"</code></b> Banner, before redirecting the manager 
to the <b><code>"Customer Experience Management"</code></b> dashboard.</p>
<br/>
</li>
</list>
<img alt="ProcessCustomerSecurityReports.png" src="ProcessCustomerSecurityReports.png" thumbnail="true"/>
<img alt="ProcessCustomerSecurityReportsRBD.png" src="ProcessCustomerSecurityReportsRBD.png" thumbnail="true"/>
<img alt="ProcessCustomerSecurityReportsACT.png" src="ProcessCustomerSecurityReportsACT.png" thumbnail="true"/>
</def>
<def title="Process Refund Requests">
<list>
<li><b><format color="CornFlowerBlue">Related Requirement Definitions</format></b>: <i>ACCMA06, 
ORDMA06</i></li>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>:
<p>The Customer Manager attempts to log in through the <b><code>"Log In"</code></b> view from a 
number of pages. The manager inputs their credentials and clicks the <b><code>"Log 
In"</code></b> button. The system validates those credentials internally. Upon validation, 
system redirects the manager to the <b><code>"Customer Experience Management"</code></b> 
dashboard through the system's web interface. The customer manager clicks the <b><code>"Review 
Customer Support Tickets"</code></b> button, and accesses the <b><code>"Customer 
Support"</code></b> dashboard through the system's web interface. The system loads all stored 
Tickets raised by customers. The manager selects at most one ticket, and the system redirects the 
manager to the <b><code>"Review Ticket Details"</code></b> view. They review order details, 
delivery confirmation, and customer history. The manager reviews the refund request status, and 
upon business-logic-dependent validation, the manager clicks the <b><code>"Process 
Refund"</code></b> button. The system communicates the request to the PaymentProcessingSystem to 
initiate a refund, handled in its entirety by the API system. The manager receives confirmation 
through the <b><code>"Refund Successful"</code></b> banner. The manager clicks the 
<b><code>"Close Ticket"</code></b> button. The system then notifies the customer of the decision 
and refund status, closing the ticket and logging all information in the underlying 
CustomerManagementSubsystem.</p>
</li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>:
<p>During credential validation, if the system encounters any errors through the validation, 
the system will alert the manager through an <b><code>"Invalid Credentials"</code></b> banner. 
If the system receives the same error three times, the account will be locked and the underlying 
CustomerManagementSubsystem will be notified through a log of the invalid log-in attempts. </p>
<br/>
<p>During the information polling from the main database, if the database fails to respond to a 
query, the system will retry at most three times, at which point it will warn the manager with 
the <b><code>"Unable to Connect to Mainframe"</code></b> Banner, before redirecting the manager 
to the <b><code>"Customer Experience Management"</code></b> dashboard. If the database fails to 
provide information, the system will poll at most three times before repeating the same warning 
process.</p>
<br/>
<p>During the refund processing, if the underlying system fails to return an appropriate 
response, the system will inform the manager of this issue through a <b><code>"Unable To Connect 
to Mainframe"</code></b> banner, redirecting them to the <b><code>"Customer Experience 
Management"</code></b> dashboard.</p>
</li>
</list>
<img alt="ProcessRefundRequests.png" src="ProcessRefundRequests.png" thumbnail="true"/>
<img alt="ProcesRefuntRequestsRBD.png" src="ProcesRefuntRequestsRBD.png" thumbnail="true"/>
<img alt="ProcessRefundRequestsACt.png" src="ProcessRefundRequestsACt.png" thumbnail="true"/>
</def>
</deflist>
</def>
</deflist>
</procedure>

<p>Some of the most noticeable things from the previous use case definitions, as well as the 
diagrams that come along with them is the level of detail that has been added upon them to 
signify the complexities of the inner system they attempt to abstract. Now, in contrast to those 
use cases we had defined before, there is a focus on grounding the use case through clear context 
lines to the use cases that we have worked on before, to the objects of the static model, and 
to the sub-function level use cases that bind these cases and their work together.
</p>
<p>To this end, several sections of the information presented in the first drafts of all use 
cases were revised and modified to make more sense in the context of the whole application, not 
only in our minds or on paper. Most use cases now communicate with each other, and use common 
logic like common fallback methods, sub-function level use cases, or terminology that make it 
simple to visualize them as part of the same system, as well as groupings of the static domain 
objects, and not just words on a piece of paper</p>
<p>Special care was put into the administrator level use cases, as in the first drafts we 
defined, these were too vague and generic, and although they presented a good view of the 
overall system, these did not in any way improve the understanding of our application due to how 
<b><code>simplified and vane they were</code></b>, to improve them, attention was paid to adding 
appropiate links to other use cases, actors within our system, and components within the static 
model, all in an effort to not only ground but improve the quality of our design by making the 
use cases live in the context of our application, not just in the context of a piece of paper 
with dreams, rather than reality.
</p>
<note>A clear difference then, is the level of realism that was added into all use cases, 
common pitfalls for all use cases are presented in the alternative paths, not just a listing 
of what could happen. Several error messages and conditions were fleshed out, allowing for a 
more robust and extendable design to be created.
</note>
<warning>Of course, this is not to say that dreaming about the functions we would want to 
see in the app is wrong, these help us flesh out the domain model and the requirements a 
whole lot more than the simple specification. However, dreaming is not going to get you 
anywhere if you don’t ground yourself at some point, as we did here!</warning>

#### First Phase ― On The Diagrams
<p>Two new types of diagrams were added into this section, robustness diagrams and activity 
diagrams. While both of these are different views of the original use case definition text, it 
is important to mention that these two are some of the greatest, if not the best tools for OOAD 
that we have encountered so far. The idea of having a directed graph where we can see the steps 
our use case has to follow, and alternative flows as well as objects that are used, not only 
sounds incredible, but it actually is too. Having this model, easy to follow and easy to extend, 
allowed us to work and focus on what the use case had to do, rather than on the wording, 
sentencing, etc.
</p>
<p>Through the first type of diagram, robustness diagrams, the project became much simpler, as 
with our previous discussions on the use of various static domain classes, we had a good idea of 
what to implement and how to define it on paper. Moreover, since we had already moved on from 
the functionality-dreaming phase, and we had grounded our use cases, it was simple for us to go 
back and forth between them and alter, improve, or append parts that seemed fit.
</p>
<note>Having the ability of adding objects into the diagram was key here, as without this our 
use cases could only mention what we needed, but we never saw their interaction with the system 
as a whole.
</note>
<p>Now, with these diagrams defined, and the parts of our systems that interacted with our use 
cases defined clearly, we could move on to <b><code>activity diagrams</code></b>. This type of 
diagrams proved a bit more challenging. Not only do we have to handle multiple paths of 
execution, in the same graph and thinking of it as a start-end diagram, but we also had to 
factor in that we needed objects and communication lines, and UI loops, etc. 
</p>
<p>Handling this information became, in some use cases, a nightmare due to the added complexity 
of having to map different alternative paths into the diagrams, without breaking the start-end 
rule that defines them. Moreover, since we had to define all steps logically, it was easy to 
lose track of the position in the use case, the objects we required, or even the type of diagram 
element that had to be used at a time.
</p>
<p>Nevertheless, the diagramming processed showed that <b><code>while activity 
diagrams are good to visualize objects and path variations</code></b>, 
<b><code>robustness diagrams are good as an overall picture of the interaction</code></b>. 
Activity diagrams can be seen as a time series of steps that have to be followed, showing 
branching steps and decision points, as well as parallel lines of execution. But robustness 
diagrams can be seen as a snapshot of everything that has to be used and done within a use case 
definition. This second view is simpler to understand, to some extent, than activity diagrams.</p>

#### First Phase ― Subfunction Level Use Cases
<p>As was, probably, visible in the previous sections, most of the subfuction level use cases 
that were defined in the previous activity were kept in the diagram. However, some of the 
<b><code>new subfunction level use cases that were found</code></b>, could be easily modelled as 
aggregations of those that already existed. As such, in this section we will focus on defining 
these subfunction level use cases in detail, improving the descriptions as done for the previous 
section, while also adding a robustness diagram to each of these to show their inner working. 
</p>
<p>Sadly, due to time limitations, activity diagrams for these will not be included.</p>

<procedure title="Use Case Listing ― Subfunction-level Use Cases ― Robustness Diagrams">
<deflist type="full" collapsible="true">
<def title="Validate Delivery Address">
<list>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>:
<p>The system receives all delivery address information associated with the customer's chosen 
delivery address. The system, using the <b><code>AddressValidatorSystem</code></b>, validates 
the information to determine if the supplied delivery address exists. Upon validation, the 
system outputs a validation signal to its caller.</p></li>
<li><b><format color="CornFlowerBlue">Branch Sequence</format></b>:
<p>During delivery address validation, if the underlying 
<b><code>AddressValidatorSystem</code></b>, fails to validate the delivery address provided as 
existing, the system will output an invalidation signal, along with error information, allowing 
for 
higher level 
management of 
this error.</p>
</li>
</list>

<img alt="ValidateDeliveryAddress.png" src="ValidateDeliveryAddress.png" thumbnail="true"/>
</def>
<def title="Validate Billing Information">
<list>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>:
<p>The system receives a request from an Order object to validate the defined billing 
information. The system, redirects the request to the 
<b><code>BillingValidationSystem</code></b> in the form of an API call to its external subsystem.
Upon successful validation, the system returns a confirmation signal to the caller of this use 
case.</p></li>
<li><b><format color="CornFlowerBlue">Branch Sequence</format></b>:
<p>During the validation process, if the <b><code>BillingValidationSystem</code></b> fails to 
identify the information as a correct billing address, the system will return an invalidation 
signal, as well as all error information, to the original caller for further processing.</p>
</li>
</list>

<img alt="ValidateBillingInformation.png" src="ValidateBillingInformation.png" thumbnail="true"/>
</def>
<def title="Validate Payment Method">
<list>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>:
<p>The system receives a request by an Order to validate a Payment method defined for it. The 
system relays this call to the underlying <b><code>PaymentProcessingSystem</code></b>. The 
underlying <b><code>PaymentProcessingSystem</code></b> resolves this call by making an API call 
to an external validation service (Stripe or Visa). Upon successful validation, the system 
returns a validation signal to the caller.</p></li>
<li><b><format color="CornFlowerBlue">Branch Sequence</format></b>:
<p>During the validation process, if the <b><code>PaymentProcessingSystem</code></b> fails to 
identify the payment method provided as valid through its external API, then the system returns 
an invalidation flag, along with all error information, to the caller for further processing.</p>
</li>
</list>
<img alt="ValidatePaymentMethod.png" src="ValidatePaymentMethod.png" thumbnail="true"/>
</def>
<def title="Initialize GPS Tracking">
<list>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>: 

<p>Once an order has been processed, the system internally initializes a bridge connection 
between the customer's live map interface, and any nearby driver that accepts the open delivery 
option. The system will proceed to wait for any driver to accept the assignment to finalize the 
connection.</p>
<p>The connection to this bridge is finalized only through an execution of the <b><code>Accept 
Delivery Assignment</code></b> use case by a Delivery Driver, where the handshake operation is 
performed, and the system links the customer's interface with the onboard telemetry on the 
driver's phone or vehicle.</p>
</li>
<li><b><format color="CornFlowerBlue">Branch Sequence</format></b>:

<p>During the handshake operation, if the bridge cannot be connected to either the customer's 
GPS or the Delivery Driver’s GPS telemetry, the system will log the event internally and revert 
to a milestone-based communication system.</p>

</li>
</list>
<note>To see the diagram of this, it is impossible to represent it alone. Rather refer to the 
Place Pizza Order (start of bridge connection), and Accept Delivery Assignment (end of bridge 
connection establishment), and Complete Delivery Assignment (end of the bridge connection)
</note>
</def>
<def title="Calculate Running Total">
<list>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>:

<p>The system receives an internal flag about a customer's shopping cart content change (this 
could be either reordering from history, updating their items, or placing an order). The system 
processes the flag and starts to calculate the running price based on internal information 
stored within the <b><code>DatabaseManagementSystem</code></b>. Upon finishing the calculation, 
the system returns the updated totals to the caller.</p></li>
<li><b><format color="CornFlowerBlue">Branch Sequence</format></b>:
<p>During price information polling, if the system cannot establish a connection to the database 
after three attempts, the system will return an invalidation flag, along with information about 
the error, to the caller for further processing.</p>
</li>
</list>
<img alt="CalculateRunningTotals.png" src="CalculateRunningTotals.png"/>
</def>
<def title="Check Ingredient Availability">
<list>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>:
<p>The system receives a signal from the ShoppingCart of a customer about an appended Pizza 
(Pizza or PizzaCombination). The system, following the registry of this signal, attempts to 
validate all ingredient information availability with the 
<b><code>DatabaseManagementSystem</code></b>. To validate the availability of an ingredient, the 
system must determine that the amount requested per item is less or equal to the amount 
available in storage. Upon successful validation, the system returns a validation signal to the 
caller.</p> </li>
<li><b><format color="CornFlowerBlue">Branch Sequence</format></b>:
<p>During the ingredient information request, if the system encounters that database 
connectivity cannot be established after three attempts, an invalidation signal, and error 
information, will be returned to the caller for further processing.</p>
<p>During the ingredient validation process, if the system detects that at least one ingredient 
has an illegal amount (i.e., requested amount is higher than stored amount), it will return an 
invalidation signal, along with error information, to the caller for further processing.</p>
</li>
</list>
<img alt="CheckIngredientAvailability.png" src="CheckIngredientAvailability.png"/>
</def>
<def title="Customer Already Logged In">
<list>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>:
<p>The system receives a call to validate access to the "Log In" view (by a customer or 
managerial account). The system reviews the login records stored in the 
<b><code>DatabaseManagementSystem</code></b>, and looks up the SessionToken reported by the web 
browser of the user. Upon a successful match the system sends a validation flag to the caller, 
indicating that the user is already logged in.</p></li>
<li><b><format color="CornFlowerBlue">Branch Sequence</format></b>:
<p>During the database connection, if, after three connection attempts, the system fails to 
acquire a connection to the <b><code>DatabaseManagementSystem</code></b>, the system will ignore 
the validation request, and send an invalidation signal, along with error information, to the 
caller to ask the user to log in again.</p>
<p>During the SessionToken validation, if the system cannot find the token internally (i.e., it 
was automatically deleted after the session token expired), the system will return an 
invalidation flag, along with an error message indicating this to the caller, to ask the user to 
log in again.</p>
</li>
</list>

<img alt="CustomerAlreadyLoggedIn.png" src="CustomerAlreadyLoggedIn.png" thumbnail="true"/>
</def>
<def title="Account Log In">
<list>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>:

<p>The system received a signal that a non-logged-in account attempted to access a logged-in 
only section. The system redirected the account to the "Log In" view. The account inputted their 
credentials (including account email and password). The account pressed the "Log In" button. The 
system calls the internal <b><code>DatabaseManagementSystem</code></b> and queries the provided 
credentials against the stored credentials. Upon finding a match, the system authorizes the "Log 
In" and redirects the account to the page they attempted to access before.</p>
</li>
<li><b><format color="CornFlowerBlue">Branch Sequence</format></b>:
<p>During the ingredient information request, if the system encounters that database 
connectivity cannot be established after three attempts, an invalidation signal, and error 
information, will be returned to the caller for further processing.</p>
<p>During the validation, if the system fails to find a complete match (email and password) for 
the inputted credentials, the system will display the "Invalid Credentials" banner prompting the 
user to reenter both fields.</p>
</li>
</list>

<img alt="AccountLogIN.png" src="AccountLogIN.png" thumbnail="true"/>
</def>
<def title="Add Payment Method">
<list>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>:
<p>The system receives the information about the payment method that is to be added. The system 
redirects the customer to the "Enter Payment Method Details" View, where all details are entered
(code, numbers, expiration date, etc.). Once done, the customer presses the "Store Information" 
button. Internally, 
the system calls upon the <b><code>PaymentProcessingSubsystem</code></b> to validate the 
provided information. Upon validation, the system calls the "Check For Duplicate Payment 
Method" use case. Upon validation, the system informs the user of the correct addition of the 
provided payment method through the "Payment Method Added Successfully" banner. The system then 
stores the information about the new payment method in a log and communicates it to the 
<b><code>CustomerManagementSubsystem</code></b>.</p></li>
<li><b><format color="CornFlowerBlue">Branch Sequence</format></b>:
<p>During the payment information validation, if the 
<b><code>PaymentProcessingSubsystem</code></b> fails to validate all input parameters, 
the user will be informed through an "Invalid Payment Method" banner, redirecting them back to 
the "Stored Payment Methods" view.</p>

</li>
</list>

<img alt="AddPaymentMethod.png" src="AddPaymentMethod.png"/>
</def>
<def title="Check For Duplicate Payment Methods">
<list>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>:

<p>The system receives, after a customer has inputted all payment fields in the "Enter Payment 
Method Details" View, and the information is valid, an internal request to validate that this 
new payment method is not duplicate. The system polls all internal payment methods registered to 
the account from the <b><code>DatabaseManagementSystem</code></b>. The system validates the 
information provided by the customer against the payment methods stored within the system and is 
associated with the account in question. Upon validation that the payment method is not a 
duplicate, it associates it with the customer’s account and reports the success of the operation 
to the method that called it such that it is updated in the payment information for a customer.</p>
</li>
<li><b><format color="CornFlowerBlue">Branch Sequence</format></b>:
<p>During the payment methods request, if the system encounters that database connectivity 
cannot be established after three attempts, an invalidation signal, and error information, will 
be returned to the caller for further processing.</p>
<p>During payment method validation, if the system detects that a payment method already stored 
matches the data inputted, it eagerly returns an invalidation signal, along with error 
information, to the caller.</p>
</li>
</list>

<img alt="CheckForDuplicatePaymentMethods.png" src="CheckForDuplicatePaymentMethods.png" thumbnail="true"/>
</def>
<def title="Remove Payment Method">
<list>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>:
<p>The system receives the payment information that is about to be deleted. The system requests 
confirmation from the customer, confirmation that is acquired when the user presses the "Confirm 
Removal" button. Upon confirmation, the system logs the change and informs the 
<b><code>CustomerManagementSubsystem</code></b> of the change done to the customer's record. The 
system proceeds to delete the payment method from the internal 
<b><code>DatabaseManagementSystem</code></b>. The system informs the customer of the successful 
deletion of the payment method, through a "Method Removed Successfully" banner. After removal, 
the system redirects the customer to the "Stored Payment Methods" View.</p></li>
<li><b><format color="CornFlowerBlue">Branch Sequence</format></b>:
<p>During the confirmation request, if the customer does not click on the "Confirm Removal" 
button, and rather presses on the "Cancel Removal" Button, the system will redirect the customer 
to the "Stored Payment Methods" view.</p>
<p>During the parsing of the payment information provided to the system, if the system detects 
that the information is being used as a primary payment method for the account, it will inform 
the customer through a "Cannot Delete Primary Payment Method" banner, proceeding to ask the user 
to define a new primary payment method before deletion. To do this, the system redirects them to 
the "Stored Payment Methods" view.</p>
</li>
</list>

<img alt="RemovePaymentMethod.png" src="RemovePaymentMethod.png" thumbnail="true"/>
</def>
<def title="Modify Payment Method">
<list>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>:
<p>The system receives a flag after a customer pressed the "Modify Payment Method" button. The 
system redirects the customer to the "Input Payment Method Fields" View. The customer inputs all 
the required information and clicks the "Save Changes" button. The system internally calls the 
<b><code>PaymentProcessingSubsystem</code></b> to validate the information provided. Upon 
validation, the system communicates the successful modification of the payment method through a 
"Payment Modification Succeeded" banner. The system then stores a log of the process in the 
<b><code>CustomerManagementSubsystem</code></b>, along with the information of the payment 
method changes. After information storage, the system redirects the customer to the "Stored 
Payment Methods" View</p></li>
<li><b><format color="CornFlowerBlue">Branch Sequence</format></b>:
<p>During the payment validation, if the <b><code>PaymentProcessingSubsystem</code></b> fails to 
validate any and all parameters passed into the modification method, the system will inform the 
user of this through an "Invalid Payment Method" banner, redirecting them to the "Stored Payment 
Methods" view.</p>
</li>
</list>

<img alt="ModifyPaymentMethod.png" src="ModifyPaymentMethod.png" thumbnail="true"/>
</def>
<def title="Record Delivery Milestone">
<list>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>:
<p>The system receives an internal flag from a Driver's "Update Delivery Status" view about a 
delivery status change initiated by a driver. The system, internally connects with the 
<b><code>DeliveryTracking</code></b> instance associated with the 
<b><code>DeliveryDriver</code></b> and the Order. The system stores internally the milestone 
change and appends it to the current Status in the <b><code>DeliveryTracking</code></b> bridge 
connection.</p></li>
<li><b><format color="CornFlowerBlue">Branch Sequence</format></b>:
<p>During the <b><code>DeliveryTracking</code></b> connection phase, if the system fails to 
connect to the <b><code>DeliveryTracking</code></b> instance held between the Customer, 
<b><code>DeliveryDriver</code></b> and wrapped around the Order in progress, the system will 
store all milestone information changes internally and await until 
connection can be reestablished.</p>
</li>
</list>

<img alt="RecordDeliveryMilestone.png" src="RecordDeliveryMilestone.png" thumbnail="true"/>
</def>
<def title="Validate Administrative Credentials">
<list>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>:
<p>The system, through the main "Log in" views, receives a set of credentials commonly 
associated with managerial accounts (e.g., different email provider or extension name) after the 
account pressed the "Log In" button. The system validates these credentials against the 
<b><code>DatabaseManagementSystem</code></b> information. Upon successful validation, the system 
informs the initiator of this use case of the correctness of the data through an internal flag, 
creating a <b><code>SessionToken</code></b>. The system then records a log of the login attempt, 
and other information, to the respective <b><code>SecurityManagementSubsystem</code></b>.
</p></li>
<li><b><format color="CornFlowerBlue">Branch Sequence</format></b>:
<p>During the credential information polling, the system will reattempt connection to the 
database at most three times. If the database fails to respond on those three times, the system 
will return an invalidation flag to the caller, along with error information, for upstream 
processing.</p>
<p>During the validation process, if the system fails to find a record that corresponds to the 
provided account username and email information, it will return a message to the caller in the 
form of an internal invalidation flag along with all error information.</p>
</li>
</list>

<img alt="ValidateAdministrtiveCredentials.png" src="ValidateAdministrtiveCredentials.png" thumbnail="true"/>
</def>
<def title="Log Administrative Action">
<list>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>:
<p>The system registers a data change done by a manager to an underlying subsystem. The system 
registers in a log file previous and current updated values. The system saves the information in 
a log file corresponding to the administrative level and specialization of the manager that 
performed the changes. The system reports this log file back to the caller of this use case for 
further processing.</p></li>
<li><b><format color="CornFlowerBlue">Branch Sequence</format></b>:
<p>During the change storage request, if the system encounters that subsystem connectivity 
cannot be established after three attempts, an invalidation signal, and error information, will 
be returned to the caller for further processing.</p>
</li>
</list>

<img alt="LogAdministrativeAction.png" src="LogAdministrativeAction.png" thumbnail="true"/>
</def>
<def title="Modify Promotional Campaign">
<list>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>:
<p>The content manager clicks on the "Modify Campaign" button. The system redirects the manager 
to the "Modify Your Campaign Information" view. The manager can change or leave unaltered a 
number of fields within this view. Once all information is registered, the manager presses the 
"Save Changes" button. The system internally validates all information. The system then logs all 
changes done into the ContentManagementSubsystem.</p></li>
<li><b><format color="CornFlowerBlue">Branch Sequence</format></b>:
<p>During validation, if any of the provided fields fails according to the business logic of the 
application, the system will inform the view from where this use case was initialized with an 
internal flag. The system then will process the flag and output a corresponding exceptional 
banner.</p></li>
</list>

<img alt="ModifyPromotionalcampaign.png" src="ModifyPromotionalcampaign.png" thumbnail="true"/>
</def>
<def title="Delete Promotional Campaign">
<list>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>:
<p>The content manager clicks on the "Remove Campaign" button. The system displays a 
confirmation banner. The manager clicks on the "Confirm Removal" button, and the system proceeds 
to remove the campaign from the internal database and management subsystem. The system 
internally records the content change through a <b><code>ChangeLog</code></b> instance, which is 
then stored within the <b><code>ContentManagementSubsystem</code></b>. Finally, the system 
redirects the manager to the "Manage Restaurant Content" Dashboard.</p></li>
<li><b><format color="CornFlowerBlue">Branch Sequence</format></b>:
<p>During the confirmation request, if the manager clicks the "Cancel Removal" button, the 
system will redirect the manager to the "Manage Restaurant Content" Dashboard.</p></li>
</list>
<img alt="DeletePromotionalCampaign.png" src="DeletePromotionalCampaign.png" thumbnail="true"/>
</def>
</deflist>
</procedure>

#### Robustness Analysis ― Second Phase
<p>The second phase of the project began with a thorough review of the use cases defined for all 
secondary, but just as important, actors that had been identified in the system. Our model 
defined these actors as externals due to their nature as services that could be acquired from 
any vendor rather than having proprietary AI services. For this reason, the use cases defined 
mostly tackle the issues that arise through internet communication, shortages in the services 
and the processing of their data. Taken together with the previous use cases, these are  
related to the proposed backend of the app, sure in the previous use cases we mentioned 
different views that could arise when there is an issue in either of the services, and how the 
ssytem would inform the user of such problems, but the problems mentioned in these use cases, 
define the process of how we are going to handle these during implementation.
</p>
<p>To do this, we divided the work into two separate groups of actors that are related to 
different view points of the app. The firs group, comprising the GPS System, the Payment 
Processing System, the Authentication Service, and Security Manager, all have something to do 
with the user, and delivery driver’s interaction with our application. On the other hand, the 
group comprising the Ingredient, Storage, Delivery and Cellular Network, are all actors whose 
relationship is closely tied to the backend of our application with respect to manager's 
interactions with our app.  
</p>
<p>Granted, these groupings are merely symbolic and useful from a design point of view, all of 
these components cannot be segregated as they closely rely on each other to function in an 
orchestra of operations that allow the app to work. The following are the use cases that we have 
defined in terms of all of these actors <i><code>improved and with both robust and 
activity diagrams present</code></i>
</p>

<procedure title="Use Case Listing ― Service Actors ― Robustness Diagrams">
<deflist type="full" collapsible="true">
<def title="GPS System Service Use Cases">
<deflist type="full" collapsible="true">
<def title="Tracking Delivery Driver Location">
<list>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>: 
<p>
The system periodically requests GPS location data from the delivery driver's device. The GPS collects the latitude 
and longitude data and transmits it to the main server. The system then updates the live tracking map for customers 
and administrators. Additionally, the estimated time of arrival (ETA) is recalculated and displayed to the user.
</p></li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>: 
<p>
If the GPS signal is lost, the system uses the last known location and provides hit-based updates until real-time 
tracking resumes. If the driver's device is not connected to the network, the system attempts to obtain location 
data less frequently and notifies the driver.
</p></li>
</list>

<img alt="TrackingDeliveryDriverLocation.png" src="TrackingDeliveryDriverLocation.png" thumbnail="true"/>
</def>
<def title="Optimizing Delivery Route">
<list>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>: 
<p>
The system collects current GPS location data from all drivers. The data is then sent to DeliveryTracking and 
traffic conditions and estimated delivery times are analyzed. Finally, the optimized route is sent to the delivery 
driver's interface.
</p></li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>: 
<p>
If external traffic data is not available, the system uses historical data to provide an estimated optimal route. If 
the driver deviates from the suggested route, the system recalculates and offers a new optimized route.
</p></li>
</list>

<img alt="OptimizingDeliveryRoute.png" src="OptimizingDeliveryRoute.png" thumbnail="true"/>
</def>
</deflist>
</def>
<def title="Security Manager Service Use Cases">
<deflist type="full" collapsible="true">
<def title="User Login Attempt Tracking">
<list>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>: 
<p>
A user enters his or her credentials on the login page. The Security Manager logs the login attempt. If the attempt 
is successful, access is granted. However, if multiple failed attempts occur, the system temporarily locks the 
account and notifies the user.
</p></li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>: 
<p>
If an account is locked due to repeated failed attempts, the user must follow a password recovery process. If the 
login attempt comes from an unusual location or device, the system requests additional authentication.
</p></li>
</list>

<img alt="UserLoginAttemptTracking.png" src="UserLoginAttemptTracking.png" thumbnail="true"/>
</def>

<def title="Session Management">
<list>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>: 
<p>
A user logs into the system, which generates and securely stores a session token. During next requests, the 
system verifies the token's validity. If the session expires, the user is logged out and must authenticate again.
</p></li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>: 
<p>
If a user logs in from a second device, the system checks the policies in place (either single session or multiple 
sessions) and acts accordingly. Additionally, if a session remains inactive for a predefined period, the system 
automatically logs the user out.
</p></li>
</list>

<img alt="SessionManagement.png" src="SessionManagement.png" thumbnail="true"/>
</def>
</deflist>
</def>
<def title="Payment Processing Service Use Cases">
<deflist type="full" collapsible="true">
<def title="Process Customer Payment">
<list>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>: 
<p>
The customer selects a payment method at checkout. The system then securely transmits the payment details to the 
Payment Processing System. The Payment Processing System validates the data and authorizes the transaction. Once 
successfully authorized, the order is confirmed and a receipt is generated for the customer.
</p></li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>: 
<p>
If the payment fails, the system notifies the user and requests an alternative payment method. In case of suspected 
fraud, the system declines the transaction and notifies the Security Manager.
</p></li>
</list>

<img alt="ProcessCustomerPayment.png" src="ProcessCustomerPayment.png" thumbnail="true"/>
</def>

<def title="Refund Processing">
<list>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>: 
<p>
The user requests a refund through customer service. The system then verifies the order details and eligibility for 
the refund. If everything is valid, the request is sent to the Payment Processing System for execution and the user 
is notified of the refund status.
</p></li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>: 
<p>
If the refund request is denied, the system provides a detailed reason. If the payment method used does not allow 
refunds, the system offers store credit or another form of compensation.
</p></li>
</list>

<img alt="RefundProcessing.png" src="RefundProcessing.png" thumbnail="true"/>
</def>
</deflist>
</def>
<def title="Authenticator Service Use Cases">
<deflist type="full" collapsible="true">
<def title="Validate User Credentials">
<list>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>: 
<p>
A user enters his or her username and password. The system securely transmits these credentials to the 
Authentication Service. The Authentication Service validates the credentials and returns an authentication token. If 
authentication is successful, the system grants the user access.
</p></li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>: 
<p>
If authentication fails, the system prompts the credentials to be re-entered or a password recovery process to be 
initiated. If multifactor authentication (MFA) is enabled, the system requests additional verification.
</p></li>
</list>

<img alt="ValidateUserCredentials.png" src="ValidateUserCredentials.png" thumbnail="true"/>
</def>
<def title="Manage Token Expiry and Renewal">
<list>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>: 
<p>
A user remains active in the system. Before the token expires, the system requests a renewal from the Authentication 
Service, which verifies the user's activity and grants a new session token.
</p></li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>: 
<p>
If token renewal fails, the user is logged out and must authenticate again. If suspicious activity is detected, the 
system invalidates all active tokens and forces re-authentication.
</p></li>
</list>

<img alt="ManageTokeExpiryAndRenewal.png" src="ManageTokeExpiryAndRenewal.png" thumbnail="true"/>
</def>
</deflist>
</def>
<def title="Ingredient Forecast AI Service Provider Use Cases">
<deflist type="full" collapsible="true">
<def title="Request Statistics and Predictions">
<list>
<li><b><format color="CornFlowerBlue">Base Sequence</format></b>: 
<p>
The system receives a request from a top-level, user-facing interface about a request for the latest AI-Driven Report. 
The system relays the call to the underlying IngredientUsageForecastService. The underlying IngredientUsageForecastService 
system relays the processing call to the OrderAnalyzer instance it is composed of. The underlying OrderAnalyzer compiles and 
analyzes current deliveries and a set of past deliveries based on its prediction guidelines. The underlying OrderAnalyzer 
wraps the information in a business-logic-defined format and returns it to the IngredientUsageForecastService. The 
IngredientUsageForecastService retrieves all information and stores it within an IngredientUsageRecord. Additionally, the 
IngredientUsageForecastService stores the information within the DatabaseManagementSystem for further polling. The system 
returns this new IngredientUsageRecord to the upper-level function caller.
</p></li>
<li><b><format color="CornFlowerBlue">Branch Sequence</format></b>: 
<p>
During the call forwarding to the OrderAnalyzer instance, the system will attempt to connect to the underlying 
DatabaseManagementSystem at most three times. After three unsuccessful attempts, the system will return a failure state signal.
</p></li>
</list>


<img alt="RequestStatisticsAndPredictions.png" src="RequestStatisticsAndPredictions.png" thumbnail="true"/>
<img alt="RequestStatisticsAndPredictionsROB.png" src="RequestStatisticsAndPredictionsROB.png" thumbnail="true"/>
<img alt="RequestStaticsAndPredictionsACT.png" src="RequestStaticsAndPredictionsACT.png" thumbnail="true"/>
</def>
</deflist>
</def>
<def title="Inventory Forecast AI Service Provider Use Cases">
<deflist type="full" collapsible="true">
<def title="Request Storage Quantity and Replenishment Estimation">
<list>
<li><b><format color="CornFlowerBlue">Base Sequence</format></b>: 
<p>
The system receives a request from a top-level, user-facing interface about a request for the latest AI-Driven Report. 
The system relays the call to the underlying InventoryForecastService. The underlying InventoryForecastService relays the 
processing call to its underlying OrderAnalyzer. The underlying OrderAnalyzer compiles and analyzes current deliveries and 
a set of deliveries based on its prediction guidelines. The underlying OrderAnalyzer wraps the information in a 
business-logic-defined format and returns it to the InventoryForecastService. The InventoryForecastService system retrieves 
that information and wraps it in an InventoryForecastRecord. The InventoryForecastService system stores the information 
within the DatabaseManagementSystem for further polling. The system returns this new InventoryForecastRecord to the upper-level function caller.
</p></li>
<li><b><format color="CornFlowerBlue">Branch Sequence</format></b>: 
<p>
During the call forwarding to the OrderAnalyzer instance, the system will attempt to connect to the underlying 
DatabaseManagementSystem at most three times. After three unsuccessful attempts, the system will return a failure state signal.
</p></li>
</list>

<img alt="RequestStorageQuantityAndReplenishmentEstimationRobust.png" 
src="RequestStorageQuantityAndReplenishmentEstimationRobust.png" thumbnail="true"/>
<img alt="RequestStorageQuantityEstimationACT.png" src="RequestStorageQuantityEstimationACT.png" 
thumbnail="true"/>
</def>
</deflist>
</def>
<def title="Delivery Forecast AI Service Provider Use Cases">
<deflist type="full" collapsible="true">
<def title="Request AI-Optimized Delivery Route">
<list>
<li><b><format color="CornFlowerBlue">Base Sequence</format></b>: 
<p>
The system receives a request from a top-level, user-facing interface about a request for the latest AI-Driven Report. 
The system relays the call to the underlying DeliveryForecastService. The underlying DeliveryForecastService system relays 
the processing call to its DeliveryAnalyzer internal composited instance. The underlying DeliveryAnalyzer compiles and 
analyzes current deliveries and a set of deliveries based on its prediction guidelines to find an optimized delivery route. 
The underlying DeliveryAnalyzer wraps the information in a business-logic-defined format and returns it to the 
DeliveryForecastService. The DeliveryForecastService retrieves all information and stores it within a 
RouteOptimizationRecord. The system returns this new RouteOptimizationRecord to the upper-level function caller.
</p></li>
<li><b><format color="CornFlowerBlue">Branch Sequence</format></b>: 
<p>
During the call forwarding to the DeliveryAnalyzer instance, the system will attempt to connect to the underlying 
DatabaseManagementSystem at most three times. After three unsuccessful attempts, the system will return a failure state signal.
</p></li>
</list>

<img alt="RequestRouteOptimization.png" src="RequestRouteOptimization.png" thumbnail="true"/>
<img alt="RouteOptimizationROB.png" src="RouteOptimizationROB.png" thumbnail="true"/>
<img alt="RouteOptimizationACT.png" src="RouteOptimizationACT.png" thumbnail="true"/>
</def>
<def title="Perform On-demand Delivery Analysis">
<list>
<li><b><format color="CornFlowerBlue">Base Sequence</format></b>: 
<p>
The system receives a request from a top-level, user-facing interface about a request for the latest AI-Driven Report. 
The system relays the call to the underlying DeliveryForecastService. The underlying DeliveryForecastService system relays 
the processing call to its DeliveryAnalyzer internal composited instance. The underlying DeliveryAnalyzer compiles and 
analyzes current deliveries and a set of deliveries based on its prediction guidelines. The underlying DeliveryAnalyzer wraps 
the information in a business-logic-defined format and returns it to the DeliveryForecastService. The DeliveryForecastService 
retrieves all information and stores it within a RouteOptimizationRecord. Additionally, the DeliveryForecastService 
stores the information within the DatabaseManagementSystem for further polling. The system returns this new 
RouteOptimizationRecord to the upper-level function caller.
</p>
</li>
<li><b><format color="CornFlowerBlue">Branch Sequence</format></b>: 
<p>
During the call forwarding to the DeliveryAnalyzer instance, the system will attempt to connect to the underlying 
DatabaseManagementSystem at most three times. After three unsuccessful attempts, the system will return a failure state signal.
</p>
</li>
</list>
<img alt="OnDemandDeliveryAnalysisROB.png" src="OnDemandDeliveryAnalysisROB.png" thumbnail="true"/>
<img alt="OnDemandDeliveryAnalysisACT.png" src="OnDemandDeliveryAnalysisACT.png" thumbnail="true"/>
</def>
</deflist>
</def>
<def title="Cellular Network Service Use Cases">
<deflist type="full" collapsible="true">
<def title="Communicate Route">
<list>
<li><b><format color="CornFlowerBlue">Normal Flow</format></b>: 
<p>
When an OptimizedRouteRecord is produced by the Request AI Optimized Delivery Route, the record containing the route 
must be handed to the delivery driver. To achieve this, the system will create an APICall for the cellular network using the 
OptimizedRouteRecord and order-associated DeliveryTracking. The resulting APICall will be inserted into a CallSenderQueue, 
which stores all pending calls waiting to be sent. 
<br/>
The CallSenderQueue requests network availability from the CellularNetworkConnection, the interface connecting the cellular network
with the system. If the network is available, the system sends the API call through the CellularNetworkConnection interface.
The cellular network is then expected to confirm the receipt of the message by notifying the CellularNetworkConnection.
If the confirmation is received before a timeout occurs, the system will signal to the CallSenderQueue that it is safe to send a new message.
</p></li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>: 
<p>
If a timeout occurs before receiving a confirmation notification from the cellular network or the cellular network notifies 
“failed sending,” the system will request the resending of the message up to three times.
</p></li>
<li><b><format color="CornFlowerBlue">Exception Flow</format></b>: 
<p>
If the cellular network isn’t available, the system will communicate a "fallen network" message. If the resend message fails 
after three failed attempts, the system will communicate a "communication error" message.
</p></li>
</list>

<img alt="CommunicationUseCase.png" src="RequestRouteOptimization.png"  thumbnail="true"/>
<img alt="CommunicateRouteROB.png" src="CommunicateRouteROB.png" thumbnail="true"/>
<img alt="CommunicateRoouteACT.png" src="CommunicateRoouteACT.png" thumbnail="true"/>
</def>
</deflist>
</def>
</deflist>
</procedure>


## Annexes
<p>The following is a singular annexe for this part of the project where we expand on the new 
classes that were included in an updated version of the domain model. For the most part, the 
classes that have been added have been done to so simplify or align the communication process 
between service layers and view layers. In addition, classes have been added to represent 
communication objects and internal inforamtion like Session Tokens, or Security Alerts that are 
used within upper level use cases</p>
<procedure title="Updated Domain Model">
<img alt="UpdateDomainModelPart2PizzaDeliverySystem.png" 
src="UpdateDomainModelPart2PizzaDeliverySystem.png" thumbnail="true"/>
</procedure>
<note><p>The original descriptions, added into the part one of this project, are still 
valid for all classes aside the ones to be mentioned now. These previous classes have 
allowed us to architect the entire application, while the new ones focused on 
streamlining communication</p></note>
<procedure title="Domain Model ― New Classes Descriptions">
<deflist type="full" collapsible="true">
<def title="ContentManagementSubsystem">
<p>This class is simply a communication layer, it is a representation added to signify the 
existance of an underlying system to which the manager sends information, and from which the 
manager gathers information. It is not a class that will be implemented as a singular class, 
rather in implementation it will most likely become  <b><code>several classes</code></b>  to 
handle the underlying system</p>
</def>
<def title="WarehouseManagerSubsystem">
<p>Similarly to the ContentManagementSubsystem, this class is simply a representation of the 
underlying system assigned to the overall branch of the Warehouse Management system in the 
application</p>
</def>
<def title="CustomerManagementSubsystem">
<p>Representation of a series of underlying classes to be designed to handle the communication, 
persistency, and other requirements that the customer maangement must handle.</p>
</def>
<def title="DeliveryManagementSubsystem">
<p>Representation of a series of underlying classes to be designed to handle the communication, 
persistency, and other requirements that the delivery management part of our app must handle.</p>
</def>
<def title="SecurityManagementSubsystem">
<p>As with the rest subsystem representations, this class is a representation to the series of 
classes that will be required, or at least to the subsystem that will be required to handle 
security management concerns.</p>
</def>
<def title="SupportTicket">
<p>This class was added as a response to different use cases requirying an object to communicate 
with, management, and modify when handling cases of client Support Alert. Due to our application 
architecture, the customer management subsystem would have a way for the customer to communicate 
to a customer management representative in order to resolve issues. For this reason this class 
was defined to represent this kind of interactions, and to allow interactions with the system to 
utilize an object.
</p>
<list>
<li><b><format color="CornFlowerBlue">customerUUI</format></b>: UUID attached to the customer 
that raised the SupportTicket.</li>
<li><b><format color="CornFlowerBlue">customerProvidedReason</format></b>: Text representing 
the message, or reason, attached to the Support Ticket that was opened by a customer.</li>
<li><b><format color="CornFlowerBlue">customerOrderUniqueID</format></b>: Internal ID 
identifying this support ticket and can be used later for storage, polling and resolution, etc.
</li> 
</list>
</def>
<def title="IngredientUsageRecord">
<p>This Record is a representation of the <b><code>new underlying communication 
mechanisms</code></b> that have been added into the model to facilitate communication between the 
underying IngredientUsageForecastService towards the Content and Warehouse managers, through 
their required interfaces. The idea of this record is to simply represent a way for services to 
communicate information, immutably, and in a structured format</p>
<list>
<li><b><format color="CornFlowerBlue">usageRecordPredictedSalesIncreases</format></b>: This is a 
parameter that can be present, or not, depending on the caller of the underlying subsystem, this 
represents the predicted sales increases that a product can have, useful for statistical 
analysis and management decision making that managers do.
</li> 
<li><b><format color="CornFlowerBlue">usageRecordStatisticsPerIngredient</format></b>: This is a 
parameter that is representative of an statistical analysis done per ingredient that can be 
used to handle information transmission and business decision making.
</li> 
<li><b><format color="CornFlowerBlue">usageRecordSuggestedRotationSchedule</format></b>: This 
si the last parameter of this record, useful to the warehouse manager that is used to 
represent information useful to handle ingredient rotation and management.</li> 
</list>
</def>
<def title="InventoryForecastRecord">
<p>This Record is used to transmit information only useful to the warehouse manager, this is a 
per ingredient analysis record that holds information about maximum, minimum and rotation 
schedules that can be used per ingredient. It is similar to the IngredientUsageRecord, but this 
works on the level of the inventory, i.e., to the amount that would be required to correctly 
handle orders.</p>
<list>
<li><b><format color="CornFlowerBlue">inventoryRecordMinimumIngredientStorageAmount</format></b
>: As mentioned, this is a way to represent the minimum amount of an ingredient that should be 
stored based on an inventory analysis done with relationship to orders.
</li> 
<li><b><format color="CornFlowerBlue">inventoryMaximumIngredientStorageAmount</format></b>: As 
mentioned, this is a way to represent the maximum amount of an ingredient that should be stored 
based on an inventory analysis done with relationship to orders.
</li>
<li><b><format color="CornFlowerBlue">inventoryRecordSuggestedRotationSchedule</format></b>: 
Like before, this is a useful communication parameter that retruns an informative rotational 
schedule defined by the AI service providers.</li> 
</list>
</def>
<def title="APIRequest">
<p>This is a representative class that includes a mention to the process of API request towards 
th AI services. Given that our model for this application includes a combination of local 
processing and external API services, we required this class to represent the communication 
process between services, and the upper view layers.</p>
<list>
<li><b><format color="CornFlowerBlue">apiRequestInformation</format></b>: This is a 
representative parameter that would hold parameter information that would be required to 
handle an API communication towards the services that our application requires.</li>
<li><b><format color="CornFlowerBlue">apiRequestSenderInformation</format></b>: An informative 
parameter representing information about the sender of the given request.
</li> 
</list>
</def>
<def title="DatabaseManagementSystem">
<p>The database management system class represents the means of data persistence that the 
application had previously lacked. As noted in some of the use cases in part one of this project,
we had neglected or took as external to the initial model, the topic of data persistence. 
However, now we have included it as an entry point to the database system within the application.
</p>
<list>
<li><b><format color="CornFlowerBlue">DBMSConnectionURL</format></b>: Parameter that refers to 
the connection URI or URL to the internal database </li>
<li><b><format color="CornFlowerBlue">DBMSAuthenticationToken</format></b>: Parameter that 
represents the authentication token of the internal database connection </li>
<li><b><format color="CornFlowerBlue">DBMSEncryptionRules</format></b>: Parameter that 
represents any encryption rules for the information to be stored in the database.</li>
<li><b><format color="CornFlowerBlue">DBMSReplicationRules</format></b>: Parameter that 
represents any and all data replication rules taht the database uses.</li> 
</list>
</def>
<def title="ChangeLog">
<p>Class used to represent the way the system stores any and all chages done to administrative 
subsystems.</p>
<list>
<li><b><format color="CornFlowerBlue">administrativeAccountUUID</format></b>: Parameter 
representative of the UUID associated with the account of a manager that has performed a change.
</li>
<li><b><format color="CornFlowerBlue">administrativeChangesRecord</format></b>: Parameter 
representative of the record of changes that were done. </li> 
<li><b><format color="CornFlowerBlue">administrativeChangesDate</format></b>: Parameter 
representative of the date in which the changes were done.</li>
<li><b><format color="CornFlowerBlue">administrativeChangesSubsystemID</format></b>: Parameter 
representative of the subsystem ID in which the changes were executed.</li> 
</list>
</def>
<def title="SecurityAlert">
<p>A class representative of an alert that was raised due to incorrect log in parameters, 
multiple incorrect log in attempts, etc. The idea of this class is to handle any and all 
security alerts raised by the security manager.</p>
<list>
<li><b><format color="CornFlowerBlue">alertCustomerUUID</format></b>: Parameter representastive 
of the customer UUID to whome the alert is associated to.</li>
<li><b><format color="CornFlowerBlue">alertCustomerLastLogin</format></b>: Parameter 
representative of the customer’s last successful login into the system.</li>
<li><b><format color="CornFlowerBlue">alertReason</format></b>: Parameter used to represent the 
reason by which the security manager raised this alert. It is a useful parameter, helpful to 
the Customer Manager to review cases and filter, etc.</li> 
</list>
</def>
<def title="SessionToken">
<p>A session token was one of those classes that was not present in the original model. This 
class is now used to represent a user's log in connection, and a class that allows the system to 
handle connections, as well as authentication without having to ask the user to authenticate 
again through login.
</p>
<list>
<li><b><format color="CornFlowerBlue">sessionTokenUUID</format></b>: Parameter representing the 
UUID of a given token, this is useful for token storage and transmission, as well as validation 
</li> 
<li><b><format color="CornFlowerBlue">sessionTokenUserUUID</format></b>: Parameter that 
represents the user UUID that is associated to the SessionToken, this ties together the token 
to the user and can be used for validation</li> 
<li><b><format color="CornFlowerBlue">sessionTokenCreationTime</format></b>: Parameter that 
represents the user token’s creation time, parameter useful for time based session token 
management, or deletion</li>
<li><b><format color="CornFlowerBlue">sessionTokenDeletionTime</format></b>: Parameter that 
represents the user’s token’s deletion time.</li> 
</list>
</def>
<def title="AddressValidationSystem"><p>
This class is used to represent a validation system that is used under the hood to validate the 
addresses provided by any users. It is modeled in the light of the real AddressValidator API 
that is offered by Google to validate addresses through an API.
</p>
<list>
<li><b><format color="CornFlowerBlue">addressValidatorAPICredentials</format></b>:  Parameter 
defining the required API credentials required to use the validation API that is provided by 
Google</li>
<li><b><format color="CornFlowerBlue">addressValidatorAPIHandler</format></b>:  Parameter 
defining a handler for the AddressValidatorAPI, this would be a parameter that represents 
perhaps an internal class that could manage multithreaded and concurrent communication.</li> 
</list>
</def>
<def title="BillingValidationSystem">
<p>The BillingValidationSystem is used as a representative class to the connection to the 
BillingValidator API that is also provided online as a tool for validating the billing 
information that can be provided. In theory this would be somewhat validated depending on the 
locality of the application, subjecting this class to local regulations</p>
<list>
<li><b><format color="CornFlowerBlue">billingValidatorAPICredentials</format></b>: Parameter 
that represents the API credentials required to handle the connection and access to the 
validation API used to validate billing information.</li>
<li><b><format color="CornFlowerBlue">billingValidatorAPIHandler</format></b>:  Parameter that, 
as in the case for the AddressValidationSystem, could represent an internal class instance that 
is used to handle multiple concurrent API requests.
</li> 
</list>
</def>
</deflist>
</procedure>