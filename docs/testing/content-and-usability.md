# Check content and usability

This task is to ensure that the service is understandable, simple to use and consistent with the GOV.UK guidance.

## System set-up

Not applicable.

## Testing notes

HMRC services should follow:

- [GOV.UK Design System](https://design-system.service.gov.uk/)
- [HMRC design patterns](https://design.tax.service.gov.uk/hmrc-design-patterns/)
- [GOV.UK Content design: planning, writing and managing content](https://www.gov.uk/guidance/content-design/)
  - [GOV.UK Style guide](https://www.gov.uk/guidance/style-guide/)
  - [HMRC content style guide](https://design.tax.service.gov.uk/hmrc-content-style-guide/)

### What to look for

- established design components and patterns followed
  - page title matches the level 1 heading and also includes the service name. Each page title should adequately describe and be distinguishable from other pages
  - hint copy and error messages conform to the standard messages
  - check support links are consistent and present on each page
  - usage of microservices, for example, address lookup
- heading hierarchy is correct - this should provide a table of contents with headings correctly nested and no heading levels skipped
- for content
  - structured with headings, paragraphs and lists
  - plain English is used
  - consistency of terminology used
  - cognition load not overloaded, for example, check your answers page follows the user journey steps
- the user is informed if selecting a link will open a new window
- on forms
  - ask only required questions. Additional inputs are marked as optional in the label
  - inputs have visible labels
  - radios and checkboxes have fieldsets with a legend that describes the grouping
  - ensure hints and error messages are associated with inputs (or with fieldsets when used)
  - no other content is present between form elements. For example, a warning message before a submit button may be missed by screen reader users navigating using shortcut keys
  - check data is re-populated when navigating through completed screens
- for tables
  - used only for comparison data, not for layout
  - have a caption
  - have correct markup for column and row headings and the headings make sense
- any auto-updating content or auto-playing video or audio can be paused, hidden or stopped
- check videos contain captions and transcripts
- make sure language translations are complete
- if the service has a session timeout, a timeout dialog allows the user to extend their session
- check printed content (print preview)
