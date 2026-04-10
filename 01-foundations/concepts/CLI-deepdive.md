# A Deepdive into Command Line Basics

**Date Learned:** 10 April 2026  
**Related Lesson:** [Command Line Basics](https://theodinproject.com/lessons/foundations-command-line-basics)  
**YouTube Explanation:** [A Deepdive Into CLI]()

## 📚 What I Learned Today
Command Line Basics — Hands-On Practice + Lesson Deep Dive
Today combined practical application (before the lesson) with structured learning. Two layers of understanding built in one day.

### 🔧 Pre-Lesson Hands-On Practice
Before reading the material, I worked through practical CLI tasks:
Commands I used:
wget <url> — Downloaded the shell lesson data zip file directly from the internet via the terminal.
sudo apt install unzip — Installed the unzip program using the package manager. Note: when sudo asks for a password, the terminal shows NO visible characters as you type — this is intentional security behavior. Just type and press Enter.
unzip shelllessondata.zip — Extracted the zip archive.
rm shelllessondata.zip — Deleted the zip file after extraction.
ls -F — Listed the current directory contents with type markers and color coding.
What ls -F revealed about file types:
MarkerColorFile Type/ at end of nameBlueDirectories/Folders* at end of nameGreenExecutable program files (e.g., Chrome).jpg, .webp, .pngPinkImage filesNo markerWhiteDocuments (PDF, HTML, Markdown, CSS, JS, some apps).deb extensionRedDebian package files.zip extensionRedZip archivesNo markerGreenAPT package files

---

### 🐚 What is a Shell?
A shell is a program whose primary purpose is to read commands and run other programs. Bash is the default shell in many Unix/Linux implementations, and it's what runs when I open my terminal.
Key advantages of the shell:

High action-to-keystroke ratio (do a lot with very little typing)
Supports automation of repetitive tasks
Can access and interact with network machines

The main challenge: Knowing which commands to run and how to use them — this comes with practice and experience.

---

### 📁 The File System
The file system is the part of the operating system responsible for managing files and directories on disk.
How it's structured: Files are stored in directories. Directories can contain other directories, forming a directory tree — like a pedigree or family tree turned upside down.

The root directory sits at the top (the ancestor), holding everything else
It's represented by a single forward slash: /
On Linux, the home directory path looks like: /home/username
The leading / in any path = root. Slashes inside a path = separators

My analogy: The pwd command is like dropping a location pin on Google Maps — it tells you exactly where you are in the file system at any given moment.

---

### 🔑 Core Commands Learned
Inspecting Location & Contents
pwd — Print Working Directory. Tells you your current location in the file system.
ls — Lists contents of the current directory.
ls -F — Lists contents with type markers (/, *, @) and color coding.
ls -a — Shows ALL files including hidden ones (files starting with a dot).
ls -lh — Combines multiple options: detailed list with human-readable file sizes. You can stack options like this.
ls <path> — Lists contents of a specific directory without navigating to it.

#### Getting help with any command:

ls --help — Displays usage information directly in terminal
man ls — Opens the full manual page (press q to exit)


#### Navigating the File System
cd <directory> — Change Directory. Moves you into the specified directory.
cd (no argument) — Takes you back to home directory from anywhere.
cd ~ — Also takes you to home directory (tilde = home).
cd - — Takes you back to the directory you were in previously.
cd .. — Moves up one level to the parent directory.
cd ../.. — Moves up two levels (parent of parent).

#### Path Types
Absolute path — Specifies location from the root of the file system. Always starts with /.
Example: /home/kuda/Documents/projects
Relative path — Specifies location relative to where you currently are. No leading /.
Example: Documents/projects (if you're already in /home/kuda)
Shortcut: Instead of cd Documents then cd projects, you can write cd Documents/projects to go directly.

### Creating Files & Directories
mkdir <name> — Make a new directory.
touch <filename> — Create a new empty file.

###3 Renaming, Moving & Deleting
mv <old> <new> — Rename OR move a file/directory (same command, two uses).
rm <filename> — Delete a file. Permanent — no recycle bin.
rmdir <directory> — Remove an empty directory.
rm -r <directory> — Remove a directory and all its contents recursively. Use carefully.

---

### 🧩 Shell Syntax
Every command follows this structure:
prompt   command   option(s)   argument(s)
  $        ls        -lh       Documents/

Prompt ($ or %) — Always there, you don't type it
Command — The instruction to execute
Option/Flag/Switch — Modifies the command's behavior (starts with -)
Argument — What the command operates on
Options + Arguments together = Parameters

Rules:

Separate each part with spaces — missing spaces cause errors
Commands don't always need parameters (e.g., pwd stands alone)
Some options are case sensitive (-F ≠ -f)


---

### 💻 Terminal Practical Notes
Copy in terminal: Ctrl + Shift + C
Paste in terminal: Ctrl + Shift + V
(Standard Ctrl+C and Ctrl+V don't work inside Linux terminals — they do different things in CLI context)

---

## 💡 Key Insights
Why CLI is indispensable as a developer: Installations, Git operations, file management, deployment, automation — all happen in the terminal. It's not optional. It's daily.
Stacking options is powerful: Commands like ls -lh or ls -la combine multiple behaviors in one stroke. This is where CLI efficiency really shines.
The file system IS a tree: Root at top, branches downward. Navigation is just moving up and down branches. Once you see it as a tree, getting lost becomes much harder.
pwd is your compass: Any time you feel disoriented in the file system, pwd tells you exactly where you are.

### 🔗 Connections
Day 1 connected back here: The SSH key setup, Git init confusion, and repo restructuring — all CLI. I was using these tools before I formally learned them. Today's lesson gave names and structure to what I'd already practiced by necessity.
That's the best kind of learning: doing first, understanding second.

---

## 🎯 What's Next

- Wildcards (*, ?) for pattern matching
- Pipes (|) and redirection (>, >>) for chaining commands
- Command history and keyboard shortcuts
- More advanced file manipulation

---
