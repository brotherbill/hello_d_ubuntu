# FROM_SCRATCH.md


## Build This Project From Scratch (Step by Step)

**Note:** PWD means "Present Working Directory"—the folder you are currently in when using the terminal. You can check your PWD by running `pwd` in the terminal.

### 0. Ensure You Are in the Correct Directory
Before starting, make sure your terminal's present working directory (PWD) is at `~/dev/d/`:
```sh
cd ~/dev/d/
```

**Precondition:** You must have an active GitHub.com account. Account creation is not covered here—see GITHUB_README.md for details.

---

### 1. Create and Enter Your Project Directory
```sh
mkdir hello_d && cd hello_d
```

### 2. Initialize a Git Repository
```sh
git init
```

### 3. Create the D Source File
Create a file named `app.d` with the following content:
```d
import std.stdio;

void main()
{
    writeln("Hello, World!");
}
```

### 4. Create VSCode Configuration
Create a `.vscode` directory:
```sh
mkdir .vscode
```

#### a. Create `.vscode/tasks.json` for Building
Add build tasks for dmd, gdc, ldc, and a clean task. (See the project’s tasks.json for details.)

#### b. Create `.vscode/launch.json` for Debugging
Add a launch configuration for debugging the compiled binary. (See the project’s launch.json for details.)

### 5. Create Documentation Files
- STUDENT_README.md
- EXPERT_README.md
- GITHUB_README.md
- GITHUB_ERRORS_README.md
- FROM_SCRATCH.md (this file)

(You can copy the content from the existing project or write your own.)

### 6. Create a .gitignore File
Add build artifacts and editor files to ignore:
```
hello_d
hello_d.o
*.exe
*.obj
*.dll
*.pdb
*.ilk
*.out
*.a
*.so
*.dSYM/
.vscode/
.DS_Store
*.log
```

### 7. Stage and Commit All Files
```sh
git add .
git commit -m "Initial commit"
```

### 8. Create a New Repository on GitHub
- Go to https://github.com/new
- Name your repo (e.g., hello_d_ubuntu)
- Do NOT initialize with a README, .gitignore, or license
- Click "Create repository"

### 9. Add the Remote and Push
```sh
git remote add origin https://github.com/my_user_name/hello_d_ubuntu.git
git push -u origin master
```

### 10. If You Encounter Errors
See GITHUB_ERRORS_README.md for troubleshooting and recovery steps.

---
For detailed GitHub steps, see GITHUB_README.md.
