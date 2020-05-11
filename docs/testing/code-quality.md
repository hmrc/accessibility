# Check code quality
This task should be completed first as it will surface lots of issues which will affect other tasks.

## System set-up
Install some automated accessibility testing tools. These are all available as Chrome browser extensions.
- [AXE](https://chrome.google.com/webstore/detail/axe-web-accessibility-tes/lhdoppojpmngadmnindnejefpokejbdd)
- [Wave](https://chrome.google.com/webstore/detail/wave-evaluation-tool/jbbplnpkjmmeebjpijfedlgcdilocofh)
- [ARC Toolkit](https://chrome.google.com/webstore/detail/arc-toolkit/chdkkkccnlfncngelccgbgfmjebmkmce?hl=en)
- HTML validator, such as [Validity](https://chrome.google.com/webstore/detail/validity/bbicmjjbohdfglopkidebfccilipgeif)

## Testing notes
Use browser developer tools. Review errors and warnings. Examine code.

### What to look for
- make sure each page is free from WCAG errors (including colour contrast checks) which can be discovered using automated tools such as axe, pa11y, wave etc. Using two or more tools ensures a good coverage
- inputs have labels
- labels are only hidden where visual duplication is to be avoided. Where labels are hidden this must be done in a way to still expose them to assistive technology.
- optional fields' labels are marked as optional
- ensure hints and error messages are associated with inputs (or with fieldsets when used)
- radios and checkboxes have fieldsets
- fieldsets have legends
- legends have content
- tables have captions
- tables are used only for data, not for layout
- tables have correct markup for headings and headings make sense
- combining h1 and label/legend where there is only one question on the page and little or no copy between the h1 and inputs. If the copy between the two is longer than would be expected for a hint, then the label or legend can be repeated.
- check for any message file properties which may have leaked into the rendered view - especially examine hidden copy intended for screen-readers
- review css - is the code up to date as possible (Gov Frontend or Assets Frontend 4.11), is it in a maintainable state
- make sure the JS doesn’t throw errors - eg keep the browser console open during testing and check for errors being thrown. This also needs to be tested in older browsers such as IE11 to ensure any JS has been correctly polyfilled
- ensure JS is placed at the end of the document to avoid render-blocking (assuming async or defer not used due to browser support)
- heading hierarchy is correct - the hierarchy of headings on a page should provide a table of contents with headings correctly nested and no heading levels skipped
- pay particular attention to any code specific to the service - components which are not present in either the HMRC or GOVUK Design Systems