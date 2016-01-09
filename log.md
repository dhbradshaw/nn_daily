2015-01-08

-- Read a post about someone committing to make a public post on Github each day and decided to test it out.

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
