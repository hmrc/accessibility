# Issue: Hint not associated with input

Hint copy is present for the form control but it is not programmatically associated with it.

This means that a screen-reader user who is navigating by form fields, or who moves directly to a field from an error summary link, will not hear the hint copy.

## To resolve

The hint copy should have a unique `id` attribute added.

For single inputs the hint can be associated adding an `aria-describedby` attribute on the `input` itself, with the hint `id` as the value.

For grouped fields where the hint refers to all the fields, the `aria-describedby` can be placed on the `fieldset`.

The `aria-describedby` attribute can take multiple `id` references as the value with spaces between.

The order of the `id` in the value will determine the order the content is read out by the screen-reader, so it should be in the same order as the content is on screen - typically the hint first, then the error message when present.

Content referenced by `aria-describedby` should be simple text with no nested elements (such as lists) as screen-readers will not always read out complex content in full.

## Labels

- wcag
- wcag 1.3.1 (A)
- text input
- fieldset

## Report

| Status | Level | Issue | Success Criterion |
| ------ | ----- | ----- | ----------------- |
| 🔴 (H) | A    | [#issue](): Hint not associated with input | 1.3.1 Info and relationships |

## Statement

### Accessibility problems

```
There is information relevant to the form which may be missed if navigating with a screen-reader by form fields or by moving directly to the fields
```

### Milestones

```
Information required to assist in correctly filling out form fields is not programmatically associated with the field. This fails WCAG 2.1 success criterion 1.3.1 Info and relationships
```

## References

[Guidance on hint copy - Gov.UK Design System](https://design-system.service.gov.uk/components/text-input/#hint-text)

[Understanding Success Criterion 1.3.1: Info and Relationships](https://www.w3.org/WAI/WCAG21/Understanding/info-and-relationships)
