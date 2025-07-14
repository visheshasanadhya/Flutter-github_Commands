Here's your full, organized, and **systematic Git + Flutter Web Deployment + GitHub Pages** command reference in a clean markdown format:

---

```markdown
# 🚀 Git & Flutter Web Deployment Commands

---

## 🔧 GitHub Setup Commands

### 1. Initialize a new Git repository
```bash
git init
```

### 2. Stage all files for commit
```bash
git add .
```

### 3. Commit the initial version
```bash
git commit -m "first commit"
```

### 4. Rename current branch to main
```bash
git branch -M main
```

### 5. Add GitHub remote repository
```bash
git remote add origin https://github.com/visheshasanadhya/Shiv-Poster-Generator.git
```

### 6. Push code to GitHub main branch
```bash
git push -u origin main
```

---

## 🔁 Basic Git Workflow

### Switch to existing branch
```bash
git checkout main
```

### Create and switch to a new branch
```bash
git checkout -b new_branch
```

### View all local branches
```bash
git branch
```

### Pull latest changes from remote main
```bash
git pull origin main
```

### Clone an existing GitHub repository
```bash
git clone https://github.com/visheshasanadhya/newsApp.git
```

---

## 📘 Git History & Cleanup

### Check status of files
```bash
git status
```

### View detailed commit history
```bash
git log
```

### View one-line commit history
```bash
git log --oneline
```

### Discard uncommitted changes to a file
```bash
git checkout -- filename
```

### Remove tracked file from Git but keep locally
```bash
git rm --cached filename
```

### Delete Git history and start fresh
```bash
rm -rf .git
git init
```

### Reset all changes to last commit
```bash
git reset --hard
```

---

## 🌐 Flutter Web Build Commands

### Build web in release mode
```bash
flutter build web --release
```

### Build web without icon tree shaking
```bash
flutter build web --release --no-tree-shake-icons
```

### Build web with custom base href (for GitHub Pages)
```bash
flutter build web --release --base-href="/your_repo_name/"
```

---

## 📁 Deploy Flutter Web to `/docs` Folder (Recommended for GitHub Pages)

### Create docs and copy web files
```bash
mkdir -p docs
cp -r build/web/* docs/
```

### Commit and push
```bash
git add .
git commit -m "Deploy Flutter Web to docs folder"
git push origin main
```

---

## 🚀 Deploy to `gh-pages` Branch (Alternative Method)

### Navigate to web build folder
```bash
cd build/web
```

### Init Git and add remote
```bash
git init
git remote add origin https://github.com/visheshasanadhya/newsApp.git
```

### Switch to `gh-pages` branch
```bash
git checkout -b gh-pages
```

### Stage and commit all files
```bash
git add .
git commit -m "Deploy Flutter Web to GitHub Pages"
```

### Force push to `gh-pages` branch
```bash
git push -f origin gh-pages
```

---

## ✅ Enable GitHub Pages

### If using `docs` folder:
1. Go to your GitHub repo.
2. Navigate to **Settings > Pages**.
3. Under **Source**, choose `main` branch and `/docs` folder.
4. Click **Save**.

### If using `gh-pages` branch:
1. Go to your GitHub repo.
2. Navigate to **Settings > Pages**.
3. Under **Source**, choose `gh-pages` branch and root (`/`) folder.
4. Click **Save**.

---

## 🛠️ Flutter Useful Commands

### Run app
```bash
flutter run
```

### Run app in Chrome
```bash
flutter run -d chrome
```

### Show connected devices
```bash
flutter devices
```

### Clean the project
```bash
flutter clean
```

### Get dependencies
```bash
flutter pub get
```

### Upgrade all packages
```bash
flutter pub upgrade
```

### Check for outdated packages
```bash
flutter pub outdated
```

### Analyze project for issues
```bash
flutter analyze
```

### Check environment setup
```bash
flutter doctor
```

---

## 🔥 Hot Reload / Restart (After `flutter run`)

- Hot Reload: Press `r`
- Hot Restart: Press `R`

---

## 💡 Common Terminal Shortcuts

### Go one directory back
```bash
cd ..
```

### Clear terminal screen
```bash
clear
```

### Open current folder in VS Code
```bash
code .
```

---
