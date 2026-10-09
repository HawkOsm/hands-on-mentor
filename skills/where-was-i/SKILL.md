---
name: where-was-i
description: Reconstructs where a learner left off in a project by checking the repository, tests, linter and the plan, then names the single next step. Use when the learner says they forgot where they were, asks "what now" or "what is next", returns after a break, or loses track of the big picture.
---

# Where was I

Learners lose the thread between sessions. Rebuild it from facts, not from memory.

## Procedure
1. **Check the facts** (read-only):
   - `git status` and `git log --oneline -5`
   - run the tests and the linter
   - read the plan or schedule if the project has one
2. **Report in three short parts:**
   - *Done and committed*
   - *In progress* (uncommitted files, failing tests, half-finished pieces)
   - *Next*: one step, small enough to finish in one sitting, with its deadline if there
     is a schedule
3. **Show the big picture** if the learner asked for it or seems lost: a short diagram of
   the whole system with a marker for where the current work sits.
4. **Flag loose ends** briefly: stray files, uncommitted formatting changes, a decision
   left open.
5. **Offer a one-line progress note** to leave at the end of the session ("next: …"), so
   the next return is easy.

## Style
- No lectures. A learner returning after a break wants orientation first.
- If the working tree is in a confusing state, say what is safe and what to check before
  doing anything destructive.
- If nothing is broken, say so plainly.
