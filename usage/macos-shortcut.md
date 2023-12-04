---
layout: page
title: macOS shortcut
parent: Usage
permalink: /usage/macos-shortcut/
---

Even though there isn't any official browser extension which supports Safari, it is possible to automatically open YouTube videos on FreeTube, with the help of [Shortcuts](https://support.apple.com/en-en/guide/shortcuts-mac/apdf22b0444c/mac). This application comes pre-installed on macOS, eliminating the need for additional packages to ensure its functionality.

**Note:** This shortcut requires administrator/sudo rights in order to run.

1. Open the Shortcuts App.

2. Click on the “+” button to create a new shortcut with the following actions:

    ![Shortcut code](/images/ShortcutMacOS.png)

    The script first checks if the currently opened Safari tab's URL contains "youtube.com". If not, it then checks the clipboard for this string. If neither contains "youtube.com", an error message appears. Otherwise, FreeTube plays the YouTube video from the link.

3. The last step is to keybind the shortcut. Click on ⓘ in the top of the right side menu. Finally, assign any combination of keys.

    ![Shortcut options - keybinding](/images/ShortcutKeybind.png)

Once this is done, it should be possible to open a Safari Youtube window and launch the shortcut with the keybind configured in the last step. The Youtube link can also be in the clipboard.

**NOTE:**
- FreeTube doesn't need to be opened in order for the shortcut to be run.
- MacOS updates might remove the shortcut keybinding.

