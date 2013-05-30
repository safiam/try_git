#Deal functionality      

##Specs     

### 1. Tranforming into a deal     

#### 1.1. Feature: Tranforming quoting scenarios into a deal      
In order to present the client with quote options
as a user
I want to be able to collate individual quotes into a bundle/deal

##### 1.1.1. Scenario: Logging in to Alphabet             
> See Functional Spec 1, Feature 1.1.          

##### 1.1.2. Scenario: Viewing the 'Transform into a deal' button    
> Given I have logged in to Alphabet         
> And I click on the 'New Quote' page     
> And I am on the 'New Quote' page      
> When I look at my basket          
> Then there should be a button above which reads, 'Transform into a deal.'       

##### 1.1.3. Scenario: Getting information on what a deal is      
> Given I am on the 'New Quote' page      
> When I hover over the 'i' button      
> Then a message should appear which provides information of what a deal is 
> And on the consequence of clicking the 'Transform' button        

##### 1.1.4. Scenario: Transforming quoting scenarios into a deal       
> Given I am on the 'New Quote' page         
> When I click on the 'Transform into a deal' button      
> Then there should be a message box which reads, 'What would you like to name your first basket?'     
> And I should be able to type in the name of my basket     

> Given I have named my Basket     
> When I click the 'Create deal' button in the message box     
> Then the deal has been created      
> And it cannot be undone      

##### 1.1.4. Scenario: Cancelling a deal before creating it
> Given I have clicked on the 'Transform into a deal' button  
> And a message box appears asking me to name the basket    
> When I click the 'cancel' button in the message box
> Then the deal should be cancelled      
> And I should be returned to the new quote page         

##### 1.1.5. Scenario: Viewing the 'Deals' page         
> Given I have created a deal        
> When I am on the 'New Quote' page      
> Then the 'transform' button should no longer be on this page        
> And it should be replaced with a label which reads, 'Deal for Client x'        
> Given I have created a deal        
> When I am on the 'New quote' page           
> Then I should see a tab created under the player box             
> And it should read as the basket name does         

> Given I have created a deal    
> When I am on the 'New quote' page            
> Then I should a 'plus' button on the right of my tabs bar     
       
##### 1.1.6. Scenario: Adding a new scenario to the deal        
> Given I am on the 'New quote' page         
> When I click on the 'plus' button      
> Then there should be a message box which reads, 'Choose a name for your basket'    
     
> Given I have clicked the 'plus' button        
> And there is a message box which reads, 'Choose a name for your basket'      
> When I enter a name for my basket        
> And I click the 'Create' button in the message box          
> Then a new tab should be created      
> And it should read as the name of my new basket      



