# Git branching

* Branch in Git is similar to the branch of a tree. Analogically, a tree branch is attached to the central part of the tree called the trunk. While branches can generate and fall off, the trunk remains compact and is the only part by which we can say the tree is alive and standing. Similarly, a branch in Git is a way to keep developing and coding a new feature or modification to the software and still not affecting the main part of the project. 

* We can also say that branches create another line of development in the project. The primary or default branch in Git is the master branch (similar to a trunk of the tree). As soon as the repository creates, so does the main branch `(or the default branch)`.

* Branch in Git is "lightweight". Light in terms of the data they carry and the little mess they create.

### Why do we need a Branch in Git and Why Branches Are Important?
* Git branches come to the rescue at many different places during the development of a project. As mentioned above, branches create another line of development that is entirely different or isolated from the main stable master branch.


## Different Operations On Branches
* Branches are the heart of Git. From the time of creating the repository until its deletion, everything will involve branches. So this is a concept to remember and analyze carefully. In this tutorial, we discussed the definition and importance of branches. This complete section of branches on ToolsQA will take you through some operations and concepts that will help you in efficiently using Git.

1. `Create a Branch:` This is the first step in the process, you can start on a default branch or create a new branch for the development.
2. `Merge a Branch:` An already running branch can merge with any other branch in your Git repository. Merging a branch can help when you are done with the branch and want the code to integrate into another branch code.
3. `Delete a Branch:` An already running branch can delete from your Git repository. Deleting a branch can help when the branch has done its job, i.e., it's already merged, or you no longer need it in your repository for any reason.
4. `Checkout a Branch:` An already running branch can pull or checkout to make a clone of the branch so that the user can work on any of them. Pulling a branch can help when you don't want to disturb the older branch and experiment on the new one.


## Steps to create a branching repository

```bash
git branch feature    # Create a branch `feature`
git checkout feature  # Switch the HEAD to feature
git commit            # Commit some changes
git commit            # Some more
git checkout master   # Migrate to master
git commit            # Commit changes
git branch release    # Create a `release` branch
git checkout release  # Migrate to `release` branch
git commit            # Commit changes
git merge feature     # Merge `feature` branch to the `release` branch
git checkout master   # Migrate to `master` branch
git commit            # Apply some changes
git commit            # Some more
git merge release     # Merge the `release` branch to the `master`
```

## A graphical visualization of the above commands

![git-flows](git-flow.png)


## Pull Requests (PR)

> Pull requests (PRs) are the primary method developers use to submit their changes to open source projects. When a developer opens a PR, it signals to the project maintainers that new code is ready for review. The maintainers carefully evaluate the PR, ensuring that the changes contribute value to the project without introducing any issues or breaking existing functionality.

> If the PR meets these criteria, it is merged into the main codebase, becoming part of the official project.

### Once you have everything set up and have chosen the project you want to contribute to, follow these steps to make your first PR

#### 1. Create a copy of the repository

* To start working on an open-source project, you first need to create your own copy of the repository. 

* This process involves forking the repository to create a copy under your GitHub account and then cloning it to your local machine, giving you a working version of the project that you can modify and experiment with.

* Forking
When you’re on the main page for the repository, a Fork button will be displayed on your upper right-hand side of the page

* You can copy the URL by using the green "Code" button from your repository page that you forked from the original repository page. Once you click the button, you’ll be able to copy the URL by clicking the clipboard button next to the URL.
* Open your terminal. navigate to the folder you want to clone the project to and clone it using this Git command
```bash
git clone https://github.com/harsh-panchal-inventyv/Git-Training-Aman-Sir.git
cd Git-Training-Aman-Sir
```

#### 2. Create new branch and start modifications

* Before you begin working on the code and making changes, it's important to create a new branch. 
* This branch will serve as a separate workspace for your code modifications, keeping them isolated from the main codebase.
* To create a new branch and switch to it, open your terminal and enter the following command:
```bash
git checkout -b develop
```

* You can now make changes and save them.

#### 3. Save local changes and commit

* After working on your changes, you'll need to save them locally by doing:

```
git add -A
git commit -m "Changes has been made" # commit your changes
```

#### 4. specify a new remote upstream repository for us to sync with the fork. This will be the original repository that we forked from.

```bash
git remote add origin https://github.com/harsh-panchal-inventyv/Git-Training-Aman-Sir/
```

We can verify that our remote pointer to the upstream repository was properly added by using the git remote -v command again from the repository directory.

#### 5. Switch to the local main branch of our repository:

```bash
git checkout main
git merge upstream/main # merge changes
```

Your fork’s main branch is now in sync with the upstream repository, and any local changes you made were not lost.

#### 6. Create a PR
At this point, you are ready to make a pull request to the original repository.
You should navigate to your forked repository, and press the New pull request button on your left-hand side of the page.

<!-- ## Rulesets

> A ruleset is a named list of rules that applies to a repository.

* Rulesets help you to control how people can interact with branches and tags in a repository.

![image](https://github.com/user-attachments/assets/55d10ac9-a0a5-41cc-aafe-138d62db863e)
-->
