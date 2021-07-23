# Error summary

The error summary component is crucial for users to easily see and correct any errors with the information entered on a page.

Failing to provide the user with adequate information would cause a service to fail the WCAG criteria [1.3.1: Info and Relationships](https://www.w3.org/WAI/WCAG21/Understanding/info-and-relationships)

## How it works

When an error occurs from user input validation, the page is displayed again with the error summary component, containing a list of all errors, clearly visible at the top of the page.

The initial focus when the page is loaded is set to the Error summary component, this aids all users in having their attention brought to the summary and the action they need to take.

This helps the user understand how many errors need to be resolved and links to take them directly to the input, or set of inputs, that require attendtion.

More information can be found on the [GOV.UK Design System - Error summary page](https://design-system.service.gov.uk/components/error-summary/)

## Common issues

During audits we consistantly see very similar issues occuring with the Error summary component, below are some of the most common findings.  

### 1. Missing error summary

#### Cause

A validation error occurs and the page is displayed again but the error summary component has not been implemented.

#### Impact

The user has to look through the whole page to indentify all the issues to be corrected.

#### Solution

Whenever there is a validation error you should add the error summary component to the top of the page.

#### How to test

1. Submit the page without entering any data.
2. Check the Error summary component appears at the top of the page before the main page heading (H1)
3. Check the Error summary component has received focus.

### 2. Links 

Links within the error summary either do not work or link to the wrong destination.

#### Cause

The main cause of this issue is that the value in the `href` does not match the corresponding `id` of the control that contains the error.

This can either by an invalid id, one that does not exist or an `id` of another part of the page, for example the fieldset containing a set of radio buttons.

#### Impact

The user is unable to quickly navigate to the issue and has to look through the whole page to indentify the issue.

#### Solution

Enasure you are linking to the correct answer by following the GOV.UK pattern - [Linking from the error summary to each answer](https://design-system.service.gov.uk/components/error-summary#linking-from-the-error-summary-to-each-answer)


#### How to test

1. Submit the page without entering any data.
2. Check the number of items in the error summary matches the number of error messages on the page.


### 3. Page title

Page title not prefixed with 'Error'

#### Cause



#### Impact



#### Solution



#### How to test



### 4. Incorrect styling

The Error summary component has specific styling to match the [GOV.UK colour pallete](https://design-system.service.gov.uk/styles/colour/)

When used properly, the up to date GOV.UK colour pallete provides enough colour contrast to satisfy WCAG critera like [WCAG 1.4.3: Contrast (Minimum)](https://www.w3.org/WAI/WCAG21/Understanding/contrast-minimum) and [1.4.11: Non-text Contrast](https://www.w3.org/WAI/WCAG21/Understanding/non-text-contrast)

#### Cause of issues

The majority of issues relate to using a depricated library like [assets-frontend](https://github.com/hmrc/assets-frontend) or an out of date version of [govuk-frontend](https://github.com/alphagov/govuk-frontend/)

#### Impact

Low colour contrast can affect users

#### Solution

#### How to test

### 5. Message text

#### Cause

A validation error occurs and the page is displayed again but the error summary is not present 

#### Impact

The user has to look through the whole page to try and indentify all the issues to be corrected.

#### Solution

#### How to test

## Related issues

See [error-message]
