# Check code quality

This task should be completed first as it will surface lots of issues which will affect other tasks.

## System set-up

Install some browser extensions for testing. We have listed the ones we recommend in [semi-automated testing](../semi-automated-testing.md).

## Testing notes

1. Use the browser developer tools and extensions.
2. Review errors and warnings.
3. Examine code.
4. Disable CSS and JS in turn.

### What to look for

- frameworks and codebases are kept up-to-date
- each page is free from HTML and WCAG errors (including colour contrast) which can be discovered using browser-based tools - use two or more tools to ensure good coverage
- each page works without CSS - the page will not look pretty but all content should still be available and all actions could still be performed
- each page works without client-side behaviour using JavaScript (JS)
  - JS should be added as a progressive enhancement. Some things may be easier with JS enabled (such as a multi-file uploader) but you should still be able to accomplish the task without JS enabled
  - any links or content dependent on JS should be hidden if it is not available, for example, backlinks using the the browser back history
  - make sure the JS does not throw errors by keeping the browser console open during testing
- for content
  - combining `h1` with `legend` or `label` elements to avoid duplication for screen reader users
  - use of `autocomplete` attribute on inputs for personal data
  - backend code is not displayed, especially examining hidden copy intended for screen reader users
  - if using `hr` element, add `aria-hidden="true"` to prevent screen readers interacting with it (ensure you cannot achieve segmentation using styling).
- on forms
  - radios and checkboxes have `fieldset` with a `legend` that describes the grouping
  - using the correct `type` attribute for inputs
- check page performance and timings
