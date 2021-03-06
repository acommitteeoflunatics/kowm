## Introduction

Having searched for many years for a usable Linux window manager that both appealed to my sense of aesthetics and had at least some of the features I feel necessary for a 'proper' WM; in all that time I only came across one which, at least partially, fit the bill. 

`Mavosxwm` was the creation of `Martin Vollrathson` and hadn't been updated since sometime in 2003. After obtaining permission from him in 2007, I forked Mavosxwm v0.2.1 to use as the base from which I will write `koWm`. I will be keeping parts of the window interface, the theming mechanism, and some of the event-handling code; these bits are, even now, making their way into various locations in kowm-core.

## kowm
`kowm` ( /kōm/ ) never wanted to be anything more when she grew up than the only X window manager that even I would take home to Mom. kowm has decided that 'extensible simplicity' is the wave of the future; and the members of the 'Committee' tend to agree. 

### Requirements
Any kowm installation will require, at a bare minimum, the first eight 'core' libraries; other requirments will be made known closer to initial release.

## kowm-core
kowm-core ( :speaker: /kōm-kôr/ ) is made up of eight modular desktop libraries; seven to handle the basic features that make for a beautifully simple window manager while the sixth is a framework for building, attaching, and manipulating new modular extensions. Since execution speed is of the essence here, we're planning on writing kowm-core in C++.

### Libraries

-   `baseAnnex` provides a basic module infrastructure and shared asset management funtions.
-   `baseConsumer` provides stubs and mount points for baseAnnex modules.
-   `baseDecor` provides a basic graphics subsystem from which all graphics toolkit modules can hook into and manipulate objects.
-   `baseFare` provides automatic menu generation of the system menu, the desktop menu and the application menus.
-   `baseFlaps` provides a robust tabbing mechanism
-   `baseGear` provides simple constructs shared by all 'objects'; e.g. Spaces, Flaps and 'windows' (including the root window).
-   `baseOverseer` provides advanced maniuplation of 'objects'; aka 'window' management.
-   `baseSpaces` provide basic workspace management and functionality.

All core libraries are to be coded in C++ unless a compelling case can be made against it.

## kowm-opts
kowm-opts /kōm-äpts/ currently has six additional modular libraries planned. These libraries - along with any others we think are needed - will provide additional services that, while not absolutely necessary, would probably be appreciated by the end user. These libraries will most likely be written in Ruby; however additional bindings for Python and Lua are currently on the RoadMap.

### Libraries

-   `optsDecor` gives access to advanced graphical toolkits from within kowm

## kowm-apps
Finally, we're planning other apps the we deem useful to the overall desktop experience. These will reside within the `kowm-apps` project. kowm-apps can use any language for which exists a language binding or a new one if you or a friend have the knowledge to write one; don't fret too much, it's not a difficult task. That being said, we definitely are expecting the first few to be all Ruby.

### Libraries

-   `appsFiler` simple file manager that sees all filesystems as objects, to be opened, read from and written to.
-   `apps3dFiler` similar to `appsFiler` and based upon it; but uses a 3d bird's-eye view. Fans of Jurassic Park and/or users of Irix will find it hauntingly familiar.

## So, to recap...
-	Want to make a new application or extension for kowm?
	-	Simply, write your new module in any of the available language bindings already written. 
-	No binding for the language you prefer to code in?
	-	Well then, write yourself a binding module for that language and continue on.

Oh yeah, one last thing I'd like to say... please... don't forget to submit a pull request once you're done, so others can enjoy the new language, application, or extension you just made possible.

============
Copyright (c) 2009-2013, Jerry W Jackson
<br />All rights reserved.
