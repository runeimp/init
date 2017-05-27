init
====

My simple initialization script for starting new text files, scripts and projects.


Rational
--------

I live in the command line and I write a LOT of scripts and text files, mostly Markdown files. And the way I like to work is to `touch` the file and load it into [Sublime Text][] for editing. Also if it's a script to start it off with a bang path. I rarely write scripts that require the use of me providing the interpreter on the command line. Just a waste of keystrokes for me in most cases. Since this is such a thing I figured I'd automate it a bit.  :-D


Usage
-----

``` bash
$ init README.md LICENSE WTF.txt
# -or-
$ init -x script1 script2 script3
# -or-
$ init -xp script script2 script3
```

This will `touch` the file and load it into your text editor of choice as long as long as one of the environment variables `$INIT_EDITOR`, `$VISUAL`, or `$EDITOR` is set. The order of precedence is `$INIT_EDITOR`, `$VISUAL`, then `$EDITOR`. Otherwise the `subl` command will be used. Make sure one of the four options is present in your current `$PATH`.

In the case of a script when using `-x`, `-exec`, or `--executable` the file will also have `chmod +x` applied to it.

Generated text files are initially empty. But generated scripts look like:

``` bash
$ init -x script_name

#!/usr/bin/env bash
###################
# script_name
#
#




```

Using one of the options `-p`, `-proj`, `--project` will also create a project directory based on the name of the first filename given and then generate all script files in that directory. Files generated will be empty text files unless you specify one of the "executable" options or use on the magic combo shortcuts `-xp` or `-px`.


ToDo
----

* [ ] Allow for definition and usage of custom templates.
* [x] Option to create a project folder as well.
* [x] Utilize the text editor specified in `$VISUAL` or `$EDITOR` environment variables if set.



[Sublime Text]: https://www.sublimetext.com

