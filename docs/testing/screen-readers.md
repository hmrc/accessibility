# Screen readers

- [Browsing with a desktop screen-reader (YouTube)](https://www.youtube.com/watch?v=KuVKQQMtRRI)
- [Browsing with a mobile screen-reader (YouTube)](https://www.youtube.com/watch?v=ev8ERS5Z3NU)

## JAWS on Windows

JAWS is a commercial screen reader available on Windows only. It is expensive but full-featured and is one of the most popular screen readers. You can access a time-limited trial which works for 40 minutes after which you will need to reboot to start the timer again. Fully licensed installs are available to use on the HMRC accessibility lab laptops.

[JAWS - Freedom Scientific website](https://www.freedomscientific.com/products/software/jaws/)

### System set-up

Install JAWS 2019 or later.

Avoid changing any settings beyond the modifier keys. Because users can modify their set-up in many different ways it is best to test with the default settings. This also makes it easier to replicate issues.

### Testing notes

1. Use Chrome or Edge browser
2. Follow our [step-by-step guide to getting started with using JAWS](https://accessibility-training.herokuapp.com/jaws/) (username: hmrc, password: a11y)
3. Perform the common checks as listed in the What to look for section below
4. Complete the user journey using the screen reader only

## NVDA on Windows

NVDA is a free screen reader for Windows

[Download NVDA - NV Access website](https://www.nvaccess.org/download/)

### System set-up

Install the latest version of NVDA

### Testing notes

1. Use Chrome or Edge browser
2. Follow our [step-by-step guide to getting started with using NVDA](https://accessibility-training.herokuapp.com/nvda/) (username: hmrc, password: a11y)
3. Perform the common checks as listed in the What to look for section below
4. Complete the user journey using the screen reader only

## VoiceOver on macOS

Voiceover is a free screen reader built into macOS

Whilst it shares much functionality with VoiceOver for iOS, the mechanisms for using it are very different and it's support for various accessibility features are different to the iOS version.

### System set-up

`System Preferences > Accessibility > VoiceOver`

### Testing notes

1. Use Safari browser
2. Follow our [step-by-step guide to getting started with using Voiceover on Mac](https://accessibility-training.herokuapp.com/voiceover/) (username: hmrc, password: a11y)
3. Perform the common checks as listed in the What to look for section below
4. Complete the user journey using the screen reader only

## VoiceOver on iOS

Voiceover is a free screen reader built into iOS.

Whilst it shares much functionality with Voiceover for macOS, the mechanisms for using it are very different and it's support for various accessibility features are different to the macOS version.

### System set-up

`Settings > Accessibility > VoiceOver`

### Testing notes

1. Use Safari browser
2. Perform the common checks as listed in the What to look for section below
3. Complete the user journey using the screen reader only

There are two ways of accessing pages with Voiceover on iOS, swiping (to access items consecutively) and by dragging a finger across the screen to have whatever is under the finger read out. You should test using the former.

## TalkBack on Android

TalkBack is a free screen reader built into Android.

### System set-up

`Settings > Accessibility > TalkBack`

### Testing notes

1. Use Chrome browser
2. Perform the common checks as listed in the What to look for section below
3. Complete the user journey using the screen reader only

## What to look for

- the content on the page is read by the screen reader in a logical order (not necessarily the same as visual order)
- moving focus to or from a component or element does not automatically trigger a change without relaying this back to the screen reader user
- check all the following are present in the correct dialog list (for example, the rotor in Voiceover), for example, all buttons are listed in form controls not in links, and all links, tables and controls have unique names
  - Links
  - Headings
  - Form controls
  - Tables
  - Landmarks
- the link text helps users identify it’s purpose and this should be unique when taken out of context
- check tables announce headings correctly as you move around the table from row to row and column to column
- moving directly to an input causes the associated label and any associated hint or error message to be read out
- submitting a page which returns an error summary causes the error summary heading to be read out as soon as the page loads
- error messages are prefixed with "error:"
- icons and other images have appropriate accessible names, for example the white exclamation mark on a black circle alongside some important information has an accessible name appropriate to the copy, such as “warning” or “note”
- video media has all information available as screen-reader accessible content for example any information presented in graphics as part of the video are presented in screen-reader accessible captions, audio
