# How to Deploy Your Portfolio to GitHub

## Step 1: Create a Repository on GitHub
1. Log in to your [GitHub account](https://github.com).
2. Click the **+** icon in the top-right corner and select **New repository**.
3. Name your repository (e.g., `my-portfolio` or `username.github.io`).
   - **Note**: If you name it `yourusername.github.io`, it will automatically be deployed to that URL.
4. Make sure it is **Public**.
5. **Do not** initialize with README, .gitignore, or license (we already have the files).
6. Click **Create repository**.

## Step 2: Push Your Code
Once the repository is created, you will see a "Quick setup" page. Copy the URL of your repository (it looks like `https://github.com/username/repo-name.git`).

Then, run the following commands in your terminal (I can run them for you if you provide the URL):

```bash
git branch -m main
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
git push -u origin main
```

## Step 3: Enable GitHub Pages (if not using username.github.io)
1. Go to your repository **Settings**.
2. Click on **Pages** in the left sidebar.
3. Under **Build and deployment**, select **Source** as `Deploy from a branch`.
4. Select `main` branch and `/ (root)` folder.
5. Click **Save**.

Your website will be live at `https://yourusername.github.io/repo-name/` (or just `https://yourusername.github.io` if you used that name).
