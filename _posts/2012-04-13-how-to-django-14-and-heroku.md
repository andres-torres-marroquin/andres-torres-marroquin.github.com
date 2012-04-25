---
layout: post
title: "How to Django 1.4 and Heroku"
description: ""
category: Django
tags: [heroku, django, git, virtualenv]
---
{% include JB/setup %}


Heroku is a very complete, scalable and reliable platform, but the last update from part of the Django guys have changed the things a bit. The Django 1.4 directory structure is different and Heroku Buildpack (at this time) has not been updated yet. So I added some code fixing this behavior, at [this pull request](https://github.com/heroku/heroku-buildpack-python/pull/35), but it seems that the Heroku guys have not updated it yet, but that is not a blocker.

When we create the Heroku instance we can define a custom buildpack, in this case the Heroku one, we just need to create it in this way:

{% highlight bash %}
    $ heroku create --stack cedar --buildpack https://github.com/heroku/heroku-buildpack-python.git
{% endhighlight %}

So this will create the new Heroku instance with Django 1.4 support.

## Creating a Heroku instance for Django from scratch

{% highlight bash %}
    $ mkdir mysite && cd mysite
    $ virtualenv --no-site-packages .
    $ source bin/activate
    $ cat > .gitignore <<EOF
# Python
*.pyc

# Virtualenv
/bin
/include
/build
/lib
/lib64
/src
/share
/man
.Python
EOF
    $ cat > requirements.txt <<EOF
django==1.4
psycopg2==2.4.2
EOF
    $ cat > Procfile <<EOF
web: python mysite/manage.py runserver 0.0.0.0:\$PORT
EOF
    $ pip install -r requirements.txt
    $ django-admin.py startproject mysite
    $ chmod 755 mysite/manage.py
    $ git init
    $ heroku create --stack cedar --buildpack https://github.com/heroku/heroku-buildpack-python.git
    $ git add .
    $ git commit -m "First commit"
    $ git push heroku master
    $ heroku open
{% endhighlight %}

And then you're done, you have a new Heroku instance running with Django 1.4.