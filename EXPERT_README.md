Replace the URL with your actual repository.
# Hello D Project: Expert Quick Reference

This project demonstrates a minimal D "Hello, World!" application, with VSCode integration for build and debug workflows. The setup supports dmd, gdc, and ldc compilers via tasks.json.

## Project Layout

```
hello_d/
├── app.d                // D source
├── hello_d              // Output binary
└── .vscode/
    ├── launch.json      // Debug config (cppdbg)
    └── tasks.json       // Build tasks for dmd, gdc, ldc, and clean
```

## Build Matrix (tasks.json)
- `build D app.d (dmd)`: Uses dmd (default, with environment activation)
- `build D app.d (gdc)`: Uses gdc (GCC frontend)
- `build D app.d (ldc)`: Uses ldc2 (LLVM backend)
- `clean`: Removes hello_d and hello_d.o

To change the default build, set `isDefault: true` in the desired task's group.

## Build/Run/Debug
- **Build:** `Ctrl+Shift+B` (default) or `Run Task` from Command Palette for explicit compiler selection.
- **Run:** `./hello_d`
- **Debug:** `F5` (launch.json uses cppdbg, expects output binary as hello_d)
- **Clean:** `Run Task` → `clean`

## Notes
- dmd task sources an activation script; gdc/ldc tasks assume compilers are in PATH.
- launch.json is configured for gdb/lldb via cppdbg; adjust as needed for custom toolchains or output names.
- All build tasks output to `hello_d` for consistency with launch.json.
- Minimal object cleanup (`hello_d.o`) is included in the clean task.

## Customization
- Extend tasks.json for additional build variants or flags as needed.
- For multi-file projects, update build commands accordingly.
- For advanced debugging, modify launch.json (e.g., args, env, pre/post tasks).

## GitHub Integration

1. Install git: `sudo apt install git`
2. `git init && git add . && git commit -m "Initial commit"`
3. Create a GitHub repo and add as remote:
    `git remote add origin https://github.com/your-username/your-repo.git`
4. Push: `git push -u origin master` (or `main`)

---
For further details, see D language documentation or VSCode tasks/launch configuration docs.
