---
layout: post
title: How to use git version control
---
Version control systems are widely used in software companies to maintain different versions of the code.Version control systems will simplify all the complexities involved in maintaining code base,  when code becomes large and multiple people are simultaneously working on it.Git is one of the popular system.Following are useful git commands
**Clone a Project**
Cloning a project is like maintaining entire code base on your local system.So you can modify code on your local system and later you can push the changes to the main repository.

$  git clone [repository url]

**Commit a change**
When you modify your code and made sure that  it passed all tests ,then you can commit your code.When you commit your code ,the changes are committed only to your local sytem not to the main repository.

In order to commit your code,you have to add files which are changed and to be committed.
Example:
You changed files  abc.txt and xyz.txt but you only want to commit abc.txt then type
\$   git add abc.txt
$ git commit -m "message"

You can check what files are changed using 

$ git status

**Push changes**
Before you push your changes to remote repository ,you have to pull changes which happened in remote repository.

\$ git pull  -- rebase
$ git push

If you get any conflict you have to resolve it and push your code.

Note: Some times you have stash your changed files which are not committed
$ git stash

To apply those stash files 

$ git stash apply
