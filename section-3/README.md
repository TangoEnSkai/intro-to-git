# Section 3 - Practice Exercises

Topics are:

* Adding multiple files of a certain type
* Adding all files in directory (including hidden)
* Removing files
* Ignoring files

---

## Instructions: 

* Create a new folder for this project, run all commands from this folder (name it `git_section_3`)
* Change directories into `git_section_3`
* Initialize a Git repository to begin tracking your project
* Create 3 new files using the `touch` command (name them `file1.txt`, `file2.html`, and `file3.js`)
* Create 1 new folder named `random_files`
* Move the text file (.txt) and the javascript file (`.js`) into the `random_files` directory
* Check the status of your repository (you will only see the `random_files` directory listed, not the files inside it)
* Add all newly created/untracked files and folders to the staging area
* Check the status of your repository
* Remove `file3.js` from the staging area
* Create 3 new files in the `random_files` directory (name them `file4.css`, `file5.css`, and `file6.js`)
* Check the status of your repository
* Add all files with the file type of `.css` to the staging area (hint: you need to be inside of the `random_files` directory)
* Check the status of your repository
* Add all files with the file type of `.js` to the staging area
* Check the status of your repository
* Create a new directory named `secret_stuff` (hint: make sure you `cd` back into `git_section_3` first)
* Create two files inside of `secret_stuff` named `file1.yml` and `file2.js`
* Create a `.gitignore` file so we can ignore the `secret_stuff` directory and all of its contents (hint: `.gitignore` should be inside of `git_section_3`)
* Add the `secret_stuff` folder to the `.gitignore` file 
* Check the status of your repository
* Add the `.gitignore` file to the staging area
* If your staging area looks like the image below then you have completed this exercise successfully. You may now commit your changes:

```bash
On branch master

Initial commit 

Changes to be commited:
  (use "git rm --cached <file>..." to unstage)

    new file:  .gitignore
    new file:  file2.html
    new file:  random_files/file1.txt
    new file:  random_files/file3.js
    new file:  random_files/file4.css
    new file:  random_files/file5.css
    new file:  random_files/file6.js
```

---

## Solution:

* Create a new folder for this project, run all commands in this exercise from this folder

```bash
mkdir git_section_3 
```

* Change directories into `git_section_3`

```bash
cd git_section_3 
```

* Initialize a Git repository to begin tracking your project

```bash
git init 
```

* Create 3 new files using the touch command (name them `file1.txt`, `file2.html`, and `file3.js`)

```bash
touch file1.txt file2.html file3.js
```

* Create 1 new folder named `random_files`

```bash
mkdir random_files 
```

* Move the text file (`.txt`) and the javascript file (`.js`) into the `random_files` directory

```bash
mv file1.txt random_files && mv file3.js random_files 
```

* Check the status of your repository (you will only see the `random_files` directory listed, not the files inside it)

```bash
git status 
```

* Add all newly created/untracked files and folders to the staging area with

```bash
git add .
```

OR 

```bash
git add -A
```

* Check your git status again

```bash
git status
```

* Remove `file3.js` from the staging area

```bash
git rm --cached random_files/file3.js 
```

* Create 3 new files in the `random_files` directory (name them `file4.css`, `file5.css`, and `file6.js`)

```bash
cd random_files ; touch file4.css file5.css file6.js ; cd .. 
```

* Check your git status

```bash
git status
```

* Add all files with the file type of `.css` to the staging area (hint: you need to be inside of the `random_files` directory if you aren't already)

```bash
cd random_files ; git add *.css ; cd .. 
```

* Check your git status

```bash
git status
```

* Add all files with the file type of `.js` to the staging area

```bash
cd random_files && git add *.js && cd .. 
```

* Check your git status

```bash
git status
```

* Create a new directory named `secret_stuff`

```bash
mkdir secret_stuff 
```

* Create two files inside of `secret_stuff` named `file1.yml` and `file2.js`

```bash
cd secret_stuff && touch file1.yml && touch file2.js && cd .. 
```

* Create a `.gitignore` file so we can ignore the `secret_stuff` directory and all of its contents (hint: `.gitignore` should be inside of `git_section_3`)

```bash
touch .gitignore 
```

* Add the `secret_stuff` folder to the `.gitignore` file (you can use the following command or do this in your text editor)

```bash
echo "secret_stuff" >> .gitignore 
```

* Check your git status

```bash
git status
```

* Add the `.gitignore` file to the staging area

```bash
git add .gitignore 
```

* If your staging area looks like the image below then you have completed this exercise successfully. You may now commit your changes

expected result:

```bash
On branch master

Initial commit 

Changes to be commited:
  (use "git rm --cached <file>..." to unstage)

    new file:  .gitignore
    new file:  file2.html
    new file:  random_files/file1.txt
    new file:  random_files/file3.js
    new file:  random_files/file4.css
    new file:  random_files/file5.css
    new file:  random_files/file6.js
```

commit the result:

```bash
git commit -m "Complete section 3 exercise"
```


