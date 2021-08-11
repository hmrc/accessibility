# Issue: HTML5 form field validation present

HTML5 validation is triggered when certain attributes are added to form controls, such as `pattern`, `required` and certain `type` values.

There are a few reasons why HTML5 validation is not desirable as an out-of-the-box solution:

- the style of the errors does not match the other error styles in the pattern library
- the error message is temporary, disappearing when focus is moved
- when used on a field with an `autocomplete` attribute, the error is obscured by the autocomplete options
- it doesn't pull attention so can be missed
- only one error is shown at a time, so a user may have to repeatedly submit the form to fix all the issues
- doesn't respond to font size zoom
- the error messages are not especially helpful

## To resolve

Add a `novalidate` attribute to the `form` element to prevent HTML5 validation.

## Labels

- wcag
- wcag 3.3.1 (A) Error identification
- recover from validation errors

## Report

| Status | Level | Issue | Success Criterion |
| ------ | ----- | ----- | ----------------- |
| 🔴 (H) | A    | [#issue](): HTML5 validation present | 3.3.1 Error identification |

## Statement

### Accessibility problems

```
some fields [name the fields] do not present error messages in ways which are easily readable or may not show an error until other errors are fixed
```

### Milestones

```
fields use HTML5 native browser validation. This fails WCAG 2.1 success criterion 3.3.1 Error identification
```

## References

[Guidance on HTML5 validation - GOV.UK Design System](https://design-system.service.gov.uk/patterns/validation/#turn-off-html5-validation)