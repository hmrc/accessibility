# Issue: No timeout dialog [draft]

The page does not contain the timeout dialog, this is critical in allowing users the time they need to work through a service and complete tasks without losing data.

People with disabilities such as blindness, low vision, dexterity impairments or cognitive limitations may require more time to read content or to complete a task like filling in a form. 

## To resolve:

Implement the service timeout, follow the [service timeout pattern](https://design.tax.service.gov.uk/hmrc-design-patterns/service-timeout/).

## Labels

- wcag
- wcag 2.2.1
- service timeout
- usability

## Report

| Status | Level | Issue | Success Criterion |
| ------ | ----- | ----- | ----------------- |
| 🔴 (H) | A    | [#issue](): No timeout dialog | 2.2.1 Timing Adjustable |

## Statement

### Accessibility problems

```
- there is no timeout dialog box in this service, so users will not be warned before being logged out
```

### Milestones

```
- a timeout occurs without prior warning that a timeout may occur. This means that users will not realise they have to complete a task within a time limit. This fails WCAG 2.1 success criterion 2.2.1 (Timing Adjustable)
```

## References
[Service timeout pattern](https://design.tax.service.gov.uk/hmrc-design-patterns/service-timeout/) 

[Understanding Success Criterion 2.2.1: Timing Adjustable](https://www.w3.org/WAI/WCAG21/Understanding/timing-adjustable)

