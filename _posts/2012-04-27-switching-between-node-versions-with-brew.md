---
layout: post
title: "Switching between node versions with brew"
description: ""
category: Programming
tags: [node, homebrew, brew]
---
{% include JB/setup %}

Sometimes as a developer, you may have to switch packages in your computer,
depending the project, do it with Mac OS X and homebrew is pretty easy. I had to
switch versions for a project, I had node v0.6.15 already and I needed to use
node v0.4.10 so I did the next:

{% highlight bash %}
    $ cd /usr/local
    $ brew versions node
{% endhighlight %}

Then it showed to me:

{% highlight bash %}
    0.6.15   git checkout e18b02f Library/Formula/node.rb
    0.6.14   git checkout 30813c8 Library/Formula/node.rb
    0.6.13   git checkout 3b771d0 Library/Formula/node.rb
    0.6.12   git checkout 0e8ea8a Library/Formula/node.rb
    0.6.11   git checkout 3eec1f4 Library/Formula/node.rb
    0.6.10   git checkout 7e202eb Library/Formula/node.rb
    0.6.9    git checkout f752570 Library/Formula/node.rb
    0.6.8    git checkout 74bff39 Library/Formula/node.rb
    0.6.7    git checkout 9a52dcf Library/Formula/node.rb
    0.6.6    git checkout 97fce9a Library/Formula/node.rb
    0.6.5    git checkout 911726f Library/Formula/node.rb
    0.6.4    git checkout 67a2615 Library/Formula/node.rb
    0.6.2    git checkout 05b94b9 Library/Formula/node.rb
    0.6.1    git checkout b6eb4fc Library/Formula/node.rb
    0.6.0    git checkout 6bec7fc Library/Formula/node.rb
    0.4.12   git checkout 3eea412 Library/Formula/node.rb
    0.4.11   git checkout b6aa338 Library/Formula/node.rb
    0.4.10   git checkout 523d360 Library/Formula/node.rb
    0.4.9    git checkout 10b3ded Library/Formula/node.rb
    0.4.8    git checkout 8d45d93 Library/Formula/node.rb
    0.4.7    git checkout cb6a4b4 Library/Formula/node.rb
    0.4.6    git checkout 7c0f0d9 Library/Formula/node.rb
    0.4.5    git checkout 8241b81 Library/Formula/node.rb
    0.4.4    git checkout 83753a9 Library/Formula/node.rb
    0.4.3    git checkout f4a925d Library/Formula/node.rb
    0.4.2    git checkout 0476235 Library/Formula/node.rb
    0.4.1    git checkout 8a60de4 Library/Formula/node.rb
    0.4.0    git checkout b4497ec Library/Formula/node.rb
    0.2.6    git checkout 8602eee Library/Formula/node.rb
    0.3.2    git checkout 168cb3d Library/Formula/node.rb
    0.2.5    git checkout f55f417 Library/Formula/node.rb
    0.2.4    git checkout 89438ae Library/Formula/node.rb
    0.2.3    git checkout 730f311 Library/Formula/node.rb
    0.2.2    git checkout 981bb41 Library/Formula/node.rb
    0.2.1    git checkout c963a35 Library/Formula/node.rb
    0.2.0    git checkout fbb93d9 Library/Formula/node.rb
    0.1.104  git checkout ed51a5b Library/Formula/node.rb
    0.1.103  git checkout f3e7c1b Library/Formula/node.rb
    0.1.20   git checkout 2baa60c Library/Formula/node.rb
    0.1.17   git checkout ab7697f Library/Formula/node.rb
    0.1.14   git checkout a82e823 Library/Formula/node.rb
{% endhighlight%}

Then I selected mine:

{% highlight bash %}
    $ git checkout 523d360 Library/Formula/node.rb
    $ brew unlink node # Do this if have not unlinked it yet.
    $ brew install node
{% endhighlight %}

Now you can switch between versions like this:

{% highlight bash %}
    $ brew switch node 0.6.15
    $ brew switch node 0.4.10
{% endhighlight %}

Easy like that! This works for every package installed with brew, PostgreSQL,
PostGIS, MySQL, etc, etc.