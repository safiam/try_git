#Functional Requirements for the PM   

##Specs

### 1. User login with AD details    

#### 1.1. Feature: Logging in and roles      
> In order to work with the quoting system in a sandbox environment      
> as a user of the system      
> I want to be able to log in      

##### 1.1.1. Scenario: Signing in with correct credentials      
> Given I am at the front page of Alphabet      
> When I click on the ‘Sign in with IS ID’ button      
> And I am directed to the ‘Log In’ page      
> And I enter my username      
> And I enter my correct password      
> And I select ‘IS Staff’      
> Then I should be logged in successfully     

##### 1.1.2. Scenario: Signing in as a PM      
> Given my name is ‘PM name’      
> When I log in successfully      
> Then my username drop-down ‘Roles’ list should contain ‘PM’      

> Given I have logged in as a PM      
> And I am on the ‘Home’ page      
> When I look under ‘My Quotes’       
> Then I should see a message which reads, ‘Product x is waiting to be activated’      

### 2. Status for product
#### 2.1. Feature: Product status ribbons      
> In order to keep track of product stages     
> as a user      
> I want its state displayed as a colour-coded ribbon      

##### 2.1.1. Scenario: Viewing product 'Pending' status       
> Given I am on the ‘New quote' page      
> When I have clicked on a product to configure     
> Then the status should be displayed as a mustard ribbon     
> And it should read ‘Pending’      

##### 2.1.2. Scenario: Viewing product 'Activate' status       
> Given I am on the ‘New Quote’ page  
> And I have configured and saved a product    
> When the product is ready to go live       
> Then the status should be displayed as a blue-grey ribbon    
> And it should read ‘Activate’      

### 3. Creating and configuring a product

#### 3.1. Feature: Product configuration      
> In order to produce an accurate product      
> as a PM      
> I want to be able to create a product specific to my client’s needs      

##### 3.1.1. Scenario: Selecting a product           
> Given I have already launched a product in Tribold      
> And I am on the ‘New Quote’ page of Alphabet      
> When I look under ‘Product List’      
> Then I should see ‘Product x’ under ‘My Products’      

##### 3.1.2. Scenario: Configuring a product       
> Given I am on the ‘New quote’ page      
> When I click on the ‘Configure Product x’ link      
> Then I should see the header ‘Configuring Product x’      
> And it should be displayed in the same screen      

##### 3.1.3. Scenario: Configuring a product      
> *Refer to Feature 4.1 of Functional Spec for R1     

##### 3.1.4. Scenario: Saving a product      
> Given I have successfully completed the product configuration      
> When I click ‘Save Product’       
> Then ‘Product x’ should appear in ‘My Basket’       

> Some rules to consider: 
> PM should be able to save the product as a quote, and calculate discounts etc. on the quote
> PM should be able to do everything which a user can do in Alphabet.
> Anything done in this mode should only be visible to the PM. No other user can see the test quotes he saves.  

### 4. Product go live   

### 4.1. Feature: Activating a new product 
> In order to allow users accessibility to a product
> as a Product Manager
> I want to be able to activate a product in Alphabet 

##### 4.1.1. Scenario: Activating a product      
> Given ‘Product x’ is successfully configured and saved      
> And I am on the ‘New Quote’ page      
> Then I should see a button which reads ‘Activate’      

----

> Given ‘Product x’ is successfully configured and saved      
> When I click the ‘Activate’ button      
> And a message box should appear which reads, ‘There are ‘x’ amount of quotes associated with this product. Activation will result in the cancellation of these quotes. Do you wish to proceed?’      
> And I click the ‘Yes’ button      
> Then ‘Product x’ should go live      
> And should be made available to BDC’s and AM’s       

##### 4.1.2. Scenario: Deleting a product      
> Given ‘Product x’ is successfully configured and saved      
> And I am on the ‘New Quote’ page      
> When I look under ‘Totals’       
> Then I should see a ‘Cancel’ button       

----

> Given ‘Product x’ is successfully configured and saved      
> When I click the ‘Cancel’ button      
> Then the product should be deleted       

###5. Notifications of 'Product x '

#### 5.1. Feature: Notifications of ‘Product x’       
> In order to       
> as a user      
> I want to be notified of new products      

##### 5.1.1. Scenario: Notification of product activation      
> Given I am a PM		
> When I have successfully activated ‘Product x’      
> Then I should receive an email detailing this       

##### 5.1.2. Scenario: Notification a new product is available      
> Given I am a BDC/AM	      
> When the new/updated product is made available by a PM      
> Then I should receive an email detailing this      

##### 5.1.3. Scenario: Notification of cancelled quotes      
> Given I am a BDC/AM      
> And I had quotes associated to the updated product       
> When the updated product goes live      
> Then I should receive an email detailing the cancelled quotes            

#### Feature : Updating a product
