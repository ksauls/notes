---
title : "Fixing OpenBSD Touchpad Palm Rejection Issues"
date : "2025-08-18T14:03:21-04:00"
#dateFormat : "2006-01-02" # This value can be configured for per-post date formatting
author : "Kevin Sauls"
#authorTwitter : "" #do not include @
#cover : ""
tags : ["projects", "OpenBSD", "technology"]
categories: ["technology", "projects"]
keywords : ["", ""]
#description : ""
showFullContent : false
readingTime : true

hideComments : true
---
# Toggling the Touchpad in OpenBSD on Lenovo X250 to Address Palm Rejection Issues.

So, one of the challenges I encountered with OpenBSD is that the touchpad does a really bad job of rejecting motion from my palm.  While writing in Emacs I'd often find my mouse jumping around and my writing not where I expected it to be.

After some digging around I found a solution:

 # How to setup OpenBSD in i3 to toggle touchpad

Create a file in ~/home/bin/ called “toggle-touchpad.sh”
```
# Get the current state of the touchpad
   current_state=$(doas /sbin/wsconsctl mouse.tp.disable | cut -d'=' -f2)
    
      if [ "$current_state" = "0" ]; then
              # If currently enabled (0), disable it (1)
	      doas /sbin/wsconsctl mouse.tp.disable=1
           echo "Touchpad disabled."
                                         else
# If currently disabled (1), enable it (0)
doas /sbin/wsconsctl mouse.tp.disable=0
          echo "Touchpad enabled."
      fi
```
Then, in /etc/doas.conf add:
```
permit nopass :wheel cmd /sbin/wsconsctl
```
Finally, in your i3 config file (~/.config/i3/config) Add

```
bindsym $mod+t ~/bin/toggle-touchpad.sh
```
Reload i3 with ```ctrl+$mod+c```.

Now you should be able to toggle the touchpad on and off with $mod+t to avoid issues related to poor palm rejection. (I chose $mod+t [for touchpad] and because it was available.  You can choose any other combination you choose.) 

NOTE: I have not tested this script with any other DE or window manager.
