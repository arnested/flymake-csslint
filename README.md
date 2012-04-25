# flymake-csslint

flymake-csslint.el is an [Emacs](http://www.gnu.org/software/emacs)
integration of [CSSLint](https://github.com/stubbornella/csslint). The
implementation is very much based on
[flymake-jshint.el](http://marmalade-repo.org/packages/flymake-jshint)
by [Wilfred Hughes](http://wilfred.me.uk).

## Installation and usage

The easiest way to install flymake-csslint is probably to install it
via the ELPA archive at
[Marmalade](http://marmalade-repo.org/packages/flymake-csslint).

ELPA (package.el) is part of Emacs 24. For Emacs 23 see
[Marmalade](http://marmalade-repo.org) for installation instructions.

If you don't install via ELPA make sure that flymake-csslint.el is in
your load-path and require the library

    (add-to-list 'load-path "~/.emacs.d/path/to/flymake-csslint")
    (require 'flymake-csslint)

## Requirements

To use [CSSLint](https://github.com/stubbornella/csslint) with emacs,
you will need to have a command line version of CSSLint installed, see
installation instructions at
https://github.com/stubbornella/csslint/wiki/Command-line-interface.

If the `csslint` executable is not available on your PATH your need to
configure the flymake-csslint-program variable and let it point to the
executable.

    M-x customize-variable <RET> flymake-csslint-program <RET>

## Debugging

If CSSLint isn't working for any reason, execute

    M-x set-variable <RET> flymake-log-level <RET> 3 <RET>

and you will see what is going wrong listed in the *Messages*
buffer.

## Development of flymake-csslint

flymake-csslint.el is developed at
[GitHub](https://github.com/arnested/flymake-csslint).  Feature
requests, ideas, bug reports, and pull request are more that welcome!
