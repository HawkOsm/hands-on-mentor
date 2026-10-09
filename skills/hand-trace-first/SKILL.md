---
name: hand-trace-first
description: Has the learner work a tiny example by hand and write the steps in plain words before writing any code or tests. Use when the learner is about to write a function, loop, parser or algorithm and does not know where to start, says their algorithm knowledge is weak, or when their code is built on a wrong model of the problem.
---

# Hand-trace first

Most "I can't code this" is really "I have not written the steps yet". The steps are the
algorithm. Writing them in plain words costs minutes and saves hours.

## Procedure
1. **One small example.** Pick a tiny input and the output the learner expects. Make the
   example include at least one awkward case (an empty input, a bad line, an item out of
   order).
2. **Work the numbers by hand.** The learner computes the expected result themselves.
   These numbers become the first test.
3. **Steps in plain words.** The learner writes the steps as comments, in the order they
   would do them by hand ("start with an empty list; for each line: skip blanks; try to
   read it; if it fails, skip it; otherwise add it; return the list").
4. **Review the steps before any code.** Check the unit of work, where the failure can
   happen, and what happens at the edges. This is where most bugs are caught.
5. **Test first.** The learner turns the example into a test and watches it fail for the
   right reason.
6. **Code, one comment at a time.** Run the test after each step.

## Requirement lists
For anything bigger than a function, first agree a requirement list: input, output,
rules, edge cases, and what is deliberately left out for now. Ask the learner to decide
the open questions (for example "what should the average be when there is no data?").

## Reviewing the learner's steps
- Praise what is right, specifically.
- Point at the step that is wrong and ask a question that shows why (for example "where
  does the error get caught: for the whole file, or for one line?").
- Do not rewrite the steps for them.

## Pointers
- If the learner needs practice with problem-solving in general, suggest a free
  introductory book or course and say which chapters apply to the task at hand.
