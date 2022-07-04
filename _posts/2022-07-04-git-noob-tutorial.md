# Git(linux)

## Git is a popular version control system.

## Before git \[[or here](https://www.howtogeek.com/howto/41418/how-to-be-more-productive-in-ubuntu-using-keyboard-shortcuts/)]

0. learn to write notes, not everyone is linus.

### Terminal  

1. open terminal - Ctrl Alt T

2. open another terminal tab in the existing terminal windows - Shift Ctrl T

3. close the current terminal( tab) - Shift Ctrl W

4. switch among the terminal tabs: 

   a. Alt [NUMBER], switch to the [NUMBER]$^{th}$ terminal tab

   b. Ctrl \<Page down>/Ctrl \<Page up>
   
   c. Shift Ctrl \<Page Up>/Shift Ctrl \<Page Down>, Move to the tab to the left/right
### CLI

1. **Shift Ctrl C/V**, you are already a master now

2. **Ctrl+A** or Home: Go to the start of a command line.

3. **Ctrl+E** or End: Go to the end of a command line.

4. Alt+B or **Ctrl+Left Arrow**: Move the cursor backward one word.

5. Alt+F or **Ctrl+Right Arrow**: Move the cursor forward one word.

6. **Ctrl+XX**: Hop between the current position of the cursor and the start of the line. Hold down Ctrl and Press X twice, quickly.

7. **Ctrl+U**: Delete all characters *before* the cursor. Ctrl+E, Ctrl+U will delete the entire line.

8. **Alt+D**: Delete all characters *after* the cursor to the end of the line.

9. **Ctrl+L**: Clear the terminal window. Same as typing `clear`.

10. **Ctrl+S**: Stop scrolling output. Freezes the output from a program, but allows the program to continue to run in the background.

11. **Ctrl+Q**: Restart scrolling output if it has been stopped with Ctrl+S.

### Interface
1. Alt+F2: launch applications, run commands, and run scripts
2. Super+D: Minimizes all windows and shows the desktop.
3. **Super+Left Arrow**: Snap the current application so that it takes up the left side of the screen.
4. **Super+Right Arrow**: Snap the current application so that it takes up the right side of the screen.
5. **Super+Up Arrow**: Maximize the current application.
6. **Super+Down Arrow**: Restore down (that is, reduce but don’t minimize) the current application.
7. **Super+M** or **Super+V**: Display the notifications are and Calendar.
8. **Super+L**: Locks the screen so that you need to log back in. Makes it safe to leave your computer unattended.

### Application 

1. **Ctrl+Q** or **Ctrl+W** or **Alt+F4**: Close application.

## Start

1. create a project dir, run `git init`
2. use `git status` to catch the sketch of what is going on
3. `git add` or `git add -all` add the files into the repo 
4. `git commit` submit all the added git files

## Branch

### In Git, a ==branch== is a new/separate version of the main repository.

![why branch](./whyBranch.png)

1. `git branch [BRANCH NAME]` to create branch
2. `git branch` list all the branches
3. `git checkout [BRANCH NAME]` to move to another branch
4. merge the master branch with the bug-fix branch, just switch to master branch and run `git merge [BUG-FIX BRANCH]`. Which makes master and bug-fix refer to the same commit, you can delete the bug-fix branch now `git branch -d [BUG-FIX BRANCH]` and ready for your promotion.
5. OK, if the other branch did not settle that bug, and we want to merge it with the master, how to deal with the conflict? Just merge like in **4.** , git will commit the new added files and alter you about the unmerged part. Edit the unmerged part, which contains the hints, modify it according to the files. Commit again, and delete the branch.

## Rush Github

1. `git remote add origin https://github.com/github_name/repo_name.git)`, creates a connection between your local repo and the remote repo on Github.
2. `git branch -M main`, changes your main branch's name to "main". The default branch might be created as "master", but "main" is the standard name for this repo now.
3. `git push -u origin main`, pushes your repo from your local device to GitHub.

