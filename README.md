# The-gym-git-solution
##Bundle 1
~
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
~
