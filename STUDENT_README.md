Replace the URL with your actual GitHub repository address.
# Getting Started: Hello D Project (Beginner Guide)

Welcome! This guide will help you set up, build, and debug a simple "Hello, World!" program in the D programming language using Visual Studio Code (VSCode). This project starts from an empty folder named `hello_d`.

## 1. Project Structure

After setup, your project folder will look like this:

```
hello_d/
├── app.d                # Your D source file
├── hello_d              # The compiled program (after building)
└── .vscode/
    ├── launch.json      # Debugger configuration
    └── tasks.json       # Build tasks for different D compilers
```

## 2. Writing Your First D Program

Create a file named `app.d` with this content:

```
import std.stdio;

void main()
{
    writeln("Hello, World!");
}
```

## 3. Building the Program

You can build your program using any of the three main D compilers:
- **dmd** (default)
- **gdc**
- **ldc**

### How to Build
- Press `Ctrl+Shift+B` to build with the default compiler.
- Or, open the Command Palette (`Ctrl+Shift+P`), type `Run Task`, and choose:
  - `build D app.d (dmd)`
  - `build D app.d (gdc)`
  - `build D app.d (ldc)`

The compiled program will be named `hello_d`.

## 4. Running the Program

After building, run this command in the terminal:
```
./hello_d
```
You should see:
```
Hello, World!
```

## 5. Debugging the Program

- Press `F5` in VSCode to start debugging.
- The output will appear in the Terminal pane.

## 6. Changing the Default Compiler

To change which compiler is used by default when you press `Ctrl+Shift+B`:
1. Open `.vscode/tasks.json`.
2. Find the build task for your preferred compiler.
3. Set `"isDefault": true` for that task, and `false` for the others.
4. Save the file.

## 7. What are launch.json and tasks.json?
- **.vscode/launch.json**: Tells VSCode how to debug your program.
- **.vscode/tasks.json**: Defines how to build your program with different compilers.

## 8. Need Help?
If you get stuck, ask your instructor or search for "D language getting started" online.

## 9. Cleaning Up Build Files

To remove the compiled program and object files, use the `clean` task:

- Open the Command Palette (`Ctrl+Shift+P`), type `Run Task`, and select `clean`.
- This will delete `hello_d` and `hello_d.o` from your project folder.

## 10. Pushing to GitHub

To save your project on GitHub:

1. Install git if needed: `sudo apt install git`
2. Initialize a git repository: `git init`
3. Add your files: `git add .`
4. Commit: `git commit -m "Initial commit"`
5. Create a new repository on GitHub (via the website).
6. Link your local repo: `git remote add origin https://github.com/your-username/your-repo.git`
7. Push: `git push -u origin master` (or `main`)


Happy coding!
