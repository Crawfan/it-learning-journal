# Journal Entry 04 - Bash History, Shell Expansion, Aliases

**Date:** 2025-07-08 
**Focus:** RHCSA — History, Shell Behavior, Startup Files

---

### ⌨️ Command History
- `~/.bash_history` stores previously executed commands.
- **Reverse search**: `Ctrl + r`
- **Repeat specific**: `!23` (repeats command #23)
- **Repeat by prefix**: `!a` (repeats last command starting with "a")

---

### 🧠 Shell Shortcuts & Editing
- `Ctrl + a`: Move to beginning of line 
- `Ctrl + e`: Move to end of line 
- `Ctrl + u`: Delete entire line 
- `Ctrl + l`: Clear screen 
- `Ctrl + d`: End of input (EOF) 
- `Ctrl + c`: Cancel process 
- `Alt + f`: Move forward one word 
- `Alt + b`: Move back one word 

---

### 🧩 Shell Expansion (Globbing)
- **Wildcards**:
  - `*` matches any number of characters 
  - `?` matches a single character 
  - `[a-e]*` matches any file starting with a–e 
- **Brace Expansion**: `touch file{1..9}` → creates file1 to file9

---

### 🔒 Escaping and Quoting
- `""` suppress globbing but allows variable/command substitution 
- `''` disables all interpretation (raw text) 
- `\` escapes the next character only

---

### 🌍 Environment Variables & Aliases
- Set variable: `export COLOR=red`
- Alias: `alias lookup='ls -ltr'`
- Remove alias: `unalias lookup`

---

### 🧬 Bash Startup Files
- `/etc/profile`: System-wide login shell config 
- `/etc/bashrc`: System-wide interactive shell settings 
- `~/.bash_profile`: User login shell config 
- `~/.bashrc`: User interactive shell config

---

### 🔬 Lab Practice
**Goal:** Persist variable `color=red` and alias `dir='ls -ltr'`

1. `vim ~/.bash_profile` 
2. Add:
   ```bash
   export COLOR=red
   alias dir='ls -ltr'
   export HISTFILESIZE=2500
   ```
3. Save and apply: source ~/.bash_profile

---


### Next Steps 
- Try ~/.bash_aliases and source it from .bashrc 
- create a custom greeting variables
- study how **PATH** **PS1** and other env variables behave 
- revisit history set and env commands in more depth 
