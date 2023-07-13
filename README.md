# The-gym-git-solution

## Bundle 1
# Exercise 1
Lenovo@DESKTOP-6LCGN4B MINGW64 ~ (main)
$ cd The-gym-git-solution/

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (main)
$ git init
Reinitialized existing Git repository in C:/Users/Lenovo/The-gym-git-solution/.git/

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (main)
$ git branch -m main

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (main)
$ git branch -m master

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (master)
$ git branch -m main

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (main)
$ touch bundle-1

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (main)
$ mv bundle-1 bundle-01

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (main)
$ vi bundle-01

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (main)
$ git add .
warning: LF will be replaced by CRLF in bundle-01.
The file will have its original line endings in your working directory

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (main)
$ git commit -m 'add bundle'
[main d1bbf23] add bundle
 1 file changed, 1 insertion(+)
 create mode 100644 bundle-01
 
Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (main)
$ git push
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 287 bytes | 41.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/ell-sie/The-gym-git-solution.git
   973d9b1..d1bbf23  main -> main

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (main)
$ git checkout -b dev
Switched to a new branch 'dev'

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (dev)
$ git checkout -b test
Switched to a new branch 'test'

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (test)
$ git checkout dev
Switched to branch 'dev'

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (dev)
$ ls
README.md  bundle-01

##Exercise 2
Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (dev)
$ touch home.html

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (dev)
$ vi home.html

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (dev)
$ git add .
warning: LF will be replaced by CRLF in home.html.
The file will have its original line endings in your working directory

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (dev)
$ git stash save "home"
Saved working directory and index state On dev: home

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (dev)
$ vi team.html

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (dev)
$ git add .
warning: LF will be replaced by CRLF in team.html.
The file will have its original line endings in your working directory

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (dev)
$ git stash save "team"
Saved working directory and index state On dev: team

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (dev)
$ vi about.html

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (dev)
$ git add .
warning: LF will be replaced by CRLF in about.html.
The file will have its original line endings in your working directory

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (dev)
$ git stash save "about"
Saved working directory and index state On dev: about

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (dev)
$ ls
README.md  bundle-01

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (dev)
$ git stach list
git: 'stach' is not a git command. See 'git --help'.

The most similar command is
        stash

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (dev)
$ git stash list
stash@{0}: On dev: about
stash@{1}: On dev: team
stash@{2}: On dev: home

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (dev)
$ git stash pop stash@{0}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{0} (6fd303f4581c18a237fb40c53b548817db5dc91e)

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (dev)
$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped stash@{1} (b94012b802afa30ef346d049c2f5acc7d7b51920)

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (dev)
$ git add .

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (dev)
$ git commit -m ' added home and about pages'
[dev 9da64fe]  added home and about pages
 2 files changed, 22 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (dev)
$ git push
fatal: The current branch dev has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin dev


Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (dev)
$ git push --set-upstream origin dev
Enumerating objects: 10, done.
Counting objects: 100% (10/10), done.
Delta compression using up to 8 threads
Compressing objects: 100% (7/7), done.
Writing objects: 100% (10/10), 1.38 KiB | 353.00 KiB/s, done.
Total 10 (delta 1), reused 3 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
remote:
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/ell-sie/The-gym-git-solution/pull/new/dev
remote:
To https://github.com/ell-sie/The-gym-git-solution.git
 * [new branch]      dev -> dev
branch 'dev' set up to track 'origin/dev'.

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (dev)
$ git stash pop stash@{2}
fatal: log for 'stash' only has 1 entries

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (dev)
$ git stash list
stash@{0}: On dev: team

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (dev)
$ git stash pop stash@{0}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html
# Bundle 2
## Exercise 1
Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (dev)
$ git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (ft/bundle-2)
$ vi services.html

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (ft/bundle-2)
$ git add .
warning: LF will be replaced by CRLF in services.html.
The file will have its original line endings in your working directory

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (ft/bundle-2)
$ git commit -m 'added service page'
[ft/bundle-2 8e86127] added service page
 1 file changed, 20 insertions(+)
 create mode 100644 services.html

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (ft/bundle-2)
$ git push
fatal: The current branch ft/bundle-2 has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/bundle-2

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (ft/bundle-2)
$  git push --set-upstream origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 592 bytes | 592.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/ell-sie/The-gym-git-solution/pull/new/ft/bundle-2
remote:
To https://github.com/ell-sie/The-gym-git-solution.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
branch 'ft/bundle-2' set up to track 'origin/ft/bundle-2'.


Dropped stash@{0} (63b9ec372000d842611d29560466a283d70c205b)

## Exercise 2

$ git reset --hard HEAD
HEAD is now at 9da64fe  added home and about pages

