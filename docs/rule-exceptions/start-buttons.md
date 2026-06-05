# Start buttons

Services use [Start buttons](https://design-system.service.gov.uk/components/button/#start-buttons) on a service's start page to ensure the main Call to Action (CTA) is easy to find and clearly identifiable.

This is achieved by using an anchor link `<a>` that is styled to look like a GOV.UK `<button>`.

As the "Start button" visually looks like a button it is important that it also behaves like a button. This means that it can be activated by using both the `Enter` key and the `Space bar`.

To do this we use javascript to listen for the `Space bar` keypress when the element has keyboard focus.

## How to test

1. Check pages that are using "Start buttons" can be activated using both the `Enter` and `Space bar` keys.
2. Check all pages that submit data (e.g. pages with form controls) are using the native `<button>` element. 

## Known issues

The standard markup for a "Start button" includes the `role=button` attribute which can cause some testing tools to recommend using a `<button>` element instead.

If the issue is raised on a start page, it can be ignored as a link `<a>` is correct in this instance. If it is raised elsewhere it should be investigated and corrected where nessesary.
