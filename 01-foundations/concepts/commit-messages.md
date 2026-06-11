# Concept Note: Commit Messages
**Date:** 11 June 2026
**Related Lesson**[Commit Messages](https://www.theodinproject.com/lessons/foundations-commit-messages)

---

## Overview

Writing good commit messages is a professional discipline that separates
developers who treat Git as a save button from those who use it as a
communication tool. A well-written commit history is a readable narrative of
a project's evolution — useful to collaborators, future maintainers, and
your future self.

---

## Why Good Commit Messages Matter

**For employability:** A thoughtful commit history demonstrates professional
habits to potential employers or clients reviewing your work. It signals that
you understand development as a collaborative, long-term practice rather than
a solo activity with no audience.

**For collaboration:** Teammates can track what changed, when, and why without
having to read through the code itself. Clear commit messages make code review
faster and more focused.

**For debugging:** When something breaks, `git log` becomes a diagnostic tool.
Descriptive commit messages allow you to identify which change introduced a
problem and revert precisely without guesswork.

**For returning to old projects:** Coming back to a project after weeks or
months is disorienting without context. A good commit history acts as a
project journal — it reconstructs your reasoning at the time each change
was made.

---

## What a Good Commit Message Looks Like

An effective commit consists of two parts: a **subject** and a **body**,
separated by a blank line.

```
Add alt text to all images in the links-images project

Images were missing alt attributes which creates accessibility gaps
for users relying on screen readers. Added descriptive alt text to
all img elements across index.html and about.html.
```

**Subject** — A brief summary of what changed. Written as a command, not a
description. Read as: "If applied, this commit will: [subject line]."

**Body** — A concise explanation of what was done, what problem it solves,
and why this approach was taken. Not how — the code shows how.

---

## Writing Multi-Line Commit Messages

The `-m` flag on `git commit` is useful for single-line subject-only commits.
For commits that need a subject and body, run the command without the flag:

```bash
git commit
```

This opens a new VS Code tab (if VS Code is configured as the Git editor)
where you can write a multi-line message. Save and close the tab to create
the commit.

---

## The Seven Rules of a Great Git Commit Message

1. **Separate subject from body with a blank line** — Many Git tools treat
   the first line as the subject and everything after the blank line as the
   body. Without the blank line they merge into one block.

2. **Limit the subject line to 50 characters** — Forces clarity and brevity.
   GitHub truncates subject lines longer than 72 characters with an ellipsis.

3. **Capitalize the subject line** — Consistent formatting, easier to read
   at a glance in `git log`.

4. **Do not end the subject line with a period** — Unnecessary punctuation
   in a title-style line.

5. **Use the imperative mood in the subject line** — Write as a command:
   "Fix bug" not "Fixed bug" or "Fixes bug." A useful test: the subject
   should complete the sentence "If applied, this commit will: ___."

6. **Wrap the body at 72 characters** — Keeps the message readable in
   terminal output without horizontal scrolling.

7. **Use the body to explain what and why, not how** — The code itself
   shows how. The commit message should explain the reasoning and context
   behind the change.

---

## When to Commit

Commit early and commit often. Specifically:

- When a piece of code works the way you intended
- When a bug is fixed
- When a typo is corrected
- When a meaningful, self-contained unit of work is complete

Each commit should represent one logical change — an atomic commit. This
keeps the history clean and makes individual changes easy to revert if needed
without disturbing unrelated work.

A finished project with one large commit tells no story. A finished project
with fifty focused commits shows the thinking behind every decision.

---

## Key Insight

A commit is a snapshot of your code at a specific moment. The commit message
is the caption on that snapshot — it tells anyone reading the history what was
happening at that moment and why. Without good captions, a commit history is
just a list of timestamps. With them, it becomes a technical journal that
documents how a project grew from nothing into something complete.

The discipline of writing good commit messages also sharpens the habit of
atomic commits. If you struggle to write a clear subject line for a commit,
it is usually because too many unrelated changes were bundled together. The
message-writing process itself becomes a quality check on the commit.

---

## Connection to Previous Learning

**Day 52 (Introduction to Git):** Introduced version control as a system for
tracking changes over time. Commit messages are the human layer on top of that
system — they translate machine-readable snapshots into developer-readable
history.

**Day 56 (Git Basics):** Introduced atomic commits as best practice. This
lesson formalises the standard for what the message attached to each atomic
commit should look like and why that standard exists.

---

**Status:** ✅ Commit Messages — Concept Note Complete