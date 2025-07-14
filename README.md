# ** Setup Commands**

---

## 🔧 GitHub Repository Setup

```bash
git init                                   # Initialize a new Git repository
git add .                                  # Stage all files for commit
git commit -m "first commit"               # Commit with message
git branch -M main                         # Rename current branch to main
git remote add origin <your_repo_url>      # Add GitHub remote repository
git push -u origin main                    # Push code to GitHub main branch
```

---

## 🔁 **Basic Git Workflow**

```bash
git checkout main                          # Switch to existing branch
git checkout -b new_branch                 # Create and switch to a new branch
git branch                                 # View all local branches
git pull origin main                       # Pull latest changes from remote main
git clone <repo_url>                       # Clone an existing GitHub repository
```

---

## 📘 **Git History & Cleanup**

```bash
git status                                 # Check status of files
git log                                    # View detailed commit history
git log --oneline                          # View one-line commit history
git checkout -- filename                   # Discard uncommitted changes to a file
git rm --cached filename                   # Untrack file but keep it locally
rm -rf .git && git init                    # Delete Git history and start fresh
git reset --hard                           # Reset all changes to last commit
```

---

## 🌐 **Flutter Web Build Commands**

```bash
flutter build web --release                             # Build Flutter web in release mode
flutter build web --release --no-tree-shake-icons       # Keep unused icons
flutter build web --release --base-href="/repo_name/"   # Add base href for GitHub Pages
```

---

## 📁 **Deploy to `/docs` Folder (Recommended for GitHub Pages)**

```bash
flutter build web --release --base-href="/Shiv-Poster-Generator/"
mkdir -p docs                         # Create docs folder
cp -r build/web/* docs/               # Copy web build to docs
git add .
git commit -m "Deploy Flutter Web to docs folder"
git push origin main
```

---

## 🚀 **Deploy to `gh-pages` Branch (Alternative)**

```bash
cd build/web                          # Navigate to build/web
git init
git remote add origin <repo_url>
git checkout -b gh-pages
git add .
git commit -m "Deploy to GitHub Pages"
git push -f origin gh-pages           # Force push to gh-pages
```

---

## 🔧 **Enable GitHub Pages**

### ✅ If using `/docs` folder:

* Go to **GitHub > Repo > Settings > Pages**
* Source: `main` branch, `/docs` folder
* Click **Save**

### ✅ If using `gh-pages` branch:

* Go to **GitHub > Repo > Settings > Pages**
* Source: `gh-pages` branch, root (`/`) folder
* Click **Save**

---

## 🛠️ **Flutter Useful Commands**

```bash
flutter run                              # Run app on default device
flutter run -d chrome                    # Run on Chrome
flutter devices                          # List connected devices
flutter clean                            # Clean build artifacts
flutter pub get                          # Get dependencies
flutter pub upgrade                      # Upgrade all packages
flutter pub outdated                     # Check for outdated packages
flutter analyze                          # Analyze project for issues
flutter doctor                           # Show environment setup issues
```

---

## 🔥 **Hot Reload / Hot Restart**

* Press `r` → **Hot Reload**
* Press `R` → **Hot Restart**
  *(After running `flutter run` in terminal)*

---

## 💡 **Terminal Shortcuts**

```bash
cd ..                                    # Move one directory up
clear                                    # Clear terminal screen
code .                                   # Open current folder in VS Code
```

---
Sure Vishesha! Here's a **complete list of Flutter commands** you've either used before or will likely use often — categorized for better clarity. These commands help in device setup, project management, dependency management, build, and debugging.

---

## 🔁 **DEVICE & EMULATOR RELATED**

```bash
flutter devices                        # List all connected devices
flutter emulators                     # List available emulators
flutter emulators --launch <id>       # Launch an emulator
flutter run                           # Run app on default device
flutter run -d <device_id>            # Run on specific device
```

---

## 🔧 **PROJECT SETUP & CREATION**

```bash
flutter create <project_name>         # Create a new Flutter project
flutter create .                      # Initialize Flutter in current folder
```

---

## 📦 **DEPENDENCY & PACKAGE MANAGEMENT**

```bash
flutter pub get                       # Get dependencies from pubspec.yaml
flutter pub upgrade                   # Upgrade all dependencies
flutter pub outdated                  # Check which packages are outdated
flutter pub add <package_name>        # Add new package
flutter pub remove <package_name>     # Remove package
```

---

## 🔍 **CLEAN & REBUILD**

```bash
flutter clean                         # Remove build/, .dart_tool/, etc.
flutter pub get                       # Re-fetch dependencies after cleaning
flutter run                           # Rebuild and run the app
```

---

## 🐛 **DEBUGGING & PERFORMANCE**

```bash
flutter doctor                        # Diagnose Flutter setup issues
flutter analyze                       # Analyze Dart code for errors/warnings
flutter run --debug                   # Run app in debug mode
flutter run --release                 # Run app in release mode
flutter run --profile                 # Run app in profile mode
```

---

## 🌐 **WEB SUPPORT**

```bash
flutter build web                     # Build the app for web deployment
flutter run -d chrome                 # Run the app in Chrome
```

---

## 🧪 **TESTING**

```bash
flutter test                          # Run all unit/widget tests
```

---

## 🏗️ **BUILD FOR DEPLOYMENT**

```bash
flutter build apk                     # Build release APK for Android
flutter build apk --debug             # Build debug APK
flutter build appbundle               # Build .aab for Play Store
flutter build ios                     # Build for iOS (Mac only)
flutter build web                     # Build for web
```

---

## 💡 **DART COMMANDS**

```bash
dart pub add <package>                # Add Dart package
dart pub get                          # Get Dart packages
dart fix --apply                      # Apply recommended Dart fixes
```

---

### ✅ Optional Git Commands (You used earlier)

```bash
git init                              # Initialize git repo
git status                            # See changes
git add .                             # Add all files
git commit -m "message"               # Save changes with message
git remote add origin <url>           # Link to remote repo
git push -u origin main               # Push to GitHub (main branch)
```

---
