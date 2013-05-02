#Functional Requirements for Release One 

A web based sales tool is required to enable the IS sales organisation to produce a quote in a standardised and consistent manner. 
Below is a list of the functional requirements for the first release of the project.

## Scope

Create a quote for the EIA product for a new client online   

## Specs

### 1. User login with AD details   

#### 1.1. Feature: Logging in and roles  
In order to work with the quoting system  
as a user of the system  
I want to be able to log in  

##### 1.1.1. Scenario: Signing in with correct credentials  
> Given I am at the front page of the Quoting System  
> When I click on the ‘Sign in with IS ID’ button   
> And I am directed to the ‘Log In’ page  
> And I enter my username  
> And I enter my correct password  
> And I select ‘Auth Provider’ as ‘Fake IS Staff’  
> Then I should be logged in successfully  
> And I should be on the main quoting page  

##### 1.1.2. Scenario: Signing in as a BDC  
> Given my name is ‘Paul Nixon’  
> When I log in successfully  
> Then my username drop-down ‘Roles’ list should contain ‘BDC’  

##### 1.1.3. Scenario: Signing in as an AM  
> Given my name is ‘Viksha Rajcoomar’  
> When I log in successfully  
> Then my username drop-down ‘Roles’ list should contain ‘AM’  

##### 1.1.4. Scenario: Signing in as an IPM  
> Given my name is ‘Alison Mack’  
> When I log in successfully  
> Then my username drop-down ‘Roles’ list should contain ‘IPM’  

### 2. User avatars

#### 2.1. Feature: Avatars  
In order to increase UX for configuring products in a quote  
as an AM, BDC or IPM  
I want to see avatars of all the role players  

##### 2.1.1. Scenario: BDC’s avatar  
> Given my role is an ‘AM’  
> And I’ve logged in successfully  
> When I click on ‘New quote’ link  
> And then I click on the ‘Add BDC’ link  
> Then I should see a drop down of available BDCs
  
> >  Given there are a list of BDC’s to select  
> >  When I select ‘Paul Nixon’  
> >  And click ‘OK’  
> >  Then I should see an avatar of ‘Paul Nixon’    

##### 2.1.2. Scenario: AM’s avatar  
> Given my role is a ‘BDC’  
> And I’ve logged in successfully  
> When I click on ‘New quote’ link  
> And then I click on the ‘Add AM’ link  
> Then I should see a drop down of available AMs  

> > Given there are a list of AM’s to select  
> > When I select ‘Viksha Rajcoomar’  
> > And click ‘OK’  
> > Then I should see an avatar of ‘Viksha Rajcoomar’     

> > > Given I am an AM (x)  
> > > And there is a quote (q) owned by AM (y)  
> > > When I click on a link to view quote (q)  
> > > Then AM (y) must still be the AM of that quote  
> > > And AM (x) should not be the AM  

##### 2.1.3. Scenario: IPM’s avatar  
> Given my role is an ‘AM’  
> And I’ve logged in successfully  
> When I click on ‘New quote’ link  
> And then I click on the ‘Add IPM’ link  
> Then I should see a drop down of available IPMs  

> > Given there are a list of IPM’s to select  
> > When I select ‘Alison Mack’  
> > And click ‘OK’  
> > Then I should see an avatar of ‘Alison Mack’     

### 3. Status for quotes  

#### 3.1.Feature: Quote status ribbons  
In order to keep track of the quote stages  
as a user  
I want its state displayed as a colour-coded ribbon  

##### 3.1.1. Scenario: Viewing quote status from ‘Home’  
> Given I am on the ‘Home’ page  
> When I look at the status column  
> Then the status bar should display the current phase of the quote  

##### 3.1.2. Scenario: Viewing quote status in Draft   
> Given I am on the ‘Home’ page  
> When the quote has been configured   
> And it has not been Finalised  
> Then the status should be displayed as a blue-grey bar  
> And it should read ‘Draft’  

##### 3.1.3. Scenario: Viewing quote status in Template   
> Given I am on the ‘Home’ page   
> And I have selected a template to configure/view  
> Then the status should be displayed as a blue bar  
> And it should read ‘Template’  

##### 3.1.4. Scenario: Viewing quote status when Awaiting Approval  
> Given I am on the ‘Home’ page  
> And the quote is awaiting approval from the BDC  
> Then the status should be displayed as a mustard bar  
> And it should read ‘Awaiting Approval’  

##### 3.1.5. Scenario: Viewing quote status when Finalized  
> Given I am on the ‘Home’ page  
> And the quote is client ready  
> Then the status should be displayed as a dark blue bar  
> And it should read ‘Finalized’  

##### 3.1.6. Scenario: Viewing quote status when Accepted  
> Given I am on the ‘Home’ page   
> And the client has signed off on the quote  
> Then the status should be displayed as a green bar  
> And it should read ‘Accepted’  

##### 3.1.7. Scenario: Viewing quote status when Loaded  
> Given I am on the ‘Home’ page   
> And the IPM has successfully loaded the product data into Siebel  
> Then the status should be displayed as a black bar  
> And it should read ‘Loaded’  


### 4. Create and configure a quote online  

#### 4.1. Feature: Creating a quote  
In order to produce an accurate product  
as an AM/BDC  
I want to be able to create a quote specific to my client’s needs  

##### 4.1.1. Scenario: Starting a quote  
> Given I am on the Home page  
> When I click the ‘New Quote’ link  
> Then I should be redirected to the ‘New quote’ page  
> And I should see a product list  
> And the product list should have ‘Enterprise Internet Access’   

##### 4.1.2. Scenario: Adding a client to the quote   
> Given I am on the ‘New quote’ page   
> When I click on the ‘Add client’ link in the player box  
> Then a dialog box should appear  
> And this contains a ‘Client’s name’ field   
 
##### 4.1.3. Scenario: Adding a new client to the quote   
> Given I am on the ‘New quote’ page  
> And I click on the ‘Add client’ link in the player box    
> And a dialog box appears   
> When I type the client’s name in the field  
> Then I should see the client added to the player box  


##### 4.1.4. Scenario: Adding an existing client to the quote  
> Given I am on the ‘New quote’ page  
> And I click on the ‘Add client’ link in the player box  
> And a dialog box appears   
> When I start typing in a client name into the field  
> And the field autocompletes the name  
> And a dropdown of existing clients are listed  
> And I select a specific client  
> And I click ‘OK’  
> Then I should see that client added to the player box  
  
##### 4.1.5. Scenario: Configuring a quote (Step 0)    
> Given I am on the ‘New quote’ page  
> When I click on the ‘Configure Enterprise Internet Access’ link  
> Then I should see the header ‘Configuring Enterprise Internet Access’ 	
> And it should be displayed on the same screen  

##### 4.1.6. Scenario: Configuring EIA (Step 1)  
> Given I am configuring ‘Enterprise Internet Access’  
> And ‘Step 1’ is highlighted  
> And I fill in ‘Site’ with ‘my site’  
> And I select ‘Contract Term’ as ‘1 year’  
> And I select ‘Node’ as ‘JHB-BRY’  
> And I select ‘Business Case’ as ‘New’  
> When I click ‘Next Step’  
> Then ‘Step 2’ is highlighted  

##### 4.1.7. Scenario: Configuring EIA (Step 2)  
> Given I am configuring ‘Enterprise Internet Access’  
> And  ‘Step 2’ is highlighted  
> And I select ‘Granular Stats Type’ as ‘7 Day Pro’  
> When I click ‘Next Step’  
> Then ‘Step 3’ is highlighted  

##### 4.1.8. Scenario: Configuring EIA (Step 3 – Local Bandwidth Branch)  
> Given I am configuring ‘Enterprise Internet Access’  
> And ‘Step 3’ is highlighted  
> And I select ‘Internet Type’ as ‘Local Bandwidth’  
> And I select ‘Access Billing Option’ as ‘Access-Local Bandwidth on Demand’  
> And I select ‘Bandwidth’ as ‘256’  
> And I select ‘Type’ as Usage  
> And I select ‘Variable Rate’ as ‘1’  
> And I select ‘Base Percentage Rate’ as ‘1’  
> And I select ‘Base Rate’ as ‘1’  
> When I click ‘Next Step’  
> Then ‘Step 4’ is highlighted   

##### 4.1.9. Scenario: Configuring EIA (Step 3 – International Branch)   
> Given I am configuring ‘Enterprise Internet Access’  
> And ‘Step 3’ is highlighted  
> And I select ‘Internet Type’ as ‘International’	  
> And I select ‘International’ as ‘Optimum’   
> And I select ‘Optimum Bandwidth’ as ‘256’  
> And I select ‘Local Bandwidth’ as '256'   
> And I select ‘Access Billing Option’ as ‘Access-Local Bandwidth on Demand’  
> And I select ‘Type’ as Usage  
> And I select ‘Variable Rate’ as ‘1’  
> And I select ‘Base Percentage Rate’ as ‘1’  
> And I select ‘Base Rate’ as ‘1’  
> When I click ‘Next Step’  
> Then ‘Step 4’ is highlighted   

##### 4.10. Scenario: Configuring EIA (Step 4)   
> Given I am configuring ‘Enterprise Internet Access’  
> And ‘Step 4’ is highlighted     
> And I select ‘Access Type’ as ‘Pure Internet’  
> And I select ‘Connection Medium’ ‘Backup Connection’ as ‘Winet’  
> And I select ‘Port Size’ as ‘256’    
> And I select  ‘Internet Handoff’ as ‘Fibre’  
> And I select ‘Fibre’ as ‘Cisco 892F’  
> And I select ‘Maintenance’ as ‘IS 3’  
> And I select  ‘Internet Handoff’ under ‘Primary Connection’ as ‘Copper’  
> And I select  ‘Fibre’ as ‘Cisco 2901-2 WIC-2CT (IPBase)’  
> And  I select ‘Maintenance’ as ‘IS 3’  
> When I click on ‘Save Product’  
> Then it will appear in my ‘Basket’     

##### 4.11. Scenario: Saving a quote    
> Given I have saved the product   
> And it appears in my ‘Basket’   
> And I click on the product in my Basket      
> And the product configuration process opens up in the same screen  
> When I click on the ‘Save Quote’ button   
> Then the quote will be saved  

 
### 5. Applying a discount for a quote  

#### 5.1. Feature: Applying Simple Discounts  
In order to simplify the quote process  
as a AM  
I want to be able to request Simple Discounts on quotes    


##### 5.1.1. Scenario: Configuring Enterprise Internet Access with a discount    
> Given I am an AM   
> And I am configuring ‘Enterprise Internet Access’  
> And any step is highlighted  
> When I click the grayed out ‘% Discount’ bar  
> Then the discount field becomes enabled  
> And I should be able to input a discount percentage below 10%  

> > Given I am an AM   
> > And I have saved the quote  
> > When I click the product in my ‘Basket’  
> > And the product configuration is displayed in the same screen      
> > And I click the grayed out ‘Target Total’ bar  
> > And the ‘Total Recurring Charge’ value is displayed   
> > And I type in an amount less than 10% of the charge value   
> > And I click ‘Save Product’  
> > Then the discount will appear as a percentage value for the product  

> > > Given I am an AM  
> > > When I have added a discount to the quote   
> > > And I have saved the quote  
> > > And I click on the ‘Submit for approval’ button  
> > > Then an email will be sent to the BDC requesting approval   

##### 5.2. Feature: Applying Simple Discounts  
In order to simplify the quote process  
as a BDC  
I want to be able to apply Simple Discounts on quotes  

##### 5.2.1. Scenario: Configuring Enterprise Internet Access with a discount   
> Given I am an BDC  
> And I am configuring ‘Enterprise Internet Access’  
> And any step is highlighted  
> When I click the grayed out ‘% Discount’ bar  
> Then the discount field becomes enabled  
> And I should be able to input a discount percentage below 10%  

> >  Given I am an BDC  
> > And I have saved the quote  
> > When I click the product in my ‘Basket’  
> > And the product configuration is displayed in the same screen  
> > And I click the grayed out ‘Target Total’ bar  
> > And the ‘Total Recurring Charge’ value is displayed   
> > And I type in an amount less than 10% of the charge value   
> > And I click ‘Save Product’  
> > Then the discount will appear as a percentage value for the product  

### 6. Items in my Basket   

#### 6.1. Feature: Basket items  
In order to keep track of my products  
as an AM/BDC  
I want to be able to view and store these in my basket  

##### 6.1.1. Scenario: Viewing my basket   
> Given I am on the ‘New quote’ page  
> And I haven’t selected a product or template yet  
> Then my ‘Basket’ should read ‘No items added yet’  

##### 6.1.2. Scenario: Adding a product to the basket  
> Given I am on the ‘New quote’ page  
> And my ‘Basket’ reads ‘No items added yet’  
> When I click on the ‘Configure Enterprise Internet Access’ link  
> Then my ‘Basket’ should read ‘No items added yet’  

##### 6.1.3. Scenario: Viewing saved basket items      
> Given I am on the ‘New Quote’ page  
> When I have successfully configured the Enterprise Internet Access product  
> And I have saved the product  
> Then my ‘Basket’ should read ‘Enterprise Internet Access’  

##### 6.1.4. Scenario: Cancelling a product  
> Given I am on the ‘New Quote’ page’  
> And I have successfully configured the ‘Enterprise Internet Access’ product   
> And it appears in my ‘Basket’   
> When I click the ‘Cancel’ button  
> Then the product should be removed  
> And my ‘Basket’ should read ‘No items added yet’  
> And I should be redirected back to the ‘Home’ page  


### 7. Auto populate pricing  

#### 7.1. Feature: Pricing matrices  
In order to correctly price products  
as a user of the system  
I require it to support complex pricing matrices  

##### 7.1.1. Scenario: Calculating a product  
> Given the product has already been saved  
> When I click on the product in my Basket  
> And the product configuration process opens up in the same screen  
> And I click on the ‘Save Quote’ button   
> Then I should see a ‘Total Non Recurring Charge’ of ‘Rx’  
> And I should see a ‘Total Recurring charge’ of ‘Rx’  

### 8. Viewing existing quotes created using the Quoting tool  
    
#### 8.1. Feature: Viewing quotes  
In order to better understand existing quotes  
as an AM or BDC  
I want to be able to view quotes  

##### 8.1.1. Scenario: Viewing a quote  
> Given I am on the ‘Home’ page  
> When I have chosen a quote to view from my ‘Saved Quotes’  
> And I click the ‘View’ button   
> Then I should directed to the ‘Viewing Quote #number’ page  

> > Given I am on the ‘Viewing Quote #number’ page  
> > When I click ‘Enterprise Internet Access’ from my ‘Basket’  
> > Then I should see ‘Configure Enterprise Internet Access’   
> > And I should see the product breakdown   
> > And I should not be allowed to change any items or discount in this view  
	
> > > Given I am on the ‘Viewing Quote #number’ page   
> > > And I have completed viewing the quote  
> > > When I click ‘Done Viewing’  
> > > Then I should be redirected back to the ‘Home’ page  

##### 8.1.2. Scenario: Exporting a quote to PDF  
> Given I am on the ‘Home’ page  
> When I have chosen a specific quote under my ‘Saved quotes’  
> And I click the ‘print PDF’ button  
> Then the quote data should be displayed to me in a PDF viewer   


### 9. Revising a quote within the tool   

#### 9.1. Feature: Revising a quote  
In order to better serve a customer's changing requirements  
as an AM or BDC  
I want to be able to edit quotes  

##### 9.1.1. Scenario: Editing a quote  
> Given I am on the ‘Home’ page  
> When I have chosen a quote to edit from my ‘Saved Quotes’  
> And I click on the ‘edit’ button  
> Then I should be directed to the ‘Editing Quote #number’ page   

> > Given I am on the ‘Editing Quote #number’ page  
> > When I click on the ‘Enterprise Internet Access’ product in my Basket  
> > Then I should see the product configuration process  
> > And I should be able to edit the product items   

### 10. Search for existing quotes  

#### 10.1. Feature: Search functionality  
In order to narrow down the quote listing  
as a AM/BDC  
I want to be able to search for specific quotes  

##### 10.1.1. Scenario: Searching for a quote  
> Given I am on the ‘Home’ page   
> And I scroll down to the end of ‘Saved quotes’  
> And I see ‘Search Quotes by Quote number’   
> When I enter the quote number in the ‘Search’ field  
> And I click ‘Search’  
> Then I should see a list of the filtered quotes   

> > Given I am on the ‘Home’ page  
> > And I see the ‘Filter field’ just below the ‘Saved Quotes’ header  
> > And I have chosen a specific attribute of the quote to filter  
> > When I enter this into the ‘Filter’ field    
> > Then I should see a list of those quotes  
	

### 11. Filtering quotes based on clients  

#### 11.1. Feature: Refining the quote listing  
In order to avoid quoting the wrong client  
as an AM/BDC  
I want a well filtered list of clients  

##### 11.1.1. Scenario: Filtering quotes  
> Given I am on the ‘Home’ page  
> And I scroll down to ‘My Clients’  
> When I enter an existing client name into the ‘Filter’ field   
> Then I should see the list of clients displayed  


### 12. Copy product details on quote to clipboard  

#### 12.1. Feature: Copy quote data  
In order to process an accepted quote  
as a IPM  
I want all relevant data in an easy-to-use format ready to be loaded into Siebel  

##### 12.1.1. Scenario: Viewing the quote  
> Given I am an IPM  
> And I am on the ‘Home’ page  
> When I click the ‘View’ button of the ‘Quote #number’  
> Then I should directed to the ‘Viewing Quote #number’ page  

##### 12.1.2. Scenario: Copying data to Siebel    
> Given I am an IPM  
> And I am on the ‘Viewing Quote #number’ page  
> And I click ‘Enterprise Internet Access’ from my ‘Basket’  
> And I see ‘Viewing Enterprise Internet Access’ in the same screen       
> And I see the product breakdown  
> When I click on the ‘Enable Click to Copy’ button   
> Then I should see a ‘copy paper’ button appear next to each product item   
> And this should be the case for each step of the process  

> > Given I have clicked the ‘Click to Copy’ button   
> > And I see a ‘copy paper’ button appear next to each product item   
> > When I click the button next to the item  
> > Then this data should be copied into my clipboard  
> > And this should be allowed to be pasted into Siebel  
> > And this process applies to all the product items required to be copied  

##### 12.1.3. Scenario: Disabling Click to Copy  
> Given I am an IPM  
> When I want to disable the copy functionality  
> And I click ‘Disable Click to Copy’  
> Then the ‘copy paper’ button displayed next to each item should disappear  

### 13. Create and configure a template online  

#### 13.1. Feature: Templates  
In order to allow AM's to quote as efficiently as possible  
as a BDC  
I want to be able to craft templated quotes for reuse   

##### 13.1.1. Scenario: Starting a template  
> Given I am on the Home page  
> When I click the ‘New Template’ link  
> Then I should be redirected to the ‘New Template’ page  
> And I should see a product list  
> And the product list should have ‘Enterprise Internet Access’  

##### 13.1.2. Scenario: Configuring a template (Step 0)  
> Given I am on the ‘New Template’ page  
> When I click on the ‘Configure Enterprise Internet Access’ link  
> Then I should see ‘Configuring Enterprise Internet Access’  
> And this should be on the same screen   

##### 13.1.3. Scenario: Locking an item in the template  
> Given I am configuring ‘Enterprise Internet Access’   
> And ‘Step 1’ is highlighted  
> And I want the a product item to be fixed  
> When I click on the ‘lock’ button next to the dropdown  
> Then this item becomes locked  
> And an AM using this template should not be able to change this  
> And this process should be applied to the other product items in the template  

##### 13.1.4. Scenario: Configuring EIA (Step 1)  
> Given I am configuring ‘Enterprise Internet Access’  
> And ‘Step 1’ is highlighted  
> And I fill in ‘Site’ with ‘my site’  
> And I select ‘Contract Term’ as ‘1 year’  
> And I select ‘Node’ as ‘JHB-BRY’  
> And I select ‘Business Case’ as ‘New’  
> When I click ‘Next Step’  
> Then ‘Step 2’ is highlighted  

##### 13.1.5. Scenario: Configuring EIA (Step 2)  
> Given I am configuring ‘Enterprise Internet Access’  
> And ‘Step 2’ is highlighted  
> And I select ‘Granular Stats Type’ as ‘7 Day Pro’  
> When I click ‘Next Step’  
> Then ‘Step 3’ is highlighted  

##### 13.1.6. Scenario: Configuring EIA (Step 3 – Local Bandwidth Branch)  
> Given I am configuring ‘Enterprise Internet Access’    
> And ‘Step 3’ is highlighted  
> And I select ‘Internet Type’ as ‘Local Bandwidth’  
> And I select ‘Access Billing Option’ as ‘Access-Local Bandwidth on Demand’  
> And I select ‘Bandwidth’ as ‘256’  
> And I select ‘Type’ as Usage  
> And I select ‘Variable Rate’ as ‘1’  
> And I select ‘Base Percentage Rate’ as ‘1’  
> And I select ‘Base Rate’ as ‘1’  
> When I click ‘Next Step’  
> Then ‘Step 4’ is highlighted   

##### 13.1.7. Scenario: Configuring EIA (Step 3 – International Branch)   
> Given I am configuring ‘Enterprise Internet Access’  
> And ‘Step 3’ is highlighted  
> And I select ‘Internet Type’ as ‘International’	  
> And I select ‘International’ as ‘Optimum’   
> And I select ‘Optimum Bandwidth’ as ‘256’  
> And I select ‘Local Bandwidth’ as '256'  
> And I select ‘Access Billing Option’ as ‘Access-Local Bandwidth on Demand’  
> And I select ‘Type’ as Usage  
> And I select ‘Variable Rate’ as ‘1’  
> And I select ‘Base Percentage Rate’ as ‘1’  
> And I select ‘Base Rate’ as ‘1’  
> When I click ‘Next Step’  
> Then ‘Step 4’ is highlighted   

##### 13.1.8. Scenario: Configuring EIA (Step 4)   
> Given I am configuring ‘Enterprise Internet Access’  
> And ‘Step 4’ is highlighted   
> And I select ‘Access Type’ as ‘Pure Internet’  
> And I select ‘Connection Medium’ ‘Backup Connection’ as ‘Winet’  
> And I select ‘Port Size’ as ‘256’  
> And I select  ‘Internet Handoff’ as ‘Fibre’  
> And I select ‘Fibre’ as ‘Cisco 892F’  
> And I select ‘Maintenance’ as ‘IS 3’  
> And I select  ‘Internet Handoff’ under ‘Primary Connection’ as ‘Copper’  
> And I select  ‘Fibre’ as ‘Cisco 2901-2 WIC-2CT (IPBase)’  
> And  I select ‘Maintenance’ as ‘IS 3’  
> When I click on ‘Save Product’  
> Then the product should be saved to my Basket    

##### 13.1.9. Scenario: Adding a product to the basket  
> Given I am on the ‘New Template’ page  
> And my ‘Basket’ reads ‘No items added yet’  
> When I have successfully completed the configuring “Enterprise Internet Access” > And I have saved the product  
> Then my ‘Basket’ should only have “Enterprise Internet Access” in it  

##### 13.1.10. Scenario: Saving a template  
> Given I have successfully configured the ‘Enterprise Internet Access’ product  > And the product has been saved to my Basket  
> When I click on ‘Save template’   
> Then a dialog box should appear asking me to provide details for the template  

> > Given I have clicked on ‘Save template’  
> > And a dialog box appears containing fields for ‘Template Name’ and ‘Description’   
> > And a Yes/No option for where discounts are preapproved  
> > When I enter a Template name and description  
> > And I select Yes/No option for discounts   
> And I click ‘Save this Template’  
> > And  a message box appears stating that ‘Your template has been saved successfully’  
> > And I click 'OK' 
> > Then the template should appear under my product list   
	
#### 13.2. Feature: Configure a template online  
In order to quote as efficiently as possible  
as an AM  
I want to be able to use preconfigured templated quotes that BDC’s have produced  

##### 13.2.1. Scenario: Starting a template  
> Given I am on the Home page  
> When I click the ‘New Quote’ link  
> Then I should be redirected to the ‘New Quote’ page  
> And I should see a product list  
> And the product list should have ‘Enterprise Internet Access’  

##### 13.2.2. Scenario: Adding a product to the basket  
> Given I am on the ‘New Template’ page  
> And my ‘Basket’ reads ‘No items added yet’  
> When I click on the ‘Configure Enterprise Internet Access’ link  
> Then my ‘Basket’ should only have “Enterprise Internet Access” in it  

##### 13.2.3. Scenario: Configuring a quote   
> Given I am on the ‘New Template’ page  
> When I click on the ‘Configure Enterprise Internet Access’ link  
> Then I should see ‘Configuring Enterprise Internet Access’  

##### 13.2.4. Scenario: Configuring a template with locked items  
> Given I am configuring ‘Enterprise Internet Access’  
> And ‘Step One’ is highlighted  
> And I want to edit the ‘Contract Term’  
> And the product item has a ‘locked’ symbol  
> When I hover over this item  
> Then a ‘no’ symbol should appear  
> And I should not be allowed to click this dropdown   
> And this should apply to any other ‘locked’ product items    

##### 13.2.5. Scenario: Configuring a template with unlocked items    
> Given I am configuring ‘Enterprise Internet Access’  
> And I want to configure a product item   
> And the dropdown button has an unlocked symbol    
> When I click the dropdown button    
> Then I should be able to select a different product item     


### 14. Notifications of quote updates    

#### 14.1. Feature: Notification of accepted quotes    
In order to progress the quote process    
as an IPM
I want to be notified of accepted quotes    

##### 14.1.1. Scenario: Receiving a notification of an accepted quote  
> Given I am an IPM     
> When a quote has been accepted by the client    
> Then I should receive an email detailing the Client and the number of the accepted quote   

> > Given I am logged in as an IPM   
> > And a quote has been accepted by the client  
> > When I receive an email detailing the accepted quote  
> > And I click on the ‘Quote Number’ link  
> > Then the quote should load in the tool  
> > And I should see the ‘Viewing Quote #number’ page  

#### 14.2. Feature: Notification of quotes awaiting approval   
In order to progress the quote process  
as a BDC  
I want to be notified of quotes awaiting my approval   

##### 14.2.1. Scenario: Receiving a notification of quotes awaiting approval 
> Given I am a BDC    
> And an AM has configured a quote   
> And has sent the quote for approval   
> When I am on my ‘Home’ page   
> And I look under ‘My Quotes’  
> Then I should see the quote under ‘Awaiting Approval’ 
 
> > Given I am an BDC    
> > When a quote has been configured by an AM    
> > Then I should receive an email detailing the quote awaiting apprval    