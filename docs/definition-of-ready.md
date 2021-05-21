# Definition of Ready

Before you can define a feature as Ready to work on, you need to meet some conditions. Your team should already have its own version of this, which you have signed-off as a team, but here are some suggestions.

Designers should make sure accessibility is part of what they do. Keep content, flows and screens simple. This helps people with learning disabilities, mental health conditions, cognitive impairments and autism.

## Be inclusive

To make sure accessibility is part of the story, include elements of the following:

- [established patterns](#established-patterns)
- [service design](#service-design)
- [content design](#content-design)
- [visual design](#visual-design)
- [design for assistive technology](#design-for-assistive-technology)
- [user research](#user-research)

Most of this should be part of standard components but may help if part of a ticket.

### Established patterns

Unless you have good reasons, which you can back up with data and research, and you plan to upstream your new pattern into the Design System, then you should stick to the established patterns with your designs.

You might question if something is tabular data or not and suggest different HTML solutions or patterns. Use the right design patterns to provide the user with consistent line spacing and whitespace.

You can find the established patterns here:

- [GOV.UK Design System](https://design-system.service.gov.uk/)
- [HMRC Design Patterns](https://design.tax.service.gov.uk/hmrc-design-patterns/)

### Service design

- URLs should be human-readable
- your service should work without JavaScript

### Content design

- write simple, easy to understand content that meets the [content style guide](https://www.gov.uk/guidance/style-guide/a-to-z-of-gov-uk-style)
- reading order should make sense when there are differences between what is visible and what is read out loud
- write page titles that are the same as the `h1` heading (but be aware of the [personally identifiable information](https://design.tax.service.gov.uk/hmrc-design-patterns/page-title/#personally-identifiable-information) caveat)

### Visual design

- colour contrast ratios should be fully accessible
- use non-breaking spaces and hyphens to stop unwanted word wrapping
- your design must be mobile-friendly (remember a zoomed in desktop screen will effectively become a mobile viewport)
- do not convey meaning by colour alone
- there should be a visual relationship between related elements

### Design for assistive technology

- add hidden context for screen readers, where necessary
- notify screen readers when onscreen content or layout changes, using relevant ARIA roles
- provide a warning when an action will take the user to a different tab or window
- all interactive elements have accessible names
- expose the correct elements to the element menu for that device (for example, the Rotor on VoiceOver, or the Elements menu on NVDA)
- label landmarks with `aria-label` if there are more than one of each (for example, *“Site navigation”*, *“In-page navigation”*, *“Footer navigation”*)
- accommodation for screen zoom and whether the screen still makes sense at +200%

### User research

- consider whether people using assistive technology might need extra time to complete tasks
- if the journey is a large one, consider allowing the user to save and come back later
