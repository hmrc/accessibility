# Issue: Using default browser link styles

Links should use the GOV.UK style which applies a highly visible focus style. This greatly assists keyboard-only users and those with vision impairments in locating the currently focussed control.

Whilst using the browser-default styles does not constitute a WCAG failure, these do vary from browser-to-browser. In some cases these default styles can conflict with other author styles on the page which will render them even less visible and could trigger a failure.

Where there are isolated examples of this it can mean a link is missed entirely as the user is looking for the standard GOV.UK styles.

## To resolve

Add `govuk-link` to all links.

Alternatively there is an [option in GOV.UK Frontend SASS](https://frontend.design-system.service.gov.uk/sass-api-reference/#govuk-global-styles) to enable this for all links without having to add the classes to each individual one, but use with caution.

## Labels

- typography

## Report

| Priority | Issue |
|----------|-------|
| 🔴 P1    | [#issue]() Using default browser link styles |

## Statement

This is not a WCAG A/AA failure so it does not have to be included on the accessibility statement, but we strongly recommend resolving the issue to improve the usability of the service.

## References

[Links - GOV.UK Design System](https://design-system.service.gov.uk/styles/typography/#links)
