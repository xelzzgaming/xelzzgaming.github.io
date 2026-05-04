---
layout: post
title:  "How to Install Jekyll on Termux"
date:   2026-05-04 13:38:13 +0700
---
Today I will make a tutorial on how to install Jekyll on Termux.

First, make sure to install Termux first on Github Releases or F-Droid.
Then, open the Termux APK. and install it. After you install Termux on
your phone, make sure you update & upgrade the dependencies with the
following command:

{% highlight bash %}
pkg update && pkg upgrade -y
{% endhighlight %}

After that, install the Ruby & Clang, then install Jekyll with `gem` command.
Its may take a while installing the Jekyll with `gem install jekyll`, you
should wait until the process has finished.

{% highlight bash %}
pkg install ruby clang -y
gem install jekyll
{% endhighlight %}

Then, make a new project with `jekyll new` command. For example:

{% highlight bash %}
jekyll new mywebsite
{% endhighlight %}

Finally, after making a new project, run the server with command:

{% highlight bash %}
bundle exec jekyll serve
{% endhighlight %}

Make sure you change the directory to your project folder, like `mywebsite`,
`myblog`, etc.

Thats it! You can customize the theme, changing the blog name, etc!
For changing the theme, blog name, etc, i will make the tutorial on
next blog. I see you later on next blog!