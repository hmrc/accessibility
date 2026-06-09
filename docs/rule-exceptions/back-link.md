# Back link

The [Back link](https://design-system.service.gov.uk/components/back-link/) component provides the user with a convienent mechanism to navigate back to the previous page.

Although this document focuses on the Back link, the same general rules and exceptions apply when using [Breadcrumbs](https://design-system.service.gov.uk/components/breadcrumbs/) .

## How to test

Use a combination of automated and manual tests to check 

- the back link is placed after the header region
- the back link is placed directly before the main region
- the skip link at the top of the page bypasses the back link
- the back link returns the user to the previous page they were on

## Known issues

Some automated testing tools may report an issue with content not being contained within a landmark.

This is not a WCAG failure, but considered best practice. The issue has previously been covered in the [Back link known issues](https://design-system.service.gov.uk/components/back-link/#known-issues-and-gaps) and can be ignored.

Example alert from [axe DevTools](https://www.deque.com/axe/devtools/extension/chrome/)

> ### All page content should be contained in landmarks
>
> Ensure all page content is contained by landmarks
