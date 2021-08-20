# Issue: Insufficient contrast (legacy styles)

With the arrival of WCAG 2.1 many of the colour palette and focus styles used in the design systems needed to be updated to be compliant.

Low colour contrast can affect users with various vision related conditions and can cause unnessessry eye strain when using the service.

If your service is using an old version of a library (eg pre Assets Frontend 3.14.0) then you should look at updating to the latest version as soon as possible.

The legacy styles affected include:
- link focus state
- input focus state
- input error state
- input error focus state

There is a [blog post](https://designnotes.blog.gov.uk/2019/07/29/weve-made-the-gov-uk-design-system-more-accessible/) which summarises what the old vs new styles look like.

## To resolve

Either:
- update Assets Frontend to the latest version (note, if you were using the [patch code](https://gist.github.com/adamliptrot-oc/f77250a6f69fb31fabd935e2002f4964) for earlier versions of Assets Frontend, you should remove this as this was incorporated into AF 3.14.0)
- migrate your service to Gov Frontend / HMRC Frontend

## Labels
- wcag
- wcag 1.4.3 (AA)
- wcag 4.1.3 (AA)

## Report

| Status | Level | Issue | Success Criterion |
| ------ | ----- | ----- | ----------------- |
| 🔴 (H) | A    | [#issue](): Contrast of form controls | 1.4.11 Non-text contrast |
| 🔴 (H) | A    | [#issue](): Contrast of links | 1.4.3 Contrast (minimum)|

## Statement

### Accessibility problems

```
some of the colours used may make it difficult to differentiate elements or see where the focus of the keyboard is at any one time
```

### Milestones

```
contrast of some elements is too low and does not meet the required levels. This fails WCAG 2.1 success criterion 1.4.11 Non-text contrast and 1.4.3 Contrast (minimum)
```
## References

[Understanding focus state styles - Gov.UK Design System](https://design-system.service.gov.uk/get-started/focus-states/)

[We’ve made the GOV.UK Design System more accessible - Design in government blog](https://designnotes.blog.gov.uk/2019/07/29/weve-made-the-gov-uk-design-system-more-accessible/)

[Understanding Success Criterion 1.4.11: Non-text Contrast](https://www.w3.org/WAI/WCAG21/Understanding/non-text-contrast.html)

[Understanding Success Criterion 1.4.3: Contrast (Minimum)](https://www.w3.org/WAI/WCAG21/Understanding/contrast-minimum.html)
