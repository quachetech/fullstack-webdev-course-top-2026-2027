# Working With Files

**Date Learned:** 27 April 2026  
**Related Lesson:** [Command Line Basics](https://theodinproject.com/lessons/foundations-command-line-basics) 
**YouTube Explanation:** [Commadn Line Basics]

## 📚 What I Learned Today
Command Line Basics — Working With Files
Today's focus was creating directory hierarchies and files from the command line, plus best practices for naming conventions.

## 📁 Creating Directories
- `mkdir <name>` — Creates a new directory in the current working directory. "mkdir" = make directory.
- `mkdir <path/to/directory>` — Creates a directory in a specific location that is NOT your current working directory. You provide the full path instead of just a name.
- `mkdir -p <path/with/nested/dirs>` — The -p flag (parent) creates a full nested directory structure in a single operation.
- Example:
    `mkdir -p projects/my-website/css`
- This creates projects, then my-website inside it, then css inside that — all at once, even if none of them existed before.

---

## ✅ Naming Conventions for Files & Directories
Good naming habits prevent headaches in the terminal:
1. **No spaces** — The command line uses spaces to separate arguments. A space in a name confuses the shell into thinking it's reading two separate things. Use a dash - or underscore _ instead.
2. **Don't start with a dash** — The shell interprets names beginning with - as options/flags, not file names.
3. **Stick to safe characters** — Lowercase letters, numbers, periods ., dashes -, and underscores _ are safe. Many other characters (like !, #, &, *) have special meanings in the shell and can cause unexpected behavior or even data loss.
If you must reference a file with spaces or special characters — wrap the name in single quotes:
 `cd 'my folder name'`

---

## 📄 Creating Files
- `touch <filename.extension>` — Creates a new blank file. The file exists but contains no data yet — it can be filled later.
- `code <filename.extension>` — Creates a file AND immediately opens it in VS Code. The file must be saved from within VS Code to be kept.
- File extensions matter for two reasons:

    - They tell you what type of data the file contains and what it's for
    - They tell the operating system which program to use to open the file
- Why create blank files? Some programs require that output files already exist before they run — they write INTO existing files rather than generating new ones themselves. `touch` handles this perfectly.

---

## 💡 Key Insight
The -p flag for `mkdir` is one of those small tools that saves significant time when scaffolding a project structure. Instead of cd-ing into each new directory to create the next one, a single command builds the entire hierarchy. This is exactly the kind of CLI efficiency that makes the terminal faster than a GUI for development work.

---