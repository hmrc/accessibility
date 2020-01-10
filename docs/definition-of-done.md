# Definition of Done

As an absolute bare minimum, we recommend following these three tasks:

1. Make sure each page contains valid HTML.
2. Make sure each page is free from WCAG errors.
3. Test each page with a screen reader.

You should make sure these tasks are complete before you request an in-house audit. The best way to do this is to validate the HTML of each page. Use a tool like [axe](https://github.com/dequelabs/axe-core) or [Pa11y](https://github.com/pa11y/pa11y) to test for WCAG errors. Test some user journeys with a screen reader at the end of each sprint.

## How you can test your service

Most of this work can be done at your own desk. The assistive tech journeys are best done in the accessibility lab, if you have one in your Delivery Centre.

### Code quality

- make sure each page contains valid HTML
- make sure each page contains valid CSS
- make sure each page works without CSS
- make sure each page works without JS
- make sure the JS doesn’t throw errors
- remove all unnecessary markup and attributes
- check for any message file properties which may have leaked into the rendered view
- make sure each page is free from WCAG errors
- run each page through tools like axe and Pa11y, fixing any errors that are flagged

### Usability

- provide appropriate context for screen readers where necessary
- check you can complete this journey without a mouse
- check you can complete this journey without a screen
- check you can complete this journey on a mobile device
- test each page is usable with **at least one** screen reader (see below)
- test each page is usable with **at least one** screen magnifier (see below)
- test each page is usable with **at least one** voice controller (see below)

### Screen readers

- test the journey is successful with VoiceOver on macOS
- test the journey is successful with VoiceOver on iOS
- test the journey is successful with JAWS on Windows
- test the journey is successful with NVDA on Windows (if you are on Linux try Orca)

### Screen magnifiers

- test the journey is successful with ZoomText on Windows
- test the journey is successful with Zoom enabled on macOS
- test the journey is successful with Zoom enabled on iOS

### Voice control

- test the journey is successful with Dragon
- test the journey is successful with Voice Control
