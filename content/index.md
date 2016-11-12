---
date: 2016-03-08T21:07:13+01:00
title: Cross Platform UI for everyone
type: index
weight: 0
---

## libUI

Simple and portable (but not inflexible) GUI library in C that uses the native GUI technologies of each platform it supports.

{{< warning title="Experimental Table support" >}}
Table stuff is currently experimental; do not use in production code. It will not build on Windows as that part has not been written yet; if you want to test other parts of the Windows code, apply nowintable.diff.
{{< /warning >}}

![Windows Controls](https://github.com/andlabs/libui/raw/master/examples/controlgallery/windows.png)
![Linux Controls](https://github.com/andlabs/libui/raw/master/examples/controlgallery/unix.png)
![macOS Controls](https://github.com/andlabs/libui/raw/master/examples/controlgallery/darwin.png)


## Runtime Requirements

* Windows: Windows Vista SP2 with Platform Update or newer
* Unix: GTK+ 3.10 or newer
* Mac OS X: OS X 10.8 or newer

## Build Requirements

* All platforms:
	* CMake 3.1.0 or newer
* Windows: either
	* Microsoft Visual Studio 2013 or newer (2013 is needed for `va_copy()`) — you can build either a static or a shared library
	* MinGW-w64 (other flavors of MinGW may not work) — **you can only build a static library**; shared library support will be re-added once the following features come in:
		* [Isolation awareness](https://msdn.microsoft.com/en-us/library/aa375197%28v=vs.85%29.aspx), which is how you get themed controls from a DLL without needing a manifest
* Unix: nothing else specific
* Mac OS X: nothing else specific, so long as you can build Cocoa programs

<hr/>