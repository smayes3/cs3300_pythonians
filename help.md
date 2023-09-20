# Resources and Documentation
Comprehensive list of resources found that might be useful for this class  
  <sub>When done adding to this, just go ahead and commit directly to main branch.</sub>




## GitHub
### Basic styling/formatting for markdown (.md) files on GitHub
- [Basic writing and formatting syntax](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
  - *Very* useful for the basics (headings, styling, links, lists, etc.) 
- [Quickstart for writing on GitHub](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/quickstart-for-writing-on-github)
  - Advanced formatting features (tables, quotes, comments, saving, README, images)
- [Edit and create documentation](https://docs.pkp.sfu.ca/contributing/en/create-and-edit)
   - Not quite as useful as the others, but has a little bit of info.  
>[!NOTE]
>If you're unfamiliar with markdown formatting, please reference these so we can keep our documentation neat!

### Setup
- [Checking for existing SSH keys](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/checking-for-existing-ssh-keys)
  - Steps to check if you have an SSH key already generated for GitHub
- [Generate SSH key and add to agent](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)
  - Steps to generate an SSH key and add it to SSH agent for authentication
- [SSH keys for GitHub](https://jdblischak.github.io/2014-09-18-chicago/novice/git/05-sshkeys.html)
  - Covers what an SSH key is, how to generate one and add it to GitHub account, and how to use it
- [Working with SSH key passphrases](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/working-with-ssh-key-passphrases)
  - What passphrases are, adding/changing, auto launching ssh-agent on Git for windows
- [Add SSH key to GitHub account](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account)
  - How to add your key to your account
- [Git Bash download](https://git-scm.com/downloads)
  - Free, open-source terminal package for Bash, bash utils, and Git
- [How to use Git Bash](https://www.geeksforgeeks.org/working-on-git-bash/)
  - Guide for setting up Git Bash and using it

### Working with GitHub
- [Deb's GitHub/Python documentation](https://docs.google.com/document/d/1GXnP1p7t8o0jhHuwP_EQaP9AdZdINGBZ/edit#heading=h.gjdgxs)
- [Changing branches](https://www.freecodecamp.org/news/git-switch-branch/)
  - Create new branch, switch to existing branch, switch to a specific commit, find commit SHA, HEAD states
- [Git bible](https://git-scm.com/docs/git/2.7.6)
  - A manual of git commands. Similar to *tutorialspoint* like we used in C, but for git commands
- [Pull requests](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests)
  - Covers what they are and when to do them
- [GitHub glossary](https://docs.github.com/en/get-started/quickstart/github-glossary)
  - Common Git and GitHub terms
- [Git cheatsheet](https://training.github.com/downloads/github-git-cheat-sheet/)
  - Cheatsheet with common commands
- [Adding file to repo](https://docs.github.com/en/repositories/working-with-files/managing-files/adding-a-file-to-a-repository)
  - Upload and commit file to a repository
- [Create repo](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-new-repository)
  - Create a new repository
- [Clone a repo](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository)
  - Clone a repository to create a local copy, syncing between local and remote copy
- [Branching and merging](https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging)
  - Background info and how to do it
- [Applying changes from one branch to another](https://www.jetbrains.com/help/go/apply-changes-from-one-branch-to-another.html)
  - Gives a bunch of different ways to combine changes between branches
- [Git and GitHub for beginners](https://product.hubspot.com/blog/git-and-github-tutorial-for-beginners)
  - A tutorial for how to use Git and GitHub
- [Intro to Git and GitHub](https://www.freecodecamp.org/news/introduction-to-git-and-github/)
  - Good resource for getting familiar with git and github, with offshoots to other resources
- [Working with Git and GitHub for Python projects](https://www.pythonguis.com/tutorials/git-github-python/)
  - Walks through how to set up/work with git, *including info for python and venv*

<details>    
<summary> Steps for syncing remote and local repo: </summary>
  
*Using CLI to merge from local to remote repo (I used Git Bash, so may differ depending on your CLI)*  
- check what you have set as remote repo (https://docs.github.com/en/get-started/getting-started-with-git/managing-remote-repositories):  
  `git remote -v` 
- in the cmd line, go to wherever you store your repo and checkout the "iteration01" branch:  
  `cd <path>`  
  `git checkout iteration01`
- the file you have  locally is prob different than whats on the remote or it's not there at all. so pull the most updated "GE01_pythonians.py" file from the remote repo to your local repo:  
  `git pull origin iteration01`  
  <sub> origin references the remote repo that you looked at in step 1  
  format is: "git pull <from/remote repo> <to/local repo>" </sub>
- make sure that the file with updates was retrieved:  
  `ls -al` <sub>(file should be shown)</sub>  
  `cat <file>` <sub>(should show contents that match what you can see on GH)</sub>
- make your edits:  
  `vim <file>`
- verify that its tracking that changes were made:  
  `git status` <sub>(mine shows "......modified: <file>" in red)</sub>
- stage file for commit and verify its been staged:
  `git add <file>`  
  `git status` <sub>(now mine shows the modified file in green)</sub>
- commit changes  
  `git commit -m "<message>"`
- merge the local and remote repos.  
  <sub>format is: "git push <to/remote repo> <from/local repo>"</sub>  
  `git push origin iteration01`
- now at this point if you check the branch on GH, you'll see the changes and you're done
</details>

## Python
### Setup
- [Deb's GitHub/Python documentation](https://docs.google.com/document/d/1GXnP1p7t8o0jhHuwP_EQaP9AdZdINGBZ/edit#heading=h.gjdgxs)
- [Venv setup](https://docs.python.org/3/library/venv.html)
  - Instructions for how to set up venv
- [Venv setup 2](https://www.geeksforgeeks.org/create-virtual-environment-using-venv-python/)
  - Another version of instructions to use for venv setup

### VSCode
- [Beginner VSCode Python tutorial](https://code.visualstudio.com/docs/python/python-tutorial)
- - Basic tutorial for how to work with Python in VSCode

## GE02 Resources 
### Troubleshoot guide
- [Webpage will not update]([https://code.visualstudio.com/docs/sourcecontrol/overview](url))
- Came across an issue where my webpage did not immediately update when modified in VSCode
- 
  


