#Functional Requirements for the PM 

Feature: Launching a new product from Tribold      

##Specs

## 1. 

#### Feature: Logging in and roles      
> In order to work with the quoting system in a sandbox environment      
> as a user of the system      
> I want to be able to log in      

##### Scenario: Signing in with correct credentials      
> Given I am at the front page of Alphabet      
> When I click on the ‘Sign in with IS ID’ button      
> And I am directed to the ‘Log In’ page      
> And I enter my username      
> And I enter my correct password      
> And I select ‘IS Staff’      
> Then I should be logged in successfully     

##### Scenario: Signing in as a PM      
> Given my name is ‘PM name’      
> When I log in successfully      
> Then my username drop-down ‘Roles’ list should contain ‘PM’      

> Given I have logged in as a PM      
> And I am on the ‘Home’ page      
> When I look under ‘My Quotes’       
> Then I should see a message which reads, ‘Product x is waiting to be activated’      

#### Feature: Product status ribbons      
> In order to keep track of the quote stages      
> as a user      
> I want its state displayed as a colour-coded ribbon      

##### Scenario: Viewing product status       
> Given I am on the ‘Home’ page      
> When the product still needs to be configured       
> Then the status should be displayed as a mustard bar      
> And it should read ‘Pending’      

##### Scenario: Viewing product status       
> Given I am on the ‘Home’ page      
> When the product is ready to go live       
> Then the status should be displayed as a blue-grey bar      
> And it should read ‘Activate’      

#### Feature: Product configuration      
> In order to produce an accurate product      
> as a PM      
> I want to be able to create a product specific to my client’s needs      

##### Scenario: Selecting a product      
> Given I have already launched a product in Tribold      
> And I am on the ‘Home’ page of Alphabet      
> When I select the product under ‘My Products’      
> And I click the ‘edit’ button      
> Then I should be directed to the ‘Configuring Product x’ page      

> OR      

##### Scenario: Selecting a product      
> Given I have already launched a product in Tribold      
> And I am on the ‘New Quote’ page of Alphabet      
> When I look under ‘Product List’      
> Then I should see ‘Product x’ under ‘My Products’      

##### Scenario: Configuring a product       
> Given I am on the ‘New quote’ page      
> When I click on the ‘Configure Product x’ link      
> Then I should see the header ‘Configuring Product x’      
> And it should be displayed in the same screen      

##### Scenario: Configuring a product      
> *Same steps as the Functional Spec       

##### Scenario: Saving a product      
> Given I have successfully completed the product configuration      
> When I click ‘Save Product’       
> Then ‘Product x’ should appear in ‘My Basket’      

*PM should be able to save the product as a quote, and calculate discount etc on the quote. However, this is only for the PM and no one else can see the quotes he saves.      

##### Scenario: Activating a product      
> Given ‘Product x’ is successfully configured and saved      
> And I am on the ‘New Quote’ page      
> Then I should see a button which reads ‘Activate’      

> Given ‘Product x’ is successfully configured and saved      
> When I click the ‘Activate’ button      
> And a message box should appear which reads, ‘There are ‘x’ amount of quotes associated with this product. Activation will result in the cancellation of these quotes. Do you wish to proceed?’      
> And I click the ‘Yes’ button      
> Then ‘Product x’ should go live      
> And should be made available to BDC’s and AM’s       

##### Scenario: Deleting a product      
> Given ‘Product x’ is successfully configured and saved      
> And I am on the ‘New Quote’ page      
> When I look under ‘Totals’       
> Then I should see a ‘Cancel’ button       

> Given ‘Product x’ is successfully configured and saved      
> When I click the ‘Cancel’ button      
> Then the product should be deleted       

#### Feature: Notifications of ‘Product x’       
> In order to       
> as a user      
> I want to be notified of new products      

##### Scenario: Notification of product activation      
> Given I am a PM		
> When I have successfully activated ‘Product x’      
> Then I should receive an email detailing this       

##### Scenario: Notification a new product is available      
> Given I am a BDC/AM	      
> When the new/updated product is made available by a PM      
> Then I should receive an email detailing this      

##### Scenario: Notification of cancelled quotes      
> Given I am a BDC/AM      
> And I had quotes associated to the updated product       
> When the updated product goes live      
> Then I should receive an email detailing the cancelled quotes       

