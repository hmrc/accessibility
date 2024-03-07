# Semi-automated testing

Generally this is some form of per-page testing done using an automated tool in the browser.

It requires more effort than the fully automated testing but because it gives visual feedback it can be easier to identify and fix the issue.

This is also the only option where fully automated solutions have not yet been implemented.

## Browser-based tools

These are tools that any member of the team can use at their desk while they’re testing the service.

### Chrome DevTools

DevTools
: It’s worth looking at the native features available in your browser’s DevTools. Some now have dedicated accessibility panels which provide a lot of information about the page and the [accessibility tree](https://developers.google.com/web/fundamentals/accessibility/semantics-builtin/the-accessibility-tree)
:
- [Accessibility features reference - Chrome Developers (The Accessibility pane)](https://developer.chrome.com/docs/devtools/accessibility/reference/#pane)
- [Accessibility In Chrome DevTools - Smashing Magazine](https://www.smashingmagazine.com/2020/08/accessibility-chrome-devtools/)

### Accessibility checking tools

axe - Web Accessibility Testing
: Probably one of the more popular automated tools. The basic version adds a panel to DevTools and allows a full page to be checked. There is a pro version which adds partial page checking and some guided tests.
: [AXE on the Chrome WebStore](https://chrome.google.com/webstore/detail/axe-web-accessibility-tes/lhdoppojpmngadmnindnejefpokejbdd)

ARC Toolkit
: Adds a panel to the browser’s DevTools and also has useful additional features like a text-spacing and reflow checker.
: [ARC Toolkit on the Chrome WebStore](https://chrome.google.com/webstore/detail/arc-toolkit/chdkkkccnlfncngelccgbgfmjebmkmce)

WAVE Evaluation Tool
: WAVE is a web accessibility evaluation tool developed by WebAIM.org. It provides visual feedback about the accessibility of your web content by injecting icons and indicators into your page.
: [WAVE on the Chrome WebStore](https://chrome.google.com/webstore/detail/wave-evaluation-tool/jbbplnpkjmmeebjpijfedlgcdilocofh)

Accessibility Insights for Web (Microsoft)
: This has a number of self-guided tests as well as some automated checks. Results primarily open in a new window.
: [Accessibility Insights for Web on the Chrome WebStore](https://chrome.google.com/webstore/detail/accessibility-insights-fo/pbjjkligggfmakdaogkfomddhfmpjeni)

### Specialised tools

Pattern checker
: This was developed in-house at HMRC to help government service teams build better services. It checks the code to provide guidance and indicate potential improvements for services using the [GOV.UK Design System](https://design-system.service.gov.uk/) and the [HMRC design patterns](https://design.tax.service.gov.uk/hmrc-design-patterns/).
: [Pattern checker on the Chrome WebStore](https://chrome.google.com/webstore/detail/pattern-checker/amjjliajblignodfdjalnfkekkeflkph?hl=en-GB&authuser=0)

Web Developer Toolbar
: Adds a toolbar button to the browser with various web developer tools. Use to validate the HTML and to disable JavaScript and CSS.
: [Web Developer Toolbar on the Chrome WebStore](https://chrome.google.com/webstore/detail/web-developer/bfbameneiokkgbdmiekhjnmfkcnldhhm)

WCAG Color contrast checker
: 
- [WebAIM: Contrast and Color Accessibility - Evaluating Contrast with Chrome DevTools](https://webaim.org/articles/contrast/devtools)
- [WebAIM: Contrast Checker](https://webaim.org/resources/contrastchecker/)

## Prototyping tools

It’s good practice to write good, error-free code. And once you’re out testing your prototype with users who have access needs, you’re going to be wanting well-formed HTML with zero errors, and as few accessibility problems as possible. While these tools won’t make your prototype bulletproof, they’ll go a long way towards fixing your mistakes and guiding you in the right direction.

HTMLHint
: Static code analysis tool for your HTML.
: Available at [github.com/htmlhint/HTMLHint](https://github.com/htmlhint/HTMLHint)

ESLint
: Tool for identifying and reporting on patterns found in JavaScript code.
: Available at [github.com/eslint/eslint](https://github.com/eslint/eslint)

Stylelint
: CSS linter that helps you avoid errors and enforce conventions.
: Available at [github.com/stylelint/stylelint](https://github.com/stylelint/stylelint)
