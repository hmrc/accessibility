# Issue: Timeout dialog - cannot extend session

While the service has a timeout dialog and it is presented correctly, the user's session is being lost.

This can be for a number of reasons:

- the endpoint is not triggering a renewed session either in the frontend or in the database
- the service is timing out due to the user being passed temporarily to another service where the user spends longer than the originator service's timeout period

Being able to extend a session is critical in allowing users the time they need to work through a service and complete tasks without losing data.

People with disabilities such as blindness, low vision, dexterity impairments or cognitive impairments may require more time to read content or to complete a task like filling in a form.

## Labels

- wcag
- wcag 2.2.1 (A)
- service timeout
- usability

## Report

| Status | Level | Issue | Success Criterion |
| ------ | ----- | ----- | ----------------- |
| 🔴 (H) | A    | [#issue](): Session timing out | 2.2.1 Timing Adjustable |

## Statement

### Accessibility problems

```
the dialog allowing users to extend the time allowed to complete any particular page is not working / users are not being warned before being logged out when their session ends
```

### Milestones

```
a timeout occurs without the ability for the user to extend their session. This fails WCAG 2.1 success criterion 2.2.1 (Timing Adjustable)
```

## References

[Service timeouts - HMRC Design System](https://design.tax.service.gov.uk/hmrc-design-patterns/service-timeout/)

[Understanding Success Criterion 2.2.1: Timing Adjustable](https://www.w3.org/WAI/WCAG21/Understanding/timing-adjustable)
