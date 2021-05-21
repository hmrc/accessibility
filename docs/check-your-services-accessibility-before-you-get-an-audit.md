# Check the accessibility of your service before you get an audit

**The accessibility of your service is your team’s responsibility.**

Before you [request an accessibility audit](https://github.com/hmrc/accessibility/blob/master/docs/request-an-accessibility-audit.md), you should check the accessibility of your service.

As an absolute bare minimum, we strongly suggest following these three tasks:

1. Make sure each page contains valid HTML.
2. Make sure each page is free from WCAG errors.
3. Test each page with a screen reader.

You should complete these tasks before you request an in-house audit, fixing any errors that may arise. Carrying out these checks will help you:

- improve the accessibility of your service
- save time by eliminating issues early
- make sure it meets the [public sector accessibility regulations](regulations-to-make-public-sector-websites-and-mobile-applications-accessible.md)

You can validate your HTML on a page-by-page basis using browser plugins. However, it is time consuming. We recommend that you automate your HTML validation as part of your (HMRC-only) CI build; see [Stage three: Continuous Integration tools](stage-three--ci-tools.md).

## When should you consider accessibility

Accessibility is a user need. You should be thinking about the access needs of your users from the start of design, research and development. **Do not leave it until the end.**

Build accessibility tasks into each sprint and include them in your workflow. Here are some examples that you can use.

- [Definition of Ready](definition-of-ready.md)
- [Definition of Done](definition-of-done.md)

## Accessibility quick wins

​Ideally you should test your service regularly in the accessibility lab, using a range of devices. This will get you a long way towards avoiding the most common accessibility failings.

- [Accessibility quick wins](accessibility-quick-wins.md)

## Design and usability quick wins

Avoid the most common GOV.UK Design System and usability issues that we see when auditing services.

- [Design and usability quick wins](design-and-usability-quick-wins.md)

## Make use of automated helpers

We recommend that you share the load between all team members so that everybody owns at least one accessibility task.

- [Stage one: browser plugins](stage-one--browser-plugins.md)
- [Stage two: prototyping tools](stage-two--prototyping-tools.md)
- [Stage three: Continuous Integration tools](stage-three--ci-tools.md)
