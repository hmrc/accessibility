# Colour
It is important that interfaces do not rely on colour alone.

## System set-up

### Chrome
This is available from Chrome 82, or in Chrome Canary
Dev tools > Rendering > Emulate vision deficiencies
- Achromatopsia
- Protanopia
- Deuteranopia
- Tritanopia

### Windows
Settings > Ease of Access > Colour Filters
- Inverted
- Greyscale (Achromatopsia)
- Greyscale Inverted
- Red/Green filter(Protanopia)
- Green/Red filter (Deuteranopia)
- Blue/Yellow filter (Tritanopia)

### Mac OS
System Preferences > Accessibility > Display >Colour filters
- Greyscale (Achromatopsia)
- Red/Green filter(Protanopia)
- Green/Red filter (Deuteranopia)
- Blue/Yellow filter (Tritanopia)

### iOS
Settings > Accessibility > Display & Text Size > Colour filters
- Greyscale (Achromatopsia)
- Red/Green filter(Protanopia)
- Green/Red filter (Deuteranopia)
- Blue/Yellow filter (Tritanopia)


## Testing notes
Enable the setting, check the service.

## What to look for
For each overlay check colour contrast hasn't been impeded by the change in colours and that everything is still readable