# Accessible autocomplete

The [accessible autocomplete](https://github.com/alphagov/accessible-autocomplete) is an GOV.UK styled autocomplete component maintained by the GOV.UK Design System team.

The component supports progressive enhancement, as required by the [service standard](https://www.gov.uk/service-manual/technology/using-progressive-enhancement) and should be implemented using that pattern on applicable services.

As the component uses progressive enhancement it is important to test with both JavaScript enabled and disabled.

## How to test

### Test with JavaScript off

1.	When JavaScript is disabled, check the native `<select>` box is displayed.
2.	Check the `<label>` “for” attribute matches the `<select>` “id”

### Test with JavaScript on
1.	The native `<select>` is disabled and hidden (the html contains the css property `display: none`).
2.	The “id” of the `<select>` is changed so it no longer matches the `<label>` "for" attribute.
3.	A new `<input>` control, with `role='combobox'`, is added to the page and the “id” is set to match the `<label>` “for” attribute.
4.	A list element `<ul>`, with `role=listbox`, is added after the `<input>` with an `aria-labelledby` attribute matching the `<input>` “id”.

## Known issues

### Missing label

When JavaScript is enabled the `<select>` is effectively disabled but some automated tests may flag the control as not having a `<label>`, this is ok as it is never available when the JavaScript version is enabled.

Example alert from [WAVE](https://wave.webaim.org/extension/) (Web Accessibility Evaluation Tool)
 
> #### Select missing label
> 
> A select element does not have an associated label
> 

### Aria labelledby target has no copy

The [Pattern Checker](https://chromewebstore.google.com/detail/pattern-checker/amjjliajblignodfdjalnfkekkeflkph?hl=en-GB) plugin reports this as an issue because the `<input>` control does not contain any text. This is a false positive as the `<input>` text is provided by the associated label and as long as the above tests pass, this is not an issue.

Example alert from the HMRC Pattern Checker

> #### Aria labelledby target
>
> target id="xxxx" has no copy
>
 

