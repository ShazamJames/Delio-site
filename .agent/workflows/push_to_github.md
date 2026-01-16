---
description: How to push the project to GitHub
---

Follow these steps to push your local project to a new GitHub repository.

### 1. Initialize Git (if not done)
Run these commands in your project terminal:

```powershell
git init
git add .
git commit -m "Initial commit"
```

### 2. Create a Repository on GitHub
1.  Go to [github.com/new](https://github.com/new).
2.  Enter a repository name (e.g., `delio-site`).
3.  **Do not** initialize with README, .gitignore, or License (since you already have code locally).
4.  Click **Create repository**.

### 3. Connect and Push
Copy the commands provided by GitHub under "…or push an existing repository from the command line" and run them. They will look like this:

```powershell
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/delio-site.git
git push -u origin main
```

**Note**: Replace `YOUR_USERNAME` with your actual GitHub username.
