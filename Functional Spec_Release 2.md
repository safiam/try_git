#Functional Requirements for Release One 

A web based sales tool is required to enable the IS sales organisation to produce a quote in a standardised and consistent manner. 
Below is a list of the functional requirements for the first release of the project.

## Specs

#### 1. Feature: Create and configure a quote online 
In order to produce an accurate product
as an AM/BDC/PM
I want to be able to create a quote specific to my client’s needs

##### Scenario:
> Same as Feature 4 of Functional Spec R1

2. Create and configure a proposal online  

Rules: 
The proposal should consist of:
1.	a cover page
2.	a table of contents
3.	an executive summary
4.	a pricing table
5.	the quote itself

Executive summary should consist of:
1.	Salutations (standard format)
2.	Two editable fields – First field should just be a short message for the client (ie: ‘Thanks Jon for second meeting, here within is etc etc’). Second field should be the service/technical description. 
3.	Ability to insert an image in either field
4.	Sign off section (standard format)

1.2.1. Feature: Creating an executive summary
In order to produce an accurate product
as an AM/BDC
I want to be able to create a proposal specific to my client’s needs

     Scenario: Starting an executive summary
  Given I am on the ‘Home’ page
  When I have chosen a quote to edit from my ‘Saved Quotes’
  And I click on the ‘edit’ button
  Then I should be directed to the ‘Editing Quote #number’ page 

  Given I am on the ‘Editing Quote #number’ page
  And I have clicked on the ‘Enterprise Internet Access’ product in my                 ‘Basket’
  When I click on the ‘Create Executive Summary’ button
  Then a rich text editor should appear in the same screen  
  And I should be able to enter text in either field below ‘Salutations’

     Scenario: Inserting an image 
  Given I am in the ‘Executive Summary’ editor
  And I want to insert a diagram in the field
  When I have copied the diagram from my doc/other source
  And I press the ‘insert diagram’ button / or CTRL-V 
  Then the diagram should be inserted in the selected field 

Scenario: Saving an executive summary
  Given I am on the ‘Editing Quote #number’ page
  And I have successfully created the executive summary
  When I click the ‘Save Exec Summary’ button
 Then it should be saved and attached to the quote 

        Scenario: Printing the ‘proposal’
Given I am on the ‘Home’ page
And I click on the ‘View’ button of a ‘Finalized’ or ‘Accepted’ quote
And I see ‘Viewing Quote #number’ page
When I click the ‘Print’ dropdown
Then I should see a list reading ‘Proposal,’ ‘Additional Services letter,’ ‘Upgrade,’ and ‘Service Schedule.’

Given I have clicked the ‘Print’ dropdown on the ‘Viewing Quote #number’ page
When I click on ‘Proposal’
Then the quote content and executive summary should be displayed in a PDF viewer 
OR
Given I am on the ‘Home’ page
When I have chosen a ‘Finalized’ or ‘Accepted’ quote under my ‘Saved    quotes’
And I click the ‘print PDF’ button
Then the quote content and executive summary should be displayed in a PDF viewer 

     Scenario: View basket as a pricing table
Given I am on the ‘Home’ page
And I click on the ‘view’ button of a specific quote
And I see ‘Viewing Quote #number’ page
When I click the ‘View Basket as a Pricing Table’ button in my Basket
Then my ‘Basket’ contents should be converted to HTML format 
And I should be able to copy this information

