## 2015-01-09
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



## 2015-01-08

I read a post about someone committing to make a public post on Github each day and decided to test it out.  I'll see how it works to try to post something most days that aren't Sundays.

In this log I'll add a bit about setup and things not reflected in the code.

For example, to set up venv for python3 on ubuntu, python3-venv failed.  Had to be more specific:
```bash
    $ sudo apt-get install python3.4-venv
```
The the following created the venv:
python3 -m venv ~/.virtualenvs/nn_daily

To get github synched up, I just created nn_daily on github and then cloned it
(using
```bash
$ git clone git@github.com:dhbradshaw/nn_daily.git
```
.)
Since I'm already up and running on github, that was all it took.  Maybe the next thing is to learn basic markdown.

Okay, the first thing I learned is that triple back-ticks can be used to set apart code.  You can give a language hint after the opening back-ticks.

To activate the venv, use
```bash
. ~/.virtualenvs/nn_daily/bin/activate
```
Note the '.' and the beginning, which is shorthand for 'source'.

With the venv turned on, you can add the latest version of django.
```bash
$ pip install Django
```

I ran into an error when running the pip install, which took me here:

    http://stackoverflow.com/questions/34371266/django-1-9-installation-syntaxerror-invalid-syntax
I followed the suggestion of updating pip (using pip itself!) and the error left.

```bash
$ pip install -U pip
```
