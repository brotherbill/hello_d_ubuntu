# GITHUB_ERRORS_README.md

# Note: You must have an active GitHub.com account before starting these steps. Creating a GitHub account is not covered in this document.

## Troubleshooting GitHub Push (Beginner, Sad Path)


If you have not yet tried the main workflow, see GITHUB_README.md for the step-by-step happy path guide.

This guide helps you recover from common errors when pushing your project to GitHub. Replace `my_user_name` with your actual GitHub username.

### 1. Install git (if not already installed)
```sh
sudo apt install git
```

### 2. Set your git user name and email (if prompted)
```sh
git config --global user.name "my_user_name"
git config --global user.email "my_email@example.com"
```

### 3. If you see "Repository not found" or wrong username
- Double-check your remote URL:
```sh
git remote -v
```
- If incorrect, update it:
```sh
git remote set-url origin https://github.com/my_user_name/hello_d_ubuntu.git
```
- Make sure the repo exists on your GitHub account and is empty.

### 4. If you see "Authentication failed" or are asked for a password
- GitHub no longer accepts passwords for git operations.
- You must use a Personal Access Token (PAT):
    - Go to https://github.com/settings/tokens
    - Click "Generate new token (classic)"
    - Name it, set an expiration (e.g., 30 days), and check `repo` scope
    - Click "Generate token" and copy the token
- When prompted for password, paste your PAT instead.

### 5. If you need to log out of GitHub in your browser
- Go to https://github.com
- Click your profile icon (top right)
- Click "Sign out"

### 6. If you need to reset your GitHub password
- Go to https://github.com/login
- Click "Forgot password?"
- Follow the instructions to reset your password

### 7. If you need to change your branch name
- To rename the default branch:
```sh
git branch -m main
```
- Then push:
```sh
git push -u origin main
```

### 8. If you need to re-add the remote
```sh
git remote remove origin
git remote add origin https://github.com/my_user_name/hello_d_ubuntu.git
```

### 9. If you need to start over
- Delete the .git folder in your project:
```sh
rm -rf .git
```
- Then repeat the happy path steps from GITHUB_README.md

---
If you encounter a different error, search the error message online or ask for help with the exact message.
