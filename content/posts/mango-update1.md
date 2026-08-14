+++
title = "A Quick Update on MangoWM"
author = ["Kevin Sauls"]
date = 2026-08-14T00:00:00-04:00
publishDate = 2026-08-14T00:00:00-04:00
lastmod = 2026-08-14T11:40:21-04:00
draft = false
+++

In my last post about MangoWM I noted that there were several things that I wanted to do but hadn't quite figured out.  In today's post  I want to share a few of the things I've figured out since then.


## Getting a Good Basic Configuration {#getting-a-good-basic-configuration}

To get started, you can simply copy the default configuration from /etc/mango.

```nil
# cp /etc/mango/config.conf ~/.config/mango/
```

But I wanted a bit more, so I used [DreamMaoMao's](https://github.com/DreamMaoMao/mango-config) configuration files. From what I understand, DreamMaoMao created Mango, so I figured that would be an even better starting point.

So far I've been pleased.


## Default Window Scrolling {#default-window-scrolling}

One of the differences I noted between how Niri works for me and how Mango works is that by default Niri scrolls your windows horizontally. As you open more applications, they are opened to the right (usually) of the current set of windows. This allows you to easily scroll to another application. So, for example, I can open a browser window, an Emacs window, and a terminal windows and move between simply by pressing Alt+arrow key.  In Mango, the default action is to tile the windows. As you open more applications, each window gets smaller and becomes quite cluttered. I wanted the default to scroll.

Here's how I did that:
In the rule.conf file (assuming DreamMaoMao config) the first couple of lines refer to window management. Change the line

```nil
tagrule=id:*,layoutname:tile
```

to:

```nil
tagrule=id:*,layoutname:scroller
```

The default action should now be for your apps to scroll rather than tile.

It's important to note, though, that you can set different windows to act differently. That is, the default window may scroll, but the second window could be set to tile, the third to vertical scrolling, etc.


## Opening Apps Automatically on Startup {#opening-apps-automatically-on-startup}

Another option I wanted was to have certain apps open on startup. Because this is a writing device, having Emacs open as soon as I log in is quite convenient. In addition, I wanted Firefox and a terminal to open so that each is readily available as needed.

Doing this turned out to be trival:

In the .config/mango/autostart.sh file, near the bottom, I added the following:

```nil
#Custom apps
emacs > 2/&1 /dev/null &
firefox > 2/&1 /dev/null &
kitty > 3/&1 /dev/null &
```

This, of course, will cause each of the three apps to open as tiles on the same screen. To get around that and have them open in their own screen (window?) I added the following to the rule.conf file:

```nil
windowrule=tags:2,appid:firefox
windowrule=tags:3,appid:kitty #my preferred terminal emulator
windowrule=tags:1,appid:emacs
```

Now, whenever I start my computer and log into MangoWM, these three programs will start, each in their own window and I can scroll horizontally to access them at any time.


## Turning Off the Trackpad {#turning-off-the-trackpad}

One of my greatest frustrations is to be typing along, when suddenly I realize that my cursor has jumped to somewhere else in the document and I'm messing up work that's already been completed. Generally, if I'm typing the trackpad should not respond. However, there are times when I'm not actively typing that my thumb (usually) hits the trackpad causing the cursor to move. Not good!

To get around this problem, I need to be able to turn my trackpad on or off as needed. In Niri, this required a script to be created and run, attached to a keybinding. Not so in Mango.  Mango has a built-in IPC function that can be easily attached to a keybinding. No script needed.

Here is the code which I put under the "Custom app bind" section of  bind.conf:

```nil
bind=ALT,t,toggle_trackpad_enable
```

That's it!  Now, simply using the key combo of ALT+t will toggle my trackpad.

That's all the changes I've made for now.  As I continue to use and explore MangoWM I'll share additional tips.
