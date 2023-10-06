# HMRC accessibility audit request
## Service name
[Template completion instruction — enter the name of the product, **website**, mobile app or digital service you want us to arrange an accessibility audit for.]
## About the service
### Description
[Template completion instruction — to help us understand your service use this section to give a description of your service and any other information you feel is important.]
### Component/shared service
[Template completion instruction — use this section to say whether this audit request is for a service that is called upon and used by other services in their full end to end journey, and it is not a service in its own right.  If it is not a service in its own right name the services that will be using it.]
### Third party involvement
[Template completion instruction — use this section to say whether a third party has been involved in the building or development of the service and/or third party software has been used.]
## Project details
### Business area
[Template completion instruction — use this section to give the name of the commissioning business area.]
### Delivery Centre
[Template completion instruction — use this section to give the Delivery Centre location where it is being built.]
### Project Clarity code
[Template completion instruction — use this section to give the Clarity code being used to charge time against.]
### Cost Centre
[Template completion instruction — use this section to give the cost centre to be used to charge the accessibility audit against. Needed should the audit be carried out by our external partners the Digital Accessibility Centre (DAC)]
## Service contacts
### Product Manager
[Template completion instruction — use this section to give the name of the Product Manager for this service.]
- Contact name:
- Contact phone number:
- Contact email address:

### Main contact for the accessibility audit
[Template completion instruction — use this section to give the main contact for this service and your audit request.]
- Contact name:
- Contact phone number:
- Contact email address:
### User journey contact
[Template completion instruction — use this section to give details of the person to be contacted if there are problems with the user journeys provided and who can reset data.]
- Contact name:
- Contact phone number:
- Contact email address:
### Names of people to invite to slack channel
When a service has its accessibility audit carried out within HMRC by the Digital Inclusion and Accessibility Standards team we will set up a dedicated slack channel to post details of the issues we find in real time. It is also an opportunity to engage with us about the issues and discuss solutions. 

[Template completion instruction — use this section to list the slack usernames and the role in the team of those you want us to invite when we set up the slack channel.  As a minimum you should list the UX, Content Designer, Dev and QA].
## GitHub details
[Template completion instruction — as well as regular contact information, please provide your team name for us to contact you on GitHub and receive updates on your audit. You can find this here: https://github.com/orgs/hmrc/teams.

In the example, The Really Great Team (TRGT) is working on the really-great-service-name-frontend service]
- GitHub team: @hmrc/trgt
- GitHub repository: /hmrc/really-great-service-name-frontend/
### A11y Jenkins job
[Template completion instruction — use this section to give details of the most recent run of the A11y Jenkins job, including a link to the snapshot of the report. Issues reported must be fixed prior to the audit beginning.]
## Timeline
[Template completion instruction — to help us plan and arrange the accessibility audit use this section to give details of any known dates or information about your project timetable. For example, when the service is entering public beta. As a minimum we need to know the following dates.]
- Move to private beta: [give date]
- Public beta release date: [give date]
- GDS public beta assessment date: [give date]
## Details to access the service and user journeys to be tested
[Template completion instruction — use this section to give details of the user journeys that will be used to test your service. There should rarely be a need for more than 8 journeys to be submitted from a service.

The aim of these audits is not to test every single page of your service, but all the major component types and patterns.  Some aspects, for example, functionality such as changing data on a ‘Check your answers’ page, or error messages we always test so you don’t need to supply user journeys or instructions specifically to test these aspects.

Your user journeys should be short enough that they hit all the right pages and avoid the need to visit the same pages repeatedly so the audit is not duplicating testing time and effort. 

For each user journey you must provide details of how to access the service, the step by step actions needed to complete the user journey together with the dummy data that needs to be entered.  The next section gives an example of what a well-presented user journey looks like.

Please be aware that when carrying out the audit there will be more than one user accessing the service at the same time and carrying out multiple iterations so ensure access accommodates this. If creds are consumable, you can't re-use them because it logs a change to the user, then enough creds should be supplied to complete each journey 12 times. More may be requested if necessary during the audit.]
### Journey 1: Example of a well-presented user journey
[Additional journey instructions
- accessing the service: **always** use staging, and only mention fields which are changed from their default values. If values should be exact, say so; if values within a range are okay, say so; otherwise, indicate any values which values need changing for multiple testers to test concurrently.
- for each page/step listed in the user journey, make it clear if
  - the page is part of shared service, where you don't have control over a particular page 
  - a subsequent journey results in a page being visited that is one that has been visited as part of a previous journey.  This will save time and effort testing the same page several times.  See journey 2 example in next section.]
### Instructions to access the service
- Connect to VPN
- Go to: [enter staging auth server url]
  - Enter details of credentials setup actions needed here
  - select ‘submit’
### Steps/instructions to test the service
1. Do you have a UK Unique Taxpayer Reference (UTR)?
   - a. Select ‘Yes’
   - b. select ‘Continue’
2. What type of business do you have?
   - a. Select ‘Limited company’
   - b. select ‘Continue’
3. What is your Corporation Tax Unique Taxpayer Reference?
   - a. Enter: 1234567890
   - b. select ‘Continue’
4. What is the registered name of your business?
   - a. Enter: Business
   - b. select ‘Continue’
5. Is this your business?
   - a. Select ‘Yes’
   - b. select ‘Continue’
6. Who should we contact if we have any questions about your disclosures?
   - a. enter name: Mary Jones
   - b. select ‘Continue’
7. What is Mary Jones’s email address?
   - a. Enter: test@gmail.com
   - b. select ‘Continue’
8. Does Mary Jones have a telephone number?
   - a. Select ‘Yes’
   - b. select ‘Continue’
9. What is Mary Jones’s telephone number?
   - a. Enter: 07777777777
   - b. select ‘Continue’
10. Is there someone else we can contact if Mary Jones is not available?
    - a. Select ‘Yes’
    - b. select ‘Continue’
11. What is the name of the individual or team we should contact?
    - a. Enter: DAC6 Team
    - b. select ‘Continue’
12. What is the email address for DAC6 Team?
    - a. Enter: test@gmail.com
    - b. select ‘Continue’

13. Does DAC6 Team have a telephone number?
    - a. Select ‘Yes’
    - b. select ‘Continue’
14. What is the telephone number for DAC6 Team?
    - a. Enter: 07888888888
    - b.select ‘Continue’
15. Check your answers before you register
    - a. select ‘Confirm and send’
16. Registration successful
17. End of journey
### Journey 2: Another example of a well-presented user journey

**Instructions to access the service**
   - Connect to VPN
   - Go to: [enter staging auth server url]
     - Enter details of credentials setup actions needed here
     - select ‘submit’

**Steps/instructions to test the service**
1. Do you have a UK Unique Taxpayer Reference (UTR)? [page tested at step 1 in journey 1]
   - a. Select ‘No’
   - b. select ‘Continue’
2. What are you registering as?
   - a. Select ‘An individual’
   - b. select ‘Continue’
3. Do you have a National Insurance number?
   - a. Select ‘No’
   - b. .select ‘Continue’
4. What is your name?
    - a. enter Given name: Jim
    - b. enter Family name: Smith
    - c. select ‘Continue’
5. What is your date of birth?
    - a. Enter: 01-02-1985
    - b. select ‘Continue’
6. Do you live in the United Kingdom?
    - a. Select ‘No’
    - b. select ‘Continue’
7. What is your home address?
    - a. enter Address line 1: 11 High Street
    - b. enter City: City
    - c. select Country ‘Andorra’
    - d. select ‘Continue’
8. What is your email address?
    - a. Enter: test@gmail.com
    - b. select ‘Continue’
9. Do you have a telephone number?
    - a. Select ‘Yes’
    - b. select ‘Continue’
10. What is your telephone number?
    - a. Enter: 07777777777
    - b. select ‘Continue’
11. Check your answers before you register
    - a. Select ‘Confirm and send’
12. Registration successful 
13. End of journey

On completion please email this completed audit request to accessibility.team@hmrc.gov.uk
