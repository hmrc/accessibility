# Check for increased text size and spacing

This task is to ensure that there is no loss of content when modifying the text either through zoom or styling.

## System set-up

Windows or macOS
: The browser matters less than testing to increase in text size and spacing, so this test can be done on any desktop operating system and browser combination.
- First ensure the browser width is set to 1280px
- To zoom in the Chrome browser, <kbd>Ctrl</kbd> +/- to 400%
- To increase the text size in the Chrome browser, go to chrome://settings/fonts. Increase the default font size from 16px to 32px
- To increase the text spacing, use the [text spacing editor plugin](https://chrome.google.com/webstore/detail/text-spacing-editor/amnelgbfbdlfjeaobejkfmjjnmeddaoj)
- To check target size, use the [target size bookmarklet](https://html5accessibility.com/stuff/2023/08/28/quick-and-very-dirty-target-size-checker/)

Android
: In the Chrome browser go to Settings > Accessibility > Text scaling. Increase the size to 200%

iOS
: In the Safari browser, tap `aA` in the address bar to increase to 200%

## Testing notes

1. Zoom to 400% on desktop and review the service.
2. Change text size to 200% and review the service.
3. Increase text spacing and review the service.
4. Ensure interactive elements are at least 24px x 24px in size or distance when page zoomed or text resized.

### What to look for

- check layout is not broken by the larger text or increased spacing
- check text is not cut-off, overlapped or hidden
- especially look at places where the following are used:
  - columns of content
  - tabs
  - tables
