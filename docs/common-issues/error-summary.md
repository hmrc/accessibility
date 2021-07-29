# Error summary

The [error summary component](https://design-system.service.gov.uk/components/error-summary/) is crucial for users to easily see and correct any errors with the information entered on a page.

Failing to provide the user with adequate information could cause a service to fail the WCAG criteria [1.3.1: Info and Relationships](https://www.w3.org/WAI/WCAG21/Understanding/info-and-relationships)

During audits we consistently see similar issues occurring with the component, below are some of the most common findings.  

## 1. Missing error summary

### Cause

A validation error occurs and the page is redisplayed to the user but the error summary component has not been implemented.

### Impact

The user has to look through the whole page to indentify all the issues to be corrected.

For screen reader and screen magnification users this can be difficult, and time consuming, to systemattically navigate through the entire page to find all the errors.

### Solution

Whenever there is a validation error you should add the error summary component to the top of the page.

Details about the placement of the Error summary component can be found in the design system documentation [Where to put the error summary
](https://design-system.service.gov.uk/components/error-summary/#where-to-put-the-error-summary)

### How to test

1. Submit the page without entering any data.
2. Check the Error summary component appears at the top of the page before the main page heading (H1)
3. Check the Error summary component has received focus.

## 2. Links 

Links within the error summary either do not work or link to the wrong destination.

### Cause

The main cause of this issue is that the value in the `href` does not match the corresponding `id` of the control that contains the error.

This can either be an invalid `id`, one that does not exist, or an `id` of another part of the page, for example linking to a fieldset that contains a set of radio buttons.

### Impact

The user is unable to quickly navigate to every issue and has to look through the whole page and indentify which issue relates to the broken link.

### Solution

Enasure you are linking to the correct answer by following the GOV.UK pattern - [Linking from the error summary to each answer](https://design-system.service.gov.uk/components/error-summary#linking-from-the-error-summary-to-each-answer)


### How to test

1. Submit the page without entering any data.
2. Check the number of items in the error summary matches the number of error messages on the page.


## 3. Page title

Page title not prefixed with 'Error'

### Cause



### Impact



### Solution



### How to test



## 4. Incorrect styling

The Error summary component has specific styling to match the [GOV.UK colour pallete](https://design-system.service.gov.uk/styles/colour/)

When used properly, the up to date GOV.UK colour pallete provides enough colour contrast to satisfy WCAG critera like [WCAG 1.4.3: Contrast (Minimum)](https://www.w3.org/WAI/WCAG21/Understanding/contrast-minimum) and [1.4.11: Non-text Contrast](https://www.w3.org/WAI/WCAG21/Understanding/non-text-contrast)

### Cause of issues

The majority of issues relate to using a depricated library like [assets-frontend](https://github.com/hmrc/assets-frontend) or an out of date version of [govuk-frontend](https://github.com/alphagov/govuk-frontend/)

### Impact

Low colour contrast can affect users

### Solution

### How to test

## 5. Message text

### Cause

A validation error occurs and the page is displayed again but the error summary is not present 

### Impact

The user has to look through the whole page to try and indentify all the issues to be corrected.

### Solution

### How to test

