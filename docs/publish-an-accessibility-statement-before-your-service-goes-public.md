# Publish an accessibility statement before your service goes into public beta

To comply with [public sector accessibility regulations](https://confluence.tools.tax.service.gov.uk/display/DISC/Regulations+to+make+public+sector+websites+and+mobile+applications+accessible) your service (this includes websites and mobile applications) must meet Web Content Accessibility Guidelines (WCAG) 2.1 AA standards and publish an accessibility statement before going into public beta. 

A new accessibility statement service is now available in GitHub for creating and publishing your accessibility statements (www.github.com/hmrc/accessibility-statement-frontend). You do not need any coding experience, you just need to be familiar with GitHub as it involves creating YAML files and using pull requests as part of the process. 

This new service replaces the current Herokuapp templates for external services only. For internal facing services you must continue to use the Herokuapp templates.

## About the new accessibility statement service 

The accessibility statement service is a centralised set of templates that contain all the ‘legal’ wording needed for each of the different types of the statement; fully compliant statement; partially compliant statement and non-compliant statement. The templates are available in English and Welsh. This text has been set by GDS who are the regulatory body and it cannot be changed. Service teams now need to only focus on content specific to their service. 

The benefit of having centrally held templates:

- They can be updated centrally when changes are needed, rather than individually. This will save time and resource, and will ensure the latest wording is always used. It also keeps maintenance overheads to a minimum.
- Statements will be held in a central public repository for all to see and will provide data to report compliance activity on accessibility issues and fix dates. The open repository also provides wider view access to stakeholders such as GDS without the need for GG access for auditing purposes. 
- Allows everyone to see all our published statements creating a resource to help others complete their statements. It is a further step to help us build consistency.

## Accessing the accessibility statement service 

You must have a [GitHub account linked to the HMRC organisation](https://confluence.tools.tax.service.gov.uk/display/DTRG/HMRC+on+GitHub).  

To access the service front-end use this link: https://github.com/hmrc/accessibility-statement-frontend

Guidance on how to use the service: 

https://github.com/hmrc/accessibility-statement-frontend#to-add-your-services-accessibility-statement

## Creating your statement

To help you create your statement new templates have been created. 

### External service 

New templates have been produced to help create statement content. This will avoid confusion between what content is part of the accessibility statement service and what service teams have to provide. 

These templates replace the previous Herokuapp templates. 

[Fully compliant statement](https://docs.google.com/document/d/1ooO9o1Awc8xEsSTcijGncHgKPm0nhWiX0y0qiFR_cls/edit?usp=sharing) 

[Partially compliant statement - audit taken place](https://docs.google.com/document/d/1UZUTlsjypuZCtq6BP41kv_hW5l8WYg_a3J95TrsZhhs/edit?usp=sharing)

[Partially compliant statement - automated tool testing](https://docs.google.com/document/d/1mGda0ERoUSGWfm5qzaQxKCdvkOo75CnOtsT6jGuMZ4o/edit?usp=sharing)  

[Non-compliant statement](https://docs.google.com/document/d/1TyGLhG29Zw18fTlDIYbQJKWaavjLVjkqRDLl_dqmwfI/edit?usp=sharing) 

### Internal service

ou should continue to use the Herokuapp templates.

They can be accessed at: https://accessibility-statement.herokuapp.com/

User name: accessibilitystatement
Password: hmrca11ystatement
Only text in the square brackets within the statement templates can be changed. Do not change any other wording. 

The format of the URL for the statement should be: https://www.tax.service.gov.uk/accessibility-statement/service-name

## Linking the accessibility statement to your service 

Your accessibility statement must appear in the footer of your service and be accessed through a link that says ‘Accessibility statement’. 

## Welsh language

The statement service has Welsh templates built into the service for the legal text of the statement. Service teams will need to arrange for the translation of the service-specific content and a final QA of the complete statement before publishing. 

 **Note**: for statements for the 23 September 2020 accessibility regulations deadline it has been agreed with the Welsh Language Unit that the final QA check can be done after the deadline. 

To arrange a translation, email: [translations.welshlanguage@hmrc.gov.uk](translations.welshlanguage@hmrc.gov.uk) 

An internal facing service does not need to publish a Welsh language version of an accessibility statement.

## Deskpro and reporting an accessibility problem

To enable users to report accessibility problems with your service, a Deskpro form has been created in the contact-frontend service specifically for the accessibility statement. This has been built into the statement service and is configured via the YAML file per service. Please read the README documentation in Github.

Once you have published the statement you must contact the DeskPro team to arrange routing of any tickets raised by users. 

To do this you must contact Shashi Patel (shashi.patel@hmrc.gov.uk) and provide: 

- name of the service
- top level URL of the service
- name and HMRC address of who will be responsible for handling the responses. This is usually the same person who already handles DeskPro tickets for the service. Generally this is the DSM or members of their Service Analyst team. 

## Help and support to use the service

There is a dedicated Slack channel for the service: #event-accessibility-statements

This is monitored by the PlatUI developers of the service. You should use this route for any questions or issues about the service. 

## Practical surgeries to support introducing the service 

To help introduce the service the PlatUI team are running practical surgeries to walk teams through the process of creating a statement. The aim is to have a created statement in the service by the end of the session. 

**Note**: Teams must come along with statement content ready to be used in the session. 

These sessions are being run twice a week. The hangout link is posted in the service Slack channel on the morning of the event. Please check there for more details. 

Thursday 17 September - 2:00pm- 4:00pm

Monday 21 September - 2:00pm - 4:00pm

Monday 28 September 2:00pm -4:00pm

Thursday 1 October 2:00pm- 4:00pm

## If you have already published an accessibility statement

Statements published under the old process need to be migrated to the new service.

Ideally this needs to be done as soon as possible after the 23rd September 2020 accessibility deadline. But we know there are other priorities and work to consider.  

If you have an upcoming audit or retest and your statement needs updating as a result, then you must use the statement service as part of that work.

If you do not have an accessibility audit or re-rest in the immediate future and the fix dates on your statement are correct then please contact [gaynor.harvey@hmrc.gov.uk](gaynor.harvey@hmrc.gov.uk) to talk about migrating your existing statement. 

## Reviewing and monitoring statement compliance 

Under the [public sector accessibility regulations](https://confluence.tools.tax.service.gov.uk/display/DISC/Regulations+to+make+public+sector+websites+and+mobile+applications+accessible) all accessibility statements **must** be reviewed every 12 months. 

The [Digital Inclusion, Standards and Culture (DISC)](https://confluence.tools.tax.service.gov.uk/display/DISC/Digital+Inclusion%2C+Standards+and+Culture) team will now be monitoring the compliance of accessibility issues listed on statements including fix dates and accuracy to audit (and retest) reports. This will be done using data from the statement service. 

There will also be regular reporting within CDIO and to wider stakeholders about where we are in terms of compliance as a department. 

This is in addition to any reviewing and reporting that GDS may do as the accessibility regulatory body. 

## Contact us

If you have any questions or need further support, please email us at [accessibility.team@hmrc.gov.uk](accessibility.team@hmrc.gov.uk) 
