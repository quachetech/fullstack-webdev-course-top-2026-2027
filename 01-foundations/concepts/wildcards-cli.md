# Operations With Multiple Files & Directories

**Date Learned:** 29 April 2026
**Related Lesson:** [Command Line Basics](https://theodinproject.com/lessons/foundations-command-line-basics)
**YouTube Explanation:** [Command Line Basics]

---

## 🎯 What Is This?

Command Line Basics — Operations With Multiple Files & Directories (Wildcards)

## 🃏 What Are Wildcards?
Wildcards are special characters that represent unknown characters or sets of characters in file and directory names. They allow you to apply a command to multiple files at once by specifying a naming pattern rather than listing every file individually.
This is where CLI efficiency really compounds — instead of running the same command ten times on ten files, one command with a wildcard handles all of them simultaneously.

## ✳️ The Asterisk *
Represents zero or more characters — the most flexible wildcard.
Examples:
bash*.pdb
Matches ALL files with a .pdb extension, regardless of name.
bashp*.pdb
Matches all .pdb files whose name starts with the letter p — like protein.pdb, peptide.pdb, etc.
bashcp *.html backup/
Copies every HTML file in the current directory into the backup folder in one stroke.

## ❓ The Question Mark ?
Represents exactly one character — more precise than *.
Examples:
bash?.pdb
Matches .pdb files whose name is exactly one character long — so a.pdb, b.pdb, 1.pdb would all match, but ab.pdb would not.
bash?.txt
Same logic applied to text files.

## 💡 Key Insight
The difference between * and ? is precision. The asterisk is broad — match anything, any length. The question mark is surgical — match exactly one unknown character. Used together or separately, wildcards turn what would be tedious multi-step operations into single commands. This directly connects to the CLI principle established on Day 13: high action-to-keystroke ratio. Wildcards are a big part of how that ratio stays high as projects grow in complexity.

---

## 🚀 Next Steps

Git & Version Control

---

**Feynman Test:** Can I explain this to someone with zero coding knowledge?  
✅ Yes