=========
 git-bzr
=========

----------------------------------------
Bidirectional bridge between git and bzr
----------------------------------------

:Date:   2012-12-07
:Manual section: 1
:Manual group: Git-Bzr-Ng

SYNOPSIS
========

| `git bzr init`
| `git bzr clone` [--strip_tags] <url> [<target>]
| `git bzr clear` [<bzr_branch>]
| `git bzr push` [--overwrite] [--parent_branch=<parent_branch>] [<url>]
| `git bzr sync` [--overwrite] <bzr_branch>
| `git bzr pull` [--overwrite] <bzr_branch>
| `git bzr import` [--strip_tags] <url> <new_branch>
| `git bzr marks` [--file] [--git|--bzr]

DESCRIPTION
===========

A bidirectional bridge between git and bzr that lets you stop worrying
which version control the code you love is using -- as long as they are
using git or bzr.

COMMANDS
========

Several subcommands are available.
With no arguments specified, shows the available subcommands.

`init`
------

Initialize a new bzr tracking branch based on master.

`clone`
-------

Clone a bzr branch from <url> into the `master` branch of a newly
created git repository in <target>.
If the <target> isn't specified, it's deduced from the <url>.
Like `git clone`, it creates remote-tracking bzr branches.

With ``--strip_tags``, tags are stripped from bzr when importing.

`clear`
-------

Remove bzr tracking branches for <bzr_branch>, or the current branch, if
not specified.

`push`
------

Push to the bzr repository <url> (or the remembered url, if not
specified).

With ``--parent_branch=<parent_branch>``, <parent_branch> is used as the
parent branch.

With ``--overwrite``, history can be overwritten.

`sync`
------

Sync bzr tracking branch <bzr_branch>.

With ``--overwrite``, history can be overwritten.

`pull`
------

Sync bzr tracking branch <bzr_branch> and pull from it.

With ``--overwrite``, history can be overwritten.

`import`
--------

Import bzr branch <url> into a git repository, as <new_branch>.

With ``--strip_tags``, tags are stripped from bzr when importing.

`marks`
-------

Display the current marks files for the current branch.
By default, the git marks are shown, with ``--bzr``, the bzr marks are
shown.

With ``--file``, the marks file name is shown, rather than its contents.

SEE ALSO
========

``git``\ (1),
``bzr``\ (1)
