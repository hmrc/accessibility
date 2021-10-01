# Issue: Text is clipped [Draft]

Text is present which does not wrap to stay within the bounds of its parent container when user rely on text resizing. Increasing font size causing the text to either extend beyond the container, causing the layout to break or scrollbars to appear, or the text is clipped by the parent container and content is lost.
This create difficulties for people who rely on text to be resized without loss of the content.


## To resolve

Most recent govuk-frontend should containe fix for this issue panel heading
https://github.com/alphagov/govuk-frontend/pull/2347.
Or apply `.text-overflow` class on element

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
  when text is resized [named] text is cut off and so may not display the entire information intended.
```

### Milestones

```
  when text is resized, content is lost. This fails WCAG 2.1 success criterion 1.4.4 Resize text 
  date: TBC

```

## References

[govuk-font mixin - GOV.UK  Frontend](https://frontend.design-system.service.gov.uk/sass-api-reference/#govuk-typography-responsive-usage)

[Understanding Success Criterion 1.4.4 Resize text ](https://www.w3.org/TR/UNDERSTANDING-WCAG20/visual-audio-contrast-scale.html)
