+++
title = "Using rich python library to beautify CLI app"
date = 2021-04-06
[taxonomies]
tags = ["python"]
+++

Rich is an opensource python library by *Will McGugan* for beautiful text formatting in the terminal. Rich has close to 30k stars in github and more than [500 packages](https://github.com/willmcgugan/rich/network/dependents?dependent_type=PACKAGE&package_id=UGFja2FnZS02OTk5NjU1NDU%3D) are using it.

<!-- more -->

 I wrote a [script](https://github.com/neelabalan/gca) a while back to clone all publicly available repositories of a github user along with the user's gists so I thought I could maybe use rich here to beautify the app.

I've previously used [rich](https://github.com/willmcgugan/rich) for my [stoicquote](https://github.com/neelabalan/stoicquote) script but wanted to try something more with it. Rich's [Progress Display](https://rich.readthedocs.io/en/latest/progress.html) is pretty cool so I went ahead and used that.

Here's how it looks like 
![gif](https://i.imgur.com/3UJQech.gif)


Other cool projects using rich

- [ghtop](https://github.com/nat/ghtop) 
> provides a number of views of all current public activity from all users across the entire GitHub platform
![gif](https://user-images.githubusercontent.com/1483922/105071141-0c3ea580-5a39-11eb-8808-34952c0bf26d.gif)

- [ward](https://github.com/darrenburns/ward) 
> a modern python test framework that uses rich for highlighting difference to help fix issues faster

- [clubhouse-py](https://github.com/stypr/clubhouse-py)
