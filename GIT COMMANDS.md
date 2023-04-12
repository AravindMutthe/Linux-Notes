# 1. GIT COMMANDS:

* Git was designed and developed by Linus Torvalds for Linux kernel development.
* Git provides support for non-linear, distributed development, allowing multiple contributors to work on a project simultaneously. 
* Git is the most popular distributed version control and source code management system.

# 2. GitHub:

1. FORK:
2. BRANCH: is a parallel version of a repository. 
		It is contained within the repository, but does not affect the primary or master branch allowing you to work freely without disrupting the "live" version.
3. FETCH:
4. CLONE:  A clone is a copy of a repository or the action of copying a repository
5. COMMIT:
6. REPOSITORY:
7. INDEX:
8. MASTER:
9. MERGING:
10. PULL:
11. PUSH:
12. ORGIN:
13. CHECKOUT: to create a new branch,change your current working branch to a different branch,

# 3. Git vs GitHub:

1. git== local(pc).
*  github== remote(cloud)

2. git: it is local(installed on ur pc) inbuilt in linux.
* github: its remote(cloud) microsoft

3. git: focusd on version control and code sharing(DVCS)
* github: focused on centralized code hosting(CVCS)

4. git:creates a local repositoty to track changes in locally rather then server
* github:its stored in centralized server its accesible by everybody

5. git: it can work without github
* github:alternatives are gitlab,bitbucket

6. git:its a tool to manage versions of source code and repositories provides functions like VCS, source code management.
* github: its a space to uplaod git repository it manages git repositories on cloud provides same functions like git with some add features

# 4. Terminology:

1. **repo:** is a collection of files and folders and the history of their changes.
	1. turn local dir into vcs
	2. clone from git

```sh
	$ git add *.c
	$ git add LICENSE
	$ git commit -m 'Initial project version'
```

2. **Commit:** Changes are tracked through commits, which are like snapshots of a file at various points in the file’s history.

3. **Master:** The main branch is normally named master and is usually reserved for clean, working code.

4. **Branch:** are used for editing files without disturbing the working portions of a project


# 5. git local repository commands:

```sh
$ git config --list: # To verify username and mail
$ git config --global core.editor editor-name: #Set your default text editor
$ git init: #creates a new .git subdirectory in the current directory.
$ git add: #command tells Git to add a file to the repository and track that file’s changes:

$ git add #Add a file to a repository.
$ git rm #Remove a file from a repository.
$ git mv #Move or rename a tracked file, directory, or symlink. 	
$ git branch #List all the local and remote branches.
			-r	#List the remote branches.
			-a	#Show both local and remote branches.
			-m	#Rename an old branch.
			-d	#Delete a branch.
			-r -d	#Delete a remote branch.
$ git commit # Commit all staged objects. Optionally, you can append a msg with the -m flag.
$ git pull # Dwnld all changes from the remote repo and merge them in a specified repo file.
$ git push # Publish the changes to the remote repo.

```

# 6. github remote repository commands:

* GitHub, GitLab, and Bitbucket all provide ways to store Git repositories remotely and facilitate collaboration.

```sh
$  git clone: #To copy every file from a remote repository to your local system.
$ git status: #To check the status of the files within the current branch of your repository.
			command will tell you if any tracked files have been modified.

$ git remote: #will display the short names of your remote repositories. If your repository was cloned, you will see a repository called origin. The default name origin comes from the cloned repository.

$ git remote add [remote-name] [url] #Add a new remote repository.
$ git fetch [repository [refspec]] #Gather all the data from a remote project that you do not have yet.
$ git pull #Obtain and merge a remote branch into your current branch.
$ git push [remote-name] [branch-name] #Move your data from your branch to your server.
```