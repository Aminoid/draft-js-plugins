# Fork of DraftJS Plugins
This repo is a fork of [DraftJS Plugins][1]. It fixes the issue with the inline-toolbar going beyond of viewport by maintaining toolbar width and the adjust pointer tip accordingly.

[1]: https://github.com/draft-js-plugins/draft-js-plugins
[2]: https://github.com/Aminoid/draft-js-plugins/blob/master/draft-js-inline-toolbar-plugin/src/toolbarStyles.css
[3]: https://github.com/Aminoid/draft-js-plugins/blob/master/draft-js-inline-toolbar-plugin/src/components/Toolbar/index.js
## Fix
The fix touches two files:
* [toolbarStyles.css][2]
* [Toolbar/index.js][3]

The idea is to:
* Fix the width of toolbar to 147px
* Check where the toolbar lies on the viewport. If it lies at a left/right distance of less than 73.5px (147/2 px), then fix it's left/right distance as 73px and change the pointer tip to the selected word. 
