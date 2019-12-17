# In-house audit screener

To get the best out of an in-house accessibility review or a formal external audit by Digital Accessibility Centre (DAC), you can help yourselves by carrying out some checks beforehand.

To help you we've listed some things you can use to help you throughout development; from prototyping through to deployment.

The accessibility of your service is your responsibility.  Carrying out these checks will help improve the accessibility of your service, save time by eliminating issues early, and help ensure it meets
 the [public sector accessibility regulations](https://confluence.tools.tax.service.gov.uk/display/DSA/Regulations+to+make+public+sector+websites+and+mobile+applications+accessible).

<!-- TOC -->

- [In-house audit screener](#in-house-audit-screener)
  - [Three tasks for your Definition of Done](#three-tasks-for-your-definition-of-done)
  - [Most common accessibility failings](#most-common-accessibility-failings)
  - [Most common design and usability issues](#most-common-design-and-usability-issues)
    - [Further information about WCAG 2.1](#further-information-about-wcag-21)
  - [Make use of automated helpers](#make-use-of-automated-helpers)
    - [Stage one: browser plugins](#stage-one-browser-plugins)
    - [Stage two: prototyping tools](#stage-two-prototyping-tools)
    - [Stage three: Continuous Integration tools](#stage-three-continuous-integration-tools)

<!-- /TOC -->

## Three tasks for your Definition of Done

We recommend having the following three tasks in your team’s Definition of Done.

1. Make sure each page contains valid HTML.
2. Make sure each page is free from WCAG errors.
3. Test each page with at least one screen reader.

You should be positive that these tasks are completed to satisfaction before you consider requesting an in-house audit before your DAC audit. The best way to achieve that is to validate the HTML of each page and use a tool like axe or Pa11y to test for WCAG errors as you’re test driving your service with a screen reader at the end of each sprint.

## Most common accessibility failings

Ideally, you would be testing your service regularly in your accessibility lab, using the range of devices that are available. That will get you a long way towards avoiding the most common accessibility failings that we see.

- Failure of [WCAG 2.0 (A) 4.1.1 Parsing](https://www.w3.org/WAI/WCAG21/Understanding/parsing.html), due to invalid or badly-formed markup. Read more about this at [How to Meet Parsing](https://www.w3.org/WAI/WCAG21/quickref/#parsing).
- Services are not always using the [alphagov autocomplete](https://github.com/alphagov/accessible-autocomplete) component, or the most up-to-date version (the ones being used are inaccessible with screen readers).
- `details` components do not always work with JAWS and Internet Explorer, preventing many users from accessing the content. It is presented in its open state, but announced as collapsed, leading the user to believe that there is content that they are unable to access. This occurs when the [details polyfill](https://github.com/hmrc/assets-frontend/blob/master/assets/javascripts/modules/details.polyfill.js) has not been used or initialised.
- Ideally, refrain from using tabs, as they are only partially implemented and don’t follow the [design system](https://design-system.service.gov.uk/components/tabs/) — which itself is listed as experimental. Their behaviour is not exposed correctly to screen readers, failing [WCAG 2.0 (A) 4.1.2 Name, role, value](https://www.w3.org/TR/UNDERSTANDING-WCAG20/ensure-compat-rsv.html).
- Ambiguous links such as ‘Change’, ‘Edit’, ‘Delete’, and ‘Remove’ are not always descriptive when reading out of context. Sometimes the additional unique text is missing such as “Change **‘name’**”. [WCAG 2.1 (A) 2.4.4: Link Purpose](https://www.w3.org/WAI/WCAG21/Understanding/link-purpose-in-context.html).
- Service time-outs are often present, but do not warn the user that they are about to be timed out or allow the user to extend their time within the service. [WCAG 2.1 (A) 2.2.1: Timing Adjustable](https://www.w3.org/WAI/WCAG21/Understanding/timing-adjustable.html), [WCAG 2.1 (AAA) 2.2.6: Timeouts](https://www.w3.org/WAI/WCAG21/Understanding/timeouts.html).
- The `autocomplete` attribute is usually always set to ‘off’ on the `form` element, failing [WCAG 2.1 (AA) 1.3.5: Identify input purpose](https://www.w3.org/WAI/WCAG21/Understanding/identify-input-purpose.html).
- The new contrast of the focus states is not always used and therefore fails to meet [WCAG 2.1 (AA) 1.4.11: Non-Text Contrast](https://www.w3.org/WAI/WCAG21/Understanding/non-text-contrast.html).
- Error skip links do not always function correctly, failing [WCAG 2.1 (A) 2.4.1: Bypass Blocks](https://www.w3.org/WAI/WCAG21/Understanding/bypass-blocks.html).
- There are often non-descriptive error messages such as ‘This field is required’ that are not very helpful. [WCAG 2.1 (A) 3.3.1: Error Identification](https://www.w3.org/WAI/WCAG21/Understanding/error-identification.html), [WCAG 2.1 (AA) 3.3.3: Error Suggestion](https://www.w3.org/WAI/WCAG21/Understanding/error-suggestion.html).
- The [`legend`](https://html.spec.whatwg.org/multipage/form-elements.html#the-legend-element) is not always the first element within the [`fieldset`](https://html.spec.whatwg.org/multipage/form-elements.html#the-fieldset-element). This is invalid markup, failing [WCAG 2.0 (A) 4.1.1 Parsing](https://www.w3.org/TR/UNDERSTANDING-WCAG20/ensure-compat-parses.html).
- `fieldset` and `legend` not being used on date patterns, also known as not following the established [date input](https://design-system.service.gov.uk/components/date-input/) pattern.
- Page `title` and `h1`s remaining the same on multiple pages throughout a section of the service. Use a unique page title on every page, as instructed in the [page title](https://design.tax.service.gov.uk/hmrc-design-patterns/page-title/) pattern. [WCAG 2.1 (A) 2.4.2 Page Titled](https://www.w3.org/WAI/WCAG21/Understanding/page-titled.html).
- Focus order of page items is confusing. [WCAG 2.1 (A) 2.4.3 Focus Order](https://www.w3.org/WAI/WCAG21/Understanding/focus-order.html).
- Using the presentational `<hr/>` element as a decoration without adding `aria-hidden` to prevent screen readers from trying to interact with it.

## Most common design and usability issues

Of course, accessibility isn't just about compliance with regulations—your services have to be usable as well. Using the [GDS Design System](https://design-system.service.gov.uk/) and our own HMRC [Design Patterns library](https://design.tax.service.gov.uk/hmrc-design-patterns/) is the best way to create a usable and accessible service, but there are still plenty of wrong turns you can take.

These are the most common GOV.UK Design System and Usability issues that we see.

- The ‘(Optional)’ information is not always included within non-mandatory field labels.
- [Page title](https://design.tax.service.gov.uk/hmrc-design-patterns/page-title/)s do not always use the HMRC pattern of ‘Page purpose - service name - GOV.UK’.
- The [page title](https://design.tax.service.gov.uk/hmrc-design-patterns/page-title/) and `h1` often don’t mirror each other.
- Hint text isn’t announced by screen readers when using the <kbd>tab</kbd> key, or list of form elements because `aria-describedby` has not been used on the input field.
- Incorrect input `type` being used, which results in the wrong software keyboard being shown on mobile devices.
- The `fieldset` and `legend` is often used for a single field and not grouped elements.
- The [error handling requirements](https://design-system.service.gov.uk/components/error-summary/) are not always followed (for example, the phrase ‘Error:’ is sometimes not inserted at the start of the page title).
- Groups of `radio` buttons often include a hidden `legend` that duplicates the `h1` rather than placing the `h1` inside the `legend`.
- Sometimes a page has a `legend` that contains the `h1` **and** a paragraph of hint text which can be very verbose for screen reader users. This can also be the case where hint text is included within the `label`.
- Some [Check your answers](https://design-system.service.gov.uk/patterns/check-answers/) pages are using the ancient `table`-based layout rather than the established definition list.
- Sub headings are marked up as bold rather than appropriate heading level.
- When a role of `button` is used, JavaScript handler should be used to ensure that the link behaves like a button and responds to the <kbd>spacebar</kbd> key press. This handler was added in [govuk-frontend](https://github.com/alphagov/govuk-frontend/blob/master/src/govuk/components/button/button.js) quite some time ago. [WCAG 2.1 (A) 4.1.2 Name, role, value](https://www.w3.org/TR/UNDERSTANDING-WCAG20/ensure-compat-rsv.html).
- Error summaries sometimes appear after the `h1`. Use the [error summary component](https://design-system.service.gov.uk/components/error-summary/) at the top of a page, *before* the `h1`.

### Further information about WCAG 2.1

- [GOV.UK WCAG 2.1 Primer](https://alphagov.github.io/wcag-primer/#what-is-wcag-2-1)
- [What’s New in WCAG 2.1](https://www.w3.org/WAI/standards-guidelines/wcag/new-in-21/)
- [Techniques for WCAG 2.1](https://www.w3.org/WAI/WCAG21/Techniques/)
- [How to Meet WCAG (Quick Reference)](https://www.w3.org/WAI/WCAG21/quickref/)

## Make use of automated helpers

### Stage one: browser plugins

These are tools that any member of the team can use at their desk while they're testing the service. These examples are all for Chrome, but they’re available for Firefox as well.

While there are many plugins listed here, you don’t have to use all of them. With the exception of Toggle JavaScript, they do a lot of the same things but there is some overlap. Take them all for a spin, see which ones you prefer.

- [ARC Toolkit](https://chrome.google.com/webstore/detail/arc-toolkit/chdkkkccnlfncngelccgbgfmjebmkmce): The ARC Toolkit is a set of accessibility tools which aids developers in identifying accessibility problems and features for WCAG 2.0, WCAG 2.1, EN 301 549, and Section 508.
- [axe - Web Accessibility Testing](https://chrome.google.com/webstore/detail/axe-web-accessibility-tes/lhdoppojpmngadmnindnejefpokejbdd): Accessibility checker for WCAG 2 and Section 508 accessibility. Find accessibility defects on your website or web application by using the axe Chrome extension. Drop the axe on your accessibility defects!
- [Siteimprove Accessibility Checker](https://chrome.google.com/webstore/detail/siteimprove-accessibility/efcfolpjihicnikpmhnmphjhhpiclljc): The Siteimprove Accessibility Checker is your tool to evaluate any web page for accessibility issues at any given time.
- [Toggle JavaScript](https://chrome.google.com/webstore/detail/toggle-javascript/cidlcjdalomndpeagkjpnefhljffbnlo): Toggle JavaScript provides a simple, easy-to-access browser button to enable or disable JavaScript globally.
- [WAVE Evaluation Tool](https://chrome.google.com/webstore/detail/wave-evaluation-tool/jbbplnpkjmmeebjpijfedlgcdilocofh): WAVE is a web accessibility evaluation tool developed by WebAIM.org. It provides visual feedback about the accessibility of your web content by injecting icons and indicators into your page. No automated tool can tell you if your page is accessible, but WAVE facilitates human evaluation and educates about accessibility issues..
- [Web Developer](https://chrome.google.com/webstore/detail/web-developer/bfbameneiokkgbdmiekhjnmfkcnldhhm): The Web Developer extension adds a toolbar button to the browser with various web developer tools.
- [webhint.io](https://chrome.google.com/webstore/detail/webhint/gccemnpihkbgkdmoogenkbkckppadcag): Quickly test your website to see if there are any issues with accessibility, browser compatibility, security, performance and more.

### Stage two: prototyping tools

It's good practice to write good, error-free code. And once you're out testing your prototype with users who have access needs, you're going to be wanting well-formed HTML with zero errors, and as few accessibility problems as possible. While these tools won't make your prototype bulletproof, they'll go a long way towards fixing your mistakes and guiding you in the right direction.

- [HTMLHint](https://github.com/htmlhint/HTMLHint): The static code analysis tool you need for your HTML.
- [ESLint](https://github.com/eslint/eslint): A fully pluggable tool for identifying and reporting on patterns in JavaScript.
- [stylelint](https://github.com/stylelint/stylelint): A mighty, modern linter that helps you avoid errors and enforce conventions in your styles.
- [stylelint-a11y](https://github.com/YozhikM/stylelint-a11y): Plugin for stylelint with a11y rules.
- [husky](https://github.com/typicode/husky): Git hooks made easy.
- [prettier](https://github.com/prettier/prettier): Prettier is an opinionated code formatter.

### Stage three: Continuous Integration tools

Once your service is deployed to staging you'll want to be running tests against it. We have the following available which you can use.

- [hmrc/accessibility-testing-library](https://github.com/hmrc/accessibility-testing-library): This library can be used to integrate a number of automated tools into Selenium UI test repositories to help identify a number of potential accessibility issues in web front-ends.
- [hmrc/accessibility-assessment](https://github.com/hmrc/accessibility-assessment): This project contains the Dockerfile and images assets required to create the accessibility-assessment image that is used in CI for the assessment of captured pages using `axe`, `pa11y` and `vnu`. The violations found during the assessment are pushed to ELK.
