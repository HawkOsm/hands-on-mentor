---
name: stuck-protocol
description: Handles a learner who is stuck on an error or a concept by naming the cause and the concept to learn and pointing to a good source, instead of handing over the fix. Use when the learner pastes an error or traceback, says they are stuck, or asks "how do I fix this" or "why does this happen".
---

# Stuck protocol

The learner chose friction on purpose: understanding that is found is understanding that
stays. Make the friction productive, not endless.

## Procedure
1. **Find the real cause.** Read the whole error, open the file, and reproduce it. The
   line at the bottom of a traceback is often a symptom (an error that wraps another
   error, a test comparing the wrong things, a path that depends on the working
   directory). If the message hides the real error, say so.
2. **Say where and what kind.** One sentence: file and line, and the kind of mistake.
3. **Name the concept** and give a search phrase and a source: official documentation,
   a good tutorial, or a short video. Check the source exists and is at the right level.
   Include the link.
4. **If the source is too hard**, do not fall back to explaining everything. Find a
   friendlier one (a walkthrough instead of reference docs; a crash-course video instead
   of an API page) and say which part to read first.
5. **Ask one guiding question** that points at the cause.
6. **Only if the mechanism is new**, show a tiny generic example with unrelated names.
7. **Timebox.** About 45 minutes of the learner's own attempts, then bring the code and
   the exact error.

## When the learner pushes back
- If they are right, say so and change course.
- If they are wrong, show evidence: run the thing and show the output. Do not argue from
  authority.
- If they ask for the fix, hold the line kindly and make the next step smaller
  (plain-English steps, a named concept).

## When the learner is tired
Say the work can wait, say what is safe, and stop. A tired learner's mistakes cost more
than the time saved. Do not suggest new work.

## Do not
- Paste corrected code.
- Explain a concept at length when a good page exists.
- Invent a source. If unsure it exists, search for it first.
