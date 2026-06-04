# Accessible autocomplete

https://github.com/alphagov/accessible-autocomplete

## How to test

### Test with JavaScript off
1.	When JavaScript is disabled, the native select box is displayed.
2.	The visible label’s “for” attribute is associated with the select box’s “id”

### Test with JavaScript on
1.	The native select box is disabled (css display: none).
2.	The “id” of the select box is changed so it is not associated with the visible label.
3.	A new input control, with the role of combobox, is added and the “id” is set to match the visible label’s “for” attribute.
4.	A list element `<ul>`, with the role of listbox, is added after the input control with an aria-labelledby attribute matching the visible label’s “id”.
