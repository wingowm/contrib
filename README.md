The Wingo contrib repository is a collection of user-provided programs that 
take advantage of the scripting features in Wingo. At the moment, that only 
includes running bash commands with `wingo-cmd` or using the `pywingo` Python 
library to run commands.

Most of the scripts in this repository make use of `pywingo`, so you'll need to 
have that installed. It's on PyPI, so it can be installed with:

```bash
pip2 install pywingo
```

Note that some scripts may have other dependencies. Please refer to their 
individual `README` files for the specifics.

Finally, you can manage your scripts with `wingo-contrib`:

```bash
go get github.com/wingowm/wingo-contrib
```

And use it, for example:

```bash
wingo-contrib install newproject
```

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

You may also include a configuration file named `your-script-name.cfg`. If 
you're using `pywingo`, then it is convenient to use the `ini` format 
compatible with Python's 
[ConfigParser](http://docs.python.org/2.7/library/configparser.html#module-ConfigParser), 
but you're free to use your own format.

