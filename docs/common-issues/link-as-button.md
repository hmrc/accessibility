# Issue: Link styled as a button [Draft]

For a link styled as a button, add `role="button"` and `data-module="govuk-button"` to initialise the JavaScript polyfill to ensure it acts as a button.

- Adding ARIA `role="button"` will identify the link as a button to assistive technologies.
- Adding `data-module="govuk-button"` makes sure that the link responds to the <kbd>enter</kbd> and <kbd>spacebar</kbd> keypress.

## To resolve

Follow guidance [Using links as buttons](https://github.com/hmrc/accessibility/blob/master/docs/design-and-usability-quick-wins.md#using-links-as-buttons).

## Labels
- wcag
- wcag 4.1.2 (A)
- button
- code quality
- keyboard-only

## Report

| Status | Level | Issue | Success Criterion |
| ------ | ----- | ----- | ----------------- |
| 🔴 (H) | A    | [#issue](): Link styled as a button | 4.1.2 Name, Role, Value |

## Statement

### Accessibility problems
```
on the [page title] page, the [link text] link has been styled as a button, but is not seen as one with assistive technologies and does not work with the spacebar keypress
```

### Milestones
```
for a link styled as a button, the role="button" and the data-module="govuk-button" is missing to ensure it acts like a button. This fails WCAG 2.1 success criterion 4.1.2: Name, Role, Value
```

## References

[Using links as buttons](https://github.com/hmrc/accessibility/blob/master/docs/design-and-usability-quick-wins.md#using-links-as-buttons)

[Understanding Success Criterion 4.1.2 Name, Role, Value](https://www.w3.org/WAI/WCAG21/Understanding/name-role-value)
