*hello world*

#hey

##ho

====

###hello

-----

####hi

>Feature: Logging in and roles
In order to work with the quoting system
as a user of the system
I want to be able to log in

> > This is a nested blockquote

> Scenario: Signing in with correct credentials
>Given I am at the front page of the Quoting System
>When I click on the ‘Sign in with IS ID’ button
>And I am directed to the ‘Log In’ page
>And I enter my username
>And I enter my correct password
>And I select ‘Auth Provider’ as ‘Fake IS Staff’
>Then I should be logged in successfully
>And I should be on the main quoting page


	Scenario: Signing in with correct credentials
	Given I am at the front page of the Quoting System
	When I click on the ‘Sign in with IS ID’ button
	And I am directed to the ‘Log In’ page
	And I enter my username
	And I enter my correct password
	And I select ‘Auth Provider’ as ‘Fake IS Staff’
	Then I should be logged in successfully
	And I should be on the main quoting page


* 	Scenario: Signing in with correct credentials
*	Given I am at the front page of the Quoting System
	When I click on the ‘Sign in with IS ID’ button
	And I am directed to the ‘Log In’ page
	And I enter my username
	And I enter my correct password
	And I select ‘Auth Provider’ as ‘Fake IS Staff’
	Then I should be logged in successfully
	And I should be on the main quoting page



+ red
+ green 

*blue
*purple

-red
-blue

1. Bird
2. Bees
3. Dogs

3. happy
1. sad
8. mediocre