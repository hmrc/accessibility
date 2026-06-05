# Change links

Change links are used on a [Check answers](https://design-system.service.gov.uk/patterns/check-answers/) page to provide users with an easy way to update their answers before submitting their information.

The change links are provided as part of the [Summary list](https://design-system.service.gov.uk/components/summary-list/) component.

Visually all the change links look the same, they simply say "Change". But to improve accessibility, hidden text is added to each link to make them unique, this benefits screen reader users when stepping through their answers as well as viewing the links out of context (e.g. when using JAWS linked list dialog)

It is important to add the hidden text after the word "Change" to ensure maximum compatibility with voice control software, where partial matches are easier to trigger, for example by just saying "Click change".

Where possible the summary list key and hidden text should match the original question, for example:

- Original question: What is your name?
- Summary list key: Your name
- Change link: Change your name

## How to test

Use a combination of automated tools and manual testing to ensure all change links 

- contain hidden text
- hidden text appears after the word Change
- hidden text matches the summary list key (or as close as possible)
- returns the user to the correct page

## Known issues

The standard pattern is to provide a change link for each question asked. When pages contain more than one question we still provide a change link for both questions even though they take the user to the same page.

Because of this automated testing tools will raise a redundant link issue, but as long as each change link is for an individual question and navigates the user to the correct page this issue can be ignored.

Example alert from [WAVE](https://wave.webaim.org/extension/) (Web Accessibility Evaluation Tool)

> ### Redundant link
> 
> Adjacent links go to the same URL
> 
