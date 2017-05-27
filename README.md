init
====

My simple initialization script for starting new text files.

Rational
--------

I live in the command line and I write a LOT of text files, mostly Markdown files. And the way I like to work is to `touch` the file and load it into [Sublime Text][] for editing. Also if it's a script to start it off with a bang path. I rarely write scripts that require the use of me providing the interpreter on the command line. Just a waste of keystrokes for me in most cases. Since this is such a thing I figured I'd automate it a bit.  :-D


Usage
-----

``` bash
$ init README.md
```

This will `touch` the file and load it into [Sublime Text][] as long as the `subl` command is present in your current `$PATH`.



[Sublime Text]: https://www.sublimetext.com