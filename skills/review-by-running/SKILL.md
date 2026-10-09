---
name: review-by-running
description: Reviews a learner's code by actually running it (tests, linter, and small scratch scripts that reproduce suspected bugs) and reports findings in order of severity without fixing them. Use when the learner says "check this", "is this right", "this works?", "done I think", or shows code and tests for feedback.
---

# Review by running

Do not review from reading alone. A claim that can be checked in a few seconds must be
checked before it is stated.

## Procedure
1. **See what changed.** `git status`, `git diff`, and read the files in full.
2. **Run the project's checks.** Tests and linter. Note the exact result.
3. **Ask what the green tests prove.** A passing test that does not cover the risky case
   proves nothing. List what is not covered.
4. **Reproduce every suspected bug** with a short scratch script (use the session's
   scratch directory, never the project). Report the real output, not an assertion about
   what "should" happen. Try the edge cases: empty input, out-of-order input, a missing
   field, a crash inside a callback, a different casing.
5. **Check the tests would fail if the bug came back.** Temporarily reason, or run, to
   confirm the test is not passing by accident (for example because a global such as a
   frozen clock leaks between tests).
6. **Simplicity check.** For each function, ask two questions:
   - Could a beginner read it at a glance? Clever one-liners, chained conditions and
     tricks that need a comment to decode usually have a plainer form.
   - Is anything in it not needed yet? Extra options, extra layers, or handling for cases
     that cannot happen are premature. Say "this is more than the task needs", name what
     to remove, and let the learner decide.
   Simplicity findings go below real bugs, never above them.
7. **Report.**
   - What is right, in specifics.
   - Problems ordered by severity: breaks, wrong but passing, simplicity, style.
   - For each: file and line, what is wrong, why, and the name of the concept to look up.
   - Do not paste the fix.
8. **Correct your own earlier mistakes plainly.** If an earlier claim turned out wrong,
   say so with the evidence.
9. **End with one next step**, small enough to finish in a sitting.

## Calibration
- When a result looks surprisingly good, suspect the measurement first.
- If tests are green but lint is red, say both.
- If the learner says "fixed" but the code did not change, say what you saw, kindly.
- Keep the review proportional: five real problems, not twenty.
