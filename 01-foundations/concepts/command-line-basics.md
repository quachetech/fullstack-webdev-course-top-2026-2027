# Command Line Basics (Pre-Reading Synthesis)

**Date Learned:** 09 April 2026  
**Related Lesson:** [Command Line Basics](https://theodinproject.com/lessons/foundations-command-line-basics)  
**YouTube Explanation:** [What I know About Command Line]()


## What Is It

**Important Note:** These notes are based on my hands-on experience using the terminal so far. Tomorrow I'll validate against the curriculum and fill knowledge gaps.

---

## 🎯 Learning Objectives

1. Describe what the command line is
2. Open the command line on your computer
3. Use the command line to navigate directories and display contents
4. Use the command line to create new directories and files
5. Use the command line to rename or destroy directories and files
6. Use the command line to open files/folders in programs

---

## 💻 What is the Command Line?

**Command Line Interface (CLI) = Terminal = Shell**

These terms all refer to the same thing: **a text-based interface for giving the computer direct instructions.**

### My Analogy: The Computer Whisperer

Using the CLI is like having a servant or assistant. When you want coffee, you simply instruct them to get it. You could get it yourself (GUI), but the assistant (CLI) makes it faster and more efficient.

**Key characteristics:**
- Direct access to everything on the computer
- Input ONLY via keyboard (no mouse)
- Text-based commands and output
- Excels at making repetitive tasks automatic and fast

### Why CLI Matters

**GUI (Graphical User Interface):**
- Click through menus and icons
- Visual, intuitive
- Presents choices automatically
- Slow for repetitive tasks

**CLI (Command Line Interface):**
- Type commands directly
- Must be learned (no automatic choices)
- More fail-proof and accurate for repetitive tasks
- Highly efficient and fast
- **Commands can be combined and saved into scripts** → automation

---

## 🚀 How It Works

### The Prompt

When you open the terminal, you see a **prompt** indicating it's ready for input:

**Typical format:**
username@hostname:~$

**Breaking it down:**
- `username` = your login name
- `@` = separator
- `hostname` = computer name (e.g., `localhost`, `thinkpad`)
- `:` = separator
- `~` = current directory (tilde = home directory)
- `$` = prompt symbol (Linux uses `$`, some shells use `%`)

### The Cursor

After the prompt, you see a **cursor**:
- Usually a flashing/blinking block
- Can also be a pipe (`|`) or underscore (`_`)
- Shows where your text will appear when you type

### Executing Commands

After typing a command, **press Enter/Return** to execute it.

The computer processes the command and displays output (if any).

---

## 🔧 Opening the Terminal

**Linux (Ubuntu):**

**Method 1: GUI**
- Go to Apps/Programs menu
- Click Terminal icon

**Method 2: Keyboard Shortcut** (faster)
Ctrl + Alt + T

**This instantly opens the terminal.**

---

## 📂 Navigating Directories

### Key Concept: Directory = Folder

These terms mean the same thing. CLI uses "directory," GUI uses "folder."

### Display Current Directory Contents

**Command:**
```bash
ls
```

**What it does:** Lists files and folders in the current directory

**Alternative:**
```bash
ls .
```
(The `.` explicitly means "this directory")

### Change Directory

**Command:**
```bash
cd <directory-name>
```

**Example:**
```bash
cd Documents
```

**Tab Completion (Pro Tip):**
- Type first few letters: `cd Doc`
- Press Tab
- Terminal autocompletes to `cd Documents/`
- Press Enter

**This saves massive time.**

### Special Directory Symbols

**`~` (tilde)** = Home directory
```bash
cd ~
```
(Takes you home from anywhere)

**`.` (dot)** = Current directory

**`..` (double dot)** = Parent directory
```bash
cd ..
```
(Moves up one level)

---

## 🆕 Creating Directories and Files

### Create a New Directory

**Command:**
```bash
mkdir <directory-name>
```

**Example:**
```bash
mkdir my-project
```

**What happens:** A new folder called `my-project` is created in the current directory.

### Create a New File

**Command:**
```bash
touch <filename.extension>
```

**Example:**
```bash
touch index.html
```

**What happens:** An empty HTML file called `index.html` is created.

**Why this matters:** When building websites, you'll create HTML/CSS/JS files this way constantly.

---

## ✏️ Renaming and Moving

### Rename a File or Directory

**Command:**
```bash
mv <old-name> <new-name>
```

**Example (renaming file):**
```bash
mv index.html home.html
```

**Example (renaming directory):**
```bash
mv my-project my-website
```

### Move a File to a Different Directory

**Command:**
```bash
mv <filename> <destination-directory>
```

**Example:**
```bash
mv index.html Documents/
```

**Note:** `mv` does BOTH rename and move (same command).

---

## 🗑️ Deleting Files and Directories

### Delete a File

**Command:**
```bash
rm <filename>
```

**Example:**
```bash
rm old-file.txt
```

**Warning:** This is PERMANENT. No recycle bin.

### Delete a Directory

**Empty directory:**
```bash
rmdir <directory-name>
```

**Directory with contents:**
```bash
rm -r <directory-name>
```

**The `-r` flag means "recursive" (delete everything inside).**

**WARNING:** `rm -r` is VERY powerful. Use carefully.

---

## 🔓 Opening Files/Folders in Programs

### Open File in VS Code

**Command:**
```bash
code <filename>
```

**Example:**
```bash
code index.html
```

**What happens:** VS Code opens with that file loaded.

### Open Current Directory in VS Code

**Command:**
```bash
code .
```

**What happens:** VS Code opens with the entire current folder as a project.

**This is how I work daily:** Navigate to project folder, run `code .`, start coding.

### Open Specific Directory in VS Code

**Command:**
```bash
code /path/to/directory
```

**Example:**
```bash
code ~/Documents/my-project
```

---

## 💡 Key Insights from Hands-On Experience

### 1. CLI is Faster Once You Learn It

**GUI:** Click → Navigate → Click → Navigate → Click  
**CLI:** Type one command, press Enter, done

**For repetitive tasks, CLI wins by a mile.**

### 2. Tab Completion is a Superpower

You don't type full names—just enough letters + Tab.

**This alone saves hours over a career.**

### 3. Commands Can Be Scripted

You can save sequences of commands into files (shell scripts) and run them with one command.

**This is automation = efficiency.**

### 4. Direct Access = Power

CLI gives you access to things GUI hides or restricts.

**Being "in the computer's brain" = control.**

---

## To Research Further
- What do the command abbreviations actually stand for? (mkdir, ls, cd, rm, mv)
- Additional flags and options for each command
- Read Odin Project materials and fill gaps

---
*Notes primarily from CLI practice before reading curriculum materials*