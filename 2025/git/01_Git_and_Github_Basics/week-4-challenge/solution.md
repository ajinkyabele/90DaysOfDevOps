Week 4 Challenge - Git and GitHub Commands Documentation

Task 1: Fork and Clone the Repository

Fork the Repository:

Visit the repository and fork it to your own GitHub account.

Clone Your Fork Locally:

git clone <your-fork-url>
cd 2025/git/01_Git_and_Github_Basics

Task 2: Initialize a Local Repository and Create a File

Set Up Your Challenge Directory:

mkdir week-4-challenge
cd week-4-challenge

Initialize a Git Repository:

git init

Create a File:

echo "Your Name - Brief Introduction" > info.txt

Stage and Commit Your File:

git add info.txt
git commit -m "Initial commit: Add info.txt with introductory content"

Task 3: Configure Remote URL with PAT and Push/Pull

Configure Remote URL with Your PAT:

git remote add origin https://<your-username>:<your-PAT>@github.com/<your-username>/90DaysOfDevOps.git
git remote set-url origin https://<your-username>:<your-PAT>@github.com/<your-username>/90DaysOfDevOps.git

Push Your Commit to Remote:

git push -u origin main

(Optional) Pull Remote Changes:

git pull origin main

Task 4: Explore Your Commit History

View the Git Log:

git log

Task 5: Advanced Branching and Switching

Create a New Branch:

git branch feature-update

Switch to the New Branch:

git switch feature-update
# OR
 git checkout feature-update

Modify the File and Commit Changes:

echo "Additional details" >> info.txt
git add info.txt
git commit -m "Feature update: Enhance info.txt with additional details"
git push origin feature-update

Merge to Main Branch via Pull Request on GitHub

(Advanced) Optional Extra Challenge

Create Another Branch and Simulate a Merge Conflict:

git branch experimental
git switch experimental
echo "Conflicting Change" >> info.txt
git add info.txt
git commit -m "Experimental change: Introduce conflicting update"
git switch feature-update
git merge experimental

Resolve the Conflict Manually and Commit Resolution:

git add info.txt
git commit -m "Resolve merge conflict between feature-update and experimental"

Importance of Branching Strategies in Collaborative Development

Branching strategies play a crucial role in managing source code efficiently in collaborative environments. Below are key reasons why they are important:

1. Isolating Features and Bug Fixes

Each new feature or bug fix can be developed in an isolated branch without affecting the main codebase.

Developers can work on multiple tasks simultaneously without interfering with one another.

2. Facilitating Parallel Development

Multiple teams or contributors can work on different features concurrently.

Enables efficient coordination between frontend, backend, and DevOps teams.

3. Reducing Merge Conflicts

Keeping feature branches separate minimizes conflicts when merging changes into the main branch.

Developers can frequently rebase or merge main into their branches to keep changes up-to-date.

4. Enabling Effective Code Reviews

Code reviews can be conducted on separate branches before merging.

Ensures high code quality and adherence to best practices.

By following a well-defined branching strategy, teams can maintain a clean and manageable codebase while ensuring smooth collaboration across multiple developers.
