# st - simple terminal
--------------------
st is a simple terminal emulator for X which sucks less. This is my patched version
of st which includes these features:

  * Mouse/keyboard scrollback
  * Transparency and theme control using Xresources
  * Dynamic cursor colour and blinking cursor
  * Image preview with w3m support
  * Multiple font support, coloured emojis


# Requirements
------------
Xlib header files, libxft-bgra and dmenu

# Installation
------------
Edit config.mk to match your local setup (st is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install st (if
necessary as root):

1. ```make clean install```
2. Symlink st-copyout and st-urlhandler scripts to somewhere in the $PATH or just copy them

# Keybinds

  * follow urls by pressing alt-l
  * copy urls in the same way with alt-y
  * copy the output of commands with alt-o
  * copy selected text to clipboard with Alt+C
  * Paste with Shitf+Insert or Alt+V
  * Increase or decrease font with Ctrl+ and Ctrl-
  * Scrollback with Alt+j and Alt+k or using mousewheel

# Running st
----------
If you did not install st with make clean install, you must compile
the st terminfo entry with the following command:

    tic -sx st.info

See the man page for additional details.

# Credits
-------
Based on Aurélien APTEL <aurelien dot aptel at gmail dot com> bt source code.

Patched and configured by madvillain, 2023
