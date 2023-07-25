# The-gym-git-solution

## Bundle 1
# Exercise 1
```
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
```
# Bundle 2
## Exercise 1
```
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
```

## Exercise 2

```
Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/services-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ ls
Bundle-1  Readme.md

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ ls
Bundle-1  Readme.md

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ git pull
remote: Enumerating objects: 4, done.
remote: Counting objects: 100% (4/4), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 2 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (2/2), 754 bytes | 75.00 KiB/s, done.
From https://github.com/ell-sie/Gym-Git-Exercise-Solutions
   6783228..f1f0d91  main       -> origin/main
Updating 6783228..f1f0d91
Fast-forward
 services.html | 16 ++++++++++++++++
 1 file changed, 16 insertions(+)
 create mode 100644 services.html

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ ls
Bundle-1  Readme.md  services.html

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ vi services.html

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ ls
Bundle-1  Readme.md  services.html

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ git checkout ft/
ft/bundle-2            ft/services-redesign

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ git checkout ft/service-redesign
error: pathspec 'ft/service-redesign' did not match any file(s) known to git

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ git checkout ft/service-redesign
error: pathspec 'ft/service-redesign' did not match any file(s) known to git

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ git checkout ft
error: pathspec 'ft' did not match any file(s) known to git

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ git checkout -b ft/services-redesign
fatal: a branch named 'ft/services-redesign' already exists

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ ls
Bundle-1  Readme.md  services.html

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ git checkout ft/services-redesign
Switched to branch 'ft/services-redesign'

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/services-redesign)
$ ls
Bundle-1  Readme.md

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/services-redesign)
$ git pull
There is no tracking information for the current branch.
Please specify which branch you want to merge with.
See git-pull(1) for details.

    git pull <remote> <branch>

If you wish to set tracking information for this branch you can do so with:

    git branch --set-upstream-to=origin/<branch> ft/services-redesign


Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/services-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ git push
Everything up-to-date

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ git add .

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ git commit -m 'pulled services'
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ git checkout ft/services-redesign
Switched to branch 'ft/services-redesign'

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/services-redesign)
$ ls
Bundle-1  Readme.md

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/services-redesign)
$ git add .

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/services-redesign)
$ git commit -m 'b and r'
On branch ft/services-redesign
nothing to commit, working tree clean

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/services-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ git branch -d ft/services-redesign
Deleted branch ft/services-redesign (was 6783228).

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ git checkout -b ft/services-redesign
Switched to a new branch 'ft/services-redesign'

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/services-redesign)
$ ls
Bundle-1  Readme.md  services.html

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/services-redesign)
$ vi services.html

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/services-redesign)
$ git add .

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/services-redesign)
$ git commit -m 'added changes to services'
[ft/services-redesign 4fb0b17] added changes to services
 1 file changed, 3 insertions(+), 5 deletions(-)

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/services-redesign)
$ git push orgin ft/services-redesign
fatal: 'orgin' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/services-redesign)
$ git push
fatal: The current branch ft/services-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/services-redesign


Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/services-redesign)
$ ^C

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/services-redesign)
$  git push --set-upstream origin ft/services-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 329 bytes | 329.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/services-redesign' on GitHub by visiting:
remote:      https://github.com/ell-sie/Gym-Git-Exercise-Solutions/pull/new/ft/services-redesign
remote:
To https://github.com/ell-sie/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/services-redesign -> ft/services-redesign
branch 'ft/services-redesign' set up to track 'origin/ft/services-redesign'.

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/services-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ vi services.html

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ git add .

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ git commit -m 'Add conflicting changes to services.html'
[main d98ebbd] Add conflicting changes to services.html
 1 file changed, 3 insertions(+), 5 deletions(-)

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 358 bytes | 358.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/ell-sie/Gym-Git-Exercise-Solutions.git
   f1f0d91..d98ebbd  main -> main

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (main)
$ git checkout ft/services-redesign
Switched to branch 'ft/services-redesign'
Your branch is up to date with 'origin/ft/services-redesign'.

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/services-redesign)
$ git diff main
diff --git a/services.html b/services.html
index 20a8fa0..474ce62 100644
--- a/services.html
+++ b/services.html
@@ -8,7 +8,7 @@
 </head>
 <body>
     <h1>
-      second change is the service page
-    <h1>
+       sercvices page
+    </h1>
 </body>
 </html>

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/services-redesign)
$ git merge main
Auto-merging services.html
CONFLICT (content): Merge conflict in services.html
Automatic merge failed; fix conflicts and then commit the result.

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/services-redesign|MERGING)
$ git commit -m 'merge main branch into ft/services-redesign'
error: Committing is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.
U       services.html

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/services-redesign|MERGING)
$ git add .

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/services-redesign|MERGING)
$ git commit -m 'merge main branch into ft/services-redesign'
[ft/services-redesign e7c9d6d] merge main branch into ft/services-redesign

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/git-exercises (ft/services-redesign)
$ git push
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 391 bytes | 130.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/ell-sie/Gym-Git-Exercise-Solutions.git
   4fb0b17..e7c9d6d  ft/services-redesign -> ft/services-redesign
```
# Bundle 3
## Exercise 1

```

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (ft/service-redesign)
$ git checkout -b ft/team-page
Switched to a new branch 'ft/team-page'

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (ft/team-page)
$ vi team.html

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (ft/team-page)
$ git add .
warning: LF will be replaced by CRLF in team.html.
The file will have its original line endings in your working directory

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (ft/team-page)
$ git commit -m 'team'
[ft/team-page b3021b3] team
 1 file changed, 32 insertions(+)
 create mode 100644 team.html

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (ft/team-page)
$ git push
fatal: The current branch ft/team-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/team-page


Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (ft/team-page)
$ git push --set-upstream origin ft/team-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 568 bytes | 568.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/ell-sie/The-gym-git-solution/pull/new/ft/team-page
remote:
To https://github.com/ell-sie/The-gym-git-solution.git
 * [new branch]      ft/team-page -> ft/team-page
branch 'ft/team-page' set up to track 'origin/ft/team-page'.

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (ft/team-page)
$ git checkout main
Switched to branch 'main'
Your branch is behind 'origin/main' by 3 commits, and can be fast-forwarded.
  (use "git pull" to update your local branch)

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (main)
$ git pull
Updating 419644b..8e0e480
Fast-forward
 services.html | 2 +-
 1 file changed, 1 insertion(+), 1 deletion(-)

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (main)
$ git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (ft/contact-page)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (ft/team-page)
$ git log
commit b3021b383d693355ee710bb50a768004af67695f (HEAD -> ft/team-page, origin/ft/team-page)
Author: ll-sie <e.ndiramiye@alustudent.com>
Date:   Tue Jul 25 12:13:00 2023 +0200

    team

commit 8ca0f809eeafbd3081436d54f1a56ae1b29fb466 (origin/ft/service-redesign, ft/service-redesign)
Merge: 8297f51 f284299
Author: ll-sie <e.ndiramiye@alustudent.com>
Date:   Tue Jul 25 12:09:24 2023 +0200

    changes

commit 8297f51fa28c9077ce2ac22fdec761aa625438bd
Merge: 383b0c5 419644b
Author: ll-sie <e.ndiramiye@alustudent.com>
Date:   Tue Jul 25 11:29:49 2023 +0200

    resolved

commit f284299ee9078daca24e7eeb964822093ab821e7

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (ft/team-page)
$ ^C

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (ft/team-page)
$ git checkout ft/contact-page
Switched to branch 'ft/contact-page'

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (ft/contact-page)
$ git cherry-pick b3021b383d693355ee710bb50a768004af67695f
[ft/contact-page 9a9dd1c] team
 Date: Tue Jul 25 12:13:00 2023 +0200
 1 file changed, 32 insertions(+)
 create mode 100644 team.html

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (ft/contact-page)
$ git add .

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (ft/contact-page)
$ git commit -m 'contact'
On branch ft/contact-page
nothing to commit, working tree clean

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (ft/contact-page)
$ git push --set-upstream origin ft/contact-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 573 bytes | 573.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/ell-sie/The-gym-git-solution/pull/new/ft/contact-page
remote:
To https://github.com/ell-sie/The-gym-git-solution.git
 * [new branch]      ft/contact-page -> ft/contact-page
branch 'ft/contact-page' set up to track 'origin/ft/contact-page'.

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (ft/contact-page)
$ git checkout -b ft/faq-page
Switched to a new branch 'ft/faq-page'

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (ft/faq-page)
$ vi faq.html

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (ft/faq-page)
$ git add .
warning: LF will be replaced by CRLF in faq.html.
The file will have its original line endings in your working directory

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (ft/faq-page)
$ git commit -m 'faq'
[ft/faq-page 4545155] faq
 1 file changed, 12 insertions(+)
 create mode 100644 faq.html

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (ft/faq-page)
$ git push --set-upstream origin ft/faq-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 470 bytes | 470.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/ell-sie/The-gym-git-solution/pull/new/ft/faq-page
remote:
To https://github.com/ell-sie/The-gym-git-solution.git
 * [new branch]      ft/faq-page -> ft/faq-page
branch 'ft/faq-page' set up to track 'origin/ft/faq-page'.

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (ft/faq-page)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (ft/team-page)
$ git revert ^C

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (ft/team-page)
$ git revert b3021b383d693355ee710bb50a768004af67695f
[ft/team-page 3b757f8] Revert "team"
 1 file changed, 32 deletions(-)
 delete mode 100644 team.html

Lenovo@DESKTOP-6LCGN4B MINGW64 ~/The-gym-git-solution (ft/team-page)
$ git push
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 241 bytes | 241.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/ell-sie/The-gym-git-solution.git
   b3021b3..3b757f8  ft/team-page -> ft/team-page
```
