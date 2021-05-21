# Accessibility statement templates for internal services

This page gives advice about creating an accessibility statement, and how to implement an accessibility feedback form.

To comply with [public sector accessibility regulations](regulations-to-make-public-sector-websites-and-mobile-applications-accessible.md) your service must meet WCAG 2.1 AA standards and include an accessibility statement before going into public beta.

On this page you will find accessibility statement templates, details of where to link to your statement, and a Deskpro form to enable users to ‘report an accessibility problem’.

## Accessibility statement template prototype

To ensure HMRC accessibility statements are consistent, we have developed templates for you to use. Each accessibility statement contains fixed text that must appear and information that is specific to the service, website or app.

There are two accessibility statement templates currently available.

- **Compliant statement** — to be used when there are no accessibility issues identified and it meets WCAG 2.1 AA.
- **Partially compliant statement** — to be used when it does not meet WCAG2.1 AA. For each WCAG guideline that it does not meet you’ll need to specify the accessibility problem, the WCAG 2.1 AA success criteria the problem fails on, and when you plan to fix it.

There is a Welsh language version of each template but you will need to get translations of the information that is specific to your service, website or app.  To get Welsh translations email <translations.welshlanguage@hmrc.gov.uk>

### How to access the templates

You can access the accessibility statement templates at [accessibility-statement.herokuapp.com](https://accessibility-statement.herokuapp.com/)

- User name: `accessibilitystatement`
- Password: `hmrca11ystatement`

### Information required that is specific to your service, website or app

You’ll need to add the following details to the statement.

- Name of your service
- Sub domain name (if your service has one)
- A description of what your service does (single paragraph)
- Any additional information a disabled user may need to act on if there are parts of your service some people may find difficult to use
- How to directly contact your service by phone or email if users need support
- The dates you tested your service, when the statement was last updated, and link to your most recent accessibility audit if you have one

If your service is partially compliant you’ll also need to list the accessibility problems, and for each problems state

- which of the WCAG 2.1 AA success criteria the problem fails on. You’ll be able to get this from your DAC audit report
- when you plan to fix the problem

You must only change or remove text that appears in square brackets within the template statement. Don’t change anything else because the content needs to closely mirror the [GDS sample accessibility page](https://www.gov.uk/service-manual/helping-people-to-use-your-service/publishing-information-about-your-services-accessibility) and we want to have consistency across the statements we publish in HMRC.

## How to create a link to your accessibility statement

Users will access the accessibility statement from a link in the footer within your service.

You can show the accessibility link in your service by passing the url of your accessibility statement to your template provider (`govuk-template` or `play-ui` in most cases). There is an optional link that will show up when you pass the url to it. This is either in `govuk-template.mustache.html` for TAAS/Frontend Template Provider or `FooterLinks.scala.html` for Play-ui.

The link to the accessibility statement should **open in the same window or tab**.

## Implementing the ‘report an accessibility problem’ Deskpro form

To enable users to report accessibility problems with your GOV.UK service, a Deskpro form has been created in the contact-frontend service specifically for the accessibility statement.

Once you have set up your accessibility statement to use the Deskpro form you must contact <shashi.patel@hmrc.gov.uk> to say that the accessibility statement for your service is using it.  This will ensure they are ready for anything that may be submitted and know how to deal with it.

The link to the Deskpro form should **open in a new window or tab**.

### Technical advice

In your accessibility statement under the heading 'Reporting accessibility problems with this service' code the text 'accessibility problem (opens in the same window)' as a link.  Please make sure the link opens in a new window or tab.

There are a few optional query parameters that should be used, one to help Deskpro identify your service, and one to identify exactly where in your service the accessibility statement was clicked. The query parameters are named `service` and `userAction`.

The `service` parameter is how your service is known e.g. `pta`.

The `userAction` parameter is the page where the accessibility statement link was clicked e.g. `/personal-account/personal-details` so the link in your accessibility statement should be something like <https://www.tax.service.gov.uk/contact/accessibility?service=pta&userAction=%2Fpersonal-account%2Fpersonal-details>

## Contact us

If you have any questions or need further support, please email us at <accessibility.team@hmrc.gov.uk>
