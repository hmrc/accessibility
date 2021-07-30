# Issue: No timeout dialog [draft]

The page does not contain the timeout dialog, this is critical in allowing users the time they need to work through a service and complete tasks without losing data.

People with disabilities such as blindness, low vision, dexterity impairments or cognitive limitations may require more time to read content or to complete a task like filling in a form. 

## To resolve:

Implement the service timeout, follow the [service timeout pattern](https://design.tax.service.gov.uk/hmrc-design-patterns/service-timeout/).

## Labels

- wcag
- wcag 2.2.1 (A)
- service timeout
- usability

## Report

| Status | Level | Issue | Success Criterion |
| ------ | ----- | ----- | ----------------- |
| 🔴 (H) | A    | [#issue](): No timeout dialog | 2.2.1 Timing Adjustable |

## Statement

### Accessibility problems

```
users are not being warned before being logged out when their session ends
```

### Milestones

```
a timeout occurs without the ability for the user to extend their session. This fails WCAG 2.1 success criterion 2.2.1 (Timing Adjustable)
```

## References

[Service timeout pattern - HMRC Design Pattern](https://design.tax.service.gov.uk/hmrc-design-patterns/service-timeout/) 

[Understanding Success Criterion 2.2.1: Timing Adjustable](https://www.w3.org/WAI/WCAG21/Understanding/timing-adjustable)

