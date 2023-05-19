# Programming Basics
This repository contains a collection of resources and exercises for beginners to learn programming basics. It covers fundamental concepts, code examples, and hands-on exercises to help you get started with programming.

## Getting Started
To get started with this project, follow the steps below:

## Prerequisites
Install a code editor of your choice. We recommend using Visual Studio Code for its versatility and extensive plugin ecosystem.

Install Git on your system. You can download it from the official website: https://git-scm.com/downloads
## Cloning the "Programming-basics" Repository and Specifying a Folder

1. Open a terminal or command prompt.

2. Navigate to the directory where you want to create the folder for the repository.

3. Clone the repository using the `git clone` command and specify the folder name after the repository URL:
   ~~~
   git clone https://github.com/SolidDeath/Programming-basics.git your-folder-name
   ~~~
   Replace `your-folder-name` with the desired name of the folder where you want to keep the repository files.

4. Change to the newly created directory:
   ~~~
   cd your-folder-name
   ~~~

## Keeping Your Local Repository Up to Date

1. Configure remote tracking:
   ~~~
   git remote add upstream https://github.com/SolidDeath/Programming-basics.git
   ~~~

2. Fetch updates from the upstream repository:
   ~~~
   git fetch upstream
   ~~~

3. Merge changes into your local branch (e.g., `main`):
   ~~~
   git checkout main
   git merge upstream/main
   ~~~

4. Resolve conflicts (if any).

5. Commit the merge:
   ~~~
   git commit -m "Merge upstream changes"
   ~~~

## Pushing Your Code to Your Own Repository

1. Create a new repository:
   Go to your GitHub account and create a new repository. Let's assume the new repository is named `your-new-repo`.

2. Update the remote URL:
   ~~~
   git remote set-url origin https://github.com/your-username/your-new-repo.git
   ~~~

   Replace `your-username` with your GitHub username.

3. Commit your changes:
   ~~~
   git add .
   git commit -m "Your commit message"
   git push origin main
   ~~~

   Note: If you're working on a branch other than `main`, replace `main` with the appropriate branch name.
