# File Upload Enhanced

The improved [File upload](https://design-system.service.gov.uk/components/back-link/) component has been designed to provide users with an accessible way to upload files.

## How to test

Use a combination of automated and manual tests to check 

- the control is clearly identifiable
- the instructions are announced when the button is focused
- the file upload progress is announced to screen readers

## Known issues

Some automated testing tools may report an issue with the form control not have an associated label.

If the form control is the hidden `<input>` control (contains the attribute `hidden="hidden"`) it is ok and does not require a label.

Example alert from [WAVE](https://wave.webaim.org/extension/) (Web Accessibility Evaluation Tool)

> ### Missing form label
>
> A form control does not have a corresponding label.
