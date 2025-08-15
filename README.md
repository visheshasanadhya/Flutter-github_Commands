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
git branch                                 # View all local branches # Check if main exists locally
git pull origin main                       # Pull latest changes from remote main
git clone <repo_url>                       # Clone an existing GitHub repository
```
---

## **Git is asking for your GitHub login   **


```bash
git remote set-url origin <Github repo link>       # <Github repo link - https://github.com/visheshasanadhya/  .git>
git push -u origin main

```

**Generate and use a Personal Access Token:**

1. Go to GitHub → Settings → Developer settings → Personal access tokens → Tokens (classic).
2. Click Generate new token,
3. select:repo (full control for private/public repos)
4. Set an expiry date.
5. Copy the token (you won’t see it again).
6. In the terminal, when it asks for a password, paste this token instead.

It will ask for:

```bash
Username for 'https://github.com': your_github_username
Password for 'https://github.com': <paste your token here>

```
## methord 2 -

1. The URL in your Git repo is still using HTTPS without the token

If you just run git push and enter username/token, it should work — but if it keeps failing, you can embed the token directly into your remote URL to skip prompts:

```bash
git remote set-url origin https://<USERNAME>:<TOKEN>@github.com/visheshasanadhya/BMDU-E_Commerce-_app.git
Example (replace <USERNAME> and <TOKEN>):
```
```bash
git remote set-url origin https://visheshasanadhya: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@github.com/visheshasanadhya/BMDU-E_Commerce-_app.git
```
Then push:

```bash
git push -u origin main

```

---

---

## 🌐 **Setup Git In system Commands**


To check your Git username and email configuration, use the following commands in your terminal:
1. To view all Git configuration settings, including username and email:
Code
```bash
git config --list
This command displays all configured Git settings. Look for user.name and user.email in the output.
```
2. To view only your Git username:
Code
```bash
git config user.name
```
3. To view only your Git email:
Code
```bash
git config user.email
```
4. To check global-level username configuration specifically:
Code
```bash
git config --global user.name
```
5. To check global-level email configuration specifically:
Code
```bash
git config --global user.email
```
These commands will display the configured values if they are set. If no output is returned, it means the specific configuration is not set at that level (global or local, depending on whether --global is used).


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
git branch -d main                         # Delete branch locally in system
git push origin --delete main              # Delete branch from GitHub too (if pushed)
git checkout main                          # switch back to your working branch (e.g., main)
git fetch --tags                           # fetch the tags from the remote first: tags (ex.-v1 and v2) build when release apk on github
git tag                                    # Then check the tags list: You should see v1 and v2 listed.
                                           
git checkout Calling-Api-Outside           # switch back to your working branch Calling-Api-Outside branch to GitHub
git push origin Calling-Api-Outside        # Push Calling-Api-Outside branch to GitHub
```





---

## 🌐 **Flutter Android app Build Commands**

```bash
flutter build apk --release                             # Build Flutter app in release mode
flutter build apk --release --no-tree-shake-icons       # Keep unused icons
```
The generated APK will still be in:

```swift
build/app/outputs/flutter-apk/app-release.apk
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

flutter build web --release --no-tree-shake-icons --base-href "/repo_name/"     # Step 1: Build the web app with proper base href

cd build/web                          # Navigate to build/web
git init
git remote add origin <repo_url>
git checkout -b gh-pages
git add .
git commit -m "Deploy to GitHub Pages"
git push -f origin gh-pages           # Force push to gh-pages
```

---

## 🚀 **Deploy to `gh-pages` Branch (Alternative)**

```bash

flutter build web --release --no-tree-shake-icons --base-href "/repo_name/"     # Step 1: Build the web app with proper base href

cd build/web                          # Navigate to build/web
git init
git remote add origin <repo_url>
git checkout -b gh-pages
git add .
git commit -m "Deploy to GitHub Pages"
git push -f origin gh-pages           # Force push to gh-pages
```

---




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

## 🔁 **DEVICE CONNECTION  &  EMULATOR RELATED**

To restart device
```bash
adb kill-server
adb start-server

```



```bash
ipconfig                                 # check IP of system
adb devices                           # First-Time Setup (Needs USB Once) and Enable Developer Options & USB Debugging on your phone
adb tcpip 5555                        # Enable Wireless Debugging
adb connect 192.168.29.27:5555        # adb connect <Your-Phone-IP> . Go to Settings → About Phone → Status or Wi-Fi details. 
flutter devices                        # List all connected devices

flutter emulators                     # List available emulators
flutter emulators --launch <id>       # Launch an emulator
flutter run                           # Run app on default device
flutter run -d <device_id>            # Run on specific device 
```

##To use web app by adb device


 Run Flutter web server bound to your IP
```bash
flutter run -d web-server --web-hostname=0.0.0.0 --web-port=8080
```
This will serve the app on all network interfaces.


---

Open the URL on Android

In the Flutter console, you’ll see something like:

Running on http://0.0.0.0:8080

Replace 0.0.0.0 with your actual IPv4 address from Step 1, e.g.:
```bash
http://192.168.1.5:8080
```
Make sure your Android device is connected to the same Wi-Fi network as your computer.

Open that link in Chrome (or any browser) on your Android device.



---

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
