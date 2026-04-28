# Moving, Copying & Removing Files & Directories in Command Line

**Date Learned:** April 28 2026  
**Related Lesson:** [Command Line Basics](https://theodinproject.com/lessons/foundations-command-line-basics) 
**YouTube Explanation:** [Command Line Basics]

---

## 📚 What I Learned Today
Command Line Basics — Moving, Copying, and Removing Files & Directories
Today covered the three essential file manipulation commands: mv, cp, and rm. The critical thread running through all three is being deliberate — the command line does not ask for confirmation by default and has no undo.

## 🚚 Moving & Renaming — mv
- `mv` handles both moving and renaming. Same command, two uses depending on what you provide as the destination.
- Rename a file:
    `mv old-name.html new-name.html`
- Move a file to a different directory:
    `mv index.html projects/my-website/`
**⚠️ Silent overwrite warning:** 
- If a file with the same name already exists at the destination, `mv` will overwrite it without warning. The original is gone. No recovery prompt, no trash bin.
- Safe alternative — use the `-i` flag (interactive):
    `mv -i index.html projects/my-website/`
    This makes `mv` ask for confirmation before overwriting anything. Good habit when working with files you can't afford to lose.

## 📋 Copying — cp
-`cp` works the same way as `mv` except the original file stays where it is — only a copy is placed at the destination.
- Copy a file:
    `cp index.html backup/index.html`
- Copy a directory and all its contents — use `-r` (recursive):
    `cp -r my-website/ my-website-backup/`
    Without `-r`, `cp` will return an error when you try to copy a directory. The recursive flag tells it to include everything inside.

## 🗑️ Removing — rm
- Delete a file:
    `rm filename.txt`
- Delete a directory and all its contents — use `--recursive` or `-r`:
    `rm -r my-directory/`
    Without the recursive flag, rm only works on files and will return an error if you point it at a directory.
**⚠️ No trash bin.** 
- Deleted files are gone. While recovery tools exist, recovery is not guaranteed. 
- Treat every `rm` command as permanent.
- Safe alternative — use `-i` (interactive):
    `rm -i filename.txt`
    Prompts for confirmation before each deletion. Worth using whenever you're cleaning up important directories.

## 💡 Key Insight
The `-i` flag is available on both `mv` and `rm` and does the same thing on both — it inserts a confirmation step before the irreversible action executes. This is a small habit that can prevent significant data loss, especially when working quickly or using wildcards. The command line trusts you to know what you're doing. The `-i` flag is how you double-check yourself.

## 📊 Quick Reference
|Command|What it does
|mv <file> <new-name>|Rename a file|
|mv <file> <path/>|Move a file|
|mv -i|Ask before overwriting|
|cp <file> <destination>|Copy a file
|cp -r <dir> <destination>|Copy a directory recursively|
|rm <file>|Delete a file|
|rm -r <dir>|Delete a directory and contents|
|rm -i|Ask before deleting|

---

## 🚀 Next Steps

**Operations with multiple files and directories**

---

**Feynman Test:** Can I explain this to someone with zero coding knowledge?  
✅ Yes