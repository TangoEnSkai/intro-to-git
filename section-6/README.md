# Section 6 - GitHub

---

Topics are:

* Sing up to [GitHub](https://github.com/)
  * [Join](https://github.com/join)
* Adding a remote and pushing to origin
  * `git remote add origin <url>`
    * `git remote add origin git@github.com:/intro-to-git.git`
  * `git push -u origin master`
* To check the `remote` is successfully defined or not:
  * `git remote -v`
* if you want to push / upload code to GitHub repository
  * `git push -u origin master`
    * this means your local branch `master` is now on a `remote` branch, the `remote` is also called `origin`. You can also check this directly going to the GitHub webpage: [TangoEnSkai/intro-to-git](https://github.com/TangoEnSkai/intro-to-git)

* `git push`
  * `-u` or `--set-upstream`
    * in addition to `git pull` this setting also affects default behaviour of `git push`. If you get in the habit of using `-u` to capture the remote branch you intend to track, I recommend setting your `push.default` config value to upstream.
    * `git push -u <remote> HEAD` will push the current branch to a branch of the same name on `<remote>` (and also set up tracking so you can do `git push` after that).

---
