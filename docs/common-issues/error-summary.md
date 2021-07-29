# Error summary

The [error summary component](https://design-system.service.gov.uk/components/error-summary/) is crucial for users to easily see and correct any errors with the information entered on a page.

Failing to provide the user with adequate information could cause a service to fail the WCAG criteria [1.3.1: Info and Relationships](https://www.w3.org/WAI/WCAG21/Understanding/info-and-relationships).

During audits we consistently see similar issues occurring with the component, below are some of the most common findings.  

## 1. Missing error summary

A validation error occurs, the page is redisplayed, but the error summary component is not present.

### Impact

The user has to look through the whole page to indentify all the issues to be corrected.

For screen reader and screen magnification users this can be difficult, and time consuming, to systemattically navigate through the entire page to find all the errors.

### Solution

Whenever there is a validation error you should implement the error summary component at the top of the page, before the main page heading (H1).

Details about the placement of the Error summary component can be found in the design system documentation [Where to put the error summary](https://design-system.service.gov.uk/components/error-summary/#where-to-put-the-error-summary).

### How to test

1. Submit the page without entering any data.
2. Check the Error summary component appears at the top of the page before the main page heading (H1)
3. Check the Error summary component has received focus.
4. Check the number of entries in the summary match the number of errors on the page.

## 2. Invalid links 

Links within the error summary either do not work or link to the wrong destination.

The main cause of this issue is that the value in the `href` does not match the corresponding `id` of the control that contains the error.

This can either be an invalid `id`, one that does not exist, or an `id` to another part of the page, for example linking to a fieldset that contains a set of radio buttons.

### Impact

The user is unable to quickly navigate to every issue and has to look through the whole page and indentify which issue relates to the broken link.

### Solution

Ensure you are linking to the correct answer by following the GOV.UK pattern - [Linking from the error summary to each answer](https://design-system.service.gov.uk/components/error-summary#linking-from-the-error-summary-to-each-answer).

### How to test

1. Submit the page without entering any data.
2. Check each item in the error summary focuses the field with the associated error.
3. Check multiple choice answers, radio and checkboxes, focus the first item in the group.
4. Check date input fields focus the first field containing an error.


## 3. Page title not prefixed with the word 'Error'

The page title not does not follow the service standard [validation pattern](https://design-system.service.gov.uk/patterns/validation/) when an error occurs.

Although not strictly an issue with the Error summary component the two are inherently linked. Assistive technology users will become familar with the pattern and know that when the page title is proceeded with the word "Error: " an error has occured and their focus will be automatically set to a specific place on the page, i.e. to the Error Summary.

### Impact

Without the page title being prefixed with the word "Error: " assistive technology users could get confused or disorientated having the focus moved from the default location (the top of the page)

### Solution

Whenever an error occurs with input validation the returned page should have it's `<title>` element prefixed with the word "Error: "

### How to test

1. Submit the page with 1 or more invalid entries.
2. Check the title in the browser tab is prefixed with "Error: ".

## 4. Incorrect styling

The Error summary component has specific styling to match the [GOV.UK colour pallete](https://design-system.service.gov.uk/styles/colour/).

When used properly, the up to date GOV.UK colour pallete provides enough colour contrast to satisfy WCAG critera [1.4.3: Contrast (Minimum)](https://www.w3.org/WAI/WCAG21/Understanding/contrast-minimum) and [1.4.11: Non-text Contrast](https://www.w3.org/WAI/WCAG21/Understanding/non-text-contrast).

### Cause of issues

The majority of issues relate to using a depricated library like [assets-frontend](https://github.com/hmrc/assets-frontend) or an out of date version of [govuk-frontend](https://github.com/alphagov/govuk-frontend/).

### Impact

Low colour contrast can affect users with various vision related conditions and can cause unnessessry eye strain when using our services. 

### Solution

Always use the latest compatible version of the library your service is built on and, if posible, existing services should update to use [govuk-frontend](https://github.com/alphagov/govuk-frontend/) if they haven't already.

### How to test

1. Submit the page with 1 or more invalid entries.
2. Visually check the service matches the [GOV.UK colour pallette](https://design-system.service.gov.uk/styles/colour/).
3. Use a tool like [WAVE for Chrome](https://chrome.google.com/webstore/detail/wave-evaluation-tool/jbbplnpkjmmeebjpijfedlgcdilocofh) to test the contast of items on a page.

## 5. Message text

### Cause

A validation error occurs, the error summary is displayed, but the error messages are ambigous or convoluted. 

### Impact

The user has to look through the whole page to try and indentify all the issues to be corrected.

### Solution

Ensure for each error scenario you write [clear and concise error messages](https://design-system.service.gov.uk/components/error-message#be-clear-and-concise).

### How to test

As with all content, testing with real users, with a wide range of requirements, provides the best results. User feedback and the ability to witness users quickly and easily understand, and correct, mistakes will ensure your error messaging is optimised for all users.

