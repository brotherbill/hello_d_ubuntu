# GITHUB_README.md

# Note: You must have an active GitHub.com account before starting these steps. Creating a GitHub account is not covered in this document.

## How to Push Your Project to GitHub (Beginner, Happy Path)

If you encounter errors, see GITHUB_ERRORS_README.md for troubleshooting and recovery steps.

This guide walks you through pushing your project to GitHub from scratch, using Ubuntu and VSCode. Replace `my_user_name` with your actual GitHub username.

### 1. Install git (if not already installed)
```sh
sudo apt install git
```

### 2. Initialize a git repository in your project folder
```sh
git init
```

### 3. Add all files to the repository
```sh
git add .
```

### 4. Commit your changes
```sh
git commit -m "Initial commit"
```

### 5. Create a new repository on GitHub
- Go to https://github.com/new
- Name your repo (e.g., `hello_d_ubuntu`)
- Set visibility (public/private)
- Do NOT initialize with a README, .gitignore, or license
- Click "Create repository"

### 6. Add the remote URL (replace `my_user_name` and repo name)
```sh
git remote add origin https://github.com/my_user_name/hello_d_ubuntu.git
```

### 7. Generate a Personal Access Token (PAT)
- Go to https://github.com/settings/tokens
- Click "Generate new token (classic)"
- Name it, set an expiration (e.g., 30 days), and check `repo` scope
- Click "Generate token" and copy the token to a secure location (you won't see it again)

### 8. Push your code to GitHub
```sh
git push -u origin master
```
When prompted for username, enter your GitHub username (`my_user_name`).
When prompted for password, paste your PAT. The terminal will not display the PAT as you type or paste—this is normal for security. Just press Enter after pasting.

### 9. Done!
Your project is now on GitHub. You can view it at:
```
https://github.com/my_user_name/hello_d_ubuntu
```
