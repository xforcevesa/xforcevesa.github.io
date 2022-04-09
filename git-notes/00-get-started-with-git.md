# Get Started With git

## man gittutorial

### NAME 
gittutorial - A tutorial introduction to Git

### SYNOPSIS
git *

### START
- Let's have this git installed on GNU/Linux distribution. [Click here](https://git-scm.com/download/linux).
- Before any operations, It's a good idea to introduce yourself to git with your name and email.Use this:
```bash
git config --global user.name xforcevesa
git config --global user.email nomodeset@qq.com
```

### IMPORTING A NEW PROJECT
- It is easy. Let us do this:
```bash
cd YOUR_PROGECT
git init
```
- Take a snapshot:
```bash
git add .
```
- Formally register a git repository
```bash
git commit
```

### MAKING CHANGES
- Add files:
```bash
git add file1 file2
```
- You can see whatever is about to be committed:
```bash
git diff --cached
```
- Get the current status:
```bash
git status
```
- Commit your change:
```bash
git commit
git commit -a
```
