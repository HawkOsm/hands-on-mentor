# hands-on-mentor

Claude Code skills for teaching someone to code **by having them build a real project**,
where the learner writes every line and the assistant explains, plans and reviews.

They were distilled from a long real session of one person learning Python by building a
tool. The method: picture first, work an example by hand, review by running the code,
and when stuck, point to a source instead of handing over the fix.

## Skills
| Skill | Use it when |
|---|---|
| `learner-owns-the-code` | starting a learning project, or the learner asks for the answer |
| `teach-by-picture` | the learner cannot picture how the parts fit together |
| `hand-trace-first` | the learner does not know where to start with an algorithm |
| `review-by-running` | the learner asks "is this right?" or shows finished code |
| `stuck-protocol` | the learner pastes an error or says they are stuck |
| `where-was-i` | the learner returns after a break or asks "what now?" |

## Try it locally
From any project:

```bash
claude --plugin-dir /path/to/hands-on-mentor
```

Skills from a plugin are namespaced, for example `/hands-on-mentor:where-was-i`.
Claude also loads them on its own when the description matches the situation.

## Status
Early draft (v0.1.0). The skills have not been tested by anyone but the author.
Released under the MIT license (see `LICENSE`). Ideas and contributions are welcome.
