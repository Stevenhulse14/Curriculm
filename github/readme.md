# GitHub

GitHub is a powerful tool for collaboration. Developers worldwide use GitHub to back up their code, work with other developers asynchronously, and share their code with the world.

In this lesson, you'll learn about the GitHub platform. You'll connect the repositories you've created on your computer to other repositories hosted by GitHub, allowing you to back up and share your code. Finally, you'll learn the process for creating a pull request, one of the main ways developers collaborate on GitHub.

## Learning Objectives

By the end of this lesson, you should be able to:

- Differentiate between git and GitHub.
- Identify critical visual aspects of the GitHub repository page.
- Connect your local git repository with a remote GitHub repository.
- Push from your local git repository to your remote repository.
- Fork and clone a repository.
- Create a pull request using a forked repository.

---

## Git and GitHub

The `git` program is different than GitHub, the online service. One of the easiest ways to differentiate the two is to think of _where_ each one "lives."

- The `git` program "lives" on your computer. You can use the `git` program without being connected to the internet.

- GitHub is an online service. The majority of GitHub-specific features can only be done on the website.

> **Note:** There _are_ some ways to perform `git` actions on the web and access GitHub features from your computer. However, in general, this distinction holds.

On its own, git is a powerful tool for managing versions of your programs. GitHub allows that version control to go global. You can work with other developers worldwide by sharing your code on GitHub. GitHub also has a few specific features that can help manage projects, even if you're working independently.

## GitHub repositories

Repositories on GitHub are essentially well-designed file systems with extra features. Like the repositories you've created with the `git` program, they include files, folders, and commits.

![Image of the 8.0 Technical Curriculum's repository](./assets/repository.png)

The above image highlights several essential parts of any repository's page.

1. At the top of the page is the name of the account that owns the repository (e.g., `joinpursuit`) and the name of the repository (e.g., `8-0-technical-curriculum`).

2. The green "Code" button lets you get information about connecting this repository to your local machine.

3. The light blue bar at the top shows the latest commit. It should show you who made the commit, the commit message, and other details about it.

To the right, you can see how many commits are a part of the repository's history. You can also click the link (i.e., "51 commits") to see the entire commit history.

4. The files and folders associated with the repository are listed here. You can view these files similarly to how you would with a program like VSCode.

5. If there is a `readme.md` file in the current folder, it will be shown below. `readme.md` is a special file that GitHub looks for to display.

## Connecting local to remote

While it's possible to work on GitHub alone, it is more typical that a GitHub repository is connected to a repository on someone's local machine.

This way, GitHub can serve as a "backup" for your code. Connecting your local repository to a GitHub repository will allow your code to live in two places. However, as is the case whenever you have duplicate files, you want the different versions of these files to stay in sync.

### Local vs. remote

You'll often hear the terms "local" and "remote" when learning about GitHub.

The word "local" typically refers to your machine. For example, your "local repository" is a repository you've initialized with `git init`.

The word "remote" typically refers to the version of your repository hosted on GitHub. This is the public version of your repository. Remote repositories are useful for several reasons, but one of the most important is that it makes your code easier to share.

Can you imagine working with a team of ten developers and having to send `.zip` files back and forth to each other? This would be inefficient and error-prone.

### Getting ready on your local machine

Before creating a remote repository on GitHub, you'll need a local repository with at least a single commit. That means you'll need to:

- Create a new directory with at least one file.

- Initialize that directory as a git repository with `git init`.

- Stage and commit files with `git add` and `git commit`.

You can always check if your directory is a git repository with a single commit by running `git log`.

### Creating a new repository

You can create a new repository from the [GitHub.com](https://github.com) homepage. Click the green New button to get the process started.

![New repository button on GitHub](./assets/new-repository.png)

Alternatively, you can click the "+" button in the top-right corner of any GitHub page. You will then be brought to a page where you can name your repository.

![New repository page on GitHub](./assets/new-repo-settings.png)

You should give your repository a name that is meaningful as opposed to the nonsense names GitHub typically suggests, like "curly-rotary-phone." It's also typical to give your repository the same name as the folder that contains your repository on your local machine.

At the bottom of the screen, it gives you the option to initialize your repository with some files. You will have already initialized your repository on your local machine, so you _do not need to check these boxes._

After clicking the "Create repository" button, you will be brought to a new page with several code blocks.

![Repository setup page.](./assets/repository-setup.png)

Because you should have already created a repository, you'll follow the instructions under the heading "...or push an existing repository from the command line."

## Push your code

Three commands are run to connect your local repository to your remote repository. Typically, you can copy and paste these commands directly into your terminal. However, it's essential to generally understand what each command is doing.

**`git remote add origin <url>`**

When you run this command inside your local git repository, this command connects your local repository with your remote repository.

As you can see by reading the command, a new "remote" is added to the URL. The name "origin" is just that -- a name for the remote. This name _could_ be whatever you want, but you can leave it as origin.

**`git branch -M main`**

This command sets the name of the main "branch" to " main`. You will learn more about branches later on. Know that your commit history will live in the `main`branch. Your local repository also has a`main` branch -- these two branches will be connected.

**`git push -u origin main`**

The `git push` command moves all of the commits from your local repository to your remote repository. This is the command that gets the two synchronized.

The `-u` flag sets the "upstream" default for this branch always to be the remote with a name of "origin" and the branch with the name of "main."

Because of the `-u` flag, moving forward, you can write `git push` from your local `main` branch, and git will know that you want to push to the `main` branch of the remote repository by the name of "origin".

## Asynchronous collaboration

GitHub is designed to work particularly well for sharing code and collaborating with other developers. To facilitate this, GitHub has a few valuable features that you will both use throughout the class and when working on group projects.

### Forking

Forking a repository means duplicating it to your own GitHub _account._ The "forked" repository maintains a connection to the original repository.

Anyone can fork a public repository, which makes it an excellent way for developers to work together on open-source projects without having to manage permissions for a repository.

![Image of the Fork button.](./assets/forking.png)

To Fork a repository, you can click the Fork button at the top of any repository you have access to. After a brief moment, you'll be brought to a new page, your version of the forked repository.

![Image of the forked repository.](./assets/forked.png)

You should see your account name as the owner of the repository, which will have the same name. You should also notice that your repository is forked from the original repository.

Now you have a forked version of the code, which means you can update and change it as you like.

### Cloning

Cloning is the process of taking a remote repository from GitHub and creating a synchronized version of it on your computer.

Before cloning, you should do the following on your local machine:

1. Navigate to a directory that _is not_ a git repository.

1. Navigate to a directory that is the _parent_ directory where you want this repository to live.

1. Make sure that there is not already a folder inside the directory with the same name as the repository.

Once you've confirmed the above, you will click on the green "Code" button and copy the URL there.

![Image of clicking the Clone and copy button.](./assets/clone.png)

You will run the following command on the command line, replacing `<url>` with the URL you just copied.

```bash
git clone <url>
```

This will start downloading all of the files associated with your forked repository. Those files will go into a new folder with the same name as the repository.

You now have a local version of your remote repository. Your local repository:

- Already has its remote set to be your forked repository.

- Has the same history as the remote repository.

- Is yours, which means you can add your commits!

### Making changes

You can now work on your forked repository in the same way you would work on any local repository. Make changes, stage those changes, and make new commits. You can also push your changes from your local repository to the forked repository in the same way.

## Pull requests

Once you've added at least one new commit, you can create a pull request. Pull requests are a way to suggest changes to a repository without forcefully changing that repository. In an actual development workflow, someone would be tasked with reviewing that pull request and determining whether or not your code should be accepted.

At Pursuit, you will begin by using pull requests to submit your work. Your instructors can then add feedback to your pull requests as if it were a code review.

### Creating a pull request

To create a pull request, click on the "Contribute" dropdown and then click the green "Open pull request" button.

![Image of the Create Pull Request button.](./assets/create-pull-request-button.png)

### Anatomy of a pull request

The page you will be brought to has several important parts.

![Image of the Pull Request view.](./assets/pull-request-view.png)

The image above shows the following:

1. After clicking the "Open pull request" button on _your_ forked repository, you'll find you are now on the original repository. This is because you are making a pull request that will be compared to the original repository.

2. This allows you to choose what you're going to compare. You can typically leave this alone for now.

3. All of the commits you are sharing will be listed here.

4. Whatever changes you've made are listed here. In red are the lines you deleted, while in green are the lines you've added.

5. You'll click this green button to create the pull request.

6. You can switch between a "Unified" or "Split" view when comparing changes.

### Completing your pull request

After you click the "Create pull request" button, you'll see an area where you can add more details about your pull request.

![Image of the creating a new pull request.](./assets/create-pull-request.png)

As a developer, this is where you might describe what changes you're suggesting. If you're using a pull request to submit an assignment for Pursuit, you can press the "Create pull request" button.

You can find your pull request by returning to the original repository and clicking the Pull Requests tab. There you will see all of the pull requests for this repository.

![Image of the pull requests page.](./assets/pull-requests-page.png)

You can click on the link to your specific pull request to get back to the page that shows you the details of your pull request.

![Image of the specific pull request page with URL highlighted.](./assets/pull-request-show.png)

The URL on this page is a direct URL to your pull request. Keep this in mind, as you will need to submit a link to your pull request URL on some assignments.
