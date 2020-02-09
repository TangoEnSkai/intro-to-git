# Section 5 - Checking out Commits

---

## Checking Out Commits

Git allows us to checkout any of the commits from our log. This means we can go back and look at the code from our earlier commits without losing any of our current commits. This is especially useful when you're current codebase is broken, but you have an earlier commit with working code.

**The steps are as follows:**

1) Make sure you're inside of your project's directory, using the `cd` command.

2) Once inside of the directory, use `git log` to view your log history.

3) You can scroll down to earlier commits by hitting enter (return)

4) Once you locate the commit you want to checkout, copy the hash key from the commit.

  - The hash key is the alphanumeric string that comes after the word "`commit`" (see yellow text in image below
  - The hash from above is the string of characters that begins with `5765946b`. You don't have to copy the entire sequence of characters, the first few will do.

![Commit](commit.png)

5) Exit out of `git log` by pressing `Q`

6) Type `git checkout 5765946b` (replace the hash with one from your selected commit) and hit enter

7) Now you can look around inside of this commit and copy any code that you need. If you'd like to start working from this commit, but don't want to overwrite any of the code from the branch that you're currently on (in this case it's master) then you can type `git checkout -b <branch_name>` to create a new branch to begin working from.

8) Once you're done working from this commit, you can return to the most recent commit on the branch of your choosing by typing `git checkout <branch_name>`, in this case I typed `git checkout master` and it returned me to my most recent commit on the master branch.

Note: When you checkout an earlier commit, you are now in a "`detached HEAD`" state, this means that you are no longer on the commit that is being pointed to by the `HEAD`. The `HEAD`, in git, is a **pointer to the most recent commit of whichever branch you are currently on**.

---

## Instruction

- Use your terminal to open up the **git_section_4** directory from the last set of practice exercises.
- You should have 2 commits in this git repository, if you don't have 2 then go ahead and create some changes and commit them so you will have 2 to work with
- Check your repository commit history
- Checkout the first commit
- Make some changes to **file1.txt**
- Checkout a new branch to save these changes into
- Check the status of the repository
- Add **file1.txt** to the staging area
- Check the status of the repository again
- Commit the changes
- Switch back to the master branch
- Check your repo commit history (notice how the changes from your new branch do not exist in master)

---

## Solution

- Use your terminal to open up the **git_section_4** directory from the last set of practice exercises.
  - `cd git_section_4`
- You should have 2 commits in this git repository, if you don't have 2 then go ahead and create some changes and commit them so you will have 2 to work with
  - e.g. you can add any files or changes on the files and add commits like this:
    - `touch example.txt`
    - `git add example.txt`
    - `git commit -m "Create a file"` // the first commit
    - `echo "example message" >> example.txt` // write a message into the `txt` file
      - if you want to check out it successfully writes the message, you may use `echo example.txt` and will see `example message` on your terminal right after you run the command.
    - `git add -p example.txt` // add the changes
    - `git commit -m "Write a message"`
    - Thus, you get 2 commits
- Check your repository commit history
  - `git log`
- Checkout the first commit
  - `git checkout <SHA-1_hash_key_here>`
- Make some changes to **file1.txt**
  - `echo "hello world" >> file1.txt`
- Checkout a new branch to save these changes into
  - `git checkout -b feature2`
- Check the status of the repository
  - `git status`
- Add **file1.txt** to the staging area
  - `git add file1.txt`
- Check the status of the repository again
  - `git status`
- Commit the changes
  - `git commit -m "Update file1.txt"`
- Switch back to the master branch
  - `git checkout master`
- Check your repo commit history (notice how the changes from your new branch do not exist in master)
  - `git log`

---
