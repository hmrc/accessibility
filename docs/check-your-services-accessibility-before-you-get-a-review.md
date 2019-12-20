# Check your service’s accessibility before you get a review

The accessibility of your service is your team’s responsibility.

Before you have an in-house accessibility review or a formal external audit by Digital Accessibility Centre (DAC), you should check the accessibility of your service.

To help you we’ve listed some things you can check for throughout development.

Carrying out these checks will help you:
- improve the accessibility of your service
- save time by eliminating issues early
- make sure it meets
 the [public sector accessibility regulations](https://confluence.tools.tax.service.gov.uk/display/DSA/Regulations+to+make+public+sector+websites+and+mobile+applications+accessible)

## When should you consider accessibility

Accessibility is a user need. You should be thinking about the access needs of your users from the start of design, research and development. Do not leave it until the end.

### Definition of Ready

Designers should make sure accessibility is part of what they do. Keep content, flows and screens simple. This helps people with learning disabilities, mental health conditions, cognitive impairments and autism.

To make sure accessibility is part of the story, include:

- human readable URLs
- page titles that are different to headings to stop personally identifiable information being stored in Google Analytics, for example ‘What is Gordon’s date of birth?’ would need to be ‘What is the child’s date of birth?’
- reading order when there are differences between what is visible and what is read out loud
- hidden text for screen readers, where necessary
- colours and colour contrast
- if something is tabular data or not and suggest HTML solutions or patterns
- line spacing and whitespace
- non-breaking spaces and hyphens to stop unwanted word wrapping
- simple, easy to understand content that meets the content style guide
- how will this look on mobile (remember a zoomed in desktop screen will effectively become a mobile viewport)
- how this will work without javascript
- if the journey more than a few screens and whether we allow the user to save and come back later
- whether people using assistive technology might need extra time to complete tasks
- accommodation for screen zoom and whether the screen still makes sense at +200%
- secondary methods to convey meaning rather than just colour alone
- reasonable distance between related elements, rather than remote from each other

Most of this should be part of standard components but may help if it is part of a ticket.

### Definition of Done

As an absolute bare minimum, we recommend following these three tasks:

1. Make sure each page contains valid HTML.
2. Make sure each page is free from WCAG errors.
3. Test each page is usable with at least one screen reader.

You should make sure these tasks are complete before you request an in-house audit. The best way to do this is to validate the HTML of each page. Use a tool like axe or Pa11y to test for WCAG errors as you’re test driving your service with a screen reader at the end of each sprint.

Most of this work can be done at your own desk. The assistive tech journeys are best done in the accessibility lab, if you have one in your Delivery Centre.

- make sure each page contains valid HTML
- make sure each page contains valid CSS
- make sure each page works without CSS
- make sure each page works without JS
- make sure the JS doesn’t throw errors
- provide appropriate context for screen readers where necessary
- remove all unnecessary markup and attributes
- check for any message file properties which may have leaked into the rendered view
- make sure each page is free from WCAG errors
- run each page through aXe, WAVE, or both, fixing any errors that are flagged
- check you can complete this journey without a mouse
- check you can complete this journey without a screen
- check you can complete this journey on a mobile device
- test each page is usable with at least one screen reader
- test the journey is successful with Voice Control on macOS
- test the journey is successful with Voice Control on iOS
- test the journey is successful with VoiceOver on macOS
- test the journey is successful with VoiceOver on iOS
- test the journey is successful with JAWS on Windows
- test the journey is successful with NVDA on Windows
- test the journey is successful with Orca on Ubuntu
- test the journey is successful with Dragon
- test the journey is successful with ZoomText on Windows
- test the journey is successful with Zoom enabled on macOS
- test the journey is successful with Zoom enabled on iOS

## Most common accessibility failings

Ideally you should test your service regularly in the accessibility lab, using a range of devices. This will get you a long way towards avoiding the most common accessibility failings that we see.

### Failure of WCAG 2.0 (A) 1.3.1 info and relationships

Most commonly caused by using unestablished patterns. Read more about this at [How to Meet Info and Relationships](https://www.w3.org/WAI/WCAG21/quickref/#info-and-relationships).

### Failure of WCAG 2.0 (A) 4.1.1 parsing

Most commonly caused by invalid HTML. Read more about this at [How to Meet Parsing](https://www.w3.org/WAI/WCAG21/quickref/#parsing).

### Not using the alphagov autocomplete

You should use the most up-to-date version of the [alphagov accessible autocomplete component](https://github.com/alphagov/accessible-autocomplete), rather than the ones which are inaccessible with screen readers.

### Details components not working with JAWS and Internet Explorer

This stops many users from accessing content. Content is presented in its open state, but announced as collapsed. This leads the user to think that there is content that they are not able to access. This happens when the [`details` polyfill](https://github.com/hmrc/assets-frontend/blob/master/assets/javascripts/modules/details.polyfill.js) has not been used or initialised.

### Tabs

It’s best to not use tabs, because they are only partially implemented and do not follow the [design system](https://design-system.service.gov.uk/components/tabs/). The behaviour of tabs is not shown correctly to screen readers, so this fails [WCAG 2.0 (A) 4.1.2 Name, role, value](https://www.w3.org/TR/UNDERSTANDING-WCAG20/ensure-compat-rsv.html).

### Ambiguous links

Link text such as ‘Change’, ‘Edit’, ‘Delete’, and ‘Remove’ are not always descriptive when read out of context. Sometimes the additional unique text is missing such as “Change **‘name’**”.
[WCAG 2.1 (A) 2.4.4: Link Purpose](https://www.w3.org/WAI/WCAG21/Understanding/link-purpose-in-context.html).

### Not warning users that they are about to be timed out

Service time-outs are often present, but do not warn the user that they are about to be timed out. You must also allow the user to extend their time within the service. [WCAG 2.1 (A) 2.2.1: Timing Adjustable](https://www.w3.org/WAI/WCAG21/Understanding/timing-adjustable.html).

### The autocomplete attribute

This is usually set to ‘off’ on the `form` element, but you will want to turn it on for certain input fields, or you risk failing [WCAG 2.1 (AA) 1.3.5: Identify input purpose](https://www.w3.org/WAI/WCAG21/Understanding/identify-input-purpose.html). Further information available: [Autofill - HTML Standard](https://html.spec.whatwg.org/multipage/form-control-infrastructure.html#autofill).

### Contrast on focus states

The new colour contrast of the focus states is not always used. This fails [WCAG 2.1 (AA) 1.4.11: Non-Text Contrast](https://www.w3.org/WAI/WCAG21/Understanding/non-text-contrast.html).

### Error skip links

These do not always function correctly, failing [WCAG 2.1 (A) 2.4.1: Bypass Blocks](https://www.w3.org/WAI/WCAG21/Understanding/bypass-blocks.html).

### Error messages

There are often non-descriptive error messages such as ‘This field is required’. This type of vague message is not helpful for the user. [WCAG 2.1 (A) 3.3.1: Error Identification](https://www.w3.org/WAI/WCAG21/Understanding/error-identification.html)

### Duplicate page titles and H1s

Page titles and `h1`s are often the same on multiple pages throughout a section of the service. You must use a unique page title on every page, as shown in the [page title pattern](https://design.tax.service.gov.uk/hmrc-design-patterns/page-title/). [WCAG 2.1 (A) 2.4.2 Page Titled](https://www.w3.org/WAI/WCAG21/Understanding/page-titled.html).

### Focus order of page items is confusing

These should maintain a logical order. For example, do not focus on an edit link before the section heading tells the user what they are editing. [WCAG 2.1 (A) 2.4.3 Focus Order](https://www.w3.org/WAI/WCAG21/Understanding/focus-order.html).

### Using the presentational `<hr/>` element as a decoration

This needs an `aria-hidden` to prevent screen readers from trying to interact with it.

### Service not working if JavaScript is unavailable

Progressive enhancement must be used to provide a usable service at all times. The GOV.UK Service Manual offers guidance on this: [Building a resilient frontend using progressive enhancement](https://www.gov.uk/service-manual/technology/using-progressive-enhancement).

## Most common design and usability issues

These are the most common GOV.UK Design System and usability issues that we see.

### Page title

[Page titles](https://design.tax.service.gov.uk/hmrc-design-patterns/page-title/) do not always use the HMRC pattern of ‘Page purpose - service name - GOV.UK’. Page titles and `h1`s often do not mirror each other.

### Hint text

Hint text is often not announced by screen readers when using the <kbd>tab</kbd> key or list of form elements. This is because `aria-describedby` has not been used on the input field.

### Incorrect input type

When the incorrect input type is used, the wrong software keyboard is shown on mobile devices. You can research which type has which keyboard on MDN Web Docs:
- [`email`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/email)
- [`number`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/number)
- [`search`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/search)
- [`tel`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/tel)
- [`url`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/url)

### Fieldset and legend not grouped elements

The `fieldset` and `legend` is often misused for a single field and not grouped elements.

### Error handling requirements not followed

The [error handling requirements](https://design-system.service.gov.uk/components/error-summary/) are not always followed. For example, the phrase ‘Error:’ is sometimes not inserted at the start of the page title.

### H1 not inside the legend

Groups of `radio` buttons often include a hidden `legend` that duplicates the `h1`. Instead, you should place the `h1` inside the `legend`.

### Legend includes H1 and hint text

Sometimes a page has a `legend` or a `label` that contains the `h1` and a paragraph of hint text. This can be very verbose for screen reader users.

### Tables on check you answers pages

Some [Check your answers](https://design-system.service.gov.uk/patterns/check-answers/) pages use the old table-based layout. Instead, you should use the established definition list.

### Sub-headings not marked up properly

Sub-headings are marked up as bold rather than appropriate heading level. This is a failure of [WCAG 2.0 (A) 1.3.1 Info and Relationships](https://www.w3.org/WAI/WCAG21/Understanding/info-and-relationships.html).

### JavaScript handler not used for buttons

When a role of button is used, JavaScript handler should be used. This makes sure that the link behaves like a button and responds to the <kbd>spacebar</kbd> key press. This handler is in [govuk-frontend](https://github.com/alphagov/govuk-frontend/blob/master/src/govuk/components/button/button.js). [WCAG 2.1 (A) 4.1.2 Name, role, value](https://www.w3.org/TR/UNDERSTANDING-WCAG20/ensure-compat-rsv.html).

### Error summaries appearing after the H1

Error summaries sometimes appear after the `h1`. Use the [error summary component](https://design-system.service.gov.uk/components/error-summary/) at the top of a page, after the Back link and before the `h1`.

## Make use of automated helpers

### Stage one: browser plugins

These are tools that any member of the team can use at their desk while they’re testing the service. These examples are all for Chrome, but they’re available for Firefox as well.

While there are many plugins listed here, you don’t have to use all of them. With the exception of Toggle JavaScript, they do a lot of the same things but there is some overlap. Take them all for a spin, see which ones you prefer.

#### ARC Toolkit

> “The ARC Toolkit is a set of accessibility tools which aids developers in identifying accessibility problems and features for WCAG 2.0, WCAG 2.1, EN 301 549, and Section 508.”

Available for [Chrome](https://chrome.google.com/webstore/detail/arc-toolkit/chdkkkccnlfncngelccgbgfmjebmkmce).

#### axe - Web Accessibility Testing

> “Accessibility checker for WCAG 2 and Section 508 accessibility. Find accessibility defects on your website or web application by using the axe Chrome extension. Drop the axe on your accessibility defects!”

Available for [Chrome](https://chrome.google.com/webstore/detail/axe-web-accessibility-tes/lhdoppojpmngadmnindnejefpokejbdd) or [Firefox](https://addons.mozilla.org/en-US/firefox/addon/axe-devtools/?src=search).

#### Siteimprove Accessibility Checker

> “The Siteimprove Accessibility Checker is your tool to evaluate any web page for accessibility issues at any given time.”

Available for [Chrome](https://chrome.google.com/webstore/detail/siteimprove-accessibility/efcfolpjihicnikpmhnmphjhhpiclljc) or [Firefox](https://addons.mozilla.org/en-US/firefox/addon/digital-certainty-index/?src=search).

#### WAVE Evaluation Tool

> “WAVE is a web accessibility evaluation tool developed by WebAIM.org. It provides visual feedback about the accessibility of your web content by injecting icons and indicators into your page. No automated tool can tell you if your page is accessible, but WAVE facilitates human evaluation and educates about accessibility issues.”

Available for [Chrome](https://chrome.google.com/webstore/detail/wave-evaluation-tool/jbbplnpkjmmeebjpijfedlgcdilocofh) or [Firefox](https://addons.mozilla.org/en-US/firefox/addon/wave-accessibility-tool/).

#### Web Developer

> “The Web Developer extension adds a toolbar button to the browser with various web developer tools.”

Available for [Chrome](https://chrome.google.com/webstore/detail/web-developer/bfbameneiokkgbdmiekhjnmfkcnldhhm) or [Firefox](https://addons.mozilla.org/en-US/firefox/addon/web-developer/?src=search).

#### Webhint

> “Quickly test your website to see if there are any issues with accessibility, browser compatibility, security, performance and more.”

Available for [Chrome](https://chrome.google.com/webstore/detail/webhint/gccemnpihkbgkdmoogenkbkckppadcag) or [Firefox](https://addons.mozilla.org/en-US/firefox/addon/webhint/?src=search).

#### Easily disable JavaScript

Available for [Chrome](https://chrome.google.com/webstore/detail/toggle-javascript/cidlcjdalomndpeagkjpnefhljffbnlo) or [Firefox](https://addons.mozilla.org/en-US/firefox/addon/quick-js-switcher/?src=search)

### Stage two: prototyping tools

It’s good practice to write good, error-free code. And once you’re out testing your prototype with users who have access needs, you’re going to be wanting well-formed HTML with zero errors, and as few accessibility problems as possible. While these tools won’t make your prototype bulletproof, they’ll go a long way towards fixing your mistakes and guiding you in the right direction.

#### HTMLHint

> “The static code analysis tool you need for your HTML.”

Available at [github.com/htmlhint/HTMLHint](https://github.com/htmlhint/HTMLHint).

#### ESLint

> “A fully pluggable tool for identifying and reporting on patterns in JavaScript.”

Available at [github.com/eslint/eslint](https://github.com/eslint/eslint).

#### Stylelint

> “A mighty, modern linter that helps you avoid errors and enforce conventions in your styles.”

Available at [github.com/stylelint/stylelint](https://github.com/stylelint/stylelint)

#### Stylelint-a11y

> “Plugin for Stylelint with a11y rules.”

Available at [github.com/YozhikM/stylelint-a11y](https://github.com/YozhikM/stylelint-a11y).

#### Husky

> “Git hooks made easy.”

Available at [github.com/typicode/husky](https://github.com/typicode/husky).

#### Prettier

> “Prettier is an opinionated code formatter.”

Available at [github.com/prettier/prettier](https://github.com/prettier/prettier).

### Stage three: Continuous Integration tools

Once your service is deployed to staging you’ll want to be running tests against it. We have the following available which you can use.

#### Accessibility testing library

> “This library can be used to integrate a number of automated tools into Selenium UI test repositories to help identify a number of potential accessibility issues in web front-ends.”

Available at [hmrc/accessibility-testing-library](https://github.com/hmrc/accessibility-testing-library).

#### Accessibility assessment

> “This project contains the `Dockerfile` and images assets required to create the `accessibility-assessment` image that is used in CI for the assessment of captured pages using `axe`, `pa11y` and `vnu`. The violations found during the assessment are pushed to ELK.”

Available at [hmrc/accessibility-assessment](https://github.com/hmrc/accessibility-assessment).
