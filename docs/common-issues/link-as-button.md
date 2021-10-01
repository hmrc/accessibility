# Issue: Link styled as a button [Draft]

What about revising it to...

For a link styled as a button, add role="button" and initialise the JavaScript polyfill to ensure it acts as a button.

- Adding ARIA role="button" will identify the link as a button to assistive technologies.
- The JavaScript polyfill makes sure that the link responds to the enter and spacebar keypress.

## To resolve
Make sure element uitilising [button.js](https://github.com/alphagov/govuk-frontend/blob/28ca6d5f61df309c00490f22d809bb6d7aaec7ab/src/components/button/button.js) allowing users to activate it using `space` key.

Follow Using links as buttons guidance .

## Labels

- code quality
- usability
- keyboard-only
- wcag
- wcag 4.1.2 (A)

## Report

| Status | Level | Issue | Success Criterion |
| ------ | ----- | ----- | ----------------- |
| 🔴 (H) | A    | [#issue]():Link styled as a button | 4.1.2 Name, Role, Value |

## Statement

### Accessibility problems
```
  - description: On the xxx page, the xxx link has been styled as a button but does not work with the spacebar key press. A keyboard only user will need to use the enter key to activate this.

```

### Milestones

```
  - description: The link styled as button does not respond to the spacebar for keyboard only users. This fails WCAG 2.1 success criterion 4.1.2 Name, Role, Value
  date: tbc
```

## References

[Using links as buttons](https://github.com/hmrc/accessibility/blob/master/docs/design-and-usability-quick-wins.md#using-links-as-buttons)

[Understanding Success Criterion 4.1.2 Name, Role, Value ](https://www.w3.org/WAI/WCAG21/Understanding/name-role-value)