# Understanding Git Branching – A Beginner’s Guide

## Overview
This guide explains how **Git branching** works and how to use it effectively when collaborating on projects.  
It’s aimed at beginners who want to understand **how to create, switch, merge, and manage branches** in Git and GitHub.

> **Author:** Miracle Chisom Ikechukwu  
> **GitHub:** [Chisney25](https://github.com/Chisney25)  
> **Last Updated:** November 2025  

---

## Objectives
After reading this guide, you will:
- Understand the concept of branching in Git
- Learn how to create, switch, and delete branches
- Know how to merge branches and handle conflicts
- Follow best practices for using branches in team environments

---

## 1. What Is a Git Branch?
A **branch** in Git is an independent line of development.  
Think of it as a separate workspace where you can make changes **without affecting the main codebase**.

> Example:  
> The `main` branch is your stable production code.  
> A new branch (e.g., `feature/login-page`) is where you build or test new features.

Visual representation:
main
│
├── feature/login-page
│
└── fix/ui-bug

---

## 2. Checking Existing Branches
To see all branches in your repository:
```bash
git branch

You’ll see:
* main
  feature/login-page
The asterisk * shows your current branch.
```

---

## 3. Creating a New Branch
To create a branch:
git branch feature/login-page

Then switch to it:
git checkout feature/login-page

Or do both at once:
git checkout -b feature/login-page

Now you’re working inside the new branch. Changes made here won’t affect the main branch until you merge them.

---

## 4. Making Changes in a Branch
Make edits to your project (e.g., update a file).
Then commit your changes:
git add .
git commit -m "Added login page layout"

To view branch history:
git log --oneline --graph --decorate --all

---

## 5. Merging a Branch into Main
When your feature is ready:
1. Switch back to the main branch
git checkout main

2. Merge the feature branch
git merge feature/login-page

3. Push changes to GitHub
git push origin main

---

## 6. Handling Merge Conflicts
Conflicts occur when two branches change the same lines of code.
Git will mark the conflict inside the file like this:
<<<<<<< HEAD
print("Welcome to the app!")
======= *
print("Hello, user!")
>>>>>>> feature/login-page

To resolve:
1. Manually edit the file to keep the correct version.
2. Save the file.
3. Commit the fix:
git add .
git commit -m "Resolved merge conflict in app.py"

---

## 7. Deleting Old Branches
Once merged, delete the branch to keep your repo clean:
git branch -d feature/login-page

If you already pushed it to GitHub:
git push origin --delete feature/login-page

---

## 8. Best Practices for Branching
1) Use clear, descriptive names:
.feature/signup-form
.bugfix/payment-error
.docs/update-readme
2) Keep branches small and focused.
3) Regularly pull updates from main to avoid conflicts.
4) Always write meaningful commit messages.

---

## 9. Visualizing Branches
You can use:
git log --graph --oneline (command-line visualization)
Or GUI tools like GitKraken, SourceTree, or VS Code Git Graph for better visualization.

---

## 10. Example Workflow Summary
### Create a branch for new work
git checkout -b feature/new-feature

### Make changes and commit
git add .
git commit -m "Add new feature"

### Merge to main after testing
git checkout main
git merge feature/new-feature

### Push updates to GitHub
git push origin main

---

## 11. Contributing
Contributions are welcome!
If you’d like to improve this guide:
1) Fork the repository.
2) Edit the documentation in Markdown.
3) Submit a pull request with your suggestions.

---

## 12. License
This project is licensed under the MIT License — you are free to use and share it with attribution.

---

## Summary
By completing this guide, you now know how to:
1. Create and manage Git branches
2. Merge changes safely
3. Resolve conflicts
4. Follow best practices for collaborative development

---






