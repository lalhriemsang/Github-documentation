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

> 🔹 **For a starter:** It’s like saving your school project in Google Drive, but better for code. It helps you stay organized and learn teamwork early.

## How to Get Started on GitHub? 🚀

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
