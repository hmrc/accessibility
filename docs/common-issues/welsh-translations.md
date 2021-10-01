# Issue: Content not translated to Welsh [draft]

When switching the language of the page to Welsh some parts remain as English and are not marked up with the appropriate language attribute to differentiate them from the other content.

This is a WCAG 2.1 failure: 3.1.2: Language of Parts - [Understanding Success Criterion 3.1.2: Language of Parts](https://www.w3.org/WAI/WCAG21/Understanding/language-of-parts.html)

## To Resolve:

For each item if content that should not be translated into Welsh, add the english language attribute.

For all other content add the Welsh translation into the relevent configuration files.

### Skip link

The skip link is currently hard-coded as English in the Gov template in play-frontend-govuk.

However it is possible to send an override skip link to the @skipLinkBlock code block and with that send the correct translation. If doing this you should ensure you use the skip link component (as the template does) rather than developing your own version.

### Labels

* wcag
* wcag 3.1.2 (AA)
* welsh language toggle

## Report

| Status | Level | Issue | Success Criterion |
| ------ | ----- | ----- | ----------------- |
| 🟠 (M) | AA    | [#issue](): Content not translated to Welsh | 3.1.2 Language of parts |

## Statement

### Accessibility problems
```
  - description: When switching to the Welsh language version, the parts of the text is not translated. Additionally, the not translated text may not be pronounced correctly by screen readers.

```

### Milestones

```
  - description: Missing Welsh translations and appropriate language attributes on the copy can cause screen readers to mispronounce the copy. This fails WCAG 2.1 success criterion 3.1.2 Language of parts
  date: tbc
```

## References

[Language toggle - HMRC Design System](https://design.tax.service.gov.uk/hmrc-design-patterns/welsh-language-toggle/)

[Understanding Success Criterion 3.1.2: Language of Parts](https://www.w3.org/WAI/WCAG21/Understanding/language-of-parts.html)
