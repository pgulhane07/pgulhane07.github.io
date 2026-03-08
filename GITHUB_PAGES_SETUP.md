# Steps to Host Your Portfolio on GitHub Pages

## Prerequisites
- A GitHub account (create one at https://github.com if you don't have one)
- Git installed on your computer (download from https://git-scm.com/)

## Step-by-Step Instructions

### Step 1: Create a New GitHub Repository

1. Go to https://github.com and sign in
2. Click the **"+"** icon in the top right corner
3. Select **"New repository"**
4. Fill in the repository details:
   - **Repository name**: `your-username.github.io` (e.g., `piyushgulhane.github.io`)
     - ⚠️ **Important**: Use your GitHub username followed by `.github.io` for automatic GitHub Pages hosting
     - OR use any name like `portfolio` (you'll need to configure it differently)
   - **Description**: "My Personal Portfolio Website"
   - **Visibility**: Choose **Public** (required for free GitHub Pages)
   - **DO NOT** initialize with README, .gitignore, or license (we'll add files manually)
5. Click **"Create repository"**

### Step 2: Initialize Git in Your Project (if not already done)

Open your terminal/command prompt and navigate to your project folder:

```bash
cd /Users/piyushgulhane/Documents/personal-portfolio-website-template
```

Check if git is already initialized:
```bash
git status
```

If you see "not a git repository", initialize it:
```bash
git init
```

### Step 3: Add All Files to Git

```bash
# Add all files to staging
git add .

# Commit the files
git commit -m "Initial commit: Portfolio website"
```

### Step 4: Connect to GitHub and Push

1. Copy the repository URL from GitHub (it will look like: `https://github.com/your-username/your-repo-name.git`)

2. Add the remote repository:
```bash
git remote add origin https://github.com/your-username/your-repo-name.git
```

3. Push your code to GitHub:
```bash
git branch -M main
git push -u origin main
```

You'll be prompted for your GitHub username and password (or personal access token).

### Step 5: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click on **"Settings"** (top menu bar)
3. Scroll down to **"Pages"** in the left sidebar
4. Under **"Source"**, select:
   - **Branch**: `main` (or `master` if that's your default branch)
   - **Folder**: `/ (root)`
5. Click **"Save"**

### Step 6: Access Your Live Portfolio

- If you named your repo `your-username.github.io`:
  - Your site will be live at: `https://your-username.github.io`
  - It may take a few minutes to deploy (up to 10 minutes)

- If you used a different name:
  - Your site will be at: `https://your-username.github.io/repo-name`
  - Example: `https://piyushgulhane.github.io/portfolio`

### Step 7: Update Your Portfolio (Future Changes)

Whenever you make changes to your portfolio:

```bash
# Navigate to your project folder
cd /Users/piyushgulhane/Documents/personal-portfolio-website-template

# Add changed files
git add .

# Commit changes
git commit -m "Description of your changes"

# Push to GitHub
git push
```

GitHub Pages will automatically rebuild your site within a few minutes.

## Troubleshooting

### If images don't load:
- Make sure all image paths in `index.html` are relative (e.g., `img/logo.png` not `/img/logo.png`)
- Check that all image files are committed and pushed to GitHub

### If styles don't load:
- Verify CSS file paths are relative
- Check browser console for 404 errors

### If the site shows 404:
- Wait 5-10 minutes after enabling GitHub Pages
- Check repository Settings > Pages to ensure it's enabled
- Verify the branch name matches (main vs master)

## Custom Domain (Optional)

If you have a custom domain (e.g., `piyushgulhane.com`):

1. Add a file named `CNAME` (no extension) in your repository root
2. Add your domain name inside: `piyushgulhane.com`
3. Configure DNS settings with your domain provider:
   - Add a CNAME record pointing to `your-username.github.io`
4. In GitHub Settings > Pages, add your custom domain

## Need Help?

- GitHub Pages Documentation: https://docs.github.com/en/pages
- Git Documentation: https://git-scm.com/doc
