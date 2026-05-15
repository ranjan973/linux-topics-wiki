# GIT Introduction and commands

### What is git?

GIT is a distributed version control and Source Code management (SCM) tool which solves the problem of versioning and collaboration in the software development. It works very similar to Linux and was developed by Linus Torvalds in 2005.

- Track file version
- Document History
- Manage Branches ( A branch is seperate line of development where you can work without effecting the main and working code)
- Provide Merging solutions
- Identify conflicts while merging and help resolve them. ( Conflict happens when same line or part of the code was modified differently in 2 branches)

### Installing GIT on Linux Distros
   #### Debian/Ubuntu:
   - sudo apt-get update
   - sudo apt-get install git
   - git --version OR git -v

  #### Fedora/RHEL:
  - sudo dnf install git

Config User Name and User Email in Git so that all the commits are named

#### git config --global user.name "Anand Ranjan"

#### git config --global user.email "anand.ranjan@fisglobal.com"

### How does GIT work under the hood?

Its a persistent map which uses key value pair to store the content. The value is the content (Ex: "Apple Pie") & the key to it is the SHA1 value of it. SHA is secure hash algorithm.

[aranjan@mycentosVM cookbook]$ echo "Apple Pie" | git hash-object --stdin --> Plumbing command
23991897e13e47ed0adb91a0082c31c82fe0cbe5

The first thing to start working with GIT is to create a repository using the command "git init" from the directory which needs to be the git repo. This will create a .git folder which stores all the history,metadata and configuration that Git uses to track and manage the project.

.git is the brain of the git repository.

<img width="804" height="978" alt="image" src="https://github.com/user-attachments/assets/8c6e75ee-70b4-41ff-8ea0-75e3f51b2f0c" />


