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
<<<<<<< HEAD
> When I click on the ‘Sign in with IS ID’ button   
> And I am directed to the ‘Log In’ page  
=======
> When I click on the ï¿½Sign in with IS IDï¿½ button  
> And I am directed to the ï¿½Log Inï¿½ page  
>>>>>>> 90b76d751d6998de32fc0a9e1347d509511cb519
> And I enter my username  
> And I enter my correct password  
> And I select ï¿½Auth Providerï¿½ as ï¿½Fake IS Staffï¿½  
> Then I should be logged in successfully  
> And I should be on the main quoting page  

##### 1.1.2. Scenario: Signing in as a BDC  
> Given my name is ï¿½Paul Nixonï¿½  
> When I log in successfully  
> Then my username drop-down ï¿½Rolesï¿½ list should contain ï¿½BDCï¿½  

##### 1.1.3. Scenario: Signing in as an AM  
> Given my name is ï¿½Viksha Rajcoomarï¿½  
> When I log in successfully  
> Then my username drop-down ï¿½Rolesï¿½ list should contain ï¿½AMï¿½  

##### 1.1.4. Scenario: Signing in as an IPM  
> Given my name is ï¿½Alison Mackï¿½  
> When I log in successfully  
> Then my username drop-down ï¿½Rolesï¿½ list should contain ï¿½IPMï¿½  

### 2. User avatars

#### 2.1. Feature: Avatars  
In order to increase UX for configuring products in a quote  
as an AM, BDC or IPM  
I want to see avatars of all the role players  

##### 2.1.1. Scenario: BDCï¿½s avatar  
> Given my role is an ï¿½AMï¿½  
> And Iï¿½ve logged in successfully  
> When I click on ï¿½New quoteï¿½ link  
> And then I click on the ï¿½Add BDCï¿½ link  
> Then I should see a drop down of available BDCs
  
> >  Given there are a list of BDCï¿½s to select  
> >  When I select ï¿½Paul Nixonï¿½  
> >  And click ï¿½OKï¿½  
> >  Then I should see an avatar of ï¿½Paul Nixonï¿½    

##### 2.1.2. Scenario: AMï¿½s avatar  
> Given my role is a ï¿½BDCï¿½  
> And Iï¿½ve logged in successfully  
> When I click on ï¿½New quoteï¿½ link  
> And then I click on the ï¿½Add AMï¿½ link  
> Then I should see a drop down of available AMs  

> > Given there are a list of AMï¿½s to select  
> > When I select ï¿½Viksha Rajcoomarï¿½  
> > And click ï¿½OKï¿½  
> > Then I should see an avatar of ï¿½Viksha Rajcoomarï¿½     

> > > Given I am an AM (x)  
> > > And there is a quote (q) owned by AM (y)  
> > > When I click on a link to view quote (q)  
> > > Then AM (y) must still be the AM of that quote  
> > > And AM (x) should not be the AM  

##### 2.1.3. Scenario: IPMï¿½s avatar  
> Given my role is an ï¿½AMï¿½  
> And Iï¿½ve logged in successfully  
> When I click on ï¿½New quoteï¿½ link  
> And then I click on the ï¿½Add IPMï¿½ link  
> Then I should see a drop down of available IPMs  

> > Given there are a list of IPMï¿½s to select  
> > When I select ï¿½Alison Mackï¿½  
> > And click ï¿½OKï¿½  
> > Then I should see an avatar of ï¿½Alison Mackï¿½     

### 3. Status for quotes  

#### 3.1.Feature: Quote status ribbons  
In order to keep track of the quote stages  
as a user  
I want its state displayed as a colour-coded ribbon  

##### 3.1.1. Scenario: Viewing quote status from ï¿½Homeï¿½  
> Given I am on the ï¿½Homeï¿½ page  
> When I look at the status column  
> Then the status bar should display the current phase of the quote  

##### 3.1.2. Scenario: Viewing quote status in Draft   
> Given I am on the ï¿½Homeï¿½ page  
> When the quote has been configured   
> And it has not been Finalised  
> Then the status should be displayed as a blue-grey bar  
> And it should read ï¿½Draftï¿½  

##### 3.1.3. Scenario: Viewing quote status in Template   
> Given I am on the ï¿½Homeï¿½ page   
> And I have selected a template to configure/view  
> Then the status should be displayed as a blue bar  
> And it should read ï¿½Templateï¿½  

##### 3.1.4. Scenario: Viewing quote status when Awaiting Approval  
> Given I am on the ï¿½Homeï¿½ page  
> And the quote is awaiting approval from the BDC  
> Then the status should be displayed as a mustard bar  
> And it should read ï¿½Awaiting Approvalï¿½  

##### 3.1.5. Scenario: Viewing quote status when Finalized  
> Given I am on the ï¿½Homeï¿½ page  
> And the quote is client ready  
> Then the status should be displayed as a dark blue bar  
> And it should read ï¿½Finalizedï¿½  

##### 3.1.6. Scenario: Viewing quote status when Accepted  
> Given I am on the ï¿½Homeï¿½ page   
> And the client has signed off on the quote  
> Then the status should be displayed as a green bar  
> And it should read ï¿½Acceptedï¿½  

##### 3.1.7. Scenario: Viewing quote status when Loaded  
> Given I am on the ï¿½Homeï¿½ page   
> And the IPM has successfully loaded the product data into Siebel  
> Then the status should be displayed as a black bar  
> And it should read ï¿½Loadedï¿½  


### 4. Create and configure a quote online  

#### 4.1. Feature: Creating a quote  
In order to produce an accurate product  
as an AM/BDC  
I want to be able to create a quote specific to my clientï¿½s needs  

##### 4.1.1. Scenario: Starting a quote  
> Given I am on the Home page  
> When I click the ï¿½New Quoteï¿½ link  
> Then I should be redirected to the ï¿½New quoteï¿½ page  
> And I should see a product list  
> And the product list should have ï¿½Enterprise Internet Accessï¿½   

##### 4.1.2. Scenario: Adding a client to the quote   
> Given I am on the ï¿½New quoteï¿½ page   
> When I click on the ï¿½Add clientï¿½ link in the player box  
> Then a dialog box should appear  
> And this contains a ï¿½Clientï¿½s nameï¿½ field   
 
##### 4.1.3. Scenario: Adding a new client to the quote   
> Given I am on the ï¿½New quoteï¿½ page  
> And I click on the ï¿½Add clientï¿½ link in the player box    
> And a dialog box appears   
> When I type the clientï¿½s name in the field  
> Then I should see the client added to the player box  


##### 4.1.4. Scenario: Adding an existing client to the quote  
> Given I am on the ï¿½New quoteï¿½ page  
> And I click on the ï¿½Add clientï¿½ link in the player box  
> And a dialog box appears   
> When I start typing in a client name into the field  
> And the field autocompletes the name  
> And a dropdown of existing clients are listed  
> And I select a specific client  
> And I click ï¿½OKï¿½  
> Then I should see that client added to the player box  
  
##### 4.1.5. Scenario: Configuring a quote (Step 0)    
> Given I am on the ï¿½New quoteï¿½ page  
> When I click on the ï¿½Configure Enterprise Internet Accessï¿½ link  
> Then I should see the header ï¿½Configuring Enterprise Internet Accessï¿½ 	
> And it should be displayed on the same screen  

##### 4.1.6. Scenario: Configuring EIA (Step 1)  
> Given I am configuring ï¿½Enterprise Internet Accessï¿½  
> And ï¿½Step 1ï¿½ is highlighted  
> And I fill in ï¿½Siteï¿½ with ï¿½my siteï¿½  
> And I select ï¿½Contract Termï¿½ as ï¿½1 yearï¿½  
> And I select ï¿½Nodeï¿½ as ï¿½JHB-BRYï¿½  
> And I select ï¿½Business Caseï¿½ as ï¿½Newï¿½  
> When I click ï¿½Next Stepï¿½  
> Then ï¿½Step 2ï¿½ is highlighted  

##### 4.1.7. Scenario: Configuring EIA (Step 2)  
> Given I am configuring ï¿½Enterprise Internet Accessï¿½  
> And  ï¿½Step 2ï¿½ is highlighted  
> And I select ï¿½Granular Stats Typeï¿½ as ï¿½7 Day Proï¿½  
> When I click ï¿½Next Stepï¿½  
> Then ï¿½Step 3ï¿½ is highlighted  

##### 4.1.8. Scenario: Configuring EIA (Step 3 ï¿½ Local Bandwidth Branch)  
> Given I am configuring ï¿½Enterprise Internet Accessï¿½  
> And ï¿½Step 3ï¿½ is highlighted  
> And I select ï¿½Internet Typeï¿½ as ï¿½Local Bandwidthï¿½  
> And I select ï¿½Access Billing Optionï¿½ as ï¿½Access-Local Bandwidth on Demandï¿½  
> And I select ï¿½Bandwidthï¿½ as ï¿½256ï¿½  
> And I select ï¿½Typeï¿½ as Usage  
> And I select ï¿½Variable Rateï¿½ as ï¿½1ï¿½  
> And I select ï¿½Base Percentage Rateï¿½ as ï¿½1ï¿½  
> And I select ï¿½Base Rateï¿½ as ï¿½1ï¿½  
> When I click ï¿½Next Stepï¿½  
> Then ï¿½Step 4ï¿½ is highlighted   

##### 4.1.9. Scenario: Configuring EIA (Step 3 ï¿½ International Branch)   
> Given I am configuring ï¿½Enterprise Internet Accessï¿½  
> And ï¿½Step 3ï¿½ is highlighted  
> And I select ï¿½Internet Typeï¿½ as ï¿½Internationalï¿½	  
> And I select ï¿½Internationalï¿½ as ï¿½Optimumï¿½   
> And I select ï¿½Optimum Bandwidthï¿½ as ï¿½256ï¿½  
> And I select ï¿½Local Bandwidthï¿½ as '256'   
> And I select ï¿½Access Billing Optionï¿½ as ï¿½Access-Local Bandwidth on Demandï¿½  
> And I select ï¿½Typeï¿½ as Usage  
> And I select ï¿½Variable Rateï¿½ as ï¿½1ï¿½  
> And I select ï¿½Base Percentage Rateï¿½ as ï¿½1ï¿½  
> And I select ï¿½Base Rateï¿½ as ï¿½1ï¿½  
> When I click ï¿½Next Stepï¿½  
> Then ï¿½Step 4ï¿½ is highlighted   

##### 4.10. Scenario: Configuring EIA (Step 4)   
> Given I am configuring ï¿½Enterprise Internet Accessï¿½  
> And ï¿½Step 4ï¿½ is highlighted     
> And I select ï¿½Access Typeï¿½ as ï¿½Pure Internetï¿½  
> And I select ï¿½Connection Mediumï¿½ ï¿½Backup Connectionï¿½ as ï¿½Winetï¿½  
> And I select ï¿½Port Sizeï¿½ as ï¿½256ï¿½    
> And I select  ï¿½Internet Handoffï¿½ as ï¿½Fibreï¿½  
> And I select ï¿½Fibreï¿½ as ï¿½Cisco 892Fï¿½  
> And I select ï¿½Maintenanceï¿½ as ï¿½IS 3ï¿½  
> And I select  ï¿½Internet Handoffï¿½ under ï¿½Primary Connectionï¿½ as ï¿½Copperï¿½  
> And I select  ï¿½Fibreï¿½ as ï¿½Cisco 2901-2 WIC-2CT (IPBase)ï¿½  
> And  I select ï¿½Maintenanceï¿½ as ï¿½IS 3ï¿½  
> When I click on ï¿½Save Productï¿½  
> Then it will appear in my ï¿½Basketï¿½     

##### 4.11. Scenario: Saving a quote    
> Given I have saved the product   
> And it appears in my ï¿½Basketï¿½   
> And I click on the product in my Basket      
> And the product configuration process opens up in the same screen  
> When I click on the ï¿½Save Quoteï¿½ button   
> Then the quote will be saved  

	

 
### 5. Applying a discount for a quote  

#### 5.1. Feature: Applying Simple Discounts  
In order to simplify the quote process  
as a AM  
I want to be able to request Simple Discounts on quotes    


##### 5.1.1. Scenario: Configuring Enterprise Internet Access with a discount    
> Given I am an AM   
> And I am configuring ï¿½Enterprise Internet Accessï¿½  
> And any step is highlighted  
> When I click the grayed out ï¿½% Discountï¿½ bar  
> Then the discount field becomes enabled  
> And I should be able to input a discount percentage below 10%  

> > Given I am an AM   
> > And I have saved the quote  
> > When I click the product in my ï¿½Basketï¿½  
> > And the product configuration is displayed in the same screen      
> > And I click the grayed out ï¿½Target Totalï¿½ bar  
> > And the ï¿½Total Recurring Chargeï¿½ value is displayed   
> > And I type in an amount less than 10% of the charge value   
> > And I click ï¿½Save Productï¿½  
> > Then the discount will appear as a percentage value for the product  

> > > Given I am an AM  
> > > When I have added a discount to the quote   
> > > And I have saved the quote  
> > > And I click on the ï¿½Submit for approvalï¿½ button  
> > > Then an email will be sent to the BDC requesting approval   

##### 5.2. Feature: Applying Simple Discounts  
In order to simplify the quote process  
as a BDC  
I want to be able to apply Simple Discounts on quotes  

##### 5.2.1. Scenario: Configuring Enterprise Internet Access with a discount   
> Given I am an BDC  
> And I am configuring ï¿½Enterprise Internet Accessï¿½  
> And any step is highlighted  
> When I click the grayed out ï¿½% Discountï¿½ bar  
> Then the discount field becomes enabled  
> And I should be able to input a discount percentage below 10%  

> >  Given I am an BDC  
> > And I have saved the quote  
> > When I click the product in my ï¿½Basketï¿½  
> > And the product configuration is displayed in the same screen  
> > And I click the grayed out ï¿½Target Totalï¿½ bar  
> > And the ï¿½Total Recurring Chargeï¿½ value is displayed   
> > And I type in an amount less than 10% of the charge value   
> > And I click ï¿½Save Productï¿½  
> > Then the discount will appear as a percentage value for the product  

### 6. Items in my Basket   

#### 6.1. Feature: Basket items  
In order to keep track of my products  
as an AM/BDC  
I want to be able to view and store these in my basket  

##### 6.1.1. Scenario: Viewing my basket   
> Given I am on the ï¿½New quoteï¿½ page  
> And I havenï¿½t selected a product or template yet  
> Then my ï¿½Basketï¿½ should read ï¿½No items added yetï¿½  

##### 6.1.2. Scenario: Adding a product to the basket  
> Given I am on the ï¿½New quoteï¿½ page  
> And my ï¿½Basketï¿½ reads ï¿½No items added yetï¿½  
> When I click on the ï¿½Configure Enterprise Internet Accessï¿½ link  
> Then my ï¿½Basketï¿½ should read ï¿½No items added yetï¿½  

##### 6.1.3. Scenario: Viewing saved basket items      
> Given I am on the ï¿½New Quoteï¿½ page  
> When I have successfully configured the Enterprise Internet Access product  
> And I have saved the product  
> Then my ï¿½Basketï¿½ should read ï¿½Enterprise Internet Accessï¿½  

##### 6.1.4. Scenario: Cancelling a product  
> Given I am on the ï¿½New Quoteï¿½ pageï¿½  
> And I have successfully configured the ï¿½Enterprise Internet Accessï¿½ product   
> And it appears in my ï¿½Basketï¿½   
> When I click the ï¿½Cancelï¿½ button  
> Then the product should be removed  
> And my ï¿½Basketï¿½ should read ï¿½No items added yetï¿½  
> And I should be redirected back to the ï¿½Homeï¿½ page  


### 7. Auto populate pricing  

#### 7.1. Feature: Pricing matrices  
In order to correctly price products  
as a user of the system  
I require it to support complex pricing matrices  

##### 7.1.1. Scenario: Calculating a product  
> Given the product has already been saved  
> When I click on the product in my Basket  
> And the product configuration process opens up in the same screen  
> And I click on the ï¿½Save Quoteï¿½ button   
> Then I should see a ï¿½Total Non Recurring Chargeï¿½ of ï¿½Rxï¿½  
> And I should see a ï¿½Total Recurring chargeï¿½ of ï¿½Rxï¿½  

### 8. Viewing existing quotes created using the Quoting tool  
    
#### 8.1. Feature: Viewing quotes  
In order to better understand existing quotes  
as an AM or BDC  
I want to be able to view quotes  

##### 8.1.1. Scenario: Viewing a quote  
> Given I am on the ï¿½Homeï¿½ page  
> When I have chosen a quote to view from my ï¿½Saved Quotesï¿½  
> And I click the ï¿½Viewï¿½ button   
> Then I should directed to the ï¿½Viewing Quote #numberï¿½ page  

> > Given I am on the ï¿½Viewing Quote #numberï¿½ page  
> > When I click ï¿½Enterprise Internet Accessï¿½ from my ï¿½Basketï¿½  
> > Then I should see ï¿½Configure Enterprise Internet Accessï¿½   
> > And I should see the product breakdown   
> > And I should not be allowed to change any items or discount in this view  
	
> > > Given I am on the ï¿½Viewing Quote #numberï¿½ page   
> > > And I have completed viewing the quote  
> > > When I click ï¿½Done Viewingï¿½  
> > > Then I should be redirected back to the ï¿½Homeï¿½ page  

##### 8.1.2. Scenario: Exporting a quote to PDF  
> Given I am on the ï¿½Homeï¿½ page  
> When I have chosen a specific quote under my ï¿½Saved quotesï¿½  
> And I click the ï¿½print PDFï¿½ button  
> Then the quote data should be displayed to me in a PDF viewer   


### 9. Revising a quote within the tool   

#### 9.1. Feature: Revising a quote  
In order to better serve a customer's changing requirements  
as an AM or BDC  
I want to be able to edit quotes  

##### 9.1.1. Scenario: Editing a quote  
> Given I am on the ï¿½Homeï¿½ page  
> When I have chosen a quote to edit from my ï¿½Saved Quotesï¿½  
> And I click on the ï¿½editï¿½ button  
> Then I should be directed to the ï¿½Editing Quote #numberï¿½ page   

> > Given I am on the ï¿½Editing Quote #numberï¿½ page  
> > When I click on the ï¿½Enterprise Internet Accessï¿½ product in my Basket  
> > Then I should see the product configuration process  
> > And I should be able to edit the product items   

### 10. Search for existing quotes  

#### 10.1. Feature: Search functionality  
In order to narrow down the quote listing  
as a AM/BDC  
I want to be able to search for specific quotes  

##### 10.1.1. Scenario: Searching for a quote  
> Given I am on the ï¿½Homeï¿½ page   
> And I scroll down to the end of ï¿½Saved quotesï¿½  
> And I see ï¿½Search Quotes by Quote numberï¿½   
> When I enter the quote number in the ï¿½Searchï¿½ field  
> And I click ï¿½Searchï¿½  
> Then I should see a list of the filtered quotes   

> > Given I am on the ï¿½Homeï¿½ page  
> > And I see the ï¿½Filter fieldï¿½ just below the ï¿½Saved Quotesï¿½ header  
> > And I have chosen a specific attribute of the quote to filter  
> > When I enter this into the ï¿½Filterï¿½ field    
> > Then I should see a list of those quotes  
	

### 11. Filtering quotes based on clients  

#### 11.1. Feature: Refining the quote listing  
In order to avoid quoting the wrong client  
as an AM/BDC  
I want a well filtered list of clients  

##### 11.1.1. Scenario: Filtering quotes  
> Given I am on the ï¿½Homeï¿½ page  
> And I scroll down to ï¿½My Clientsï¿½  
> When I enter an existing client name into the ï¿½Filterï¿½ field   
> Then I should see the list of clients displayed  


### 12. Copy product details on quote to clipboard  

#### 12.1. Feature: Copy quote data  
In order to process an accepted quote  
as a IPM  
I want all relevant data in an easy-to-use format ready to be loaded into Siebel  

##### 12.1.1. Scenario: Viewing the quote  
> Given I am an IPM  
> And I am on the ï¿½Homeï¿½ page  
> When I click the ï¿½Viewï¿½ button of the ï¿½Quote #numberï¿½  
> Then I should directed to the ï¿½Viewing Quote #numberï¿½ page  

##### 12.1.2. Scenario: Copying data to Siebel    
> Given I am an IPM  
> And I am on the ï¿½Viewing Quote #numberï¿½ page  
> And I click ï¿½Enterprise Internet Accessï¿½ from my ï¿½Basketï¿½  
> And I see ï¿½Viewing Enterprise Internet Accessï¿½ in the same screen       
> And I see the product breakdown  
> When I click on the ï¿½Enable Click to Copyï¿½ button   
> Then I should see a ï¿½copy paperï¿½ button appear next to each product item   
> And this should be the case for each step of the process  

> > Given I have clicked the ï¿½Click to Copyï¿½ button   
> > And I see a ï¿½copy paperï¿½ button appear next to each product item   
> > When I click the button next to the item  
> > Then this data should be copied into my clipboard  
> > And this should be allowed to be pasted into Siebel  
> > And this process applies to all the product items required to be copied  

##### 12.1.3. Scenario: Disabling Click to Copy  
> Given I am an IPM  
> When I want to disable the copy functionality  
> And I click ï¿½Disable Click to Copyï¿½  
> Then the ï¿½copy paperï¿½ button displayed next to each item should disappear  

### 13. Create and configure a template online  

#### 13.1. Feature: Templates  
In order to allow AM's to quote as efficiently as possible  
as a BDC  
I want to be able to craft templated quotes for reuse   

##### 13.1.1. Scenario: Starting a template  
> Given I am on the Home page  
> When I click the ï¿½New Templateï¿½ link  
> Then I should be redirected to the ï¿½New Templateï¿½ page  
> And I should see a product list  
> And the product list should have ï¿½Enterprise Internet Accessï¿½  

##### 13.1.2. Scenario: Configuring a template (Step 0)  
> Given I am on the ï¿½New Templateï¿½ page  
> When I click on the ï¿½Configure Enterprise Internet Accessï¿½ link  
> Then I should see ï¿½Configuring Enterprise Internet Accessï¿½  
> And this should be on the same screen   

##### 13.1.3. Scenario: Locking an item in the template  
> Given I am configuring ï¿½Enterprise Internet Accessï¿½   
> And ï¿½Step 1ï¿½ is highlighted  
> And I want the a product item to be fixed  
> When I click on the ï¿½lockï¿½ button next to the dropdown  
> Then this item becomes locked  
> And an AM using this template should not be able to change this  
> And this process should be applied to the other product items in the template  

##### 13.1.4. Scenario: Configuring EIA (Step 1)  
> Given I am configuring ï¿½Enterprise Internet Accessï¿½  
> And ï¿½Step 1ï¿½ is highlighted  
> And I fill in ï¿½Siteï¿½ with ï¿½my siteï¿½  
> And I select ï¿½Contract Termï¿½ as ï¿½1 yearï¿½  
> And I select ï¿½Nodeï¿½ as ï¿½JHB-BRYï¿½  
> And I select ï¿½Business Caseï¿½ as ï¿½Newï¿½  
> When I click ï¿½Next Stepï¿½  
> Then ï¿½Step 2ï¿½ is highlighted  

##### 13.1.5. Scenario: Configuring EIA (Step 2)  
> Given I am configuring ï¿½Enterprise Internet Accessï¿½  
> And ï¿½Step 2ï¿½ is highlighted  
> And I select ï¿½Granular Stats Typeï¿½ as ï¿½7 Day Proï¿½  
> When I click ï¿½Next Stepï¿½  
> Then ï¿½Step 3ï¿½ is highlighted  

##### 13.1.6. Scenario: Configuring EIA (Step 3 ï¿½ Local Bandwidth Branch)  
> Given I am configuring ï¿½Enterprise Internet Accessï¿½    
> And ï¿½Step 3ï¿½ is highlighted  
> And I select ï¿½Internet Typeï¿½ as ï¿½Local Bandwidthï¿½  
> And I select ï¿½Access Billing Optionï¿½ as ï¿½Access-Local Bandwidth on Demandï¿½  
> And I select ï¿½Bandwidthï¿½ as ï¿½256ï¿½  
> And I select ï¿½Typeï¿½ as Usage  
> And I select ï¿½Variable Rateï¿½ as ï¿½1ï¿½  
> And I select ï¿½Base Percentage Rateï¿½ as ï¿½1ï¿½  
> And I select ï¿½Base Rateï¿½ as ï¿½1ï¿½  
> When I click ï¿½Next Stepï¿½  
> Then ï¿½Step 4ï¿½ is highlighted   

##### 13.1.7. Scenario: Configuring EIA (Step 3 ï¿½ International Branch)   
> Given I am configuring ï¿½Enterprise Internet Accessï¿½  
> And ï¿½Step 3ï¿½ is highlighted  
> And I select ï¿½Internet Typeï¿½ as ï¿½Internationalï¿½	  
> And I select ï¿½Internationalï¿½ as ï¿½Optimumï¿½   
> And I select ï¿½Optimum Bandwidthï¿½ as ï¿½256ï¿½  
> And I select ï¿½Local Bandwidthï¿½ as '256'  
> And I select ï¿½Access Billing Optionï¿½ as ï¿½Access-Local Bandwidth on Demandï¿½  
> And I select ï¿½Typeï¿½ as Usage  
> And I select ï¿½Variable Rateï¿½ as ï¿½1ï¿½  
> And I select ï¿½Base Percentage Rateï¿½ as ï¿½1ï¿½  
> And I select ï¿½Base Rateï¿½ as ï¿½1ï¿½  
> When I click ï¿½Next Stepï¿½  
> Then ï¿½Step 4ï¿½ is highlighted   

##### 13.1.8. Scenario: Configuring EIA (Step 4)   
> Given I am configuring ï¿½Enterprise Internet Accessï¿½  
> And ï¿½Step 4ï¿½ is highlighted   
> And I select ï¿½Access Typeï¿½ as ï¿½Pure Internetï¿½  
> And I select ï¿½Connection Mediumï¿½ ï¿½Backup Connectionï¿½ as ï¿½Winetï¿½  
> And I select ï¿½Port Sizeï¿½ as ï¿½256ï¿½  
> And I select  ï¿½Internet Handoffï¿½ as ï¿½Fibreï¿½  
> And I select ï¿½Fibreï¿½ as ï¿½Cisco 892Fï¿½  
> And I select ï¿½Maintenanceï¿½ as ï¿½IS 3ï¿½  
> And I select  ï¿½Internet Handoffï¿½ under ï¿½Primary Connectionï¿½ as ï¿½Copperï¿½  
> And I select  ï¿½Fibreï¿½ as ï¿½Cisco 2901-2 WIC-2CT (IPBase)ï¿½  
> And  I select ï¿½Maintenanceï¿½ as ï¿½IS 3ï¿½  
> When I click on ï¿½Save Productï¿½  
> Then the product should be saved to my Basket    

##### 13.1.9. Scenario: Adding a product to the basket  
> Given I am on the ï¿½New Templateï¿½ page  
> And my ï¿½Basketï¿½ reads ï¿½No items added yetï¿½  
> When I have successfully completed the configuring ï¿½Enterprise Internet Accessï¿½ > And I have saved the product  
> Then my ï¿½Basketï¿½ should only have ï¿½Enterprise Internet Accessï¿½ in it  

##### 13.1.10. Scenario: Saving a template  
> Given I have successfully configured the ï¿½Enterprise Internet Accessï¿½ product  > And the product has been saved to my Basket  
> When I click on ï¿½Save templateï¿½   
> Then a dialog box should appear asking me to provide details for the template  

> > Given I have clicked on ï¿½Save templateï¿½  
> > And a dialog box appears containing fields for ï¿½Template Nameï¿½ and ï¿½Descriptionï¿½   
> > And a Yes/No option for where discounts are preapproved  
> > When I enter a Template name and description  
> > And I select Yes/No option for discounts   
> And I click ï¿½Save this Templateï¿½  
> > And  a message box appears stating that ï¿½Your template has been saved successfullyï¿½  
> > And I click 'OK' 
> > Then the template should appear under my product list   
	
#### 13.2. Feature: Configure a template online  
In order to quote as efficiently as possible  
as an AM  
I want to be able to use preconfigured templated quotes that BDCï¿½s have produced  

##### 13.2.1. Scenario: Starting a template  
> Given I am on the Home page  
> When I click the ï¿½New Quoteï¿½ link  
> Then I should be redirected to the ï¿½New Quoteï¿½ page  
> And I should see a product list  
> And the product list should have ï¿½Enterprise Internet Accessï¿½  

##### 13.2.2. Scenario: Adding a product to the basket  
> Given I am on the ï¿½New Templateï¿½ page  
> And my ï¿½Basketï¿½ reads ï¿½No items added yetï¿½  
> When I click on the ï¿½Configure Enterprise Internet Accessï¿½ link  
> Then my ï¿½Basketï¿½ should only have ï¿½Enterprise Internet Accessï¿½ in it  

##### 13.2.3. Scenario: Configuring a quote   
> Given I am on the ï¿½New Templateï¿½ page  
> When I click on the ï¿½Configure Enterprise Internet Accessï¿½ link  
> Then I should see ï¿½Configuring Enterprise Internet Accessï¿½  

##### 13.2.4. Scenario: Configuring a template with locked items  
> Given I am configuring ï¿½Enterprise Internet Accessï¿½  
> And ï¿½Step Oneï¿½ is highlighted  
> And I want to edit the ï¿½Contract Termï¿½  
> And the product item has a ï¿½lockedï¿½ symbol  
> When I hover over this item  
> Then a ï¿½noï¿½ symbol should appear  
> And I should not be allowed to click this dropdown   
> And this should apply to any other ï¿½lockedï¿½ product items    

##### 13.2.5. Scenario: Configuring a template with unlocked items    
> Given I am configuring ï¿½Enterprise Internet Accessï¿½  
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
> > And I click on the ï¿½Quote Numberï¿½ link  
> > Then the quote should load in the tool  
> > And I should see the ï¿½Viewing Quote #numberï¿½ page  

#### 14.2. Feature: Notification of quotes awaiting approval   
In order to progress the quote process  
as a BDC  
I want to be notified of quotes awaiting my approval   

##### 14.2.1. Scenario: Receiving a notification of quotes awaiting approval 
> Given I am a BDC    
> And an AM has configured a quote   
> And has sent the quote for approval   
> When I am on my ï¿½Homeï¿½ page   
> And I look under ï¿½My Quotesï¿½  
> Then I should see the quote under ï¿½Awaiting Approvalï¿½ 
 
> > Given I am an BDC    
> > When a quote has been configured by an AM    
> > Then I should receive an email detailing the quote awaiting apprval    
