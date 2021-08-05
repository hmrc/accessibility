# Issue: HTML validation (WCAG)

There are HTML validation issues which will have an effect on assistive technology:

- improper nesting outside of specification (eg an `li` without a parent `ul` or `ol`)
- missing start or end tags (where mandatory)
- poorly formed attributes, for example:
  - unquoted href with querystring
  - unbalanced attribute quotes
  - missing spaces between attributes
- incorrect attribute values
- duplicate attributes where this has an effect on accessibility, for example:
  - duplicate IDs where referenced by aria
  - duplicate accessible name attributes (eg `alt` or `aria-label`)

Other issues are non-WCAG (unless they can be shown to affect assistive technology) and should use the nonWCAG HTML validation issue.

## To resolve

Fix the issue in code and ensure the error is cleared by running an HTML validator such as:
- [W3C Nu Validator (online service)](https://validator.w3.org/nu/)
- [Validity Chrome browser plugin](https://chrome.google.com/webstore/detail/validity/bbicmjjbohdfglopkidebfccilipgeif?hl=en-GB)

Note the Jenkins Continuous Integration accessibility checker performs HTML validation alongside the accessibility checks.

## Labels

- wcag
- wcag 4.1.1 (A) Parsing

## Report
| Status | Level | Issue | Success Criterion |
| ------ | ----- | ----- | ----------------- |
| 🔴 (H) | A    | [#issue](): HTML validation | 4.1.1 Parsing |

## Statement

## Accessibility problems
```
[dependant on issue]
```

## Milestones
```
[dependant on issue] This fails WCAG success criterion 4.1.1 Parsing
```

## Reference 

[Understanding Success Criterion 4.1.1: Parsing](https://www.w3.org/WAI/WCAG21/Understanding/parsing.html)
