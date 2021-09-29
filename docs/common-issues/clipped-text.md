# Issue: Text is clipped [Draft]

Long string of text not breaking to accommodate the width of the parent container. The text gets clipped.

## To resolve

Most recent govuk-frontend should containe fix for this issue panel heading
https://github.com/alphagov/govuk-frontend/pull/2347.
Or apply `.text-overflow` class on element
This is create difficulties for people who rely on text to be resized without loss of the content.

```
.text-overflow {
    word-wrap: break-word; /* old version of overflow-wrap for IE and Edge and FF < 49*/
    overflow-wrap: anywhere; /* modern, tries to fit word on a new line rather than fitting on remnants of the current line */
}
```
## Labels

- wcag
- wcag 1.4.4 (AA)
- large text

## Report

| Status | Level | Issue | Success Criterion |
| ------ | ----- | ----- | ----------------- |
| 🟠 (M) | AA    | [#issue]():Text is clipped | 1.4.4 Resize text |

## Statement

### Accessibility problems
```
  - description: When entering a long string of text it does not break to fit the container it is being added to, so it will overflow. Users will have to scroll horizontally to read it. This will also be a problem if the text size is increased. Additionally, seeing it will be difficult as it imight blend in with background colour.
```

### Milestones

```
  - description: Copy missing text wrapping CSS properties, what causes issues when the text font size increased. This fails WCAG 2.1 success criterion 1.4.4 Resize text 
  date: TBC

```

## References

[govuk-font mixin - GOV.UK  Frontend](https://frontend.design-system.service.gov.uk/sass-api-reference/#govuk-typography-responsive-usage)

[Understanding Success Criterion 1.4.4 Resize text ](https://www.w3.org/TR/UNDERSTANDING-WCAG20/visual-audio-contrast-scale.html)
