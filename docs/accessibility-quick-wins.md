# Accessibility quick wins

​Ideally you should test your service regularly in the accessibility lab, using a range of devices. This will get you a long way towards avoiding the most common accessibility failings.

## Use the approved patterns and components

Make sure your service has used patterns and components from [GDS](https://design-system.service.gov.uk/) and [HMRC](https://design.tax.service.gov.uk/hmrc-design-patterns/) as these have been tested both for accessibility and browser and device support.

If your service uses patterns not in one of these libraries you should do additional work to ensure they work as needed.

Read more about this at [How to Meet Info and Relationships](https://www.w3.org/WAI/WCAG21/quickref/#info-and-relationships).

### Use the alphagov autocomplete component

Rather than using `select` inputs for long lists, consider using the latest version of the [autocomplete component](https://github.com/alphagov/accessible-autocomplete). This is not currently in the Design System as it is a complex component, but it is the preferred way of picking an item from a long list of options. Do not use other third-party variants.

### Make sure you initialise any details components

The [details component](https://design-system.service.gov.uk/components/details/) is a native browser control, but is not supported in some older browsers (most notably IE 11) and some assistive technology (JAWS) without the use of a [polyfill](https://github.com/hmrc/assets-frontend/blob/master/assets/javascripts/modules/details.polyfill.js).

You can initialise the component by adding the following code in your JavaScript.

    GOVUK.details.init();

Better still, you can initialise all of the components in one go.

     GOVUK.initAll();

### Avoid using tabs

True tabs are difficult to correctly implement in an accessible manner. Whilst there is a tabs pattern in the Design System, we do not recommend their use currently and they have been marked as Experimental for this reason. If you feel you need to use tabs, contact a member of the accessibility team.

Success criteria for [WCAG 2.0 (A) 4.1.2 Name, role, value](https://www.w3.org/TR/UNDERSTANDING-WCAG20/ensure-compat-rsv.html).

### Tell users if they are about to be timed out of a session

Most services have some sort of session timeout. Before a user is redirected to the timeout page they should be given both a warning that it is about to happen and the option to extend their session. There is an [HMRC timeout dialog component](http://hmrc.github.io/assets-frontend/patterns/help-users-when-we-time-them-out-of-a-service/index.html) for this; [Github repo](https://github.com/hmrc/hmrc-frontend/tree/master/src/components/timeout-dialog).

Success criteria for [WCAG 2.1 (A) 2.2.1: Timing Adjustable](https://www.w3.org/WAI/WCAG21/Understanding/timing-adjustable.html).

### Error summary and links

Error summaries should receive focus when the page loads, to bring the error to the attention of people using assistive technology and also help people who are only using a keyboard. Additionally, when clicking a link in the error summary the focus should be placed in either the input (in the case of text inputs) or on the first input in a group (for radios, checkboxes and date inputs).

Success criteria for [WCAG 2.1 (A) 2.4.1: Bypass Blocks](https://www.w3.org/WAI/WCAG21/Understanding/bypass-blocks.html).

### Error messages

Make sure your error messages [follow the standard](https://design-system.service.gov.uk/components/error-message/#be-clear-and-concise) and that you help prevent users seeing the error message in the first place by providing enough information around formatting and data required.

Success criteria for [WCAG 2.1 (A) 3.3.1: Error Identification](https://www.w3.org/WAI/WCAG21/Understanding/error-identification.html).

## Validate your HTML

If HTML is not valid it will cause parsing issues for assistive technology (among other side-effects). Many accessibility auditing plugins (like AXE) will check for invalid HTML alongside accessibility issues.

Read more about this at [How to Meet Parsing](https://www.w3.org/WAI/WCAG21/quickref/#parsing).

## Check link text is unique when taken out of context

Screen readers can list all link text in a dialog to enable the user to quickly access links on a page. If more than one link has the same text as a link but point to different URLs this can be very confusing. This is easy to miss on pages where you have repeating content (such as add-to-a-list) or are reviewing answers. Generally the fix is to add additional hidden content to add context for screen readers.

Success criteria for [WCAG 2.1 (A) 2.4.4: Link Purpose](https://www.w3.org/WAI/WCAG21/Understanding/link-purpose-in-context.html).

## Use an autocomplete attribute on inputs for personal data

If we are asking a user for data which they have likely entered elsewhere (like name or address) then we can help them fill in forms by using `autocomplete` attributes on form fields. This will prompt the browser to fill in fields we mark up in this way. Use the [correct attributes](https://html.spec.whatwg.org/multipage/form-control-infrastructure.html#autofill) to tell the browser which data to put where.

Success criteria for [WCAG 2.1 (AA) 1.3.5: Identify input purpose](https://www.w3.org/WAI/WCAG21/Understanding/identify-input-purpose.html).

## Contrast and focus states

If you are using Gov Frontend, the latest [WCAG 2.1 updates for colour and focus states](https://designnotes.blog.gov.uk/2019/07/29/weve-made-the-gov-uk-design-system-more-accessible/) are in place already. If you are using Assets Frontend, then you may need to add the new focus states and colour updates for [AF 3.11](https://gist.github.com/adamliptrot-oc/f77250a6f69fb31fabd935e2002f4964) or [AF 4.11](https://gist.github.com/adamliptrot-oc/f77250a6f69fb31fabd935e2002f4964).

Success criteria for [WCAG 2.1 (AA) 1.4.11: Non-Text Contrast](https://www.w3.org/WAI/WCAG21/Understanding/non-text-contrast.html).

## `h1` and page title should be the same

The visible `h1` on the page and the page title (in the browser tab) should be the same. However you should also make sure that the pages which follow each other have different titles/`h1` so when the user navigates they know they have moved to a different page and the last page hasn't just reloaded. See the [page title pattern](https://design.tax.service.gov.uk/hmrc-design-patterns/page-title/) for more information.

Success criteria for [WCAG 2.1 (A) 2.4.2 Page Titled](https://www.w3.org/WAI/WCAG21/Understanding/page-titled.html).

## Check focus order

This is best checked with a screen reader. Make sure that when traversing the page the information you are presented with comes in a logical order. For example, an edit link doesn't come before the thing you are going to edit is announced.

Success criteria for [WCAG 2.1 (A) 2.4.3 Focus Order](https://www.w3.org/WAI/WCAG21/Understanding/focus-order.html).

## Hide `hr` from screen readers

If you have used the `hr` element you should add `aria-hidden="true"` to it. Otherwise screen readers will attempt to interact with it. Also check that if you are using the `hr` to segment content that this has been done in some semantic way in the HTML as well.

## Make sure your service works without JavaScript

One of the [core principles of building services for the government](https://www.gov.uk/service-manual/technology/using-progressive-enhancement) is reaching as many people as possible by using progressive enhancement to build a resilient frontend. With this in mind any service should work without JavaScript and have appropriate fallbacks in place where it is used and is not available.
