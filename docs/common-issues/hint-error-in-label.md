# Issue: Hint or error message nested inside label or legend

Before aria was well supported this was common practice (and was part of the old component libraries), however now there are better ways of doing this which don't overload the label.

With nested hints or error messages inside labels or legends, these accessible names become overly long and less clear.

For screen-reader users, by using `aria-describedby` to programatically associate the copy with the form control this adds a pause after the label is read out so a clear boundary is heard. Additionally this also means that the accessible names of the form controls is much shorter in element lists.

For speech recognition users, the shorter accessible name means it is easier to target a specific control by using the full accessible name.

## To resolve

Follow the Gov.UK Design Patterns:
- [text input](https://design-system.service.gov.uk/components/text-input/)
- [fieldsets](https://design-system.service.gov.uk/components/fieldset/)
- [error messages](https://design-system.service.gov.uk/components/error-message/)

Move the hint and error messages out of the label or legend, assign each an `id` attribute and add an `aria-describedby` attribute to the `input` (in the case of single fields) or `fieldset` (in the case of a group) and reference the new `id`s in the aria.

## Report

| Priority | Issue |
|----------|-------|
| 🔴 P1    | [#issue]() Hint or error message nested inside label or legend |

## References

[Text input - GOV.UK Design System](https://design-system.service.gov.uk/components/text-input/)

[Fieldsets - GOV.UK Design System](https://design-system.service.gov.uk/components/fieldset/)

[Error messages - GOV.UK Design System](https://design-system.service.gov.uk/components/error-message/)