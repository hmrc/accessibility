# Issue:  Opening content in a new tab [draft]

Links that open in a new tab should contain text informing the user that they will be taken to a new browser tab and include the appropriate `rel` attributes for the type of content being accessed.

The additional text will help all users understand the result of the action and help prevent them possibly getting disorientated when the browser back button is unresponsive.

The purpose of the `rel="noreferrer noopener"` attributes is to ensure linking to cross-origin destinations (webpages outside the gov.uk domain) are safe for the user.

## To resolve:

Follow the [opening links in a new tab guidance](https://design-system.service.gov.uk/styles/typography/#opening-links-in-a-new-tab).

Add ‘opens in new tab’ as part of the visible link to make it clear for all users as well as being announced as part of the link for assistive technology users.

## Labels

* wcag
* wcag 3.2.5 (AAA)
* design pattern
* usability
* typography


## Report

| Priority | Issue |
| -------- | ----- |
| 🔴 P1    | [#issue](): Missing ‘opens in new tab’ as part of the link |

## Statement

This is not a WCAG A/AA failure so it does not have to be included on the accessibility statement, but we strongly recommend resolving the issue to improve the usability of the service.
## References

[Links - GOV.UK Design System](https://design-system.service.gov.uk/styles/typography/#links)

[Using the target attribute to open a new window on user request and indicating this in link text](https://www.w3.org/WAI/WCAG21/Techniques/html/H83)

[Understanding Success Criterion 3.2.5: Change on Request](https://www.w3.org/WAI/WCAG21/Understanding/change-on-request)

