# Issue: Error summary contains invalid links [draft]

Links within the error summary either do not work or link to the wrong destination.

The value in the `href` does not match the corresponding `id` of the control that contains the error.

This could either be an invalid `id`, one that does not exist, or an `id` that links to another part of the page, for example linking to a fieldset that contains a set of radio buttons.

The user is unable to quickly navigate to every issue and has to look through the whole page and identify which issue relates to the broken link.

## To resolve:

Ensure you are linking to the correct answer by following the [GOV.UK Design System pattern](https://design-system.service.gov.uk/components/error-summary#linking-from-the-error-summary-to-each-answer).

## Labels

- usability
- error message

## Report

| Priority | Issue |
| ------ | ----- |
| 🔴 P1 | [#issue](): Error summary contains invalid links |


## Statement

This is not a WCAG A/AA failure so it does not have to be included on the accessibility statement, but we strongly recommend resolving the issue to improve the usability of the service.

## References

[Error summary - GOV.UK Design System](https://design-system.service.gov.uk/components/error-summary/)
