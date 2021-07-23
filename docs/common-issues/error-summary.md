# Error summary

The error summary component is crucial for users to easily see and correct any errors with the information entered on a page.

Failing to provide the user with adequate information would cause a service to fail the WCAG criteria [1.3.1: Info and Relationships](https://www.w3.org/WAI/WCAG21/Understanding/info-and-relationships)

## How it works

When an error occurs from user input validation, the page is displayed again with the error summary component, containing a list of all errors, clearly visible at the top of the page.

The initial focus when the page is loaded is set to the Error summary component, this aids all users in having their attention brought to the summary and the action they need to take.

This helps the user understand how many errors need to be resolved and 

## Common issues

### Missing error summary

When an error occurs the page is displayed again but the error summary is not present 


2. Links within the error summary either do not work or link to the wrong destination
3. Page title not prefixed with 'Error'
4. Incorrect styling
5. Message text

## How to test

Submit a page without entering any information.

## Related issue

See [error-message]
