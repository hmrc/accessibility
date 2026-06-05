# Conditional reveal

The conditional reveal is a feature available in both [Radios](https://design-system.service.gov.uk/components/radios#conditionally-revealing-a-related-question) and [Checkboxes](https://design-system.service.gov.uk/components/checkboxes/#conditionally-revealing-a-related-question) that allows for an addition question to be displayed when user selects a specific option.

This can be useful in certain circumstances where grouping two related questions on the same page makes them easier to answer. For example, asking for a phone number when the user selects ‘Contact me by phone’. 

There is a caveat that only a single (simple) question is revealed, as nested field sets and content with links are not translated adequately to assistive technology to be fully accessible.

## How to test

Use a combination of automated and manual tests to check 

- only one input is revealed
- the input has no other content other than a label and possibly hint text
- no links are present in the hint text
- all controls follow a logical tab order when navigating by keyboard

## Known issues

Some automated testing tools may report an issue with using unsupported aria role `aria-expanded` on radio buttons.

This is technically correct, but it does work with some assistive technologies and so it's still beneficial for some users. For this reason the issue can be ignored. 

Example alert from [ARC Toolkit](https://chromewebstore.google.com/detail/arc-toolkit/chdkkkccnlfncngelccgbgfmjebmkmce)

> ### ARIA attribute is not allowed
>
> The `aria-expanded` attribute is not allowed on the `radio` role
> 

For more information on this issue you can read the GDS blog post [an update on the accessibility of conditionally revealed questions](https://accessibility.blog.gov.uk/2021/09/21/an-update-on-the-accessibility-of-conditionally-revealed-questions/) 
