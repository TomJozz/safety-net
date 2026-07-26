# [Safety Net ](https://hyperskill.org/projects/500)
An advanced Git branching project from JetBrains Academy / Hyperskill
> **Provided by:** JetBrains Academy

- **Difficulty:** Challenging

- **Completions:** 154 completions

- **Estimated Time:** ~5 hours

- **Rating:** 4.4

## About
Git is a version control system that helps multiple developers collaborate on a project. It tracks changes made to the project's files over time and allows you to revert to a previous snapshot if something goes wrong. Git's branching and merging capabilities help you work on new features or bug fixes, experiment safely, and integrate changes smoothly. This project offers you a chance to work and prepare your branches.

### Project Goals
This project will teach you how to:

- Use Git branches to work on different tasks separately.

- Cherry-pick, undo, or revert changes if needed.

- Create new features and release them.

### Graduate Project
This project covers the core topics of the **Introduction to Git course**, making it sufficiently challenging to be a proud addition to your portfolio.

---
## Objectives
## [Stage 1/7: Clone and switch](https://hyperskill.org/projects/500/stages/2934/implement)

- Open a terminal and clone the remote Git repository to your local machine at the project root. This will create a local copy of the remote repository. You can use either SSH or HTTPS:

- After cloning, move into the newly created repository directory to work with the project files.

- Switch to the development branch `0.2.x-dev` to work on the latest development code. Ensure you create a local copy from the remote.

- List all available branches in your local repository to confirm that the correct branches are present.


## [Stage 2/7: New feature](https://hyperskill.org/projects/500/stages/2935/implement#comment)

- Create a new branch named `feature/math` from the existing `0.2.x-dev` branch. This branch will serve as the isolated environment where you will add new functionality. Ensure that this new branch is active before proceeding to the next steps.

- In the newly created `feature/math` branch, create a file named `math_operations.py` in the `root` directory of the project.

- The file should contain a basic mathematical function that performs the addition of two integers and returns the result:

    ```python
    def addition(a, b):
        return a + b
    ```

- Stage and commit the changes with the commit message: `feat: new function addition`



## [Stage 3/7: Merge and Delete](https://hyperskill.org/projects/500/stages/2936/implement#comment)

- Switch to the `main` branch. This is the branch where the production-ready version of the project is stored.

- Merge `feature/math` into the `main.` This will integrate the new file containing the new feature into the main codebase.

- Delete the `feature/math` branch as it's no longer needed. This helps keep the repository clean and avoids clutter from unused branches.


## [Stage 4/7: Cherry-pick](https://hyperskill.org/projects/500/stages/2937/implement)

- Switch to the `0.2.x-dev` branch: this is your development branch, where new features should be integrated. Ensure that you are working from this branch before proceeding;

- Cherry-pick the last commit from the `main` branch: use the appropriate command to transfer the most recent commit from `main` to `0.2.x-dev`. This will allow the feature to be correctly integrated into the development branch.

- After cherry-picking the commit, return to the `main` branch to prepare for the reset;

- Reset the `main` branch to its original state: reset the `main` branch to the state it was in before the last merge, leaving only the initial commit (`feat: Initial`).


## [Stage 5/7: Restore](https://hyperskill.org/projects/500/stages/2938/implement)

- Switch to the `feature/case` branch: create a local copy of `feature/case` from the remote repository.

- Restore `case_operations.py` to a previous state: using the commit `6b2ec72`, restore the file `case_operations.py` to its state from that commit. This will undo changes that were made from that point.

- Commit the changes: after restoring the file, stage and commit the changes with the following commit message: `refactor: restored case operations from 6b2ec72`.

- Verify the branch: ensure that the `feature/case` branch contains the correct number of commits and that the restored file matches the content from the `6b2ec72` commit.

## [Stage 6/7: Another feature](https://hyperskill.org/projects/500/stages/2939/implement)

- Rebase the `feature/case` branch with `0.2.x-dev`: before merging, rebase the `feature/case` branch with the `0.2.x-dev` branch to ensure that it includes the latest changes from the development branch. This is necessary to avoid conflicts and ensure that the feature branch is up to date.

- Switch to the `0.2.x-dev` branch: after rebasing, switch to the `0.2.x-dev` branch. This is the development branch where the latest features are integrated.

- Merge the `feature/case` branch into `0.2.x-dev`: perform the merge operation to integrate the changes from the `feature/case` branch into the `0.2.x-dev` branch. This will bring the new feature into the development branch without creating a separate merge commit.

- Delete the `feature/case` branch: once the merge is complete, delete the `feature/case` branch. This helps keep the repository clean by removing branches that are no longer needed.

- Verify the repository state: ensure that the `0.2.x-dev` branch now contains the commits from the `feature/case` branch and that the `feature/case` branch has been successfully deleted.

## [Stage 7/7: Release](https://hyperskill.org/projects/500/stages/2940/implement)

- Create a release branch (`0.2.x`): create a new branch named `0.2.x` from the `0.2.x-dev` branch. This branch will serve as the release branch, containing the final version of the code that will be deployed to production;

- Fix the bug in the `make_upper` function: in the `case_operations.py` file, the `make_upper` function currently prints the uppercase version of the text instead of returning it. Modify the function so that it returns the uppercase text, as shown in the provided code snippet:

    ```python
    def make_upper(text):
        return text.upper()
    ```

- Commit the bug fix: after fixing the bug, commit the changes to the `0.2.x` branch with the commit message: `fix: bug-fix make_upper`.

- Verify the repository: ensure that the `0.2.x` branch contains the correct number of commits (9 commits in total, including the bug fix), and that the `make_upper` function has been correctly updated.

