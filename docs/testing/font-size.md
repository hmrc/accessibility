# Check for increased font size on mobile and desktop (page deprecated)

For updated guidance, read [increased text size and spacing](increased-text-size-and-spacing.md)

---
DELETE BELOW
---

Font-size-only zoom is important to check as it is a modification which is easy for users to do themselves and provides a user with a subjectively better layout than a full-page zoom where the layout moves towards a mobile or tablet layout on desktop. On smaller screens it is also a way of increasing readability without having to pinch & zoom all the time.

## System set-up

### Desktop
The browser matters less than testing the font size increase on both the mobile and desktop layouts, so this test can be done on any desktop OS. We want to test with font size set to 200%.

To do this in Chrome, go to http://chrome://settings/fonts

Increase the default font size from 16px to 32px.

### Mobile Android
In Chrome go to Settings > Accessibility > Text scaling

Increase the size to 200%

### Mobile iOS
Settings > Accessibility > Display & Text Size

These are the settings we will be testing with:
- Bold Text
- Larger Text

## Testing notes
Change font-size and review the service.

## What to look for
Perform the [common font tests](common/font.md)
