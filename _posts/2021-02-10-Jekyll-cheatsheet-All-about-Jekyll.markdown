---
layout: post
title:  "Jekyll cheatsheet - All about Jekyll"
date:   2021-02-10 10:14:16 +0530
categories: jekyll update
---
# Jekyll cheatsheet

- To locate a theme’s files on your computer
```console
$ bundle info --path minima
```

- To add new site
```console
$ jekyll new myblog
$ cd myblog
```

- To build the site and make it available on a local server.
```console
$ bundle exec jekyll serve
```

If <b>cannot load such file -- webrick (LoadError)</b> load error occurs after serving like this -
```console
Jekyll 4.2.0   Please append `--trace` to the `serve` command 
                     for any additional information or backtrace. 
                    ------------------------------------------------
/usr/local/lib/ruby/gems/3.0.0/gems/jekyll-4.2.0/lib/jekyll/commands/serve/servlet.rb:3:in `require': cannot load such file -- webrick (LoadError)
```
then add
```console
$ bundle add webrick
```

