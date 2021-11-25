# Issue: Validation [draft]

When validating data, spaces and upper/lower-casing should be permitted as long as it does not change the meaning of the data. This applies even if a format is indicated in hint copy.

The user may be copying & pasting from another source which has different formatting.

Voice control software often inserts spaces (including leading spaces) as the user speaks and having to go back and remove these is time-consuming.

People who struggle with numbers, such as those with dyscalculia, will benefit from being able to write numbers in space-separated groups.

Editing data can be difficult for those with mobility or dexterity issues or for those on touch devices, so we should avoid raising errors for format where possible.

## To resolve:
Follow the [validation pattern](https://design-system.service.gov.uk/patterns/validation/) which states that we should allow information in different formats as long as it is not ambiguous.

- Trim whitespace from the start and end of the data, and remove spaces within before validating
- Ensure validation is case-insensitive if case has no bearing on the meaning of the data
- Allow optional delimiters eg for sort codes allow spaces and dashes

## Labels

- recover from validation errors
- usability


## Report

| Priority | Issue |
|----------|-------|
| 🔴 P1    | [#issue]() Validation |

## Statement

This is not a WCAG A/AA failure so it does not have to be included on the accessibility statement, but we strongly recommend resolving the issue to improve the usability of the service.
## References

[Validation pattern - GOV.UK Design System](https://design-system.service.gov.uk/patterns/validation/)
