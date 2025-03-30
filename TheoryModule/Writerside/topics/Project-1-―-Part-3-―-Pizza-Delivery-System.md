# Project #1 ― Part #3 ― Pizza Delivery System

> The present file will contain all information for the last leg of the 
> Pizza Delivery System project, including all diagrams that have been 
> updated from the Robustness Diagrams of part two, and new graphs like 
> Sequence or State diagrams in part three. In addition, an updated class 
> diagram has been included.

<note><p>The following is information related to the project, group names 
and identifiers, etc.
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


## Pizza Delivery System ― All Diagrams Required
<p>
The content in this section includes all diagrams that have been revised, 
and created, based on the information of a select few of use cases. Given 
the size of the project and the time complexities that previous parts of the 
project have already entailed, we decided to reduce the number of use cases 
we grabbed and worked on.
</p>
<p>This was done mainly to reduce the load of graphics that we were 
producing, and focus on the overall quality, and roundness of the diagrams, 
To do this we re-revised our diagrams again, going over each description, 
and previous robustness diagrams to articulate the use case objective better,
include mentions to the Domain Model more clearly, and more.
</p>
<p>Moreover, changes were done to most of the original diagrams that were 
produced during previous iterations of the project in an effort to make our 
later diagrams link up and represent the use case more clearly and in line 
with our goals for the system. When we did this, we carried out a systematic 
review of each of the diagrams, taking a look at the actors that were 
involved, missing classes that we might need to add now, or even missing 
relationships or unclear relationships in diagrams.
</p>
<p>While the changes done were minimal, this approach helped us realize our 
goals better, and provide clearer and more structured diagrams that could 
not only be used as a learning tool, but also as a real stepping stone for a 
future implementation of this system.
</p>

## All Diagrams Required ― External and Administrative Actors
<procedure title="All Diagrams Required ― External and Administrative Actors">
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
customer's <b><code>ShoppingCart</code></b>. The customer presses the <b><code>"Update Shopping
Cart Items Button"</code></b> and views the <b><code>"Available Pizza Options"</code></b> view
(<b><code>PopularCombinations</code></b>, preconfigured options, and <b><code>"Create your Own
Pizza"</code></b> <b><code>PizzaMenu</code></b>). The customer selects one
<b><code>PizzaMenu</code></b>. Then the customer configures or selects a <b><code>Pizza</code></b>,
at which point the system checks for <b><code>Ingredient</code></b> availability in storage.
Upon successful <b><code>Ingredient</code></b> validation, the user is redirected to the
<b><code>"Finish Your Pizza"</code></b> tab to specify details like crust and size. Once all
details are filled, the customer clicks on the <b><code>"Add To Shopping Cart"</code></b>
button, at which point, after saving the current state within the customer's
<b><code>ShoppingCart</code></b>, the system redirects the customer to the <b><code>"My
Shopping Cart"</code></b> tab, showing the updated totals and contents.</p>
</li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>:
<p>After clicking the <b><code>"View My Shopping Cart"</code></b> button, the user might not
have any information within their <b><code>ShoppingCart</code></b>, at which point the system
shows the <b><code>"Shopping Cart Empty"</code></b> banner.
<br/><br/>
After clicking the <b><code>"Update Shopping Cart Items"</code></b> Button, if the system
encounters an internal <b><code>DatabaseManagementSubsystem</code></b> error, the
<b><code>"Failed To Communicate To Mainframe"</code></b> Banner will be shown, and the customer
will be redirected to the <b><code>"My Shopping Cart"</code></b> View.
<br/><br/>
After the system finished the <b><code>Ingredient</code></b> Availability Check, if any of the
<b><code>Ingredients</code></b> was not available to satisfy the customer's
<b><code>Order</code></b>, the system displays the <b><code>"Ingredient
Unavailability"</code></b> banner and repopulates the <b><code>"Available Pizza Options
View"</code></b>.</p>
</li>
</list>
<img alt="UpdateShoppingCartItems.png" src="UpdateShoppingCartItems.png" thumbnail="true"/>
<img alt="UpdateShoppingCartItemsRBD.png" src="UpdateShoppingCartItemsRBD.png" thumbnail="true"/>
<img src="UpdateShoppingCartItemsACT.png" thumbnail="true"/>
<img alt="UpdatedShoppingCartItemsRBD.png" src="UpdatedShoppingCartItemsRBD.png" thumbnail="true"/>
<img alt="UpdateShoppingCartItemsSEQ.png" src="UpdateShoppingCartItemsSEQ.png" thumbnail="true"/>
<img alt="UpdateShoppingCartItemsSTT.png" src="UpdateShoppingCartItemsSTT.png" thumbnail="true"/>
</def>
<def title="Place Pizza Order">
<list>
<li><b><format color="CornFlowerBlue">Related Requirement Definition</format></b>: <i>ORDMA01,
ORDMA02, ORDMA03, ORDMA04, ORDMA05, ORDMA06, ORDMA07, DELMA02</i></li>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>:
<p>After modifying their <b><code>ShoppingCart</code></b>, within the <b><code>"My Shopping
Cart"</code></b> view, the customer presses the <b><code>"Review My Order"</code></b> button
and is redirected to the <b><code>"My Order"</code></b> view to cancel or proceed with their
<b><code>Order</code></b>. Once in this view, the system displays updated totals and content.
The customer presses the <b><code>"Continue to Checkout"</code></b> button, and the system
redirects the user to a <b><code>"Checkout"</code></b> tab. The customer provides their
<b><code>DeliveryInformation</code></b>, which is internally verified. Next, the system
redirects them to a <b><code>"Select Payment Method"</code></b> view, where they select a
<b><code>PaymentMethod</code></b>, which is also validated internally. Finally, after a
redirection to the <b><code>"Provide Billing information"</code></b> they can opt to supply an
optional billing information field. Upon successful billing information validation, the system
processes the payment, and redirects the customer to the <b><code>"Order
Confirmed"</code></b> view. The system then attempts to initialize a GPS
<b><code>DeliveryTracking</code></b> connection with any driver that accepts the delivery.</p>
</li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>:
<p>After the user clicks the <b><code>"Review My Order"</code></b> button, if the customer's
<b><code>ShoppingCart</code></b> is empty, then the system will inform the user through the
<b><code>"No Content To Order"</code></b> banner and redirect them to the <b><code>"My
Shopping Cart"</code></b> view.
<br/><br/>
During checkout, if the customer's <b><code>DeliveryInformation</code></b> fails validation,
the system communicates this through a <b><code>"Incorrect Address"</code></b> banner, and
redirects to the <b><code>"Checkout"</code></b> view.
<br/><br/>
During payment processing, if the <b><code>PaymentProcessingSystem</code></b> fails to validate
the customer's <b><code>PaymentMethod</code></b> information, the system will inform the
customer of this error through a <b><code>"Invalid Payment Method"</code></b> banner and
redirect the customer to the <b><code>"Select Payment Method"</code></b> view.
<br/><br/>
During the billing information procesing, if the system fails to validate the customer's
billing information, the system will inform the customer of this error through an
<b><code>"Invalid Billing information"</code></b> banner, and redirect the customer to the
<b><code>"Define Billing Information"</code></b> view.
<br/><br/>
During the payment processing, if the <b><code>PaymentProcessingSystem</code></b> fails to
process the customer's payment, the customer will be informed through the <b><code>"Payment
Processing Failed"</code></b> banner and redirected to the <b><code>"Checkout"</code></b>
View.</p>
</li>
</list>
<img alt="PlacePizzaOrder.png" src="PlacePizzaOrder.png" thumbnail="true"/>
<img alt="PlacePizzaOrderRBD.png" src="PlacePizzaOrderRBD.png" thumbnail="true"/>
<img alt="PlacePizzaOrderACT.png" src="PlacePizzaOrderACT.png" thumbnail="true"/>
<img alt="PlacePizzaOrderUpdatedRBD.png" 
thumbnail="true"
src="PlacePizzaOrderUpdatedRBD.png"/>
<img alt="PlacePizzaOrderSEQ.png" 
thumbnail="true"
src="PlacePizzaOrderSEQ.png"/>
<img alt="PlacePizzaOrderSTT.png" 
thumbnail="true"
src="PlacePizzaOrderSTT.png"/>
</def>
<def title="Track Active Order Status">
<list>
<li><b><format color="CornFlowerBlue">Related Requirement Definitions</format></b>: <i>DELMA02,
DELMA02-01, DELMA02-02</i></li>
<li><b><format color="CornFlowerBlue">Main Flow</format></b>:
<p>The <b><code>Customer</code></b> accesses the <b><code>"Track My Order"</code></b> view
from any number of pages. If the <b><code>Customer</code></b> has an active
<b><code>Order</code></b> in the system, the <b><code>Customer</code></b> can access their
active <b><code>Order</code></b> details through this view in the system's web interface. The
system populates the view, with a live map showing both the <b><code>Order</code></b> location
and <b><code>Customer</code></b> location, as well as any meaningful
<b><code>Milestones</code></b>. The system displays the status of their <b><code>Order</code></b>,
displaying an internal flag to the user if the <b><code>Order</code></b> is still in the
kitchen. Once the order enters the delivery phase, the system's web interface will update the
live map feed through a live <b><code>GPSSystem</code></b> connection, showing the location of
the driver, the customer and an ETA for the delivery. The system automatically updates the live
map and displays new <b><code>Milestones</code></b> as they are reached.</p>
</li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>:
<p>During the display of the <b><code>"Track My Order"</code></b> view, if the system detects
that the customer does not have any current <b><code>Orders</code></b> associated with their
<b><code>ShoppingCart</code></b>, the system notifies them through a 
<b><code>"No Current 
Order"</code></b> 
banner
and redirects them to the <b><code>"My Shopping Cart"</code></b> view.</p>
</li>
</list>
<img alt="TrackActiveOrderStatus.png" src="TrackActiveOrderStatus.png" thumbnail="true"/>
<img alt="TrackActiveOrderStatusRBD.png" src="TrackActiveOrderStatusRBD.png" thumbnail="true"/>
<img alt="TrackActiveORderACT.png" src="TrackActiveORderACT.png" thumbnail="true"/>
<img alt="TrackMyOrderStatusUpdatedRBD.png" 
thumbnail="true"
src="TrackMyOrderStatusUpdatedRBD.png"/>
<img alt="TrackMyOrderStatusSEQ.png" 
thumbnail="true"
src="TrackMyOrderStatusSEQ.png"/>
<img alt="TrackMyOrderStatusSTT.png" 
thumbnail="true"
src="TrackMyOrderStatusSTT.png"/>
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
<p>The <b><code>DeliveryDriver</code></b>, already logged in, accesses the <b><code>"Available
Deliveries Near You"</code></b> view in the system's web interface. The system, upon receiving
an update about a new delivery assignment in the delivery driver's
<b><code>DeliveryRadius</code></b>, populates a <b><code>"Available Delivery For
You"</code></b> banner, and loads it into the screen, with the information about the
<b><code>Order</code></b>. The system displays the details including the customer's location,
<b><code>Order</code></b> contents, and delivery payment amount. After reviewing, the driver
accepts by clicking the <b><code>"Accept Delivery Challenge"</code></b> button in the system
interface. The system internally handles accepting the interconnection of the
<b><code>Driver</code></b>'s <b><code>GPS System</code></b> with the Customer's Live Map (i.e.
completing Place Pizza Order Use Case) and finalizing the <b><code>DeliveryTracking</code></b>
creation. The system changes the delivery driver's status to <b><code>"On
Delivery"</code></b>, showing this milestone to the customer too. The system talks to the
<b><code>DeliveryForecastService</code></b> and requests an ETA and optimized delivery route
through a <b><code>RouteOptimizationRecord</code></b>. Finally, the customer and delivery
driver's live maps are updated to show the results of the AI-driven computation.</p>
</li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>:
<p>During the Listening for Newly Placed Orders phase, it is important to note that the use
case defines itself as looping. The delivery <b><code>Driver</code></b> requires a
<b><code>Delivery Challenge</code></b> to continue with the use case.</p>
<br/>
<p>During the Delivery Tracking Handshake synchronization, the system will attempt to
synchronize the internal <b><code>DeliveryTracking</code></b> instance and the
<b><code>Driver</code></b>'s on board system's at most three times. After these three
attempts, the system will drop the connection and revert to a Milestone-based tracking
system.</p>
<br/>
<p>During the AI-driven delivery optimization request, the system will attempt to retrieve this
information at most three times. After these three attempts, the system will drop the AI
Service connection, and revert to a historical ETA. Then the system will report this issue
automatically to the <b><code>DeliveryManagementSubsystem</code></b> for further
escalation.</p>
</li>
</list>
<img alt="AcceptDeliveryAssignment.png" src="AcceptDeliveryAssignment.png" thumbnail="true"/>
<img alt="AcceptDeliveryAssignmentRBD.png" src="AcceptDeliveryAssignmentRBD.png" thumbnail="true"/>
<img alt="AcceptDeliveryAssignmentACT.png" src="AcceptDeliveryAssignmentACT.png" thumbnail="true"/>
<img alt="AcceptDeliveryAssignmentSEQ.png" 
thumbnail="true"
src="AcceptDeliveryAssignmentSEQ.png"/>
<img alt="AcceptDeliveryAssignmentSTT.png" 
thumbnail="true"
src="AcceptDeliveryAssignmentSTT.png"/>
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
<p>The content manager logs in with their <b><code>Credentials</code></b> 
through the <b><code>"Log 
In"</code></b>
view. The system validates their <b><code>Credentials</code></b>. Once 
validated, the content manager is redirected
to the <b><code>"Manage Restaurant Content"</code></b> dashboard through the system's web
interface. The system displays promotional information, pricing, product listings, and campaign
data for various <b><code>ProductCampaign</code>(s)</b>. The content manager 
selects at 
most one 
<b><code>ProductCampaign</code></b>
to manage. Once selected, the manager clicks on the <b><code>"Manage Campaign"</code></b>
button. The system loads all previously listed information solely for this 
<b><code>ProductCampaign</code></b>.
The
content manager clicks the <b><code>"Review AI-Driven Reports"</code></b> button. The system
displays an AI-driven report for orders of the 
<b><code>ProductCampaign</code></b>. The system shows 
the content
manager the <b><code>"Modify Campaign"</code></b> and <b><code>"Delete Campaign"</code></b>
buttons. The content manager clicks on either of these buttons. The system then proceeds to
follow their respective use cases. After following the internal procedures for either process,
the system reports all errors encountered to the dashboard through banners. Following this
process, the system updates the information records for the selected 
<b><code>ProductCampaign</code></b>.</p>
</li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>:
<p>During the log in process, if the content manager introduces their 
<b><code>Credentials</code></b> 
incorrectly
more than three times, their account will be blocked, and a <b><code>SecurityManager</code></b>
report will be stored within the <b><code>ContentManagementSubsystem</code></b>.</p>
<br/>
<p>During the polling of information from the <b><code>DatabaseManagementSystem</code></b>, if
the system encounters that there is no information stored about 
<b><code>Product Campaigns</code></b>, the
system will notify of this through a <b><code>"No Managed Campaigns"</code></b> banner,
displaying a templated version of the <b><code>"Manage Restaurant Content"</code></b>.</p>
<br/>
<p>During the AI-driven report the system invokes the 
<i><code>Request Statistics And Predictions, and Request Storage 
Quantity And Replenishment Estimations</code></i>,
if the system
fails to receive an AI report after three attempts on either subsystem, the 
system will 
inform the manager with an
<b><code>"Unable to Connect To Mainframe"</code></b> banner and log the information
internally.</p>
</li>
</list>
<img alt="ManagePromotionalCampaigns.png" src="ManagePromotionalCampaigns.png" thumbnail="true"/>
<img alt="ManagePromotionalCampaign.png" src="ManagePromotionalCampaign.png" thumbnail="true"/>
<img alt="ManagePromotionalCampaignACT.png" src="ManagePromotionalCampaignACT.png" thumbnail="true"/>
<img alt="ManagePromotionalCampaignSEQ.png" 
thumbnail="true"
src="ManagePromotionalCampaignSEQ.png"/>
<img alt="ManagePromotionalCampaignSTT.png" 
thumbnail="true"
src="ManagePromotionalCampaignSTT.png"/>
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
<p>The warehouse manager attempts to log in through the <b><code>"Log In"</code></b> view from
a number of pages. The manager inputs their <b><code>Credentials</code></b> and clicks the
<b><code>"Log In"</code></b> button. The system validates those <b><code>Credentials</code></b>
internally. Upon validation, system redirects the manager to the <b><code>"Inventory
Management"</code></b> dashboard through the system's web interface. The manager clicks on the
<b><code>"Configure Storage Early Warning Alerts"</code></b> button, and the system displays
the <b><code>"Early Warning Alerts List"</code></b> view loading all 
<b><code>IngredientEarlyWarning</code></b> instances stored within the system. 
Once 
inside, the manager selects at
most one <b><code>IngredientEarlyWarning</code></b> from the listing. 
The system then displays a
<b><code>"Modify Early Warning Alert"</code></b> view. The warehouse manager defines alert
thresholds for different storage conditions, configuring parameters like temperature ranges,
humidity levels, and expiration date notifications. The system logs all changes internally. The
manager presses the <b><code>"Save Changes"</code></b> button. Once pressed, the system applies
all changes to the internal subsystem, and stores the log of all changes within it too.</p>
</li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>:
<p>During <b><code>Credentials</code></b> validation, if the system encounters any errors
through the validation, the system will alert the manager through an <b><code>"Invalid
Credentials"</code></b> banner. If the system receives the same error three times, the account
will be locked and the underlying <b><code>WarehouseManagementSubsystem</code></b> will be
notified through a log of the invalid log in attempts.</p>
<br/>
<p>During the information polling from the main <b><code>DatabaseManagementSubsystem</code></b>,
if the database fails to respond to a query, the system will retry at most three times, at
which point it will warn the manager with the <b><code>"Unable to Connect to
Mainframe"</code></b> Banner, before redirecting the manager to the <b><code>"Inventory
Management"</code></b> dashboard. If the <b><code>DatabaseManagementSubsystem</code></b> fails
to provide information, the system will poll at most three times before repeating the same
warning process.</p>
</li>
</list>
<img alt="ConfigureStorageAlerts.png" src="ConfigureStorageAlerts.png" thumbnail="true"/>
<img alt="ConfigureStorageAlertsRBD.png" src="ConfigureStorageAlertsRBD.png" thumbnail="true"/>
<img alt="ConfigureStorageAlertsACT.png" src="ConfigureStorageAlertsACT.png" thumbnail="true"/>
<img alt="ConfigureStorageAlertsSEQ.png" 
thumbnail="true"
src="ConfigureStorageAlertsSEQ.png"/>
<img alt="ConfigureStorageAlertsSTT.png" 
thumbnail="true"
src="ConfigureStorageAlertsSTT.png"/>
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
number of pages. The manager inputs their <b><code>Credentials</code></b> and 
clicks the 
<b><code>"Log 
In"</code></b>
button. The system validates those <b><code>Credentials</code></b> internally. 
Upon validation, 
system 
redirects the
manager to the <b><code>"Delivery Management"</code></b> dashboard through the system's web
interface. The manager clicks on the <b><code>"Configure Delivery Zones"</code></b> button, and
the system redirects the manager to the <b><code>"Configure Delivery Zones"</code></b> view
through the system's web interface. The system communicates internally with the
<b><code>DatabaseManagementSystem</code></b> and polls all currently defined
<b><code>DeliveryZoneRecord</code>(s)</b> for the program. The manager clicks 
on the
<b><code>"Review AI-Driven Reports"</code></b> button. The system redirects the manager to the
<b><code>"AI-Driven Reports"</code></b> view, where the system polls all stored
<b><code>RouteOptimizationRecord</code></b> records returned until that query by the
<b><code>DeliveryForecastService</code></b>. Additionally, the system polls an up to date
<b><code>RouteOptimizationRecord</code></b>from the underlying AI subsystem. 
The 
manager 
selects at most one 
<b><code>RouteOptimizationRecord</code></b> at 
the time.
The system loads the respective <b><code>RouteOptimizationRecord</code></b> in a
<b><code>"Viewing Report"</code></b> view. Using this report, the manager analyzes coverage
data and traffic patterns for each zone based on this report. The system displays two options,
<b><code>"Download and Close"</code></b> or <b><code>"Close"</code></b>. The manager clicks on
either of these buttons and the system handles the required process. After review, the system
redirects the manager to the <b><code>"Configure Delivery Zones"</code></b> view. The manager
selects at most one <b><code>DeliveryZoneRecord</code></b> to configure. The system loads all
data associated with that zone into a <b><code>"Configure Zone Rules"</code></b> view. The
manager modifies any and all fields within this view, the system validating each change
internally against internal business logic. The manager clicks the <b><code>"Save
Changes"</code></b> button, the system updates the <b><code>DeliveryZoneRecord</code></b>
configurations and stores a log of all changes into the underlying
<b><code>DeliveryManagementSubsystem</code></b>.</p></li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>:
<p>During <b><code>Credentials</code></b> validation, if the system encounters 
any errors through 
the 
validation,
the system will alert the manager through an <b><code>"Invalid Credentials"</code></b> banner.
If the system receives the same error three times, the account will be locked and the underlying
<b><code>DeliveryManagementSystem</code></b> will be notified through a log of the invalid log
in attempts.</p>
<br/>
<p>During all <b><code>DatabaseManagementSystem</code></b> polling steps (<b><code>"Configure
Delivery Zones"</code></b> view loading and <b><code>"Review AI-driven Reports"</code></b>
loading), if the system is unable to establish a connection to the underlying mainframe, after
three attempts, it will display an <b><code>"Unable To Connect to Mainframe"</code></b> banner,
and redirect the manager to the <b><code>"Delivery Management"</code></b> dashboard.</p>
<br/>
<p>During the Configuration of a defined <b><code>DeliveryZoneRecord</code></b>, if the system
encounters any incorrect state being introduced, the system will alert the manager through a
<b><code>"Invalid Configuration Parameter"</code></b> banner, and request correction before
proceeding.</p>
</li>
</list>
<img alt="ConfigureDeliveryZones.png" src="ConfigureDeliveryZones.png" thumbnail="true"/>
<img alt="ConfigureDeliveryZonesRBD.png" src="ConfigureDeliveryZonesRBD.png" thumbnail="true"/>
<img alt="ConfigureDeliveryZonesACT.png" src="ConfigureDeliveryZonesACT.png" thumbnail="true"/>
<img alt="ConfigureDeliveryZonesSEQ.png" 
thumbnail="true"
src="ConfigureDeliveryZonesSEQ.png"/>

<img alt="ConfigureDeliveryZonesSTT.png" 
thumbnail="true"
src="ConfigureDeliveryZonesSTT.png"/>
</def>
</deflist>
</def>
<def title="Customer Manager Use Cases">
<p>The following are use cases defined solely for the Customer Manager (Administrator
Specialization) actor</p>
<deflist type="full" collapsible="true">
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
<b><code>SupportTicket</code>(s)</b> raised by customers. The manager selects 
at most one
<b><code>SupportTicket</code></b> and the system redirects the manager to the 
<b><code>"Review
Ticket Details"</code></b> view. They review <b><code>Order</code></b> details,
<b><code>DeliveryTracking</code></b> confirmation, and <b><code>Customer</code></b> history.
The manager reviews the refund request status, and upon business-logic-dependent validation,
the manager clicks the <b><code>"Process Refund"</code></b> button. The system communicates
the request to the <b><code>PaymentProcessingSystem</code></b> to initiate a refund, handled
in its entirety by the API system. The manager receives confirmation through the
<b><code>"Refund Successful"</code></b> banner. The manager clicks the <b><code>"Close
Ticket"</code></b> button. The system then notifies the customer of the decision and refund
status, closing the <b><code>SupportTicket</code></b> and logging all 
information in the underlying
<b><code>CustomerManagementSubsystem</code></b>.</p></li>
<li><b><format color="CornFlowerBlue">Alternative Flow</format></b>:
<p>During <b><code>Credentials</code></b> validation, if the system encounters 
any 
errors through 
the 
validation,
the system will alert the manager through an <b><code>"Invalid Credentials"</code></b> banner.
If the system receives the same error three times, the account will be locked and the underlying
<b><code>CustomerManagementSubsystem</code></b> will be notified through a log of the invalid
log in attempts.</p>
<br/>
<p>During the information polling from the main <b><code>DatabaseManagementSubsystem</code></b>,
if the <b><code>DatabaseManagementSubsystem</code></b> fails to respond to a query, the system
will retry at most three times, at which point it will warn the manager with the
<b><code>"Unable to Connect to Mainframe"</code></b> Banner, before redirecting the manager
to the <b><code>"Customer Experience Management"</code></b> dashboard. If the database fails
to provide information, the system will poll at most three times before repeating the same
warning process.</p>
<br/>
<p>During the refund processing, if the underlying <b><code>PaymentProcessingSystem</code></b>
fails to return an appropriate response, the system will inform the manager of this issue
through a <b><code>"Unable To Connect to Mainframe"</code></b> banner, redirecting them to
the <b><code>"Customer Experience Management"</code></b> dashboard.</p>
</li>
</list>
<img alt="ProcessRefundRequests.png" src="ProcessRefundRequests.png" thumbnail="true"/>
<img alt="ProcesRefuntRequestsRBD.png" src="ProcesRefuntRequestsRBD.png" thumbnail="true"/>
<img alt="ProcessRefundRequestsACt.png" src="ProcessRefundRequestsACt.png" thumbnail="true"/>
<img alt="ProcessRefundRequestSEQ.png" 
thumbnail="true"
src="ProcessRefundRequestSEQ.png"/>
<img alt="ProcessRefundRequestSTT.png" 
thumbnail="true"
src="ProcessRefundRequestSTT.png"/>
</def>
</deflist>
</def>
</deflist>
</procedure>

## Pizza Delivery System ― Class Diagrams
<p>
The last step in this journey of object-oriented software design, is the 
creation of a fully fledged and expanded class diagram. The idea behind this 
class diagram is showing the parameters, methods, and interconnections as 
close as possible to a language implementation. We have gone from structural 
classes, design classes, and have refined our use cases, diagrams, and 
understaing of the system to the point when we can now produce a class 
diagram that represents the overarching system organization we strived to 
design.
</p>
<p>Developing this model was not easy, as it required handling all of our 
use cases, scouring over them to find all possible methods and parameters 
that we might require (<b><code>For this section, at least, I 
went over all use cases again and extracted methods and 
parameters such that we had continuity even if the diagrams do 
not cover all use cases</code></b>). With this information, several 
refinements were made to the original domain model that we had, as this 
already contained the structural components that we required to be grouped in 
subsystems and modules.</p>
<p>With this base, we updated each of the classes and added more references 
to implementation details that would later come if we were implementing this 
in a real programming language. As we have had more experience with Java 
over our university years, we developed the model such that we used the 
syntax, collections API and other structural components of the language in 
our diagram, while retaining some flexibility in our design.
</p>
<note><p>Attentive readers will notice, when reviewing the diagram, 
that many Android concepts, like Fragments, Bundles and Activities 
have been used here. These provided a much more concise way of 
defining the model and the methods that we required, as it is much 
easier to think of a <b><code>Bundle</code></b> being passed in the 
UI's <b><code>Activities</code></b>, instead of retyping all of the 
data that would be required to pass between views.</p>
<p>In addition, networking concepts and database concepts have been 
used to streamline the representation of server or microservice 
connections that any view or class would require underneath.</p></note>
<p>The use of the MVC pattern as a binding concept between our classes and 
each view, as well as the use of Android components, information transfer 
concepts, and Java's NET package classes, allowed us to reinforce the feel 
of the system as an implementable system with its methods and parameters 
defined, ready to become code</p>
<p>Of course, the work done in the use cases cannot be understated here, he 
work we have carried out redefining them and centering them such that they 
made sense with respect to the requirements we had, as well as with the 
overall domain model we defined, made for a quick and simple transition from 
diagrams to classes.
</p>
<p>Each method and parameter found a home within our classes, and in the 
case we had to articulate new ones or include new parameters, all of them 
were added such that our model was coherent and represent a high cohesion 
between classes instead of tight coupling</p>
<note><p>This is not to say that no classes show coupling, some 
classes like the GPSSystem and CellularConnection require coupling as one 
depends upon the other, even so, we attempted to make the connection as 
versatile as possible, trying to decouple state in favor of a feedback loop 
representation of connections and state transitions
</p></note>
<p>The following is the finalized class diagram produced for this project, 
while it is large, it represents every possible class, parameter and method 
that might be required in an initial foundation coding of this application.</p>
<procedure title="Pizza Delivery System ― Class Diagram" 
id="pizza_delivery_system_class_diagram">
<note><p>If you are trying to view this image on a browser here are 
two things you can do:</p>
<list>
<li>If you are using <b><code>Google Chrome</code></b>, right click on the 
image and view on another tab, scrolling in allows you to see the image in 
full detail</li>
<li>If you are using <b><code>Edge</code></b>, double click 
<b><code>Control</code></b> and it will open the <b><code>Edge 
Image Viewer</code></b>, this will allow you to view the image and zoom in. 
Alternatively, follow the steps for Google and open it in another tab with 
the same steps.
</li>
</list>
</note>


<img alt="ClassDiagramFinal.png" 
thumbnail="true"
src="ClassDiagramFinal.png"/>
</procedure>