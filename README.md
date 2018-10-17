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

- To set user email and preferences
```bash
git config --global user.email irene.de.t@gmail.com
git config --global user.name "Irene de Teresa"
git config --global core.editor nano
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

- diff is a tool that shows changes between versions and repository copies:


```
git diff
```

in stage:

```
git diff --staged
```

or between two versions in the local repo:

```
git diff b856f26 b1f794b
```

to check changes since some version to the current one:

```bash
git diff 9bdd448
```

to color the changes:

```bash
git diff --color-words 9bdd448
```

- To undo commits!:

```bash
git checkout -- README.md
```

- To go back in time:

	First, you have to be in a **clean** state (commit all changes)

	And then go to the desired working copy, e.g. b856f26:

	```bash
	git checkout b856f26
	```

	Now the HEAD will be in that point in time

	- Now one can do a branch

	```bash
	git checkout -b one_sample_branch
	``` 



## Relation local/remote repos


- To push to a remote repository in GitHub:

```bash
git push
```
- To pull changes from remote repo

```bash
git pull
```

## For collaborations

- If the other person has already commited changes to the 
remote repo, you have to first **pull** those changes and then **push**:

```bash
git pull
# Add a message to explain why you will pull
git push
```
- When both change the same piece of the repository, the merging can't be done automatically. In the corresponding file one sees the
<<<<<<< >>>>>>> symbols and tokens related to the different versions. So one has to edit manually and decide what to chose:
```bash
nano conflicting_file_name
```
then delete weird symbols and choose...

```bash
git add ...
git commit ...
git push
```


## Quick markdown overview

- For bullets, use a small '-'
- Create **bold text** use '**'
- Create *emphasized text* use '*'
- Code formatting with backticks
- For [links](http://www.something.com) one uses '[link name](url)'

## Good practices in **git**

- The commit message should be descriptive

