# Git

## Learning Objectives

By the end of this lesson, you should be able to:

- Understand what _Git_ is and why it is vital to the development process.
- Create a git repository.
- Learn some basic git commands

---

## Guiding Questions

- Git is a version control system. What does this mean?

- Create a new directory and navigate inside of it on the command line.

```bash
mkdir getting-started-with-git
cd getting-started-with-git
```

Inside this folder, initialize a new repository.

```bash
git init
```

Then, from the command line, look at the files and folders inside this directory. Has anything changed on the command line? Are there any files or folders in the directory?

- What is a git repository?

- What does `main` refer to in your git repository?

- Run the following command to open up the folder with the Finder program.

```bash
open .
```

Now, press the keyboard shortcut to display all hidden files: `Command` + `Shift` + `.`.

Are there any new files and folders you couldn't see before?

- How can you tell a file or folder will be hidden?

- Drag the `.git` folder to the trash and return to the command line.

Has anything changed on the command line? (You may need to press the Return key first.)

- Any directory with a `.git` folder is a git repository. This includes all files and folders that live underneath that directory.

It is a bad idea to create a git repository inside of another git repository. Why do you think this is?

- If you accidentally create a git repository inside of another git repository, what can you do to fix it?

- Create a new file in the directory and then open the entire directory up in VSCode.

```bash
touch readme.md
code .
```

Then, re-initialize the git repository from the command line with `git init`.

After re-initializing the repository, what looks different in VSCode?

> **Note:** If nothing looks different, try closing VSCode and reopening it.

- You can view helpful information about the current state of a repository with the `git status` command.

Try running this command in your repository. What files are "untracked?"

- Try running the following command in your repository.

```bash
git add readme.md
```

Then, check the status of your repository. What has changed?

- What is the difference between a file being "unstaged" (or "untracked") and "staged"? Reference the readings and other sources to help determine your answer.

- What does the `git add` command do?

- After running `git status`, you should see the following.

```bash
On branch main

No commits yet

Changes to be committed:
(use "git rm --cached <file>..." to unstage)
new file: readme.md
```

Based on the instructions, how can you unstage the file you just added? Once you've figured it out, go ahead and do so. Then, run `git status` again.

- In VSCode, add the following to your `readme.md` file. Make sure to save the file afterward.

```md
My name is:
```

Then, restage your `readme.md` file.

After staging your file, update the `readme.md` file by including your name after the semicolon. Make sure to save the file afterward.

Finally, run `git status` once again. What do you see? Why?

- After running `git status`, you should see the following.

```bash
On branch main

No commits yet

Changes to be committed:
(use "git rm --cached <file>..." to unstage)
new file: readme.md

Changes not staged for commit:
(use "git add <file>..." to update what will be committed)
(use "git restore <file>..." to discard changes in working directory)
modified: readme.md
```

Try running `git restore <file>` on `readme.md`, then look at the file contents in VSCode.

What has changed? Why?

- Re-add your name to the file. Make sure to save the file afterward.

Then, run the following command in your repository:

```bash
git diff
```

What do you see? What does `git diff` do?

> **Note:** If it looks like you're brought to a different screen in your terminal, don't panic! You can hit the `Q` key to exit this view.

- Run `git add` again, adding the `readme.md` again.

Before, you were adding the entire file as a change. What are you adding this time?

- Try running `git status` again. What do you see? Why?

- Try running `git diff` again. What do you see? Why?

- It's time to make your first commit! What is a commit?

- To make a commit you'll use the following command. The `-m` is a flag for the `git commit` command and represents the message that will be associated with this commit.

Run the command below exactly.

```bash
git commit -m "Initial commit"
```

After running the command, what changed on your command line? What changed in VSCode?

- Try running `git status` again. What do you see? Why?

- Try running the following command.

```bash
git commit -m "Another commit"
```

What do you see? Why?

- Now that you've created a commit, your git repository has a history. To view the history, you can run `git log`.

Try running the command. What do you see?

- You should see a long string of letters and numbers after the word "commit" when running the `git log` command, like the example below.

```
b23949d4b62b4ae1153729859e50ed4f06e6615d
```

What is this called, and what does it represent?

- Make a change to your `readme.md` file. Then add your changes. Finally, type the following command and press enter.

```bash
git commit
```

Oh no! You're in some strange program! To exit the program, type `:q`.

What program were you in?

- This time, run `git commit` but use the `-m` flag with an appropriate message. Then, check your repository's history with `git log`.

What commit message did you write? What do you think makes a good commit message?
