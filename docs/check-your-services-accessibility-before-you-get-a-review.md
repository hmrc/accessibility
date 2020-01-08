# Check the accessibility of your service before you get a review

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
- page titles that are the same as the `h1` heading (but be aware of the [Personally identifiable information](https://design.tax.service.gov.uk/hmrc-design-patterns/page-title/#personally-identifiable-information) caveat)
- reading order when there are differences between what is visible and what is read out loud
- hidden text for screen readers, where necessary
- colours and colour contrast
- if something is tabular data or not and suggest HTML solutions or patterns
- the right design patterns to provide the user with consistent line spacing and whitespace
- non-breaking spaces and hyphens to stop unwanted word wrapping
- simple, easy to understand content that meets the content style guide
- how will this look on mobile (remember a zoomed in desktop screen will effectively become a mobile viewport)
- how this will work without javascript
- if the journey is more than a few screens and whether we allow the user to save and come back later
- whether people using assistive technology might need extra time to complete tasks
- accommodation for screen zoom and whether the screen still makes sense at +200%
- secondary methods to convey meaning rather than just colour alone
- reasonable distance between related elements, rather than remote from each other

Most of this should be part of standard components but may help if it is part of a ticket.

### Definition of Done

As an absolute bare minimum, we recommend following these three tasks:

1. Make sure each page contains valid HTML.
2. Make sure each page is free from WCAG errors.
3. Test each page with a screen reader.

You should make sure these tasks are complete before you request an in-house audit. The best way to do this is to validate the HTML of each page. Use a tool like [axe](https://github.com/dequelabs/axe-core) or [Pa11y](https://github.com/pa11y/pa11y) to test for WCAG errors. Test some user journeys with a screen reader at the end of each sprint.

#### How you can test your service

Most of this work can be done at your own desk. The assistive tech journeys are best done in the accessibility lab, if you have one in your Delivery Centre.

##### Code quality

- make sure each page contains valid HTML
- make sure each page contains valid CSS
- make sure each page works without CSS
- make sure each page works without JS
- make sure the JS doesn’t throw errors
- remove all unnecessary markup and attributes
- check for any message file properties which may have leaked into the rendered view
- make sure each page is free from WCAG errors
- run each page through tools like axe and Pa11y, fixing any errors that are flagged

##### Usability

- provide appropriate context for screen readers where necessary
- check you can complete this journey without a mouse
- check you can complete this journey without a screen
- check you can complete this journey on a mobile device
- test each page is usable with **at least one** screen reader (see below)
- test each page is usable with **at least one** screen magnifier (see below)
- test each page is usable with **at least one** voice controller (see below)

##### Screen readers

- test the journey is successful with VoiceOver on macOS
- test the journey is successful with VoiceOver on iOS
- test the journey is successful with JAWS on Windows
- test the journey is successful with NVDA on Windows (if you are on Linux try Orca)

##### Screen magnifiers

- test the journey is successful with ZoomText on Windows
- test the journey is successful with Zoom enabled on macOS
- test the journey is successful with Zoom enabled on iOS

##### Voice control

- test the journey is successful with Dragon
- test the journey is successful with Voice Control

## Accessibility quick wins

​Ideally you should test your service regularly in the accessibility lab, using a range of devices. This will get you a long way towards avoiding the most common accessibility failings.

### Use the approved patterns and components

Make sure your service has used patterns and components from [GDS](https://design-system.service.gov.uk/) and [HMRC](https://design.tax.service.gov.uk/hmrc-design-patterns/) as these have been tested both for accessibility and browser and device support.

If your service uses patterns not in one of these libraries you should do additional work to ensure they work as needed.

Read more about this at [How to Meet Info and Relationships](https://www.w3.org/WAI/WCAG21/quickref/#info-and-relationships).

#### Use the alphagov autocomplete component

Rather than using `select` inputs for long lists, consider using the latest version of the [autocomplete component](https://github.com/alphagov/accessible-autocomplete). This is not currently in the Design System as it is a complex component, but it is the preferred way of picking an item from a long list of options. Do not use other third-party variants.

#### Make sure you initialise any details components

The [details component](https://design-system.service.gov.uk/components/details/) is a native browser control, but is not supported in some older browsers (most notably IE 11) and some assistive technology (JAWS) without the use of a [polyfill](https://github.com/hmrc/assets-frontend/blob/master/assets/javascripts/modules/details.polyfill.js).

You can initialise the component by adding the following code in your JavaScript.

    GOVUK.details.init();

#### Avoid using tabs

True tabs are difficult to correctly implement in an accessible manner. Whilst there is a tabs pattern in the Design System, we do not recommend their use currently and they have been marked as Experimental for this reason. If you feel you need to use tabs, contact one of the accessibility team.

Success criteria for [WCAG 2.0 (A) 4.1.2 Name, role, value](https://www.w3.org/TR/UNDERSTANDING-WCAG20/ensure-compat-rsv.html).

#### Tell users if they are about to be timed out of a session

Most services have some sort of session timeout. Before a user is redirected to the timeout page they should be given both a warning that it is about to happen and the option to extend their session. There is an [HMRC timeout dialog component](http://hmrc.github.io/assets-frontend/patterns/help-users-when-we-time-them-out-of-a-service/index.html) for this; [Github repo](https://github.com/hmrc/hmrc-frontend/tree/master/src/components/timeout-dialog).

Success criteria for [WCAG 2.1 (A) 2.2.1: Timing Adjustable](https://www.w3.org/WAI/WCAG21/Understanding/timing-adjustable.html).

#### Error summary and links

Error summaries should receive focus when the page loads, to bring the error to the attention of people using assistive technology and also help people who are only using a keyboard. Additionally, when clicking a link in the error summary the focus should be placed in either the input (in the case of text inputs) or on the first input in a group (for radios, checkboxes and date inputs).

Success criteria for [WCAG 2.1 (A) 2.4.1: Bypass Blocks](https://www.w3.org/WAI/WCAG21/Understanding/bypass-blocks.html).

#### Error messages

Make sure your error messages [follow the standard](https://design-system.service.gov.uk/components/error-message/#be-clear-and-concise) and that you help prevent users seeing the error message in the first place by providing enough information around formatting and data required.

Success criteria for [WCAG 2.1 (A) 3.3.1: Error Identification](https://www.w3.org/WAI/WCAG21/Understanding/error-identification.html).

### Validate your HTML

If HTML is not valid it will cause parsing issues for assistive technology (among other side-effects). Many accessibility auditing plugins (like AXE) will check for invalid HTML alongside accessibility issues.

Read more about this at [How to Meet Parsing](https://www.w3.org/WAI/WCAG21/quickref/#parsing).

### Check link text is unique when taken out of context

Screen readers can list all link text in a dialog to enable the user to quickly access links on a page. If more than one link has the same text as a link but point to different URLs this can be very confusing. This is easy to miss on pages where you have repeating content (such as add-to-a-list) or are reviewing answers. Generally the fix is to add additional hidden content to add context for screen readers.

Success criteria for [WCAG 2.1 (A) 2.4.4: Link Purpose](https://www.w3.org/WAI/WCAG21/Understanding/link-purpose-in-context.html).

### Use an autocomplete attribute on inputs for personal data

If we are asking a user for data which they have likely entered elsewhere (like name or address) then we can help them fill in forms by using `autocomplete` attributes on form fields. This will prompt the browser to fill in fields we mark up in this way. Use the [correct attributes](https://html.spec.whatwg.org/multipage/form-control-infrastructure.html#autofill) to tell the browser which data to put where.

Success criteria for [WCAG 2.1 (AA) 1.3.5: Identify input purpose](https://www.w3.org/WAI/WCAG21/Understanding/identify-input-purpose.html).

### Contrast and focus states

If you are using Gov Frontend, the latest [WCAG 2.1 updates for colour and focus states](https://designnotes.blog.gov.uk/2019/07/29/weve-made-the-gov-uk-design-system-more-accessible/) are in place already. If you are using Assets Frontend, then you may need to add the new focus states and colour updates for [AF 3.11](https://gist.github.com/adamliptrot-oc/f77250a6f69fb31fabd935e2002f4964) or [AF 4.11](https://gist.github.com/adamliptrot-oc/f77250a6f69fb31fabd935e2002f4964).

Success criteria for [WCAG 2.1 (AA) 1.4.11: Non-Text Contrast](https://www.w3.org/WAI/WCAG21/Understanding/non-text-contrast.html).

### `h1` and page title should be the same

The visible `h1` on the page and the page title (in the browser tab) should be the same. However you should also make sure that the pages which follow each other have different titles/`h1` so when the user navigates they know they have moved to a different page and the last page hasn't just reloaded. See the [page title pattern](https://design.tax.service.gov.uk/hmrc-design-patterns/page-title/) for more information.

Success criteria for [WCAG 2.1 (A) 2.4.2 Page Titled](https://www.w3.org/WAI/WCAG21/Understanding/page-titled.html).

### Check focus order

This is best checked with a screen reader. Make sure that when traversing the page the information you are presented with comes in a logical order. For example, an edit link doesn't come before the thing you are going to edit is announced.

Success criteria for [WCAG 2.1 (A) 2.4.3 Focus Order](https://www.w3.org/WAI/WCAG21/Understanding/focus-order.html).

### Hide `hr` from screen readers

If you have used the `hr` element you should add `aria-hidden="true"` to it. Otherwise screen readers will attempt to interact with it. Also check that if you are using the `hr` to segment content that this has been done in some semantic way in the HTML as well.

### Make sure your service works without JavaScript

One of the [core principles of building services for the government](https://www.gov.uk/service-manual/technology/using-progressive-enhancement) is reaching as many people as possible by using progressive enhancement to build a resilient frontend. With this in mind any service should work without JavaScript and have appropriate fallbacks in place where it is used and is not available.

## Design and usability quick wins

Avoid the most common GOV.UK Design System and usability issues that we see when auditing services.

### Page title format

Page titles should follow the [HMRC format](https://design.tax.service.gov.uk/hmrc-design-patterns/page-title/):

> “[page name] - [service name] - GOV.UK”

### Using the correct input type

If you are asking for particular types of information, using the correct `type` attribute will mean that people using touch screens will get an on-screen keyboard more suited to what they need to enter. For example, using `type="email"` rather than `type="text"` will mean the `@` symbol will be immediately visible on the keyboard, rather than hidden away. This is especially advantageous for screen reader users, as switching keyboard views takes much longer.

Some input types are more accessible than others due to assistive technology support. For now we recommend looking at [`email`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/email), [`number`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/number), [`search`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/search), [`tel`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/tel), [`url`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/url)

### Using `fieldset`  for radios, checkboxes and dates

Generally you should just use `fieldset` for the instances above. Do not be tempted to use them for single checkboxes as it is a grouping element. When you use a `fieldset` make sure you also include an appropriate `legend` as the first element within.

### Combine `h1` with `legend` or `label` elements

If you are only asking one question on the page you should try and combine the `h1` with the question’s `label` or `legend`. This means that people using screen readers do not hear the same copy repeated more than necessary.

#### `legend + h1`
With `legend`, the `h1` sits inside the `legend`:

    <legend><h1>Page title</h1></legend>

#### `h1 + label`

With `label`, the `h1` wraps the `label`:

    <h1><label>Page title</label></h1>

### Keep your `legend` and `label` elements clean

Do not put hint copy or error messages inside the `legend` or `label`. You should follow the Design Patterns and use an `aria-describedby` attribute instead.

They will still get announced but some screen readers will add a slight pause to differentiate between them, and the label will be less noisy when the user is navigating by form control.

### Follow the patterns for error handling

Check you have followed the [error patterns](https://design-system.service.gov.uk/components/error-summary/), including:
- including an error summary between the back link and the `h1`
- only included one error per input
- prefixing the error message above the input with *‘Error:’* to ensure it is recognised as an error

### Use the latest Check Your Answers pattern

The [latest pattern](https://design-system.service.gov.uk/patterns/check-answers/) uses a `dl`. Do not be tempted to use a `table` for this. It is not tabular data and using a `table` will likely cause layout issues when it comes to smaller screens or zoomed text.

### Use headings with correct nesting

Used correctly, headings will give a person using assistive technology a pre-made table of contents for your page. If you nest headings correctly they will be able to see relationships between various sections. You should not skip heading levels, so if you have used an `h2` your next heading should be either another `h2` (for information at the same level) or an `h3` for a subsection.

CSS should then be used for styling but keep in mind the visual hierarchy should follow the element hierarchy.

Success criteria for [WCAG 2.0 (A) 1.3.1 Info and Relationships](https://www.w3.org/WAI/WCAG21/Understanding/info-and-relationships.html).

### Using links as buttons

If you have used links but added CSS classes to make them look like buttons, you should add a `role="button"` attribute to them and initialise the [javascript polyfill](https://github.com/alphagov/govuk-frontend/blob/master/src/govuk/components/button/button.js) to ensure they act like buttons. This makes sure that the link is announced as and behaves like a button and responds to the <kbd>spacebar</kbd> key press appropriately.

Success criteria for [WCAG 2.1 (A) 4.1.2 Name, role, value](https://www.w3.org/TR/UNDERSTANDING-WCAG20/ensure-compat-rsv.html).

## Make use of automated helpers

### Stage one: browser plugins

These are tools that any member of the team can use at their desk while they’re testing the service.

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
