# Issue:  Link missing JavaScript polyfill to act as button [Draft]

For link styled as a button add role="button" and initialise the JavaScript polyfill to ensure it acts as a button.
This makes sure that the link responds to spacebar keypress. 
Assistive technology will interprite anchor as `button` with the ARIA role "button" and makes it clear that this is a button control and not a link.  User would expect to activate element using `Enter` or `Space` key.

## To resolve

Add required data attribute (data-module="govuk-button") to enable button functionality. This makes sure that the link responds to the spacebar keypress.
Follow guidance [Using links as buttons](https://github.com/hmrc/accessibility/blob/master/docs/design-and-usability-quick-wins.md#using-links-as-buttons) and initialise the JavaScript polyfill so that the link acts as a button.

## Labels

- wcag
- wcag 4.1.2 (A)

## Report

| Status | Level | Issue | Success Criterion |
| ------ | ----- | ----- | ----------------- |
| 🔴 (H) | A    | [#issue]():Link missing JavaScript polyfill to act as button | 4.1.2 Name, Role, Value |

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

[Using links as buttons](https://github.com/hmrc/accessibility/blob/master/docs/design-and-usability-quick-wins.md#using-links-as-buttons)

[Understanding Success Criterion 4.1.2 Name, Role, Value ](https://www.w3.org/WAI/WCAG21/Understanding/name-role-value)
