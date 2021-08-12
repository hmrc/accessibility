# Issue: Missing fieldset or legend

When displaying multiple fields which are to be considered as a group (for example checkboxes or radio buttons) they should be wrapped in a `fieldset` and this should be accompanied by a `legend` as the `fieldset`'s first child. Whilst a `legend` is strictly optional, it forms part of the contextual placement for the fields within so should always be added. If the contained fields' individual labels do not convey the meaning alone then this becomes a WCAG issue.

## To resolve

- add a wrapping `fieldset` around the appropriate fields if one is not present
- ensure any hint is associated with the fields by adding an `aria-describedby` attribute to the `fieldset` using the `id` attribute of the hint element
- when an error is present for the fields within the `fieldset` add the `id` of the error message to the `aria-describedby` attribute
- make sure a `legend` is present as the first child of the `fieldset`
    - the legend should not be empty - it should contain the copy for the question related to the contained fields
    - the `legend` can be hidden to avoid visual duplication by the addition of a `govuk-visually-hidden` class
    - look at combining the `h1` and the `legend` if possible


## Labels
WCAG criteria is determined by whether the legend is required to make sense of the labels on the individual fields

- wcag
- wcag 1.3.1 (A) Info and relationships
- fieldset

If a legend is present but there is no fieldset then the following also applies:
- wcag 4.1.1 (A) Parsing

If the missing legend means there are instructions which are missing from the page then the following also applies:
- wcag 3.3.2 (A) Labels or instructions


## Report

| Status | Level | Issue | Success Criterion |
| ------ | ----- | ----- | ----------------- |
| 🔴 (H) | A    | [#issue](): Missing fieldset or legend] | 1.3.1 Info and relationships <br/>3.3.2 Labels or instructions <br/>4.1.1 Parsing |

## Statement

### Accessibility problems
```
fields are not grouped so it may be difficult to determine which fields relate to each other
```

### Milestones
```
there is a missing fieldset and/or legend. This fails WCAG 2.1 success criterion 1.3.1 Info and relationships, 3.3.2 Labels or instructions and 4.1.1 Parsing
```


## References

[Fieldsets - GOV.UK Design System](https://design-system.service.gov.uk/components/fieldset/)

[Using the fieldset and legend elements - Accessibility in government blog](https://accessibility.blog.gov.uk/2016/07/22/using-the-fieldset-and-legend-elements/)

[Understanding Success Criterion 1.3.1: Info and Relationships](https://www.w3.org/WAI/WCAG21/Understanding/info-and-relationships.html)

[Understanding Success Criterion 3.3.2: Labels or Instructions](https://www.w3.org/WAI/WCAG21/Understanding/labels-or-instructions.html)

[Understanding Success Criterion 4.1.1: Parsing](https://www.w3.org/WAI/WCAG21/Understanding/parsing.html)