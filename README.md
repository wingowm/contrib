The Wingo contrib repository is a collection of user-provided programs that 
take advantage of the scripting features in Wingo. At the moment, that only 
includes running bash commands with `wingo-cmd` or using the `pywingo` Python 
library to run commands.

Most of the scripts in this repository make use of `pywingo`, so you'll need to 
have that installed. It's on PyPI, so it can be installed with:

    pip2 install pywingo

Note that some scripts may have other dependencies. Please refer to their 
individual `README` files for the specifics.

Finally, you can manage your scripts with `wingo-contrib`:

    go get github.com/wingowm/wingo-contrib

And use it, for example:

    wingo-contrib install newproject

All scripts are installed in `$XDG_CONFIG_HOME/wingo/scripts`, which is usually 
at `~/.config/wingo/scripts`.


Submitting a script
===================
Anyone can submit a script by sending a pull request on Github. Every script 
should have its own directory, which should contain at least two files: the 
script itself (which must have the same name as the directory and be 
executable) and a `README.md` file with at least these sections in this format:

```
Description
===========
A short description about your script.


Example
=======
Example usage of your script.


Dependencies
============
A list of all dependencies of your script with each item on its own line.
This should include things like `pywingo` or `numpy`, but it is not necessary 
to include `wingo` or `wingo-cmd`. This list may also include the names of 
other scripts.
```


