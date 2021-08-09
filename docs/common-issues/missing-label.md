# Issue: Missing label

Each form input must have an accessible name (unless it has `type="hidden"`). When it is visible this allows users with lower dexterity to click on the label to focus the input, and allows people using voice recognition to say the visible name to access the input.

An accessible name is added to an input using a `for` attribute on the associated `label` with the correct `id` of the associated input (nesting an input within a label is also possible but can cause issues for people using Dragon speech recognition). Only resort to using `aria` instead of a visible label if the latter is not possible.

## To resolve

Follow the [text input guidance](https://design-system.service.gov.uk/components/text-input/). Ensure the label is correctly associated with the input by clicking the label - the input should receive focus.

## Labels

- wcag
- wcag 3.3.2 (A) Labels or instructions
- wcag 4.1.2 (A) Name, role, value
- text input

## Report

| Status | Level | Issue | Success Criterion |
| ------ | ----- | ----- | ----------------- |
| 🔴 (H) | A    | [#issue](): Missing label | 3.3.2 Labels or instructions <br/> 4.1.2 Name, role, value |

## Statement

### Accessibility problems

```
the form field is missing a label so it is unclear what should be entered in the field [provide more information to help user resolve issue - eg what data should be added]
```

### Milestones

```
the required data is not communicated to the user. This fails WCAG 2.1 success criterion 3.3.2 Labels or instructions and 4.1.2 Name, role, value
```

## References

[Text input - Gov.UK Design System](https://design-system.service.gov.uk/components/text-input/)

[Understanding Success Criterion 3.3.2: Labels or Instructions](https://www.w3.org/WAI/WCAG21/Understanding/labels-or-instructions.html)

[Understanding Success Criterion 4.1.2: Name, Role, Value](https://www.w3.org/WAI/WCAG21/Understanding/name-role-value.html)