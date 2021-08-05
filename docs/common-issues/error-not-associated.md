# Issue: Error not associated with input

The error message is present for the form control but it is not programmatically associated with it. 

This means that a screen-reader user who is navigating by form fields, or who moves directly to a field from an error summary link, will not hear the error message.

## To resolve

The error message should have a unique `id` attribute added.

For single inputs the error can be associated adding an `aria-describedby` attribute on the `input` itself, with the error `id` as the value.

For grouped fields where the error refers to all the fields, the `aria-describedby` can be placed on the `fieldset`.

The `aria-describedby` attribute can take multiple `id` references as the value with spaces between.

The order of the `id` in the value will determine the order the content is read out by the screen-reader, so it should be in the same order as the content is on screen - typically the hint first if available, then the error message, but only when present.

## Labels

- wcag
- wcag 1.3.1 (A)
- text input
- fieldset

## Report

| Status | Level | Issue | Success Criterion |
| ------ | ----- | ----- | ----------------- |
| 🔴 (H) | A    | [#issue](): Error not associated with input | 1.3.1 Info and relationships |

## Statement

### Accessibility problems

```
Error messages may be missed if navigating with a screen-reader by form fields or by moving directly to the fields
```

### Milestones

```
Error messages are not programmatically associated with the fields. This fails WCAG 2.1 success criterion 1.3.1 Info and relationships
```

## References

[Error message pattern - Gov.UK Design Pattern](https://design-system.service.gov.uk/components/error-message/) 

[Understanding Success Criterion 1.3.1: Info and Relationships](https://www.w3.org/WAI/WCAG21/Understanding/info-and-relationships)
