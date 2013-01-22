## Introduction

Having searched for many years for a usable Linux window manager that both appealed to my sense of aesthetics and had at least some of the features I feel necessary for a 'proper' WM; I only came across one which, at least partially, fit the bill. `Mavosxwm` was the creation of `Martin Vollrathson` and hadn't been updated in any way for a long time at that point. After obtaining permission from him, I forked Mavosxwm v0.2.1 to use as the base from which I will write `koWm`. I will be keeping the tabbed interface, the theming mechanism, and most of the event-handling code.

## kowm
`kowm` ( /kōm/ ) never wanted to be anything more when she grew up than the only X window manager that even I would take home to Mom. kowm has decided that 'extensible simplicity' is the wave of the future; and we tend to agree. 

## kowm-core
`kowm-core` is made up of six modular desktop libraries; five handle the basic features that make for a beautifully simple window manager and the sixth is a framework for building, attaching, and manipulating new modular extensions. Since speed is of the essence here, we're planning on writing kowm-core in C++.

## kowm-opts
komw-opts /kōm-äpts/ currently has six additional modular libraries planned. These libraries - along with any others we think are needed - will provide additional services that, while not absolutely necessary, would probably be appreciated by the end user. These libraries will most likely be written in Ruby; however additional bindings for Python and Lua are currently on the RoadMap.

## kowm-apps
Finally, we're planning other apps the we deem useful to the overall desktop experience. These will reside within the `kowm-apps` project. kowm-apps can use any language for which exists a language binding or a new one if you or a friend have the knowledge to write one; don't fret too much, it's not a difficult task. That being said, we definitely are expecting the first few to be all Ruby 

## So, to recap
-	Want to make a new application or extension for kowm?
	-	Simply, write your new module in any of the available language bindings already written. 
-	No binding for the language you prefer to code in?
	-	Well then, write yourself a binding module for that language and continue on.

Oh yeah, one last thing I'd like to say... please... don't forget to submit a pull request once you're done, so others can enjoy the new language, application, or extension you just made possible.

============
Copyright (c) 2009, 2010, 2011, 2012, 2013, Jerry W Jackson
<br />All rights reserved.
