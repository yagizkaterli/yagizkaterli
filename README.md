# Yagiz Katerli

Mathematical Engineering @ ITU · Istanbul

I build systems where AI agents do real work and the system can tell whether they actually
did it. Most of what I've learned came from the second half of that sentence.

---

### What I run

**A multi-agent operating discipline.** Sixty model processes can execute against one task
queue with no coordinator in the middle. Agents claim work by atomic rename, report against
receipts, and the gates are mechanical rather than honor-system — a rule that lives in
whoever remembers it decays, so none of them do.

The parts worth reading on their own are extracted here:
**[`agent-fleet`](https://github.com/yagizkaterli/agent-fleet)** — fleet runner, lease
daemon, atomic claim, Monte Carlo simulation. Go, no dependencies, ~3.7k lines.

**[LOBI](https://lobi.tech)** — a workspace for thinking with AI in a group. Your teammates
think in their own AI sessions; nothing enters yours without your hand. Next.js, TypeScript,
Supabase, row-level security, a 15-tool MCP server, and a terminal client. In production.

**Method notes.** [`foundation`](https://github.com/yagizkaterli/foundation) — the working
discipline itself: six laws and one loop, written to survive being lifted out of the system
that grew it. Plus [`frictionless`](https://github.com/yagizkaterli/frictionless) and
[`human-steps`](https://github.com/yagizkaterli/human-steps).

---

### The part I actually care about

Getting an agent to produce output is not the hard problem. Telling a run that worked apart
from a run that only looks like it did — that is the hard problem, and almost every mechanism
I've built exists because of a specific time I got it wrong:

- A fleet printed `skipped=0` on a round where a third of its agents never spoke. The line
  was true about what it measured and false about what happened. Every runner reports two
  numbers now.

- I classified a defect as a rate limit. A reviewer drawn from a different model family read
  the same evidence and called it a product-promise violation — correctly. A critic from the
  same family as the work agrees too easily, so adversarial roles now run on the other family.

- I read one fault's two symptoms as two faults, because they surfaced in different layers.
  A falsification pass caught it before I "fixed" an inconsistency that did not exist. Every
  finding now ships with the condition that would refute it.

- Sixty agents once started on my own desktop while I was using it. The design document
  written that same night already said they belong on a server. The rule was in my head; now
  it's a refusal in the code.

---

### Working with

`Go` · `Python` · `TypeScript` · `SQL` — distributed queues, lease protocols, CI gates,
Linux/VPS operations · multi-model orchestration, prompt and context engineering, tool-use
pipelines, MCP · evaluation harnesses, observability, hash-chained audit trails, statistical
simulation

---

### Also

Jazz drums. Basketball analysis. Philosophy of mind, read slowly. These are not a personality
section — the habit of watching a system from outside itself came from somewhere.

---

**Open to** research engineering and evaluation roles — San Francisco, New York, Chicago, or
remote. Visa sponsorship required.

📫 yagizkaterli@gmail.com · [LinkedIn](https://linkedin.com/in/yagizkaterli)

Most of my systems are private. I'm glad to walk through them live, including the parts that
failed.
