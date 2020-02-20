# Design and usability quick wins

Avoid the most common GOV.UK Design System and usability issues that we see when auditing services.

## Page title format

Page titles should follow the [HMRC format](https://design.tax.service.gov.uk/hmrc-design-patterns/page-title/):

> “[page name] - [service name] - GOV.UK”

## Using the correct input type

If you are asking for particular types of information, using the correct `type` attribute will mean that people using touch screens will get an on-screen keyboard more suited to what they need to enter. For example, using `type="email"` rather than `type="text"` will mean the `@` symbol will be immediately visible on the keyboard, rather than hidden away. This is especially advantageous for screen reader users, as switching keyboard views takes much longer.

Some input types are more accessible than others due to assistive technology support. For now we recommend looking at [`email`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/email), [`number`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/number), [`search`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/search), [`tel`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/tel), [`url`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/url)

Avoid using `maxlength` as it will not announce to assistive technology that there is a maximum character length, or prompt them to stop typing once the `maxlength` value has been reached.

## Using `fieldset`  for radios, checkboxes and dates

Generally you should just use `fieldset` for the instances above. Do not be tempted to use them for single checkboxes as it is a grouping element. When you use a `fieldset` make sure you also include an appropriate `legend` as the first element within.

## Combine `h1` with `legend` or `label` elements

If you are only asking one question on the page you should try and combine the `h1` with the question’s `label` or `legend`. This means that people using screen readers do not hear the same copy repeated more than necessary.

### `legend + h1`

With `legend`, the `h1` sits inside the `legend`:

    <legend><h1>Page title</h1></legend>

### `h1 + label`

With `label`, the `h1` wraps the `label`:

    <h1><label>Page title</label></h1>

## Keep your `legend` and `label` elements clean

Do not put hint copy or error messages inside the `legend` or `label`. You should follow the Design Patterns and use an `aria-describedby` attribute instead.

They will still get announced but some screen readers will add a slight pause to differentiate between them, and the label will be less noisy when the user is navigating by form control.

## Follow the patterns for error handling

Check you have followed the [error patterns](https://design-system.service.gov.uk/components/error-summary/), including:
- including an error summary between the back link and the `h1`
- only included one error per input
- prefixing the error message above the input with *‘Error:’* to ensure it is recognised as an error

## Use the latest Check Your Answers pattern

The [latest pattern](https://design-system.service.gov.uk/patterns/check-answers/) uses a `dl`. Do not be tempted to use a `table` for this. It is not tabular data and using a `table` will likely cause layout issues when it comes to smaller screens or zoomed text.

## Use headings with correct nesting

Used correctly, headings will give a person using assistive technology a pre-made table of contents for your page. If you nest headings correctly they will be able to see relationships between various sections. You should not skip heading levels, so if you have used an `h2` your next heading should be either another `h2` (for information at the same level) or an `h3` for a subsection.

CSS should then be used for styling but keep in mind the visual hierarchy should follow the element hierarchy.

Success criteria for [WCAG 2.0 (A) 1.3.1 Info and Relationships](https://www.w3.org/WAI/WCAG21/Understanding/info-and-relationships.html).

## Using links as buttons

If you have used links but added CSS classes to make them look like buttons, you should add a `role="button"` attribute to them and initialise the [JavaScript polyfill](https://github.com/alphagov/govuk-frontend/blob/master/src/govuk/components/button/button.js) to ensure they act like buttons. This makes sure that the link is announced as and behaves like a button and responds to the <kbd>spacebar</kbd> key press appropriately (given the it is initialised by running `GOVUK.shimLinksWithButtonRole.init();`).

Success criteria for [WCAG 2.1 (A) 4.1.2 Name, role, value](https://www.w3.org/TR/UNDERSTANDING-WCAG20/ensure-compat-rsv.html).
