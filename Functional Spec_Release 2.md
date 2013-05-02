#Functional Requirements for Release Two 

A web based sales tool is required to enable the IS sales organisation to produce a quote in a standardised and consistent manner. 
Below is a list of the functional requirements for the first release of the project.

## Specs   

### 1. Create and configure a quote online    

> As per Feature 4.1 of Functional Spec R1   

### 2. Create and configure a proposal online     

#### 2.1. Feature: Creating an executive summary   
In order to produce an accurate product   
as an AM/BDC   
I want to be able to create a proposal specific to my client’s needs   

##### 2.1.1. Scenario: Starting an executive summary   
  
> Given I am on the ‘Home’ page   
> When I have chosen a quote to edit from my ‘Saved Quotes’   
> And I click on the ‘edit’ button   
> Then I should be directed to the ‘Editing Quote #number’ page    

> >  Given I am on the ‘Editing Quote #number’ page    
> >  And I have clicked on the ‘Enterprise Internet Access’ product in my ‘Basket’   
> >  When I click on the ‘Create Executive Summary’ button       
> >  Then a rich text editor should appear in the same screen     
> >  And I should see a non editable field of 'Salutations'    
> >  And I should see two editable text fields below this   
> >  And I should be able to enter text in either of these field   
  
##### 2.1.2 Scenario: Inserting an image    
> Given I am on the ‘Executive Summary’ editor       
> And I want to insert a diagram into the field   
> When I click on the 'Add diagram' button    
> And a File Select Dialog Box appears     
> And I select a file    
> Then the diagram should be attached to the quote          
> OR      
> Given I am on the ‘Executive Summary’ editor       
> And I want to insert a diagram into the field   
> When I have copied the diagram from my doc/other source         
> And I press the ‘Insert diagram’ button / or CTRL-V    
> Then the diagram should be inserted into the selected field         

##### 2.1.3. Scenario: Saving an executive summary   
> Given I am on the ‘Editing Quote #number’ page   
> And I have successfully edited the fields 
> When I click the ‘Save Exec Summary’ button   
> Then it should be saved and attached to the quote    

##### 2.1.4. Scenario: Printing the ‘proposal’   
> Given I am on the ‘Home’ page   
> And I click on the ‘View’ button of a ‘Finalized’ or ‘Accepted’ quote   
> And I see ‘Viewing Quote #number’ page   
> When I click the ‘Print’ dropdown   
> Then I should see a list reading ‘Proposal,’ ‘Additional Services letter,’ ‘Upgrade,’ and ‘Service Schedule.’   

> > Given I have clicked the ‘Print’ dropdown on the ‘Viewing Quote #number’ page    
> > When I click on ‘Proposal’   
> > Then the quote content and executive summary should be displayed in a PDF viewer   
> > OR   
> > Given I am on the ‘Home’ page   
> > When I have chosen a ‘Finalized’ or ‘Accepted’ quote under my ‘Saved quotes’   
> > And I click the ‘print PDF’ button   
> > Then the quote content and executive summary should be displayed in a PDF viewer    

##### 2.1.5. Scenario: View basket as a pricing table   
> Given I am on the ‘Home’ page   
> And I click on the ‘View’ button of a specific quote   
> And I am directed to the ‘Viewing Quote #number’ page   
> When I click the ‘View Basket as a Pricing Table’ button in my Basket   
> Then my ‘Basket’ contents should appear in HTML format   

##### 2.1.6. Scenario: Copying pricing table contents     
> Given I have clicked the ‘View Basket as a Pricing Table’ button in my Basket   my 'Basket'      
> And the contents appear in HTML format    
> When I highlight the required fields    
> And I click the 'copy' button    
> Then the highlighted fields should be copied   
> And I should be able to paste them    
> OR     
> Given  my 'Basket' contents are in HTML format        
> When I click the 'copy' button    
> Then the pricing table should be copied       
> And I should be able to paste them    

### 3. Discount Approvals

> As per Feature 5.1, 5.2 and 14.2 of Functional Spec R1   

### 4. Acceptance/Rejecting a quote    

#### 4.1. Feature: BDC accepting/rejecting the quote    
In order to progress the quote process   
as a BDC   
I want to be able to accept/reject a quote awaiting approval    

##### 4.1.1. Scenario: Accepting a quote   
> Given I am a BDC    
> And I am on the ‘Home’ page       
> And I click a quote under ‘Awaiting approval’   
> And I am directed to the ‘Viewing Quote #number’ page   
> And I am satisfied with the quote content   
> When I click the ‘Accept on behalf of client’ button   
> Then the quote status should change to ‘Accepted’   

##### 4.1.2. Scenario: Accepting a quote with a discount edit   
> Given I am a BDC    
> And I am viewing a quote configured by an AM   
> And I want to edit the discount the AM has applied   
> When I click the discount bar   
> Then the field should become editable    
> And I should be able to input a more suitable amount    

> > Given I have viewed the AM’s quote    
> > And I am satisfied with the end product   
> > When I click the ‘Accept on behalf of client’ button   
> > Then the quote status should change to ‘Accepted’    

##### 4.1.3. Scenario: Rejecting a quote   
> Given I am a BDC    
> And I am on the ‘Home’ page    
> And I click a quote under ‘Awaiting approval’   
> And I am directed to the ‘Viewing Quote #number’ page   
> And I do not approve the discount the AM has applied   
> When I click the ‘Reject’ button   
> Then the quote status should change to ‘Rejected’   

> > Given I have clicked the ‘Reject’ button	   
> > And a dialogue box appears   
> > And it reads, ‘Reason for rejecting this quote’   
> > When I type in the reason for reject   
> > And I click ‘Submit’   
> > Then the quote status should remain ‘Awaiting Approval’     

##### 4.1.4. Scenario: User receives the accepted/rejected notification    
> Given I am an AM   
> And I have submitted a quote for approval    
> When the BDC has accepted/rejected the quote   
> Then I should receive an email notifying me of this  

### 5. Sharing documents on Knowzone     

#### 5.1. Feature: Uploading documents to Knowzone    
> In order to share and increase knowledge of clients amongst IS users    
> as an AM/BDC    
> I want to be able to upload documents to the Knowzone    

##### 5.1.1. Scenario: Uploading a document onto Knowzone    
> Given I am on the ‘Home’ page    
> And I click on the ‘view’ button of a ‘Finalized’ or ‘Accepted’ quote    
> And I am directed to the ‘Viewing Quote #number’ page    
> And I click on a quote in my ‘Basket’     
> When I click the ‘Upload to KnowZone’ button    
> Then the document should be uploaded to the Client folder in Knowzone    
    
  
   
