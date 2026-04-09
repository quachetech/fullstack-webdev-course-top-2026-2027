# Command Line Basics

**Date Learned:** 09 April 2026  
**Related Lesson:** [Command Line Basics](https://theodinproject.com/lessons/foundations-command-line-basics)  
**YouTube Explanation:** [What I know About Command Line]()

## Learning Objectives
1. Describe what the command line is
2. Open the command line on your computer
3. Navigate directories and display directory contents
4. Create a new directory and a new file
5. Rename or destroy a directory and a file
6. Open a file or folder in a program

---

## What is the Command Line?

The **command line**, **terminal**, and **shell** are terms for the same thing — a program that lets you give your computer direct text instructions and receive output.

Unlike a GUI (Graphical User Interface) which presents choices automatically, the CLI requires you to learn commands. The tradeoff is worth it:
- More efficient for repetitive tasks
- More accurate and fail-proof than GUI
- Commands can be combined into scripts to automate tasks

---

## How It Works

When opened the terminal shows a **prompt** — typically a `$` sign on Linux — indicating it's ready for input. A blinking cursor shows where your text will appear.

You may also see your username and hostname before the prompt.

---

## Key Commands

### Navigation
| Command | Action |
|---------|--------|
| `ls` | List contents of current directory |
| `cd directory_name` | Navigate into a directory |
| `~` | Represents home directory (tilde) |

**Tip:** Press `Tab` after typing the first few letters of a directory name to autocomplete.

### Creating
| Command | Action |
|---------|--------|
| `mkdir directory_name` | Create a new directory |
| `touch filename.extension` | Create a new file |

**Example:** `touch index.html` creates an HTML file named index.

### Renaming and Moving
| Command | Action |
|---------|--------|
| `mv old_name new_name` | Rename a file or directory |
| `mv filename directory/` | Move a file to a different directory |

**Note:** Renaming is just moving something to the same location with a different name.

### Deleting
| Command | Action |
|---------|--------|
| `rm filename` | Delete a file |
| `rm -r directory_name` | Delete a directory and its contents |

⚠️ **Important:** `rm` on its own won't work on directories — you need the `-r` flag (recursive).

### Opening in VSCode
| Command | Action |
|---------|--------|
| `code filename` | Open a specific file in VSCode |
| `code .` | Open current directory in VSCode |

---

## Opening the Terminal

- **Apps menu:** Search for Terminal
- **Keyboard shortcut (Linux):** `Ctrl + Alt + T`

---

## To Research Further
- What do the command abbreviations actually stand for? (mkdir, ls, cd, rm, mv)
- Additional flags and options for each command
- Read Odin Project materials and fill gaps

---
*Notes primarily from CLI practice before reading curriculum materials*