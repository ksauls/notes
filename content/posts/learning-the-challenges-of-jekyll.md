---
title: ' Learning the Challenges of Jekyll'
date: 2017-11-13
categories:
    - projects
tags:
    - websites
---
# Learning the Challenges of Jekyll

So a few days ago I decided to use Jekyll to generate a static website to host 
all -- well, most -- of my writing.  Jekyll, I've learned, is a different beast 
from most applications used for these purposes.  I've found several themes that 
I really liked, but they all had some sort of quirks that made them less easy to 
use.  I'm finding, though, that "easy to use" and "Jekyll" probably don't belong 
in the same sentence. Each of the themes I've looked at require slightly 
different structures, use categories differently, and just generally appear 
rather finicky.  I'm sure for people that have played with it for quite a while, <!-- more -->
these quirks are just part of the landscape. For people like me, who haven't 
really spent much time with the software, it's a challenge.

### Making Links Work

One of the challenges that I've encountered is making links work from the 
dynamically created pages..  Say 
for 
example, I have a a post entitled, "Blogging with Jekyll". When I generate the 
site, Jekyll automatically creates a link to that post.  BUT, some of the themes 
I played with didn't generate the full link. They pointed me to the title, but 
had not appended the '.html' to the page. The result? A blank page.  It took 
some Googling around to find out that adding the '.html' to the end of the 
':title' part of the permalink fixed the problem.  Simple fix, once I finally 
found it, but why was that ever a problem? Why wasn't the '.html' added by the 
theme creator?  Surely his or her copy of the script didn't work without that 
extension, either.  Not sure what I mean?

In the _config.yml file I found:
```permalink:           /:title

What is needed is 
 permalink:           /:title.html
```
x
Again, simple fix ....

## Navigation Problems.

Similarly, I wanted a theme that included navigation so that anyone reading the 
site could move around within it.  One of the themes I really like didn't have 
navigation.  I probably could have added it but, frankly, didn't want to take 
the time to figure it out.  So, I settled for one that included navigation.  
Except that the navigation didn't work correctly.  I'm not working from my 
webserver root, so a baseurl is needed.  The navigation (home, back, and next 
buttons) didn't account for a non-root structure.  So, after a bit of plugging 
about I finally found the template that contains thenavigation links (they're 
not 
always in the same 
place from one theme to another). Search about until I found the right variables 
to include.  Now, I have:

``` {% raw %}{{ site.baseurl }}\{{ page.previous.url }} {% endraw %} ```

This works correctly.  I had to do this for the home button, as well as the 
previous and next buttons.  And, I'm sure as I continue to work with the site, 
I'll find other things like this.

## Conclusion

As it stands right now, I'll use this theme.  As I work more with the scripts, 
I'm beginning to understand them a little better.  But I'd much rather spend my 
time writing than trying to fix the platform that I'm using to host that 
writing.  Yes, Wordpress or some such would have been easier, but, as I said in 
[this post](../blogging-with-jekyll) I 
really 
do think that a database driven website is overkill for my needs.
