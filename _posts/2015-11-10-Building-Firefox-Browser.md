---
layout:     post
title:      Building Firefox Browser
date:       2015-11-10 20:34:19
summary:    A beginners guide to building Firefox
categories: Firefox Mach Mercurial
---

Learning to build Firefox is essential if you want to study the intricate details of the browser and how the browser actually takes shape. Building Firefox is fairly easy to do provided you are having the minimum system requirements. The most important thing to have while building Firefox or any big software is to have patience. Even on some very good hardware softwares like Firefox can take a long time to build.
Following are the Step by Step Instructions for a Firefox build on Debian GNU/Linux (or any GNU/Linux distro).

__Stage I__
# Configure the Environment

Before building Firefox you need to get your system ready with the required essential libraries and dependencies. You can install these dependencies one by one through apt-get( or your systems package manager ). Or you can save your time by using a Python script made by Mozilla developers.
This Python script automatically detects whats installed on your system and whats not and installs the remaining.

1. [Pre Build Configurations] (https://developer.mozilla.org/en-US/docs/Mozilla/Developer_guide/Build_Instructions/Linux_Prerequisites)

__Stage II__
  _Getting the source to build._
  The source reequired to build firefox is obtained from the following [link](http://archive.mozilla.org/pub/firefox/releases/)
You can select the particular release of Firefox that you want to build and download its tar. In my case I did the build for Firefox 41.
Just extract this tar to a place where you want Firefox to build up.

__Stage III__
_Building Firefox_

Lets see the build for my system. When you download and extract the folder the following stuff is there in the folder.

{% highlight sh %}
raju@sanganak:~/dev/mozilla-release$ ls
accessible  build       config        dom          image    mach         moz.build                     parser      skip_subconfigures  uriloader
aclocal.m4  caps        config.cache  editor       intl     Makefile.in  mozglue                       probes      startupcache        view
addon-sdk   chrome      config.log    embedding    ipc      media        mozilla-config.h.in           python      storage             webapprt
Android.mk  client.mk   configure     extensions   js       memory       netwerk                       rdf         subconfigures       widget
AUTHORS     client.py   configure.in  gfx          layout   mfbt         nsprpub                       README.txt  testing             xpcom
b2g         CLOBBER     db            GNUmakefile  LEGAL    mobile       obj-x86_64-unknown-linux-gnu  security    toolkit             xpfe
browser     confdefs.h  docshell      hal          LICENSE  modules      other-licenses                services    tools               xulrunner
raju@sanganak:~/dev/mozilla-release$
{% endhighlight %}

From this source code you need to configure your system before doing the actual build. To do that you need to run the configure script like this.

{% highlight sh %}
raju@sanganak:~/dev/mozilla-release$ ./configure
{% endhighlight %}



3. run the [build](https://developer.mozilla.org/en-US/docs/Simple_Firefox_build)

I will elaborate this post when I get more time.
