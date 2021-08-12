# Issue: Error summary missing [draft]

A validation error occurs and the page is reloaded, but the error summary component is not present.

This causes the user to have to look through the whole page to indentify the issues to be corrected. For screen reader and screen magnification users this can be difficult and time consuming to navigate through the entire page to find all the errors.

## To resolve:

Whenever there is a validation error you should show the error summary component at the top of the page, before the `h1` but after the back link (if present). For more details, check the [GOV.UK Design System guidance](https://design-system.service.gov.uk/components/error-summary/#where-to-put-the-error-summary).

## Labels

- wcag
- wcag 1.3.1
- usability
- error summary

## Report

| Status | Level | Issue | Success Criterion |
| ------ | ----- | ----- | ----------------- |
| 🔴 (H) | A    | [#issue](): Error summary missing | 1.3.1 Info and Relationships |

## Statement

### Accessibility problems

```
tbc
```

### Milestones

```
tbc
```

## References

[Error summary - GOV.UK Design System](https://design-system.service.gov.uk/components/error-summary/)

[Understanding Success Criterion 1.3.1: Info and Relationships](https://www.w3.org/WAI/WCAG21/Understanding/info-and-relationships)
