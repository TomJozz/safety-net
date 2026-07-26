# [Safety Net ](https://hyperskill.org/projects/500)

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
## [Stage 1/7: Clone and switch](https://hyperskill.org/projects/500/stages/2934/implement)
### Objectives
- Open a terminal and clone the remote Git repository to your local machine at the project root. This will create a local copy of the remote repository. You can use either SSH or HTTPS:

- After cloning, move into the newly created repository directory to work with the project files.

- Switch to the development branch `0.2.x-dev` to work on the latest development code. Ensure you create a local copy from the remote.

- List all available branches in your local repository to confirm that the correct branches are present.


## [Safety Net. Stage 2/7: New feature](https://hyperskill.org/projects/500/stages/2935/implement#comment)

## Objectives
- Create a new branch named `feature/math` from the existing `0.2.x-dev` branch. This branch will serve as the isolated environment where you will add new functionality. Ensure that this new branch is active before proceeding to the next steps.

- In the newly created `feature/math` branch, create a file named `math_operations.py` in the `root` directory of the project.

- The file should contain a basic mathematical function that performs the addition of two integers and returns the result:

    ```python
    def addition(a, b):
        return a + b
    ```

- Stage and commit the changes with the commit message: `feat: new function addition`