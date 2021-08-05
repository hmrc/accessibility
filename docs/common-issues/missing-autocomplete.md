# Issue: Missing/incorrect autocomplete attribute

Autocomplete attributes are [missing from | incorrect on] form controls which are asking for personal data from the user (eg name, email address, phone numbers, address).

These attributes are important as they allow the user to rapidly enter data in multiple fields which they would otherwise have to enter manually. This has multiple benefits:
- prevents users having to remember detailed information, which particuarly helps users with memory issues
- greatly reduces typing requirements which helps a wide range of users including those with dexterity issues
- ensures details are more accurate and less prone to spelling mistakes as this data is subject to repeated scrutiny by the user

## To resolve

Add the appropriate value to an `autocomplete` attribute on the fields.

There is a [full list of values for the autocomplete attribute](https://html.spec.whatwg.org/multipage/form-control-infrastructure.html#autofill).

## Labels

- wcag
- wcag 1.3.5 (A) Identify Input Purpose

## Report
| Status | Level | Issue | Success Criterion |
| ------ | ----- | ----- | ----------------- |
| 🔴 (H) | A    | [#issue](): Missing/incorrect autocomplete attributes | 1.3.5: Identify Input Purpose |

## Statement

### Accessibility problems

```
fields for [named fields] may not offer the user the option to populate from data previously saved in the browser.
```

### Milestones

```
input fields are missing autocomplete attributes which may mean the user will be unable to use the browser's saved data to populate these fields easily. This fails WCAG 2.1 success criterion 1.3.5 Identify Input Purpose
```

## References
[Text input pattern - Gov.UK Design Patterns](https://design-system.service.gov.uk/components/text-input/#use-the-autocomplete-attribute)
[Understanding Success Criterion 1.3.5: Identify Input Purpose](https://www.w3.org/WAI/WCAG21/Understanding/identify-input-purpose.html)
