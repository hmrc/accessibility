# Issue: Type attribute incorrect

For certain fields it is better to use specific `type` attributes rather than the default `type="text"`.

Using these attributes will provide good support for specific keyboards on mobile and touchscreen devices.

Additionally there are certain `type` attributes which should be avoided because of issues with support or implementation.

## To resolve

- for a field asking for an [email address](https://design-system.service.gov.uk/patterns/email-addresses/), use `type="email"`
- for a field asking for a [phone number](https://design-system.service.gov.uk/patterns/telephone-numbers/), use `type="tel"`
- for date fields, the [date pattern](https://design-system.service.gov.uk/components/date-input/) should be followed and plain `type="text"` inputs used along with `inputmode="numeric"` and `pattern="[0-9]*"`
- do not use `type="number"` as this has [several issues](https://design-system.service.gov.uk/components/text-input/#avoid-using-inputs-with-a-type-of-number), both from an accessibility and usability standpoint. Instead you should use `inputmode="numeric"` for whole numbers (along with `pattern="[0-9]*"` for legacy support).
- for decimal numbers, due to issues with browser support you should use a plain `type="text"` with no `inputmode`.

Note, when adding a `pattern` attribute or certain `type` attributes like "email" or "url", this will trigger HTML5 form validation due to intrinsic constraints. As this is not desirable behaviour, to stop this from happening you should add a `novalidate` attribute to the `form` element.

## Labels
- text input
- date input
- telephone numbers
- email addresses

## Report

| Priority | Issue |
| -------- | ----- |
| 🔴 P1     | [#issue](): Type attribute incorrect |

## Reference

[Email address - Gov.UK Design System](https://design-system.service.gov.uk/patterns/email-addresses/)

[Telephone numbers - Gov.UK Design System](https://design-system.service.gov.uk/patterns/telephone-numbers/)

[Date pattern - Gov.UK Design System](https://design-system.service.gov.uk/components/date-input/)

[Guidance on asking for numbers - Gov.UK Design System](https://design-system.service.gov.uk/components/text-input/#avoid-using-inputs-with-a-type-of-number)

[Why the GOV.UK Design System team changed the input type for numbers - Technology in government blog](https://technology.blog.gov.uk/2020/02/24/why-the-gov-uk-design-system-team-changed-the-input-type-for-numbers/)

[Issues with lack of decimal place presented on `inputmode="decimal"` virtual keyboards - Gov.UK Design System](https://github.com/alphagov/govuk-design-system/pull/1279#issuecomment-639467489)