**📘 Git (local) \& GitHub (Web) Setup for Updating the learning journey of Manual to Playwright**

This comprehensive, step-by-step notebook documents every command, error, and resolution strategy we used to synchronize your local project folder with your existing repository on GitHub.



**🛠️ Step 1: Establishing Identity (The First-Time Setup)**	

Before saving work, Git must be told who you are so it can label your progress history.



**1. Set Identity Commands**

*git config --global user.name "Shr33kant"*

*git config --global user.email "shrikantsupekar333@gmail.com"*



**• When to use:** Run this once when setting up Git on a new machine, or if you get an identity error.

**• Why we use it:** To stamp a tracking label onto every commit. Using your official account email ensures GitHub links these uploads directly to your contribution chart.



**POSSIBLE ERROR**

If we try to run a git commit command on a fresh Git environment before providing an email address flag.

It gives an error- **❌ Author Identity Unknown:**

*\*\*\* Please tell me who you are.*

*Run git config --global user.email "you@example.com"*

*fatal: unable to auto-detect email address...*



If you accidentally use an incorrect or broken string (e.g., leaving off the @gmail.com), simply type the corrected command string again and press enter; **Git automatically overwrites old configurations.**



**🔍 Verification Commands**

To check what information Git currently has saved on your computer, run:

*git config user.name*

*git config user.email*



**Alternative Workflow**

If you share a machine and want these credentials to apply only to this specific roadmap project, remove the --global flag:

*git config user.email "shrikantsupekar333@gmail.com"*

----------------------------------------------------------------------------------------------------------------------------------------

**🚀 Step 2: Connecting a Local Project to an Existing GitHub Repo**

This sequence is used when you already have a README.md file sitting online on GitHub, but you have built new files and folders locally on your Desktop that you want to upload.



&#x09;**Local Desktop                             		Remote Cloud (GitHub)**

**\[Manual Testing Folder]   <====Sync====>   \[Existing README.md]**



**1: Open Git Bash Here**

**• Action:** Navigate to your Desktop folder - **Manual to Playwright Automation Roadmap**, right-click on an empty space, and select Git Bash Here.

**• Why:** This initializes the terminal inside the correct folder path automatically, preventing file directory navigation mistakes.

----------------------------------------------------------------------------------------------------------------------------------------

**2: Initialize the Directory**

*git init*



**• When to use:** Run this once in the root of any new project folder.

**• Why:** It creates a hidden .git tracking vault inside your folder, transforming it from a standard directory into an active Git repository.

------------------------------------------------------------------------------------------------------------------------------------------------

**3: Link to a Specific Repository**

*git remote add origin https://github.com/username/reponame*



• **When to use:** Run this immediately after initialization to bridge your local machine to the cloud.

**• Why:** It tells Git exactly which repository to target. It assigns your specific project URL to the shorthand nickname origin.



**❌ Possible Error : Targeted Path Ambiguity (Wrong URL Setup)**

**• The Scenario:** Attempting a command using a base profile URL like https://github.com to pull down files.

**• Why it fails:** Git sees a profile page containing multiple repositories. It cannot guess which individual project vault you intend to interact with, throwing an immediate connection error.

**• How we resolved it:** We supplied the absolute, precise repository ending layout identifier:



**Alternative Resolution:** If you accidentally set up a corrupted or broken URL name, reset the endpoint link using:

*git remote set-url origin https://github.com*

----------------------------------------------------------------------------------------------------------------------------------

**4: Synchronize Cloud Files Locally (Pulling)**

*git pull origin main*



**• When to use:** Run this before making local additions if your cloud repository contains files that are missing on your machine (like your online README.md).

**• Why:** It downloads the online files and merges them safely alongside your local folders, bringing both environments to an even starting line.

In our case we ran this command to pull the **redame.md** file present on oyr repo on GitHub.

--------------------------------------------------------------------------------------------------------

**5: Stage and Save Local Changes (Committing)**

*git add "manual Testing/"*

*git commit -m "docs: completed First 2 topics from Module 1- What is Software Testing \& Software Quality"*



**• git add:** Moves your new folders out of an untracked state into a staging area (the shipping box).

**• git commit -m "..."**: Seals the box with a timestamped message detailing your specific study progress.



**❌ Possible Error: Refspec Main Does Not Match Any**

*error: src refspec main does not match any*

*error: failed to push some refs to 'https://github.com...'*



**• Why it happens:** Your local environment defaults to naming its active track **master**, but your online cloud destination expects a track named **main**. When you ask to push to **main**, Git cannot find a matching local sequence matching that title.

* **How to resolved it:**

*git branch -M main*

*git push -u origin main*



**• git branch -M main:** Forces the local branch to name itself main to align with modern GitHub defaults.

**• git push -u origin main:** Uploads your sealed tracking history smoothly up to the internet repository cloud.



**Alternative Resolution:** If you prefer not to alter your machine's naming default to match the cloud branch, you could alternative-push your existing master branch straight into the cloud's tracking lane by mapping them directly:

*git push origin master:main*



**🔍 Local Verification Dashboard**

Keep these diagnostic check commands handy whenever you want to confirm your status before pushing to GitHub:



Command		What it Inspects			Expected Successful Output

git status			Active staging area state		nothing to commit, working tree clean

git branch			Active branch lane name		\* main (Printed in green text)

git log --oneline		Local save checkpoint history	Displays a list of your previous commit messages

git remote -v		Linked cloud paths			Lists your specific Manual-to-Playwright fetch \& push URLs

-------------------------------------------------------------------------------------------------------------------------------

**6. File naming and changing the file name**

GitHub lists files alphabetically by default. If your files are named exactly **1. What is Software Testing** and **2. Software Quality**, GitHub sees the digit 1 and the digit 2 and should sort them correctly.

But, if the number (Topics) grows past number 9, standard alphabetical sorting will break (computers read 10 right after 1, putting Topic 10 before Topic 2).

To prevent this completely, always prefix your files with a two-digit number format **(01-, 02-, 03-).**



* &#x20;**Rename the files inside Git Bash**

Our naming for files is not correct, hence its showing randomly in the directory. hance, we have to change the naming as starting with **(01-, 02-, 03-).**



*# Correct format if your original file was a text document*

**git mv "Topic 1 - What is SOFTWARE TESTING.txt" "01- What is Software Testing.md"**



*# Correct format if your original file was a markdown document*

**git mv "Topic 2 - Software Quality and Defect.md" "02- Software Quality and Defect.md"**



* **Push the clean names to GitHub**

*#Commit the name changes you just made*

**git commit -m "style: renamed files with 01 and 02 prefixes for correct ordering"**



*#Push the changes live to GitHub*

**git push origin main**



**🔍 What to expect:**

When you refresh your GitHub repository page, you will notice that the old file names are gone, and your new filenames (01- ... and 02- ...) will be perfectly sorted in chronological order.



Since you used the **git mv** command, Git has already tracked the renaming locally on your computer as well. 

So, the changes in naming will be visible on both GitHub and Local system (Computer).

There is no need for another commands.











