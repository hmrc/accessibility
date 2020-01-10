# Make use of automated helpers

We recommend that you share the load between all team members so that everybody owns at least one accessibility task.

## Stage one: browser plugins

These are tools that any member of the team can use at their desk while they’re testing the service.

While there are many plugins listed here, you don’t have to use all of them. With the exception of Toggle JavaScript, they do a lot of the same things but there is some overlap. Take them all for a spin, see which ones you prefer.

### ARC Toolkit

> “The ARC Toolkit is a set of accessibility tools which aids developers in identifying accessibility problems and features for WCAG 2.0, WCAG 2.1, EN 301 549, and Section 508.”

Available for [Chrome](https://chrome.google.com/webstore/detail/arc-toolkit/chdkkkccnlfncngelccgbgfmjebmkmce).

### axe - Web Accessibility Testing

> “Accessibility checker for WCAG 2 and Section 508 accessibility. Find accessibility defects on your website or web application by using the axe Chrome extension. Drop the axe on your accessibility defects!”

Available for [Chrome](https://chrome.google.com/webstore/detail/axe-web-accessibility-tes/lhdoppojpmngadmnindnejefpokejbdd) or [Firefox](https://addons.mozilla.org/en-US/firefox/addon/axe-devtools/?src=search).

### Siteimprove Accessibility Checker

> “The Siteimprove Accessibility Checker is your tool to evaluate any web page for accessibility issues at any given time.”

Available for [Chrome](https://chrome.google.com/webstore/detail/siteimprove-accessibility/efcfolpjihicnikpmhnmphjhhpiclljc) or [Firefox](https://addons.mozilla.org/en-US/firefox/addon/digital-certainty-index/?src=search).

### WAVE Evaluation Tool

> “WAVE is a web accessibility evaluation tool developed by WebAIM.org. It provides visual feedback about the accessibility of your web content by injecting icons and indicators into your page. No automated tool can tell you if your page is accessible, but WAVE facilitates human evaluation and educates about accessibility issues.”

Available for [Chrome](https://chrome.google.com/webstore/detail/wave-evaluation-tool/jbbplnpkjmmeebjpijfedlgcdilocofh) or [Firefox](https://addons.mozilla.org/en-US/firefox/addon/wave-accessibility-tool/).

### Web Developer

> “The Web Developer extension adds a toolbar button to the browser with various web developer tools.”

Available for [Chrome](https://chrome.google.com/webstore/detail/web-developer/bfbameneiokkgbdmiekhjnmfkcnldhhm) or [Firefox](https://addons.mozilla.org/en-US/firefox/addon/web-developer/?src=search).

### Webhint

> “Quickly test your website to see if there are any issues with accessibility, browser compatibility, security, performance and more.”

Available for [Chrome](https://chrome.google.com/webstore/detail/webhint/gccemnpihkbgkdmoogenkbkckppadcag) or [Firefox](https://addons.mozilla.org/en-US/firefox/addon/webhint/?src=search).

### Easily disable JavaScript

Available for [Chrome](https://chrome.google.com/webstore/detail/toggle-javascript/cidlcjdalomndpeagkjpnefhljffbnlo) or [Firefox](https://addons.mozilla.org/en-US/firefox/addon/quick-js-switcher/?src=search)

## Stage two: prototyping tools

It’s good practice to write good, error-free code. And once you’re out testing your prototype with users who have access needs, you’re going to be wanting well-formed HTML with zero errors, and as few accessibility problems as possible. While these tools won’t make your prototype bulletproof, they’ll go a long way towards fixing your mistakes and guiding you in the right direction.

### HTMLHint

> “The static code analysis tool you need for your HTML.”

Available at [github.com/htmlhint/HTMLHint](https://github.com/htmlhint/HTMLHint).

### ESLint

> “A fully pluggable tool for identifying and reporting on patterns in JavaScript.”

Available at [github.com/eslint/eslint](https://github.com/eslint/eslint).

### Stylelint

> “A mighty, modern linter that helps you avoid errors and enforce conventions in your styles.”

Available at [github.com/stylelint/stylelint](https://github.com/stylelint/stylelint)

### Stylelint-a11y

> “Plugin for Stylelint with a11y rules.”

Available at [github.com/YozhikM/stylelint-a11y](https://github.com/YozhikM/stylelint-a11y).

### Husky

> “Git hooks made easy.”

Available at [github.com/typicode/husky](https://github.com/typicode/husky).

### Prettier

> “Prettier is an opinionated code formatter.”

Available at [github.com/prettier/prettier](https://github.com/prettier/prettier).

## Stage three: Continuous Integration tools

Once your service is deployed to staging you’ll want to be running tests against it. We have the following available which you can use.

### Accessibility testing library

> “This library can be used to integrate a number of automated tools into Selenium UI test repositories to help identify a number of potential accessibility issues in web front-ends.”

Available at [hmrc/accessibility-testing-library](https://github.com/hmrc/accessibility-testing-library).

### Accessibility assessment

> “This project contains the `Dockerfile` and images assets required to create the `accessibility-assessment` image that is used in CI for the assessment of captured pages using `axe`, `pa11y` and `vnu`. The violations found during the assessment are pushed to ELK.”

Available at [hmrc/accessibility-assessment](https://github.com/hmrc/accessibility-assessment).
