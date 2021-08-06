# Missing instructions

Where there is a requirement for data to be entered in a particular way, the user needs to be informed of this up front.

If a user is only told of a format requirement in the error message, then it is being communicated too late - going back to review an error, process it, understand how it relates to the entered data and then editing the entered data is a lot of additional work.

## To resolve

Follow the [text input guidance on hint copy](https://design-system.service.gov.uk/components/text-input/#hint-text). Ensure the hint copy is correctly associated with the form controls using aria so screen-reader users are aware of it.

Hint copy should be short and only help the user with how they should enter data in the form. General guidance should precede the form.

## Labels

- wcag
- wcag 3.3.2 (A) Labels or instructions
- text input

## Report

| Status | Level | Issue | Success Criterion |
| ------ | ----- | ----- | ----------------- |
| 🔴 (H) | A    | [#issue](): Missing instructions | 3.3.2 Labels or instructions |

## Statement

### Accessibility problems

```
there is no indication of the format needed when the user is entering information, the user is only told when an error is shown
```

### Milestones

```
the required format for data entry is not communicated to the user. This fails WCAG 2.1 success criterion 3.3.2 Labels or instructions
```

## References

[Guidance on hint copy - Gov.UK Design System](https://design-system.service.gov.uk/components/text-input/#hint-text)

[Understanding Success Criterion 3.3.2: Labels or Instructions](https://www.w3.org/WAI/WCAG21/Understanding/labels-or-instructions.html)