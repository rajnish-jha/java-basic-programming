# Steps to push newly created local repository to the remote repository using PAT authentication
> $ pwd

> /d/java-local-repo 

> $ mkdir java-program

> $ cd java-program

> $ pwd

> /d/java-local-repo/java-program

> $ echo "Array based programmings">java-array.md

> $ echo "String based programmings">java-string.md

> $ cat java-array.md
> Array based programmings

> $ cat java-string.md
> String based programmings

> $ cd d:/java-local-repo

> $ pwd

> /d/java-local-repo

> $ echo "This is readme.md file">README.md

> $ cat README.md
> This is readme.md file

> $ ls
> java-program/  README.md

> $ ls -la
```
total 17
drwxr-xr-x 1 Admin 197121  0 Dec 16 02:09 ./
drwxr-xr-x 1 Admin 197121  0 Dec 16 02:03 ../
drwxr-xr-x 1 Admin 197121  0 Dec 16 02:08 java-program/
-rw-r--r-- 1 Admin 197121 23 Dec 16 02:09 README.md
```
# Now in order to push the code to the gitHub
```
$ git config --global user.name "rajnish-jha"

$ git config --global user.email "jk.rajnish@gmail.com"

$ git init
Initialized empty Git repository in D:/java-local-repo/.git/

$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        README.md
        java-program/

nothing added to commit but untracked files present (use "git add" to track)

$ git add .
warning: LF will be replaced by CRLF in README.md.
The file will have its original line endings in your working directory
warning: LF will be replaced by CRLF in java-program/java-array.md.
The file will have its original line endings in your working directory
warning: LF will be replaced by CRLF in java-program/java-string.md.
The file will have its original line endings in your working directory

$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

        new file:   README.md
        new file:   java-program/java-array.md
        new file:   java-program/java-string.md

$ git commit -m "initial commit"
[master (root-commit) a872604] initial commit
 3 files changed, 3 insertions(+)
 create mode 100644 README.md
 create mode 100644 java-program/java-array.md
 create mode 100644 java-program/java-string.md

Admin@DESKTOP-ML63O1E MINGW64 /d/java-local-repo (master)
$ git status
On branch master
nothing to commit, working tree clean

$ git remote

$ git remote add origin https://github.com/rajnish-jha/java-basic-programming.git

$ git remote
origin

$ git remote -v
origin  https://github.com/rajnish-jha/java-basic-programming.git (fetch)
origin  https://github.com/rajnish-jha/java-basic-programming.git (push)

$ git log
commit a8726049441f2cbc3fce7305404701321721eff0 (HEAD -> master)
Author: rajnish-jha <jk.rajnish@gmail.com>
Date:   Thu Dec 16 02:11:48 2021 +0530

    initial commit

$ git push origin master
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (6/6), 426 bytes | 71.00 KiB/s, done.
Total 6 (delta 0), reused 0 (delta 0)
To https://github.com/rajnish-jha/java-basic-programming.git
 * [new branch]      master -> master

Admin@DESKTOP-ML63O1E MINGW64 /d/java-local-repo (master)
$
```
