# Assignment: Inception

In this assignment, you'll practice:

* Creating folders/directories on the command line
* Creating files on the command line
* Deleting, renaming, and moving directories or files
* Finding what files your current directory contains, with `ls`
* Finding what your current working directory is, with `pwd`
* Forking a remote repository on Github
* Cloning a remote repository onto your computer locally
* Adding and committing files and directories within a repo
* Pushing changes to Github

---

# Exercise 1: Inception

This assignment will give you some practice with Git, Github, and the command line, by recreating the story of [Inception](http://www.imdb.com/title/tt1375666/?ref_=fn_al_tt_1).

You should also get a sense of what Git is, how it differs from GitHub, and how to use each of these tools.

* Locally, we'll use Git commands to work with files:
   * `git add`
   * `git commit`
   * `git status`

* Remotely, we'll use Github to fork a remote repository, clone the repo locally, and pushing changes from your local repo back to the remote repo

Instead of using dreams and characters, we will be using directories and files. Each directory will represent a level and each file will represent a character.

As you go down each level (directory), one character (file) will be left behind and you will make a commit.

The 7 characters from the movie are:

* Ariadne
* Arthur
* Cobb
* Eames
* Robert
* Saito
* Yusuf

[Here's an infographic depicting the different dream levels and who goes where](assets/inception_infographic.jpg)

## Setting Up

1. **Fork** the assignment repo so that you have a copy of it that belongs to you, living on Github

1. Open your Terminal and navigate to the folder for all of your development work:

   ```bash
   cd $DEV
   ```

1. **Clone** your fork of the assignment repo onto your computer.

   Remember to clone _your_ fork of the repo, not the instructor's, so that you can make changes to it!

   **Protip:** Replace `YOUR_USERNAME` with your actual Github user name

   ```bash
   git clone https://git.generalassemb.ly/YOUR_USERNAME/hw-01-inception.git
   ```

1. Navigate inside the folder of the newly cloned assignment repo:

   ```bash
   cd hw-01-inception
   ```

Continue with the assignment steps below. Have fun and feel free to discuss tips & tricks on our Slack discussion channel!

## Assignment Steps

**You must commit your changes after each step, otherwise you won't be taking snapshots in time!**

1. Create text files, one for each character listed above (`arthur.txt`, `cobb.txt`, etc.)
   * As an example, `ariadne.txt` was already created for you
1. **Add** your files, and **Commit** to record this chapter of the story
1. Now, all the characters will start dreaming. Create the first directory called `level_one` and move all your characters into it
1. **Add** your changes and make another **commit**!
1. Create the next directory, `level_two`. All of the characters, except for one, will dream into the second level. So move all but one character down into `level_two`
1. Keep going for 2 more levels (`level_three` and `level_four`). Do the same thing at each level by moving all but one character down, committing each step of the way
1. The final level is `limbo`. According to the movie only Saito and Cobb go into `limbo`, but you can move whoever you like here... The point is just to get some command-line practice!
1. When you are finished, push your code to GitHub

## Solution

Special only for this assignment -- the "[solution](https://git.generalassemb.ly/PYTHR-Library/hw-01-inception-solution)" is already available for you to look at.

When you are done, your repo inside your GitHub account should look similar to the solution.

Take note of the commit history!

![Inception Commit History](assets/commit_history.png)

# Tips and Tricks

## Subdirectories

When you add your changes from within a subdirectory, you will need to use the `--all` flag instead of `git add .`:

```bash
git add --all
```

## Empty Directories

Git only tracks files and not directories. You won't be able to commit a new directory unless there's at least one file in it! See [Git FAQ: Empty directories](https://git.wiki.kernel.org/index.php/GitFaq#Can_I_add_empty_directories.3F) for more details.

## Help on Command-Line Commands

If you want more information about a command-line command you can type:

```bash
man <the name of the command>
```

To quit the help screen type `q`.

## Undoing a Commit

You might also want to go back to the previous commit. To do this type:

```bash
git reset --hard HEAD^
```

If you want to know the differences between `--hard`, `--soft`, and `--mixed`, check [this StackOverflow question](http://stackoverflow.com/questions/3528245/whats-the-difference-between-git-reset-mixed-soft-and-hard) out.

## Important Git Commands Cheatsheet

### Local Repository Workflow

* Shows status of files

   ```bash
   git status
   ```

* Stages changes to all files (including deleted files)

   ```bash
   git add --all
   ```

* Creates a new commit (a snapshot in time) with associated message

   ```bash
   git commit -m "<message>"
   ```
   
* Shows history of commits

   ```bash
   git log
   ```

### Remote Repository Workflow

* Copies a remote repo to your computer

   ```bash
   git clone <server url>
   ```

* Pulls changes on the remote repo to your local repo

   ```bash
   git pull
   ```

* Pushes local repo to remote repo

   ```bash
   git push origin master
   ```

---

# Submitting

To submit this assignment:

1. In your web browser, go to the **assignment's main repo** (not your fork)
1. Click the **Issues** tab
1. Click the **New Issue** button
1. In the Title field, fill in your name
1. In the comment field, copy and paste the URL to *your* assignment repo
1. Click **Submit new issue** and you're done!

---

# The Dream is Real

![](https://media.giphy.com/media/VEfa7bl3iKG5i/giphy.gif)

If you haven't watched Inception yet, maybe give it a shot, it's pretty good!
