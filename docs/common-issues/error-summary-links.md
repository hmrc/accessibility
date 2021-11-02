# Issue: Error summary contains invalid links [draft]

Links within the error summary either do not work or link to the wrong destination.

The value in the `href` does not match the corresponding `id` of the control that contains the error.

This could either be an invalid `id`, one that does not exist, or an `id` that links to another part of the page, for example linking to a fieldset that contains a set of radio buttons.

The user is unable to quickly navigate to every issue and has to look through the whole page and identify which issue relates to the broken link.

## To resolve:

Ensure you are linking to the correct answer by following the [GOV.UK Design System pattern](https://design-system.service.gov.uk/components/error-summary#linking-from-the-error-summary-to-each-answer).

## Labels

- wcag
- wcag 1.3.1
- usability
- error message

## Report

| Status | Level | Issue | Success Criterion |
| ------ | ----- | ----- | ----------------- |
| 🔴 (H) | A    | [#issue](): Error summary contains invalid links | 1.3.1 Info and Relationships |


## Statement

### Accessibility problems

```
 the error message link in the error summary does not link to the form element in the error.
```

### Milestones

```
  the error message link in the error summary does not contain the valid link destination to the form element in error. This fails WCAG 2.1 success criterion 1.3.1 Info and relationships
 date: TBC

```

## References

[Error summary - GOV.UK Design System](https://design-system.service.gov.uk/components/error-summary/)

[Understanding Success Criterion 1.3.1: Info and Relationships](https://www.w3.org/WAI/WCAG21/Understanding/info-and-relationships)
