# Git Basics

**Date Learned:** [Date]  
**Related Lesson:** [Git Basics](https://www.theodinproject.com/lessons/foundations-git-basics#cheatsheet)

---

## Overview

Git operates through a three-stage workflow that moves changes from your local
working environment to a remote repository. Understanding these three stages
and the commands that govern movement between them is the foundation of working
with Git effectively.

---

## The Three-Stage Workflow

**Working Tree** — Your local clone of the repository. This is where active
development happens. Files here are marked as either *untracked* (newly
created, Git has never seen them) or *modified* (existing files that have been
changed since the last commit).

**Staging Area** — A waiting area where you deliberately place files before
committing them. Adding files to staging is an intentional act — it means you
are selecting exactly which changes will be included in the next snapshot. Not
everything in the working tree has to be staged at once.

**Git Repository** — Once staged files are committed, Git creates a permanent
snapshot of those changes. This snapshot becomes part of the project's
immutable history and cannot be undone. Pushing then synchronizes these
committed snapshots to the remote repository hosted on a service like GitHub.

The movement is always in one direction:
**Working Tree → Staging Area → Repository → Remote.**

---

## Core Commands

### Remote Repository

```bash
git clone git@github.com:USER-NAME/REPOSITORY-NAME.git
# Creates a local copy of a remote repository

git push
# Sends committed snapshots to the remote repository
```

### Workflow

```bash
git add .
# Stages everything in the current directory

git commit -m "Descriptive message about what changed"
# Creates a permanent snapshot of staged changes
```

### Status & History

```bash
git status
# Shows current state of working tree and staging area

git log
# Displays full commit history
```

---

## Git Syntax Structure

Every Git command follows the same logical pattern:

```
program | action | destination
```

| Command | Program | Action | Destination |
|---|---|---|---|
| `git add .` | git | add | . (everything here) |
| `git commit -m "message"` | git | commit -m | "message" |
| `git status` | git | status | none needed |

Reading commands this way makes unfamiliar Git commands much easier to decode
on sight.

---

## Best Practices

### Atomic Commits

An atomic commit contains changes related to exactly one feature or task —
nothing more. This practice serves two purposes. First, if a change introduces
a problem, you can revert that specific commit without disturbing unrelated
work. Second, it makes writing meaningful commit messages natural, because each
commit has a single clear purpose to describe.

### Meaningful Commit Messages

Commit messages are communication — with collaborators, and with your future
self. A well-written message explains *what changed and why*, not just *that
something changed*. When revisiting old code months later, the commit history
becomes a readable narrative of how the project evolved.

**Less useful:**
```bash
git commit -m "fixed stuff"
```

**More useful:**
```bash
git commit -m "Fix form validation to reject empty email field"
```

---

## Key Insight

The staging area is the most misunderstood part of the Git workflow for
beginners. It can feel like an unnecessary extra step — why not just commit
directly from the working tree? The answer is control. Staging lets you be
deliberate about what goes into each snapshot. You might have changes to three
files but only want to commit two of them right now. The staging area makes
that precision possible, which in turn makes atomic commits achievable.

Git is useful in collaboration, but it is equally valuable when working alone.
Your commit history is a log of your own thinking — a record of decisions made,
problems solved, and directions taken. The discipline of committing well now
builds a reference you will genuinely rely on later.

---

**Status:** ✅ Day 56 Complete — Git Basics  
**Next:** Applying the three-stage workflow consistently across all future
project work.