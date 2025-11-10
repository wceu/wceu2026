# WordCamp Europe 2026

## Intro
This CSS `live-css/live-css-wceu-2026.css` is included in [WordCamp Europe 2026](https://europe.wordcamp.org/2026/ "Live WordCamp 2026 website") website every time you will make a repository commit and reload remote CSS from the website admin view.

Development environment is on https://wceutest.wordcamp.org/2026 and also includes
this remote CSS.

## Edit remote CSS
To edit a CSS file we can clone it locally, use our VSC or similar editor to live editing, or the easiest option, use the web editor.

For this option, you will need to go to https://github.dev/wceu/wceu2026/blob/main/live-css/live-css-wceu-2026.css and then:

1. Make CSS changes to the file
2. Go to left bar, source control icon and make a commit (write a descriptive text to describe the change made, one change for commit).
3. Reload remote CSS from website or hitting URL (see below).

## Reload remote CSS on the website
Make one of these actions:

### Development website
1. Go to *Appearance -> Remote CSS* and click *Update* button OR
2. Got to https://wceutest.wordcamp.org/2026/wp-admin/admin-ajax.php?action=wcrcss_webhook

### Live website
1. Go to *Appearance -> Remote CSS* and click *Update* button OR
2. Got to https://europe.wordcamp.org/2026/wp-admin/admin-ajax.php?action=wcrcss_webhook

## General CSS considerations and style guides

* Don't use post IDs as selectors because they can change between development environment and production. Instead, use the slug; e.g. `body.post-slug-call-for-volunteers`, `body.page-slug-accommodation`.
* If possible, create a class and use it on the element `.button-action` because we can reuse these classes in several elements and change code only one.
* Use [CSS Coding Standards](https://developer.wordpress.org/coding-standards/wordpress-coding-standards/css/ "") if possible.
* Use CSS vars instead of direct colours, fonts, or sizes if possible. Use `background-color: var(--wp--preset--color--custom-orange-primary);` instead of `background-color: #f04614;`
* Use Slack channel `#team-website` if you have any doubts.
* Use [GitHub Issues](https://github.com/wceu/wceu2026/issues) to add new request, issues, etc. and ping users on the Issue.
* Have fun :)