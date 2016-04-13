---
layout: post
title: How to version control vector graphics from your iPad
twitter_username: pietbrauer
categories: blog
---

If you are working as a designer or are a developer and do your own graphics you might use version control for it. Until now there weren't any vector graphics apps like Sketch out for iOS but that changed on April 16, 2016.


## Meet Bez

[Bez](http://www.juicybitssoftware.com/bez/) is an app developed by fellow indie developers at [Juicy Bits](http://www.juicybitssoftware.com). It was launched today and got a [bit of traction](http://daringfireball.net/linked/2016/04/12/bez) on the interwebs. We also downloaded the app immediately. 
Seeing the potential that lies in the app is just incredible. We all know that the iPad is superior when it comes to drawing using the Apple Pencil and direct manipulation of the object, rather than using a graphics tablet and Adobe Photoshop. The only thing missing in addition to [Pixelmator](http://www.pixelmator.com/ios/) and [Procreate](http://procreate.si/) was a tool for vector graphics.

As John Gruber put it:

> It’s a serious, professional-quality design tool. Fascinating to me, too, as a long-time Mac UI nerd, at how “pro” style iOS apps are evolving.
> – John Gruber, [Daring Fireball](http://daringfireball.net/linked/2016/04/12/bez)

Most of our icons on the website are retina ready and use SVG vector graphics. So when I made the different pages we had to use a computer to produce the actual graphics. Once finished there was no way for us to try them out or alter them directly on the iOS device, this is were Bez comes in.

## Integration with Git2Go

Thanks to Bez' superior use of System Components you can import SVG graphics from apps using the Document Provider Extension by simply tapping the little download cloud at the bottom of the screen.

![Download cloud in action]({{ site.url }}/img/2016-04-13-bez-import.jgg)

You can then alter the graphics in Bez and export them to Git2Go using the export method.

![Export action]({{ site.url }}/img/2016-04-13-export-bez.jpg)

This makes it really simple to see the changes of your SVG in Git2Go at a glance.

![SVG Diff]({{ site.url }}/img/2016-04-13-svg-diff.jpg)

We would welcome inplace editing (a.k.a. Open from ...) of SVG files without the need to import/export files every time, but I am sure there were reasons to implement this option. Secondly I would love to be able import [Sketch](https://www.sketchapp.com/) files to migrate all of our work into this amazing tool.
[Mike Swanson](https://twitter.com/anyware) (the developer) pointed out [on Twitter](https://twitter.com/Anyware/status/720051314135162880) that there will be loads of future updates.

We look forward to the development of Bez and give them a warm welcome to the App Store!
