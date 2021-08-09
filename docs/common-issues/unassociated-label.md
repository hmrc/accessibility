# Issue: Unassociated label

Each form input must have an accessible name (unless it has `type="hidden"`). When it is visible this allows users with lower dexterity to click on the label to focus the input, and allows people using voice recognition to say the visible name to access the input.

An accessible name is added to an input using a `for` attribute on the associated `label` with the correct `id` of the associated input (nesting an input within a label is also possible but can cause issues for people using Dragon speech recognition). Only resort to using `aria` instead of a visible label if the latter is not possible.

In this instance the label is present visually alongside the input, but the programatic relationship is not established. This means screen-reader users will be disadvantaged when navigating by shortcut keys (eg jumping from form field to field) or when using element lists (where fields are identified by their programmatically assigned accessible name).

## To resolve

Follow the [text input guidance](https://design-system.service.gov.uk/components/text-input/). Ensure the label is correctly associated with the input by clicking the label - the input should receive focus.

## Labels

- wcag
- wcag 1.3.1 (A) Info and relationships
- wcag 4.1.2 (A) Name, Role, Value
- text input


## Report

| Status | Level | Issue | Success Criterion |
| ------ | ----- | ----- | ----------------- |
| 🔴 (H) | A    | [#issue](): Missing label | 1.3.1 Info and relationships <br/> 4.1.2 Name, role, value |

## Statement

### Accessibility problems

```
when using screen-readers, the label is not read out with the form field [specify which field]. It will be necessary to move out of the form field to access the instructions.
```

### Milestones

```
form field is missing a programatically associated name. This fails WCAG 2.1 success criterion 1.3.1 Infor and relationships and 4.1.2 Name, role, value
```

## References

[Text input - Gov.UK Design System](https://design-system.service.gov.uk/components/text-input/)

[Understanding Success Criterion 1.3.1: Info and Relationships](https://www.w3.org/WAI/WCAG21/Understanding/info-and-relationships.html)

[Understanding Success Criterion 4.1.2: Name, Role, Value](https://www.w3.org/WAI/WCAG21/Understanding/name-role-value.html)