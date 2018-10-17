# swc-sample-irene
Sample project for the git lesson of embl software carpentry course
- The official git webpage and documentation is in this [link](https://git-scm.com/)

## Starting a Git Repository in GitHub

- Create the repo in GitHub and clone to a local directory

## In general:

- To check the repo settings:
```bash
git config -l
```

- To set user email
```bash
git config --global user.email irene.de.t@gmail.com
git config --global user.name "Irene de Teresa"
```
- Add, commit:

```bash
git add filename
git commit -m "the message"
```

or, to not have restrictions to message length:

``` bash
git commit
``` 
 The basic process is **file -> add (which brings to a 'stage') -> commit (adds the version to .git)**
 **.git** is the directory where the repo will be developed so *do not modify*  

- To see the history of versons and commits

```bash
git log #or
git log --oneline
```
- To push to a remote repository in GitHub:

```bash
?
```

## Quick markdown overview

- For bullets, use a small '-'
- Create **bold text** use '**'
- Create *emphasized text* use '*'
- For [links](http://www.something.com) one uses '[link name](url)'

## Good practices in **git**

- The commit message should be descriptive

