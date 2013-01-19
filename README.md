## Introduction

Having searched for many years for a usable Linux window manager that both 
appealed to my sense of aesthetics and had at least some of the features I 
feel necessary for a 'proper' WM; I only came across one which [at least 
partially] fit the bill. `Mavosxwm` was the creation of `Martin Vollrathson` 
and hadn't been updated in any way for a long time at that point. After 
obtaining permission from him, I forked Mavosxwm to use in the creation of 
`koWm`. I will be keeping the tabbed interface, the theming mechanism, and 
most of the event-handling code; but I believe a change of language is in 
order before implementing additions and changes to the existing codebase. My 
first thoughts were to use Python as my base language; now I'm leaning towards 
something Ruby-flavored. To build this wm I have decided to, first, build a set
of six of a final twelve desktop libraries so that I may make this window 
manager as extensible as it cares to be. It will be named `koWm` [ sounds like
kohm or comb ] and will be the first application built using the `kobol` 
collection of libraries found at libs/kobol.

## Applications

Application naming preference 
would be this: 
-	all apps developed using the cyrannus methodology need to start with a 
	lower case `k` and should make a reasonable attempt to capitalize one 
	other letter from the appname in it's place. Bonus points if that capital
	letter happens to be a `W` to honor the brother I lost in childhood.

### `koWm`
The first related app to be packaged with kobol will be `koWm`, a modular and 
extensible window manager for Xorg based on xcb rather than the archaic xlib. 

### `kWomo`
I also have this crazy idea for an audio application named `kWomo`, as in Perry 
Cuomo.

### `koWala`
Not sure what to make with this name; but I do dig it...

## Libraries

### `kobol` (Collection)

`kobol` is a modular collection of twelve-plus desktop libraries and thier related
apps; it aims to be useful as a toolkit for writing massively modular graphical 
applications and aims to be truly OS-agnostic in it's execution. It is properly
referred to beginning with a lower-case `k`. 

Naming of the twelve libraries within kobol will follow the convention of naming 
each of the libraries for one of the twelve colonies of man from the original 
Battlestar Gallactica series; circa 1978. 

-   Core libraries used for basic functionality of the original intended use (`koWm`) 
are represented by inner colony names. Core libraries are almost always coded in C++.
	-	`caprica`: low-level window management 
	-	`gemoni`: low-level network management 
	-	`leonis`: low-level graphics
	-	`sagitara`: low-level module framework
	-	`piscera`: low-level system menuing
	-	`virgon`: low-level system translation 
-   Module libraries generally comprise one extension module to Core items. 
Outer colony names are used for middle level libraries which can extend on this 
vein. Modules may be written in either C++, Ruby, or a combination of the two.
	-	`aeries`: power management module
	-	`aquarus`: 
	-	`libris`:
	-	`orion`: 
	-	`scorpion`:
	-	`taura`:
-   Extras are libraries that, while very useful, aren't really part of the 
window manager. Unaligned colonies will be namesake to those that are considered 
useful for building modular X applications to use alongside `koWm`. These 'extra'
libraries are generally written in Ruby unless a lower-level abstraction is required.
	-	`hestia`:
	-	`khronos`: library for all things time-related, including ntp
	-	`pallas`:
	-	`persephone`:
	-	`phoebe`:
	-	`styx`: 
	-	`thanatos`: sleep and hibernation library
	-	`troy`: 

============
Copyright (c) 2011, Jerry W Jackson
All rights reserved.