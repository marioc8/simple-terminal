Personal build of suckless st - simple terminal
===============================================

keybindings:
------------

```
alt + c               vimBrowse     [keys and details](https://st.suckless.org/patches/vim_browse/)

ctrl + shift + h      font size -2
ctrl + shift + j      font size -1
ctrl + shift + k      font size +1
ctrl + shift + l      font size +2
ctrl + shift + Home   reset font size

ctrl + shift + c      copy to clipboard
ctrl + shift + v      paste from clipboard

alt + Enter           spawn new terminal with the same CWD

alt + h               scroll page down
alt + j               scroll one line down
alt + k               scroll one line up
alt + l               scroll page up

alt + i               find http url in terminal screen
alt + o               open selected link in browser
```

patches applied: 
----------------

(are also included separetely in its own directory)

- st-alpha-0.8.2.diff
```
This patch allows users to change the opacity of the background.
Note that you need an X composite manager (e.g. compton, xcompmgr) to make this patch effective.
```

- st-anysize-0.8.1.diff
```
This patch allows st to resize to any pixel size, makes the inner border size dynamic,
and centers the content of the terminal so that the left/right and top/bottom borders are balanced.
With this patch, st on a tiling WM will always fill the entire space allocated to it.
```

- st-clipboard-0.8.3.diff
```
This trivial patch sets CLIPBOARD on selection, the same as your browser.

You may want to replace selpaste with clippaste in your config.h bindings to complete the affect.
```

- st-copyurl-20190202-3be4cf1.diff
```
Select and copy the last URL displayed with Mod1+l. Multiple invocations cycle through the available URLs.

   URLs spanning multiple lines are not handled
```

- st-dracula-0.8.2.diff
```
Dracula is a color scheme made by Zeno Rocha based on Solarized.
This patch make the Dracula color scheme available for st.
```

- st-newterm-0.8.2.diff
```
This patch allows you to spawn a new st terminal using Ctrl-Shift-Return.
It will have the same CWD (current working directory) as the original st instance.
```

- st-openclipboard-20190202-0.8.1.diff
```
Open contents of the clipboard in a user-defined browser.

The clipboard in this case refers to the CLIPBOARD selection which gets populated when pressing e.g. C-c.
```

- st-selectionbg-alpha-0.8.2.diff
```
This patch works with selectioncolors and alpha patches to make selection background color transparent.
```

- st-spoiler-20180309-c5ba9c0.diff
```
Use inverted defaultbg/fg for selection when bg/fg are the same.
```

- st-vertcenter-20180320-6ac8c8a.diff
```
Vertically center lines in the space available if you have set a larger chscale in config.h.
```

- st-vimBrowse-20200212-26cdfeb.diff
```
This patch offers the possibility to move through the terminal history,
search for strings and use VIM-like motions, operations and quantifiers.

[keys and other details](https://st.suckless.org/patches/vim_browse/)
```

- st-visualbell2-basic-2018-10-16-30ec9a3.diff
```
Briefly renders a configurable visual indication on terminal bell event.

Two variants are available:
The basic variant supports:

    Invert the whole screen, or the border cells, or (only in 2020-05-13) the bottom-right corner
    or any custom group of cells.
        Configurable duration (default: 150ms).
```

- st-workingdir-20200317-51e19ea.diff
```
This patch allows user to specify the initial path st should use as WD (working directory).
```

# How to bypass compile warning.

The warning means You did not check the return value of system(...). To avoid this warning, simply check the return value!

```
int systemRet = system(commandLine);
if(systemRet == -1){
  // The system method failed
  }
```

This is, as system is not guaranteed to succeed.

