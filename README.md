# Github-documentation for starters

## Why Use GitHub? 🤔

GitHub is an online platform that helps you **store**, **share**, and **work on code** with others. It's especially important for beginners because:

- ✅ **Backup Your Work**  
  Never lose your code. GitHub saves it in the cloud.

- ✅ **Track Changes**  
  See what you changed and when. Go back if you break something.

- ✅ **Collaborate Easily**  
  Work with friends or teammates without messing up each other's code.

- ✅ **Showcase Your Skills**  
  Build a portfolio. Employers and schools can see your projects.

- ✅ **Learn Industry Standards**  
  Git and GitHub are used everywhere. Knowing them is essential.

## Getting started with Github? 🚀

### 1️⃣ **Create an Account**
- Go to [github.com](https://github.com).
- Click **Sign Up**.
- Enter your email, choose a username and password.
- Follow the prompts to verify your email.

### 2️⃣ **Set Up Your Profile**
- Add a picture and bio (optional but helpful).
- It makes you look professional when sharing projects.

### 3️⃣ **Create Your First Repository**
- Click **New** or **+** in the top corner.
- ![Screenshot1](https://github.com/user-attachments/assets/5431c69e-e1c7-458a-9a32-98749a6ab79b)
- Name your repo (e.g., `hello-world`).
- ![Screenshot2](https://github.com/user-attachments/assets/a257bcbf-8b95-46f4-bf7c-4ad2af4cbd56)
- Choose **Public** (free) or **Private**.
- ![Screenshot3](https://github.com/user-attachments/assets/344e5230-1cae-4762-9982-cacb92414703)
- Add a README (recommended).

### 4️⃣ **Explore & Learn**
- Check out **GitHub Docs** for guides.
- Try basic commands: `git init`, `git add`, `git commit`, `git push`.

> 💡 *Think of a repo as a folder for your project. Once it's set up, you can save, share, and update your code easily!*

### 5️⃣ **Install Git (Optional but Recommended)**
**What is Git?**  
Git is a tool on your computer that **tracks changes** to your code.

**How is it related to GitHub?**  
GitHub is like **the online home** for your Git projects. You use Git to save and manage changes locally, then **upload (push)** them to GitHub to back up or share.

**Purpose (Simple):**  
✅ Keep history of your code.  
✅ Undo mistakes.  
✅ Share with others easily.

> 💡 *Think of Git as a save button with unlimited undos. GitHub is where you store those saves online.*

- Download from [git-scm.com](https://git-scm.com).
- It lets you use Git from your computer.
- Click Downloads,
- Select your OS (eg. Microsoft), it will open up the download page for your OS.
- Click on the latest version and the installation package will start downloading.
- Install the package after
- Summarizing: Open Link > Click Downloads > Select OS > Click on latest version and download file
- Refer links: https://www.youtube.com/watch?v=t2-l3WvWvqg&t=39s (Microsoft), https://www.youtube.com/watch?v=9GZmaxaQV0c (MacOS), https://www.youtube.com/watch?v=bc3_FL9zWWs (Linux)  for demo videos

## Git Basics: Where to Run Commands 💻

Before going any further, you need to know **where** and **how** to run Git commands on your local machine:

### 1️⃣ Open Your Terminal
- **Windows**: 
  - Press `Win + R`, type `cmd` (Command Prompt) or `powershell`
  - Or use Git Bash (installed with Git)
  
- **Mac/Linux**:
  - Open Terminal (`Command + Space` → search "Terminal")

### 2️⃣ Navigate to Your Project
First, go to your project folder:
```bash
cd path/to/your/project
```
**Example**: cd Desktop/my-project

### 3️⃣ Initialize Git (If New Project)
Only needed once per project:
```bash
git init
```

### 4️⃣ Connect to GitHub (First Time)
```bash
git remote add origin https://github.com/your-username/repo-name.git
```

### 5️⃣ Basic Workflow
1. Make changes in your code editor
2. Stage changes:
```bash
git add .
```
3. Commit changes:
```bash
git commit -m "Describe your changes"
```
4. Push to GitHub:
```bash
git push origin main
```

### 6️⃣ Undoing Changes
**Undoing Unstaged Changes**
Discard changes to a specific file:
```bash
git checkout -- filename
```
Discard all unstaged changes:
```bash
git restore .
```
**Undoing Staged Changes**
Unstage a file (keep changes):
```bash
git restore --staged filename
```
Unstage all files (keep changes):
```bash
git reset
```
**Undoing Commits**
Undo last commit (keeps changes staged):
```bash
git reset --soft HEAD~1
```
Undo last commit (keeps changes unstaged):
```bash
git reset HEAD~1
```
Undo last commit (discards changes completely):
```bash
git reset --hard HEAD~1
```
Change last commit message:
```bash
git commit --amend -m "New commit message"
```
Add forgotten files to last commit:
```bash
git add forgotten-file
git commit --amend --no-edit
```
**Reverting Pushed Commits**
Create a new commit that undoes changes:
```bash
git revert COMMIT_HASH
```
> ⚠️ Warning: Be careful with git reset --hard and git push --force as they can permanently erase work.

## GitHub Branches: Beginner's Guide 🌿

Branches let you work on different versions of your project without affecting the main code. Think of them as parallel timelines!

### Key Concepts
- **`main` branch**: Default branch (your "production" code)
- **Feature branches**: Temporary branches for new work (e.g., `feature/login-page`)
- **HEAD**: Your current working branch (like a "you are here" marker)

### Essential Commands

#### Create a Branch
```bash
git branch BRANCH_NAME          # Create branch
````

#### Create and switch to a new branch
````bash
git checkout -b my-feature-branch
````

#### Check existing branches
````bash
git branch           # local branches
git branch -r        # remote branches
git branch -a        # all branches
````
#### Make changes and commit them
````bash
git add .
git commit -m "Add my new feature"
````
#### Push your branch to GitHub
````bash
git push origin my-feature-branch
````
✅ Your branch is now on GitHub.

### Create a Pull Request (PR)
- Go to your repo on GitHub.
- Click Compare & pull request.
- Add title/description.
- Submit.
- ✅ This asks to merge your changes into main.

### Keep Your Branch Updated with main
If main has new commits, sync them into your branch: 
**Merge method:** 
```bash
git checkout main
git pull origin main
git checkout my-feature-branch
git merge main
```
**Rebase method (cleaner history):**
```bash
git checkout my-feature-branch
git fetch origin
git rebase origin/main
```
### Delete a Branch After Merging
**Delete locally:**
```bash
git branch -d my-feature-branch
```
**Delete on Github**
```bash
git push origin --delete my-feature-branch
```

### ✅ Quick Command Reference
- Task	Command
- List local branches:	*git branch*
- List remote branches:	*git branch -r*
- Create and switch branch:	*git checkout -b new-branch*
- Switch branches:	*git checkout branch-name*
- Push branch to GitHub:	*git push origin branch-name*
- Delete local branch:	*git branch -d branch-name*
- Delete remote branch:	*git push origin --delete branch-name*
- Merge into main:	*git checkout main* + *git merge branch-name*
- Rebase onto main:	*git rebase main*
