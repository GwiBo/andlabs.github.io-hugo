---
date: 2016-11-12T21:45:33+05:30
title: libui
weight: 20
---

## Announcements

* **2 November 2016**
	* Added two new functions to replace the deleted `uiWindowPosition()` and friends: `uiAreaBeginUserWindowMove()` and `uiAreaBeginUserWindowResize()`. When used in a `uiAreaHandler.Mouse()` event handler, these let you initiate a user-driven mouse move or mouse resize of the window at any point in a uiArea.

* **31 October 2016**
	* @krakjoe noticed that I accidentally used thread-unsafe code in uiQueueMain() on Unix. Fixed.

* **24 October 2016**
	* `uiWindowSetContentSize()` on Unix no longer needs to call up the GTK+ main loop. As a result, bugs related to strange behavior using that function (and the now-deleted `uiWindowSetPosition()` and `uiWindowCenter()`) should go away. I'll need to go through the bugs to verify as much, though.

* **22 October 2016**
	* Due to being unable to guarantee they will work (especially as we move toward capability-driven window systems like Wayland), or being unable to work without hacking that breaks other things, the following functions have been removed: `uiWindowPosition()`, `uiWindowSetPosition()`, `uiWindowCenter()`, and `uiWindowOnPositionChanged()`. Centering may come back at some point in the future, albeit in a possibly restricted form. A function to initiate a user move when a part of a uiArea is clicked will be provided soon.

* **21 October 2016**
	* `uiDrawTextWeightUltraBold` is now spelled correctly. Thanks to @krakjoe.

* **18 June 2016**
	* Help decide [the design of tables and trees in libui](https://github.com/andlabs/libui/issues/159); the implementation starts within the next few days, if not tomorrow!

* **17 June 2016**
	* **CMake 3.1.0 is now required.** This is due to CMake's rapid development pace in the past few years adding things libui needs to build on as many systems as possible. If your OS is supported by libui but its repositories ship with an older version of CMake, you will need to find an updated one somewhere.
	* Please help [plan out a better menu API](https://github.com/andlabs/libui/issues/152).

* **5 June 2016**
	* **Alpha 3.1 is here.** This was a much-needed update to Alpha 3 that changes a few things:
		* **The build system is now cmake.** cmake 2.8.11 or higher is needed.
		* Static linking is now fully possible.
		* MinGW linking is back, but static only.

*Old announcements can be found in the [ANNOUNCE.md](https://github.com/andlabs/libui/blob/master/ANNOUNCE.md) file.*
