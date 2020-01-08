---
name: "\U0000267F Accessibility audit"
about: "Use this template for requesting an in-house accessibility audit."
title: "AUDIT: [SERVICE NAME]"
labels: audit
projects: "In-house Audits"
assignees: philsherry
---

## Accessibility audit

The accessibility of your service is your team’s responsibility.

### Before you request your audit

Before you request an in-house accessibility audit, there are some basic targets that we’d like you to hit. Meeting these targets before your request will save us all some time, meaning you’ll get your audit back sooner. If you think you need help with this, we’ve written some guidance to help you [check the accessibility of your service before you get a review](https://github.com/hmrc/accessibility/blob/master/docs/check-your-services-accessibility-before-you-get-a-review.md).

✅ **Please tick the boxes below to show you’ve read the requirements.**

Before raising this request for an in-house accessibility audit, we did the following things as a team:

- [ ] Made sure each page of our service contains valid HTML.
- [ ] Made sure each page of our service is free from WCAG errors.
- [ ] Tested each page of our service with at least one screen reader, to make sure it was usable.

### In order to request your audit

We need you to provide us with user journeys. These should cover signing into the service, the steps taken to complete the journey successfully, and any steps to exit the service in specific ways.

This is the preferred style.

#### Journey title and state if applicable

1. Page title
    1. Data entry on the page
    1. Actions taken on the page

You will also need to supply any relevant information for signing in.

With that in mind, you’d be looking at putting together something like this to attach to your request:

> ##### Connect to VPN before entering the URL
>
> URL: <https://www.staging.tax.service.gov.uk/auth-login-stub/gg-sign-in>
>
> ##### Authority Wizard
>
> - Redirect URL: `/your-service-url`
> - Affinity Group: `Organisation`
> - Enrolment Key: `IR-CT`
> - Identifier Name: `UTR`
> - Identifier Value: `1234567890`
> - Select: <kbd>Submit</kbd>
>
> #### Steps to complete the unhappy path for journey 2
>
> 1. ‘Check this is the business you want to register’
>     1. Select: <kbd>Confirm</kbd>
> 2. ‘What is your company registration number?’
>     1. Enter: `72936602`
>     2. Select: <kbd>Save and continue</kbd>

There should never be a need for more than 8 journeys to be submitted from a service.

### After you request your audit

Once your Issue is raised, you’ll be able to track its progress on our [In-house Audits](https://github.com/hmrc/accessibility/projects/1) board. You’ll also be able to see how many other audits we may have in the queue before it. Please be patient, we are a small team. 🤖🤖
