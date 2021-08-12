# Issue: Missing inputmode

Inputmodes are a useful hint for browsers to present the correct virtual keyboard for the required data. For example when asking for a number the device can use the inputmode to present a numeric keyboard.

Using this attribute saves the user addtional keystrokes which can be very helpful if the user has dexterity issues for example.

## To resolve

Typically the primary `inputmode` which will be used is `inputmode="numeric"` (along with `pattern="[0-9]*"` for legacy support). This should be used when asking for whole numbers only, such as dates.

Note, when adding a `pattern` attribute, this will trigger HTML5 form validation due to intrinsic constraints. As this is not desirable behaviour, to stop this from happening you should add a `novalidate` attribute to the `form` element.

Due to poor support in certain browsers, `inputmode="decimal"` should not be used, despite it being a good fit for currency fields. Using it could prevent a user from entering the correct information, so a plain `type="text"` field with no `inputmode` should be used.

The following should use the specific `type` attributes rather than the matching `inputmode` as these will have better support:
- email - use `type="email"`
- phone - use `type="tel"`

## Labels
- text input
- date input
- telephone numbers
- email addresses

## Report

| Priority | Issue |
| -------- | ----- |
| 🔴 P1     | [#issue](): Inputmode attribute missing |

## Statement

This is not a WCAG A/AA failure so it does not have to be included on the accessibility statement, but we strongly recommend resolving the issue to improve the usability of the service.

## Reference

[Email address - GOV.UK Design System](https://design-system.service.gov.uk/patterns/email-addresses/)

[Telephone numbers - GOV.UK Design System](https://design-system.service.gov.uk/patterns/telephone-numbers/)

[Date pattern - GOV.UK Design System](https://design-system.service.gov.uk/components/date-input/)

[Guidance on asking for numbers - GOV.UK Design System](https://design-system.service.gov.uk/components/text-input/#avoid-using-inputs-with-a-type-of-number)

[Why the GOV.UK Design System team changed the input type for numbers - Technology in government blog](https://technology.blog.gov.uk/2020/02/24/why-the-gov-uk-design-system-team-changed-the-input-type-for-numbers/)

[Issues with lack of decimal place presented on `inputmode="decimal"` virtual keyboards - Gov.UK Design System](https://github.com/alphagov/govuk-design-system/pull/1279#issuecomment-639467489)