---
layout: post
title:  "Jekyll with Github"
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
- To locate a theme’s files on your computer.
```console
$ bundle info --path minima
```

Common problems and their solution
#### Situation-
I have made changes locally on jekyll site and now I want to push these changes to github (remote) in the new branch. But I am in the gh-pages branch (or any banch). 
How to switch to new branch and commit changes to a new branch?

#### Solution-
To commit changes to a new branch - Lets name this branch <b>wonder</b>

```console
$ git checkout -b wonder
# wonder is  new branch name
```
And output of this command is
```console
Switched to a new branch 'wonder'
```
To check 
```console
$ git status
On branch wonder # Congratulations you did it.
_
_
_
```

then


```console
$ git add .
# this add all the changes at once
$ git commit -m "type-something-meaningful"
$ git push origin your-new-branch 
```
Done.

---

#### Situation-
I have added a new post my computer and now I want to upadte my github pages site.
How to push your commits to the GitHub repository from terminal? 

#### Solution-
First step - is to check status and the branch.
```console
$ git add status

On branch gh-pages
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   .DS_Store

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	_posts/2021-02-10-new-post.markdown

no changes added to commit (use "git add" and/or "git commit -a")
```

Second step - is to save the progress. 
 ```console
$ git add .
```
now check git status and it will show:
```console
$ git add .
On branch gh-pages
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	modified:   .DS_Store
	new file:   _posts/2021-02-10-new-post.markdown
```

Now commit changes:
```console
$ git commit -m "Something Meaningful"

[new 53df651]  Something Meaningful
 2 files changed, 62 insertions(+)
 create mode 100644 _posts/2021-02-10-new-post.markdown
```
Third step - is to send your changes to the remote repository.

```console
$ git push origin gh-pages
# Use git push with your branch name and done
```
Its done, go check out github pages or check your domain.
