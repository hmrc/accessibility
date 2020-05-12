# Usability and performance

## System set-up
Install the [Web Developer extension](https://chrome.google.com/webstore/detail/web-developer/bfbameneiokkgbdmiekhjnmfkcnldhhm) (available for Chrome and Firefox).

## Testing notes
Use developer tools or the Web Developer Extension to disable CSS and JS in turn.

## What to look for
- make sure each page works without CSS - the page will not look pretty but the important thing will be that the actions can all still be performed and content is available.
- make sure each page works without JS - JS should be added as an enhancement, it should not be required to make the service work. Some things may be easier with JS enabled (such as a multi-file uploader) but you should still be able to accomplish the task without JS enabled
- the user is informed if selecting a link will open a new window
- skip link is available and takes the user to the primary content, bypassing the banner
- page title matches h1
- any auto updating content or auto-playing video or audio can be paused, hidden or stopped
- if the service has a session timeout, a timeout dialog allows the user to extend their session
- if the service uses a Back Link component and it relies on JS, the Back Link is removed when JS is disabled
