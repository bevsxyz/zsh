
# ![ZSH](https://www.zsh.org/color_vertical_icon.png) THE Z SHELL (ZSH) 

## [![Version](https://img.shields.io/badge/dynamic/json?color=blue&label=Version&query=%24%5B0%5D%5B%27name%27%5D&url=https%3A%2F%2Fapi.github.com%2Frepos%2Fzsh-users%2Fzsh%2Ftags)](https://github.com/zsh-users/zsh/tags)

This is version 5.9 of the shell. This is a security and feature release.
There are several visible improvements since 5.8.1, as well as bug fixes.
All zsh installations are encouraged to upgrade as soon as possible.

Note in particular the changes highlighted under "Incompatibilities since
5.8.1" in [COMPATIBILITY](COMPATIBILITY). See [NEWS](NEWS) for more information.

## Installing Zsh

The instructions for compiling zsh are in the file [INSTALL](INSTALL).  You should
also check the file [MACHINES](MACHINES) in the top directory to see if there
are any special instructions for your particular architecture.

Note in particular the `zsh/newuser` module that guides new users through
setting basic shell options without the administrator's intervention.  This
is turned on by default.  See the section AUTOMATIC NEW USER CONFIGURATION
in [INSTALL](INSTALL) for configuration information.

## Features

Zsh is a shell with lots of features.  For a list of some of these, see the
file [FEATURES](FEATURES), and for the latest changes see [NEWS](NEWS).  For more
details, see the [documentation](https://zsh.sourceforge.io/Doc/).

## Documentation

There are a number of documents about zsh in this distribution:

Doc/Zsh/*.yo	The master source for the zsh documentation is written in
		yodl. [Yodl](https://fbb-git.github.io/yodl/) is a document language written by Karel Kubat.
		It is not required by zsh but it is a nice program so you
		might want to get it anyway, especially if you are a zsh
		developer.  It can be downloaded from
		https://fbb-git.github.io/yodl/

Doc/zsh\*.1	Man pages in *nroff* format.  These will be installed
		by `make install.man` or `make install`.  By default,
		these will be installed in `/usr/local/man/man1`, although
		you can change this with the `--mandir` option to configure
		or editing the user configuration section of the top level
		Makefile.

Doc/zsh.texi	Everything the man pages have, but in texinfo format.  These
		will be installed by `make install.info` or `make install`.
		By default, these will be installed in `/usr/local/info`,
		although you can change this with the `--infodir` option to
		configure or editing the user configuration section of the
		top level Makefile.  Version 4.0 or above of the
		Texinfo tools are recommended for processing this file.

Also included in the distribution are:

Doc/intro.ms	An introduction to zsh in troff format using the ms
		macros.  This document explains many of the features
		that make zsh more equal than other shells.
		Unfortunately this is based on zsh-2.5 so some examples
		may not work without changes but it is still a good
		introduction.

For more information, see the website, as described in the [META-FAQ](https://www.zsh.org/pub/META-FAQ).

If you do not have the necessary tools to process these documents, PDF,
Info and DVI versions are available in the separate file zsh-doc.tar.gz at
the archive sites listed in the [META-FAQ](https://www.zsh.org/pub/META-FAQ).

The distribution also contains a Perl script in `Utils/helpfiles` which
can be used to extract the descriptions of builtin commands from the
`zshbuiltins` manual page.  See the comments at the beginning of the
script about its usage.  The files created by this script can be used
by example function run-help located in the subdirectory `Functions/Misc` to
show information about zsh builtins and run `man` on external commands.
For this the shell variable `HELPDIR` should point to a directory containing
the files generated by the helpfiles script.  `run-help` should be
unaliased before loading the `run-help` function.  After that this function
will be executed by the `run-help` ZLE function which is by default bound
to `ESC-h` in emacs mode.

### Examples

Examples of zsh startup files are located in the subdirectory
[StartupFiles](StartupFiles/).  Examples of zsh functions and scripts are located in
the subdirectory [Functions](Functions/).  Examples of completion control commands
(compctl) are located in the file [Misc/compctl-examples](Misc/compctl-examples).

### Zsh FTP Sites, Web Pages, and Mailing Lists

The current list of zsh FTP sites, web pages, and mailing lists can be
found in the [META-FAQ](https://www.zsh.org/pub/META-FAQ).  A copy is included in this distribution and is
available separately at any of the zsh FTP sites.

### Common Problems and Frequently Asked Questions

Zsh has a list of [Frequently Asked Questions (FAQ)](https://zsh.sourceforge.io/FAQ/) maintained by Peter
Stephenson <pws@zsh.org>.  It covers many common problems encountered
when building, installing, and using zsh.  A copy is included in this
distribution in [Etc/FAQ](Etc/FAQ.yo) and is available separately at any of the zsh
ftp sites.

## Zsh Maintenance and Bug Reports

Zsh is currently maintained by the members of the zsh-workers mailing list
and coordinated by Peter Stephenson <coordinator@zsh.org>.  Please send
any feedback and bugs reports to <zsh-workers@zsh.org>.

Reports are most helpful if you can reproduce the bug starting zsh with
the `-f` option.  This skips the execution of local startup files except
`/etc/zshenv`.  If a bug occurs only when some options set try to locate
the option which triggers the bug.

There is a script [reporter](Util/reporter) in the subdirectory Util which will print out
your current shell environment/setup.  If you cannot reproduce the bug
with `zsh -f`, use this script and include the output from sourcing this
file.  This way, the problem you are reporting can be recreated.

The known bugs in zsh are listed in the file [Etc/BUGS](Etc/BUGS).  Check this as
well as the [Frequently Asked Questions (FAQ)](https://zsh.sourceforge.io/FAQ/) list before sending a bug
report.  Note that zsh has some features which are not compatible with
sh but these are not bugs.  Most of these incompatibilities go away
when zsh is invoked as sh or ksh (e.g. using a symbolic link).

If you send a bug report to the list and are not a subscriber, please
mention this in your message if you want a response.

If you would like to contribute to the development and maintenance of zsh,
then you should join the zsh-workers mailing list (check the [META-FAQ](https://www.zsh.org/pub/META-FAQ)
for info on this).  You should also read the [zsh-development-guide](Etc/zsh-development-guide)
located in the subdirectory Etc.

## Contributors

The people who have contributed to this software project are listed
in [Etc/CONTRIBUTORS](Etc/CONTRIBUTORS).
