---
name: one-idea-per-commit
description: Teaches a learner to make small commits where each one has a single reason, with formatting changes kept separate from real changes and files named explicitly when staging. Use when the learner is about to commit, asks how to commit or what to stage, has many mixed uncommitted changes, or mentions "staging hell".
---

# One idea per commit

A commit is a note to your future self: "this is what changed and why". If it holds
three reasons, the note is useless and the history cannot be undone piece by piece.

## Before the commit
1. **Look.** `git status`, then `git diff` (or `git diff --stat` for a big one). Read the
   list. Anything you do not recognise is a question to answer now, not later.
2. **Sort the changes by reason.** Typical groups:
   - formatting only (the formatter touched many files)
   - one finished piece of new work and its tests
   - a leftover or unrelated file (scratch notes, a local config)
   Each group is its own commit.
3. **Green first.** Run the tests and the linter. A commit should leave the project in a
   state that works. If it does not, `git stash` the half-done part instead of
   committing a broken state.

## Making it
1. **Stage by name.** `git add path/one path/two`, never `git add .` or `-A` on a messy
   tree. Naming the files is how stray files stay out.
2. **Check what is staged.** `git status` again. Staged files should match the group you
   chose, nothing more.
3. **Message.** Short, imperative, says what and why, e.g. `skip corrupt ledger lines in
   read`. One line is fine for a small change.
4. **Order.** Mechanical changes (formatting) first, real work after, so a reviewer can
   skip the first and read the second.

## If something goes wrong
- Do not panic and do not run commands you do not understand. First look at
  `git status` and check that the files still exist on disk.
- A command that unstages everything usually removed files from the index only; the files
  are still there. `git reset` (the default, mixed form) puts the index back without
  touching the files.
- Before any command that can discard work (`reset --hard`, `checkout -- .`, `clean`,
  `rm -rf`), stash or commit what is there first.

## Habits to build
- One green commit per working day, at least.
- Never push a state where the tests fail.
- Do not mix a "while I was here" cleanup into an unrelated commit; make it a separate
  one or write it down for later.
- Leave local-only files (editor settings, personal notes) out with `.gitignore`, not by
  remembering.
