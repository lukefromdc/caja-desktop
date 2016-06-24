# caja-desktop
This is a workaround for GTK 3.21.3 and later issues with Caja, the file manager for the MATE desktop.

This package runs a renamed instance of nautilus-desktop. Desktop files open in Caja in a mate session with any instance of nautilus-desktop so that part was simple. The code in nautilus-desktop-canvas-view.c is hacked to call mate-appearance-properties background when "change background" is selected from the desktop right click menu.

Because this is based on Nautilus it is built inside Nautilus and all of Nautilus must be installed to run it, like any current Nautilus compositing must be used to display the desktop background, and icons on the desktop must be switched off in Caja itself.
