This is a workaround for GTK 3.21.3 and later issues with Caja, the file manager for the MATE desktop.

This package runs a renamed instance of nautilus-desktop. Desktop files open in Caja in a mate session with any instance of nautilus-desktop so that part was simple. The code in nautilus-desktop-canvas-view.c is hacked to call mate-appearance-properties background when "change background" is selected from the desktop right click menu. Coding in nautilus-desktop-application.c to turn icons off when they are turned off in GNOME is disabled so icons on the desktop in MATE are independent of those in GNOME.

Because this is based on Nautilus it is built inside Nautilus and all of Nautilus must be installed to run it, like any current Nautilus compositing must be used to display the desktop background, and icons on the desktop must be switched off in Caja itself.

Usage is simple: install this and Nautilus, then turn composinting ON and Caja's desktop icons OFF. The desktop is now managed by this forked version of nautilus-desktop and redraws properly with GTK 3.21.3 and later.

This is rough but it works. Rename popovers are restyled to look like the normal renaming label but are limited to one line which renders at the bottom of the normal icon name. Closing the (now hidden) popover applies the renaming without having to click the now-zero-width "rename" button, as is the normal behavior in Caja and in Nemo.  CSD has been removed from the properties window.  More to come if the Caja/GTK3.21.3 issue persists.
