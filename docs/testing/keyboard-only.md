# Use keyboard-only

This task is to ensure that all functionality can be operated using a keyboard.

## System set-up

By default, the Tab key is used for navigating through the focusable elements. On macOS you may need to turn this on following the [use your keyboard like a mouse with Mac](https://support.apple.com/en-gb/guide/mac-help/mchlp1399/) guide.

## Testing notes

On page load, do not use the mouse or interact with the page. Use your keyboard to tab through each page noting the placement of the focus.

## What to look for

- first focus placement should be the skip link in the top left corner, unless an error summary is present
  - if an error summary is present focus should be immediately placed on the summary container, and subsequent tabbing should take you through the error summary links
  - skip to main content takes you to the main content landmark of the page, after which it should progress into the primary content, bypassing the main banner, language toggle and back link
- each actionable control is reachable. Note, mouse hover alone isn't required to action events
- focus states are obvious
- order of tabbable controls is logical
  - check tab order in zoomed view / mobile view on desktop
- any timeout dialog receives immediate focus when activated and tabbing is restricted to the dialog; you should not be able to tab out of the dialog into the page behind
- links styled as buttons can be actioned with the spacebar - if the page scrolls instead, initialise with the JavaScript polyfill to ensure the link acts like a button
- check focus is not fully obscured or hidden by modals, adverts, sticky headers or footers
- check dragging movements can be carried out by keyboard and touch screen
