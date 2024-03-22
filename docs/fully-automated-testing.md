# Fully-automated testing

This can be set as part of a continuous integration process or as unit tests, but is typically run without an interface and generates a list of passes or fails.

## Continuous Integration (CI) tools

Once your service has been deployed to staging you’ll want to introduce some automated tests to that service's pipeline. Continuous integration tools are a good baseline for a service as they run all the time code is being added. Because of this they can be a good second line of defence against issues creeping in. However they must be monitored and any issues investigated.

Note that just like any automated testing a CI tool cannot be relied on to find all the issues, so it should only be used as one method to keep a service accessible.

### Accessibility Test Job Builder

The HMRC job builder is a configuration setting that captures each frontend page and generates an output of actionable WCAG issues (identified using axe) and HTML issues (identified using Nu HTML Checker) which can be reviewed and fixed.

One of the benefits of implementing this as a component of the build is the low cost of adopting for teams and as improvements to the tooling are rolled out they will be available to everyone making use of the job builder. Features like improved reporting and axe / HTML validator upgrades will not require effort from delivery teams.

[HMRC AccessibilityTestJobBuilder (Confluence)](https://confluence.tools.tax.service.gov.uk/display/DTRG/AccessibilityTestJobBuilder)
