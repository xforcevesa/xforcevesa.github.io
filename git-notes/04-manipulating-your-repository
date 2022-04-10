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

- If you want to volunteer to mirror a remote git repository, e.g. github repository, you can access it by using this:

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

## Other Operations
```bash
#Viewing Differences
git diff

#Removing Files From Staging Area
git rm README

#Moving Or Renaming Files In Staging Area
git mv FILE_A FILE_B
```
