---
layout: post
title:  "How to push your blog website on GitHub Pages with Termux"
date:   2026-05-04 15:38:38 +0700
---
Hi everyone! Today, i will show you how to push your blog websites on GitHub Pages with Termux.

First, make sure you following the instructions on my previous blogs [here](https://blog.xlhst.qzz.io/2026/05/04/how-to-install-jekyll-on-termux.html) before continuing to this steps.

Next, install git in Termux with following command:

{% highlight bash %}
pkg install git
{% endhighlight %}

Then go to your project directory. Example: `myblog`, `mywebsite`, etc.

{% highlight bash %}
cd <project-directory>
{% endhighlight %}

Next, initialize your project directory with `git` and add all folder & file to `git`. Then create a first commit at your project directory.

{% highlight bash %}
git init
git add .
git commit -m "initialize jekyll"
{% endhighlight %}

Then, create your GitHub repository. Make sure you have an GitHub account, if you don't have a GitHub account, create it first.

Make your repositories name like this:

{% highlight bash %}
username.github.io
{% endhighlight %}
OR
{% highlight bash %}
myblog
{% endhighlight %}

If you choose your repository name like `myblog` etc, you will get your URL like this:
{% highlight bash %}
https://username.github.io/<repo-name>
{% endhighlight %}

After creating your repository, then connect your project directory to GitHub.
{% highlight bash %}
git remote add origin https://github.com/username/username.github.io.git
git branch -M main
git push -u origin main
{% endhighlight %}

Before pushing your project dir to your GitHub repository, make sure to create Personal Access Tokens (PAT) on GitHub. Here's how to enable it:

First go to [https://github.com/settings/tokens](https://github.com/settings/tokens) and click "Generate new token (classic)". Then add a random notes and enable all `repo` and click "Generate token". Then, copy your already generated tokens. Push your project dir with `git push -u origin main` and put your username & password (your generated tokens) on `git` dialogs.

Next, enable GitHub Pages on your repo. Here's how to enable it:
1. Go to your repo on Github
2. Go to Settings > Pages
3. Source set to "Deploy from a branch". Branch set to "main" branch, "/root" folder and save.
Wait for page deployment, and you're done! You can check your pages by visiting your github.io domain.

Okay thats it for my current blogs, and I see you on next blogs!
