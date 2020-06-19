# Keyboard-only

## System set-up
For Mac check system settings for enabling tabbing

System Preferences > Keyboard > Shortcuts > check “Use keyboard navigation to move focus between controls”

## Testing notes
On page load, do not use the mouse or interact with the page. Use your keyboard to tab through each page noting the placement of the focus.

## What to look for
- first focus placement should be the skip link in the top left corner, unless an error summary is present
- if an error summary is present focus should be immediately placed on the summary container, and subsequent tabbing should take you through the error summary links
- skip to main content takes you to the main content landmark of the page, after which it should progress, possibly via a back link or language toggle if these are in the main body, into the primary content, bypassing the main banner
- each actionable control is reachable
- hover alone isn't required to action events
- focus states are obvious
- order of tabbable controls is logical
- check tab order and focus states in mobile view on desktop - zoom page until layout changes to mobile view
- any timeout dialog receives immediate focus when activated and tabbing is restricted to the dialog and you should not be able to tab out of the dialog into the page behind
- links styled as buttons can be actioned with the spacebar - if the page scrolls instead, ensure the link has
