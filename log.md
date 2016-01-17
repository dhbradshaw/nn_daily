## 2016-01-16
django allauth had nice documentation and worked after following the installation.  There was only one hitch--it had me log in to add github information to the database, and then when I tried to test it it kept redirecting me to a nonexistant profile page because I was already logged in.  After that I logged out and tested it and it worked like a charm.  Hurray!

## 2016-01-15
Found that although there is a django-social-auth3, there is not a version compatible with django 1.9.  So I moved on to django allauth following advice from Stack Overflow.  

http://django-allauth.readthedocs.org/en/latest/installation.html

## 2016-01-14
Still working on oauth.  Tried pip install django-social-auth, but it didn't work for python3.
Found python3 compatible version:

https://pypi.python.org/pypi/django-social-auth3/0.7.23

However, it looks like it's still not caught up to the newest version of django.  So I may have to patch it.

## 2016-01-13
OAuth links:

https://developer.github.com/v3/oauth/

https://github.com/joestump/python-oauth2/wiki/Logging-into-Django-w--Twitter
```
$ python manage.py startapp nn
```


## 2016-01-12
Created a convenience script for home/bin:
```
#!/bin/bash
cd ~/projects/nn_daily
. ~/.virtualenvs/nn_daily/bin/activate
```
I call it go2nnd and invoke it using the command
```
. go2nnd
```

## 2016-01-10
Added django project and requirements.txt.  Added .git_ignore to keep .pyc and db files out of git.

## 2016-01-09
Learned about markdown headings.  Basically, use between 1 and six pound signs.  1 is like h1, and 6 is like h6.  Follow pound signs with a space, as follows:
```
# H1
## H2
### H3
#### H4
##### H5
###### H6
```
# H1
## H2
### H3
#### H4
##### H5
###### H6

Also, you can make links.  Here's an example:

```
[Markdown Basics](https://help.github.com/articles/markdown-basics/)
```

[Markdown Basics](https://help.github.com/articles/markdown-basics/)

Here's quoting:
```
> Awesome quote
```
> Awesome quote

Also, find out how to do syntax highlighting on github using this reference:

https://github.com/github/linguist/blob/master/lib/linguist/languages.yml



## 2016-01-08

I read a post about someone committing to make a public post on Github each day and decided to test it out.  I'll see how it works to try to post something most days that aren't Sundays.

In this log I'll add a bit about setup and things not reflected in the code.

For example, to set up venv for python3 on ubuntu, python3-venv failed.  Had to be more specific:
```shell
$ sudo apt-get install python3.4-venv
```
The the following created the venv:
python3 -m venv ~/.virtualenvs/nn_daily

To get github synched up, I just created nn_daily on github and then cloned it
(using
```shell
$ git clone git@github.com:dhbradshaw/nn_daily.git
```
.)
Since I'm already up and running on github, that was all it took.  Maybe the next thing is to learn basic markdown.

Okay, the first thing I learned is that triple back-ticks can be used to set apart code.  You can give a language hint after the opening back-ticks.

To activate the venv, use
```shell
. ~/.virtualenvs/nn_daily/bin/activate
```
Note the '.' and the beginning, which is shorthand for 'source'.

With the venv turned on, you can add the latest version of django.
```shell
$ pip install Django
```

I ran into an error when running the pip install, which took me here:

    http://stackoverflow.com/questions/34371266/django-1-9-installation-syntaxerror-invalid-syntax
I followed the suggestion of updating pip (using pip itself!) and the error left.

```shell
$ pip install -U pip
```
