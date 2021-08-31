# Issue: Conditionally revealing content [Draft]

When content is revealed as the user selects a radio / checkbox option it is not consistently announced to screen reader users. 

GDS guidelines advise in only using the conditional reveal when another single form control (related question) is shown, for example a single text input.

## To resolve

Move the content from within the reveal to somewhere appropriate for informing the user. 

If the content contains a link then it shouldn't be added as hint text as not all assistive technology will announce the content as a containing links to the user.

## Labels

- wcag
- wcag 4.1.2 (A)
- radios / checkboxes
- usability

## Report

| Status | Level | Issue | Success Criterion |
| ------ | ----- | ----- | ----------------- |
| 🔴 (H) | A    | [#issue]():Conditionally revealing content | 4.1.2 Name, Role, Value |

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

[Radios - HMRC Design System](https://design-system.service.gov.uk/components/radios#conditionally-revealing-a-related-question)

[Checkboxes - HMRC Design System](https://design-system.service.gov.uk/components/checkboxes#conditionally-revealing-a-related-question)

[Understanding Success Criterion 4.1.2 Name, Role, Value ](https://www.w3.org/WAI/WCAG21/Understanding/name-role-value)

