+++
title = "Creating a gist of Github Gist using Github Actions"
date = 2021-04-04
[taxonomies]
tags = ["github", "python"]
+++

*Gists are underrated*. I use gists when the code doesn't deserve it's own repository and I often refer to my gists from different devices. So I decided to write a [python script](https://github.com/neelabalan/GistOfGists/blob/master/gistofgists.py) using [pytablewriter](https://pypi.org/project/pytablewriter/) module to compose all my gists in markdown table format so that the README will render it nicely. 

<!-- more -->

Coming to Github Actions I've setup a seperate [repo](https://github.com/neelabalan/mygists) with `update_readme.yml` to update the table everyday at a specified time.


![Screenshot_2021-03-04_16-11-33.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1614854514080/Glh-JrAPh.png)

Other interesting links related to Github Gist

- [the-way](https://github.com/out-of-cheese-error/the-way) is a command line code snippet manager written in rust. The snippets can be uploaded as gist.
- [awesome gists](https://github.com/vsouza/awesome-gists)
- [gist](https://marketplace.visualstudio.com/items?itemName=kenhowardpdx.vscode-gist) access github gist from VSCode
