# Issue: Page title not prefixed with the word 'Error' [draft]

The page title not does not follow the service standard validation pattern when an error occurs.

Without the page title being prefixed with the word "Error: " assistive technology users could get confused or disorientated having the focus automatically moved away from the beginning of the web page.

## To resolve:

Whenever an input validation error occurs the returned page should have the content in the `<title>` element prefixed with the word "Error: ". Follow the [validation pattern](https://design-system.service.gov.uk/patterns/validation/).

## Labels

- usability

## Report

| Priority | Issue |
| -------- | ----- | 
| 🔴 P1     | [#issue](): Page title not prefixed with the word 'Error' |

## Statement

This is not a WCAG failure so it does not have to be included on the accessibility statement, but we strongly recommend resolving the issue to improve the usability of the service.

## References

[Error summary - GOV.UK Design System](https://design-system.service.gov.uk/components/error-summary/)

[Validation pattern - GOV.UK Design System](https://design-system.service.gov.uk/patterns/validation/)
