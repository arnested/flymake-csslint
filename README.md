# flymake-csslint.el

To use [CSSLint](https://github.com/stubbornella/csslint) with emacs,
you will need CSSLint installed and available on your path. You should
be able to do

	$ csslint

without problem. To do this, you can install node.js, npm and
csslint by doing the following:

	$ apt-get install nodejs # or your distro / OS equivalent
	$ curl http://npmjs.org/install.sh | sh
	$ npm install -g csslint

flymake-csslint.el is very much based on flymake-jshint.el by
[Wilfred Hughes](<me@wilfred.me.uk>).

## Usage

Add to your emacs config:

	(require 'flymake-csslint)
	(add-hook 'css-mode-hook 'flymake-mode)

making sure that flymake-csslint.el is on your load-path. If not,
also add to your config:

	(add-to-list 'load-path "~/.emacs.d/path/to/flymake-csslint.el")

## Debugging

If CSSLint isn't working for any reason, execute

	M-x set-variable flymake-log-level <RET> 3

and you will see what is going wrong listed in the *Messages*
buffer.
