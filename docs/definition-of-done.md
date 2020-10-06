# Definition of Done

Before you can define a feature as Done, you need to meet some conditions. Your team should already have its own version of this, which you have signed-off as a team, but here are some suggestions.

As an absolute bare minimum, we recommend following these three tasks:

1. Make sure each page contains valid HTML.
2. Make sure each page is free from WCAG errors.
3. Test each page with a screen reader.

You should complete these tasks before you request an in-house audit, fixing any errors that may arise.

The best way to do that is to validate the HTML of each page, which is a main feature of the [`AccessibilityTestJobBuilder`](stage-three--ci-tools.md) that you should be running. Test your user journeys with a screen reader at the end of each sprint.

## Configure anything configurable

Always remember to check that you’ve configured everything.

For example, in a service such as `address-lookup-frontend`, there is a default value for use as the home location:

[`homeNavHref = "http://www.hmrc.gov.uk/"`](https://github.com/hmrc/address-lookup-frontend/blob/master/conf/application.conf#L64)

In most cases, you should be redirecting users to the start page of your service. For example, you would change it to:

`homeNavHref = "http://www.hmrc.gov.uk/service-name/start-page"`

This returns the user to a more logical place within their journey. It is unlikely that users will have started their journey from the GOV.UK HMRC page.

You will also need to configure your accessibility statement.

## How you can test your service

Most of this work can be done at your own desk. The assistive tech journeys are best done in the accessibility lab, if you have one in your Delivery Centre.

See also: [Testing with assistive technologies](https://www.gov.uk/service-manual/technology/testing-with-assistive-technologies).

## Basic checks

- all acceptance criteria are met
- all bugs from the previous build have been fixed
- all features are code complete
- all tests pass (unit & functional)
- all WIP code has been removed from the build
- CI/CD pipeline is successful
- [`AccessibilityTestJobBuilder`](stage-three--ci-tools.md) has a clean report
- sign-off from all relevant people — Design Lead, Development Lead, Project Manager, Product Owner, QA, etc.

### In-browser checks

- no JS errors in the web inspector console
- each page works without CSS
- each page works without JS
- hidden context values have content, not raw message file properties

### Usability

- complete the journey without a mouse
- complete the journey without a screen
- complete the journey on a mobile device
- complete the journey with **at least one** screen reader (see below)
- complete the journey with **at least one** screen magnifier (see below)
- complete the journey with **at least one** voice controller (see below)

When time is a factor, Windows users can test with NVDA. Mac users can test with VoiceOver and Voice Control, but you get better results on iOS.

### Native OS settings

- set system font size to 36px and check what breaks
- make sure nothing disappears when inverted colours are on
- check contrast levels are good enough in greyscale mode
- ensure animation respects the OS reduce motion setting

### Screen readers

- if it looks like a heading, it should announce as a heading
- screen reader users should be able to navigate to each element
- everything should read out in a logical order
- provide appropriate context for screen readers where necessary
- actions aren’t over-explained with extra context for screen readers

### Screen magnifiers

- everything should still be usable at 200%
- everything should still be usable at 400%

### Voice control

- check each piece of functionality of the new feature is usable by voice recognition software
- make sure any hidden context isn’t preventing voice activation from working

### Orientation checks

This applies to mobile devices and is covered by [WCAG 2.1 — 1.3.4 Orientation (Level A)](https://www.w3.org/WAI/WCAG21/quickref/#orientation). Check the following in portrait and landscape:

- everything is correctly aligned
- everything still aligns correctly when the screen scrolls
- nothing important needs to be repositioned
- screen width is fully utilised in landscape orientation
- everything scrolls into view that should do
