# Manipulating Your Repository

## Initializing Your Repository

- To initialize an empty repository, use this:

```bash
mkdir /path/to/your/repo #Optional
cd /path/to/your/repo
git init
git add LICENSE #Optional
git commit
```

- If you'd like to volunteer to maintain a free software project, or simply to mirror a remote git repository, you can access it by using like this:

```bash
git clone https://github.com/xforcevesa/HelloWorld
```

## Committing Changes To Repository

- Now you've got a bone fide repository on your local machine. Let's add README file to it.

```bash
echo "Hello World!" > README
git add README
```

- Files in working directory has two status: tracked and untracked.

- The tracked status means that the file is in the latest snapshot and also in the staging area, while the untracked status is on the opposite.

- Running ```git status``` you can see the status of files.

- Running ```git add README``` makes README file status changed into tracked.

- OK, let's commit changes!

```bash
git commit
```

## Ignoring files

- Using ```ls -ahl ```, we can find a file named ".gitignore".

- It may contain this:

```bash
*.[oa]
*~
```

- They are regular expressions to specify the files needing ignoring.

- The first line ```*.[oa]``` means the files whose names are terminated by ".a" or ".o" is overlooked by git and thus their status always remains untracked. The reason why we should ignore them may be that they're often produced when we build a project and thus shouldn't be part of the repository.

- The second line ```*~``` means the files whose names end with a tlide '~' escape git. Also, it may be because the files often work as temporary buffer of some code editors, such as vim, emacs, etc, and thus shouldn't be included into a repository.

- Regular expressions will be introduced in the future.

## Viewing Commit History

- We use ```git log``` to view the commit history. The out put is like this:
 
```bash
commit	e9c14b59ea2ec19afe22d60b07583b7e08c74290
Author: Jakub Kicinski <kuba@kernel.org>
Date:    Mon Mar 14 15:28:19 2022 -0700

  Growing the network maintainers team from 2 to 3.
```

> I quote the log in Linux kernel git repository. Actually Linux kernel has millions of commits and its number increases every day.

- The log provide the detailed information of every commit, including maintainer's nickname, email, date and hash code.

- To show the difference Before and after each commit, we use:

```bash
git log --patch
git log -p
git log -p -2 #Display the first two commits
```

- To calculate how many lines and places are changed after each commit, we use ```git log --stat```

- To format the output we use "--pretty=<format>" option.

- There are too many options, most of which is seldom used. You can look up the document upon using them.

- See also: ```man git-log```

## Other Operations
```bash
#Viewing Differences
git diff

#Removing Files From Staging Area
git rm README

#Moving Or Renaming Files In Staging Area
git mv FILE_A FILE_B
```
