+++
title = "Using fzf and bat for notes and cheats"
date = 2021-02-20
[taxonomies]
tags = ["cli", "linux"]
+++

I spend most of my time in terminal, So using tools like fzf and bat comes in realy handy. fzf is  creatively used from using fzf for searching bash history for running commands to opening files in vim with the fuzzy finder.

<!-- more -->

Coming to my case, I take my notes in simple plain markdown in vim and was surfing github for some intresting scripts using fzf and found lot of scripts. Of all of them one was unique - [airbornelamb's cli notes](https://github.com/airbornelamb/cli-notes). 

I [extended](https://gist.github.com/neelabalan/4a030c198cc54891f8d4162f00905702)  the script by adding bat and couple of other things to suit my needs. This script gave me an inspiration to create a terminal cheatseet script I call [nam](https://github.com/neelabalan/nam). 

Problem I am trying to solve here with `nam`
- search and execute commands
- use already existing [cheatsheet](https://github.com/cheat/cheatsheets)
- edit the cheatsheet and store cheatsheet in plain text
- save previous command(s)
- should be working offline

[![HLEOrpV.gif](https://i.postimg.cc/c4v6dYwG/HLEOrpV.gif)](https://postimg.cc/D8K7gSxx)


