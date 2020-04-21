Personal build of suckless st - simple terminal
===============================================

patches applied:
----------------

- st-alpha-0.8.2.diff
`This patch allows users to change the opacity of the background. Note that you need an X composite manager (e.g. compton, xcompmgr) to make this patch effective.`
- st-boxdraw_v2-0.8.2.diff
`Custom rendering of lines/blocks/braille characters for gapless alignment.`
- st-copyurl-20190202-3be4cf1.diff        - Select and copy the last URL displayed with Mod1+l. Multiple invocations cycle through the available URLs. URLs spanning multiple lines are not handled.
- st-dracula-0.8.2.diff                   - Dracula is a color scheme made by Zeno Rocha based on Solarized. This patch make the Dracula color scheme available for st.
- st-font2-0.8.2.diff                     - This patch allows to add spare font besides default. Some glyphs can be not present in default font.
- st-openclipboard-20190202-3be4cf1.diff  - Open contents of the clipboard in a user-defined browser.
- st-scrollback-0.8.2.diff                - Scroll back through terminal output using Shift+{PageUp, PageDown}.
- st-spoiler-20180309-c5ba9c0.diff        - Use inverted defaultbg/fg for selection when bg/fg are the same.
- st-vertcenter-20180320-6ac8c8a.diff     - Vertically center lines in the space available if you have set a larger chscale in config.h.

