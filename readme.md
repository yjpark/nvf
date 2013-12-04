(N)ode (V)ersion manager for the (F)ish shell
=============================================

If you ever tried the [fish shell][fish] *and* you are a node.js developer, you'll have noticed that [nvm][nvm] doesn't work. I did.

After a couple of quick searches on google to find a solution, I wrote a small wrapper for [nave][nave], but it felt like a small ugly hack. So i decided to write a *big* ugly hack, and nvf was born.

It's nothing fancy, it's not meant to be a full-fledged project. It just "works for me". It doesn't even have an installer, and it probably will never have one.

Most of the code is basically a port to the fish scripting language of nave, plus a couple of small bits from nvm. Plus some new bugs. However I've decided to put it on bitbucket just in case it might help someone else, so feel free to download it.

Installation
============

Download and copy nvf.fish to *~/.config/fish/functions/*, then add this line to your *~/.config/fish/config.fish*:

    if test -d ~/.nvf; nvf init; end

Usage
=====

Install node with this command:

    nvf install stable

It will download and install the latest stable version of node. You can of course specify a different version, like:

    nvf install 0.8.2

or

    nvf install latest

to get the latest version available. Now you can enable it for the current session only with

    nvf local stable

(or `nvf local 0.8.2` or whatever). To automatically enable it when you open a new shell, run:

    nvf global stable

Running `nvf help` or just `nvf` will give you a brief list of all available commands, including a brief explanation on how to uninstall it.

Caveats
=======

It has bugs. It's not fully tested nor documented. Use it at your own risk. However it should work if you don't do anything fancy. If you need to do something fancy, feel free to do whatever you like to the source code.

Credits
=======

This script started as a simple conversion to fish of nave,
written by Isaac Z. Schlueter [https://github.com/isaacs/nave]()

Some ideas and/or code have been taken from nvm, written by
Tim Caswell [https://github.com/creationix/nvm]()

Some ideas might have been taken from rvm, rbenv and others.

All the bugs are my own.

This software is released in the public domain, just give credits
where credits are due.

---

[fish]: http://fishshell.com/
[nvm]: https://github.com/creationix/nvm
[nave]: https://github.com/isaacs/nave

