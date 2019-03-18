title: Improved Scroll behavior and closing text
date: 2014-02-22

This time we have improved the behavior of the mouse scroll. Before, when some scrolled down over a survey, it would work regardless the user intended to do so. That is, if the user scrolled the survey the page, and by chance the mouse passed over the survey, then subsequent scrolls were over the survey, and not propagated to the page.

To fix that, the new behavior only listens for mouse scroll if the user starts the survey, that can be by:

- Clicking an item or response
- Clicking the start button when the survey has Introduction text.

In addition, we have added a flag so you can enable or disable this feature, which is 'on' by default.