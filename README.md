## Use buildout with kivy

If you've never used buildout before look at buildout.cfg the list
of eggs is the set of dependencies to download and use with your
project.

It's worth noting that putting kivy in your buildout.cfg will work
on osx and linux, but not on windows; to be cross platform nicely
you are better using downloading kivy manually on the target system
and loading it manually.


### OSX

Buildout:

    kivy bootstrap.py
    ./bin/buildout

Run:

    kivy ./bin/py plasma.py


## Windows

Use msys, seriously, if you're using the default terminal, don't bother.

On the bright side, msys and kivy to work very well together~ :)

Buildout:

    /c/path/to/python/python bootstrap.py
    ./bin/buildout

Run:
    . /c/path/to/kivy/kivyenv.sh
    ./bin/py plasma.py

Didn't work? Make sure you did '. /c/kivy/kivyenv.sh', otherwise the environment
variables won't be loaded. Check with 'echo $PYTHONPATH'; it should contain a
reference to the kivy folder.
