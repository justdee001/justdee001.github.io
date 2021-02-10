---
layout: post
title:  "Jekyll with Github"
date:   2021-02-10 10:14:16 +0530
categories: jekyll update
---

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

### Situation -
I have added a new post my computer and now I want to upadte my github pages site.
How to push your commits to the GitHub repository from terminal? 

First step - is to check status and the branch 
```console
$ git add status

On branch gh-pages
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   .DS_Store

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	_posts/2021-02-10-New-post.markdown

no changes added to commit (use "git add" and/or "git commit -a")
```
