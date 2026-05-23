# Where Does Bad Code Come From? — Casey Muratori

**Source:** Invited lecture given to infura.io, posted to YouTube ([7YpFGkG-u1w](https://www.youtube.com/watch?v=7YpFGkG-u1w)).

---

## TL;DR

Casey argues that "bad code" — bloated, slow, buggy, hard-to-build modern software — is not an algorithm problem but a *glue code / infrastructure* problem. The root cause: the mental "filter" programmers develop is being trained on **unmeasured rituals** like SOLID and "clean code" instead of on **real-world costs** that can actually be measured (execution time, build time, debug time, etc.). Hardware constraints used to enforce discipline; now nothing does, so the next generation inherits libraries and ecosystems built by people who were already lost.

---

## Salient Points

### What "bad code" means in this talk
- **Not about money** — current market tolerates low quality because competition is thin.
- **Not about fun** — devs may genuinely enjoy modern stacks.
- **It's about *potential*** — the gap between what we *could* deliver to users/society and what we actually ship.

### Algorithms aren't the problem
- Algorithm theory is mature: order notation, complexity classes, hash tables, heaps, sorting.
- Online resources on algorithms are *generally fine*.
- The mess is in the **glue code** — the infrastructure that connects algorithms together.

### Why hardware used to keep us honest
- 64K RAM, slow disks, weak CPUs — there was a natural ceiling on how much glue code could exist.
- Code that wasn't disciplined simply *wouldn't run*.
- That selection pressure trained programmers' instincts. We've never built a replacement for it.

### The generator/filter model of learning
- A programmer's brain develops a **generator** (produces syntactically valid code) plus a **filter** (rejects most of what the generator emits).
- With experience the filter narrows aggressively — experienced programmers' output is highly regularized.
- *What that filter is tuned on* determines what code you write.

### The exploration metaphor
- Programming feels like **navigation without a map**, not architecture.
- You dead-reckon toward a destination you can't fully see, and you only know you've arrived once you're there.
- Bad development *feels* like being lost — because in a real sense, it is.

### The core failure: training the filter on fictions
- Modern programmers get their filter tuned by classes, code reviews, Stack Overflow, mentors, lectures — **not** by hardware feedback.
- Industry teaches **rituals** (SOLID, "clean code," Liskov substitution) which are:
  - Defined entirely in the programmer's head, not on the CPU.
  - Not tied to any measurable real-world outcome.
  - Assumed to produce good results without proof.
- "It's very much like, 'we're going to bless the food before we eat it.'"

### The WARMED counter-proposal
A deliberately parallel acronym to SOLID — but every letter is something you can **actually measure** as a cost:

| Letter | Cost                                                   |
|--------|--------------------------------------------------------|
| **W**  | **Writing** the code                                   |
| **A**  | **Agreeing** on code (or **Arguing**, if you prefer)   |
| **R**  | **Reading** the code (later, by you or someone else)   |
| **M**  | **Modifying** the code                                 |
| **E**  | **Executing** on hardware *(the most important cost)*  |
| **D**  | **Debugging** the code                                 |

Whatever practice you adopt should be evaluated by whether it *demonstrably* lowers these costs.

### Hammers, not compasses
- We hand new programmers tools (SOLID, etc.) that don't measure anything — and tell them these tools are critical for navigation.
- We talk about a map (Liskov, etc.) that doesn't correspond to any real territory — "it's like Middle-earth."

### Libraries and ecosystems as bad base camps
- "Code reuse is good" is taught uncritically.
- But the libraries / languages / platforms you reuse were **built by people who were also lost**.
- Starting from someone else's bad base camp is often worse than starting from port.

### The fix
- Stop accepting unmeasured claims. Demand: "what specific number went down, and by how much?"
- Measure GitHub round-trips per bug fix, meeting hours, onboarding time, build time, runtime — *something*.
- SOLID without a "P" for Performance was malpractice from day one.
- The bottom line: **we stopped measuring and talking about what we actually want**, and pivoted to measuring fictions. Each generation inherits only the fictions.

---

## Outline

1. **Intro** — Kickstarter promo / framing the lecture.
2. **State of software today** — Too much code, fragile builds, multi-hour build times, gigabyte working sets, still buggy.
3. **Defining "bad code"** — Not about money or fun, but about unrealized potential.
4. **Algorithms vs. glue code** — Algorithm theory is fine; infrastructure is where things rot.
5. **How programmers learn** — The generator/filter process in the brain.
6. **The exploration/navigation metaphor** — Code as a journey, not architecture.
7. **Feeling lost in modern development** — Why this metaphor rings true day-to-day.
8. **Where the filter gets tuned now** — Classes, mentors, Stack Overflow, lectures.
9. **SOLID and "clean code" as unmeasured ritual** — Imaginary metrics with no tether to the machine.
10. **The proposed WARMED acronym** — Writing, Agreeing, Reading, Modifying, Executing, Debugging.
11. **Explorers given hammers, libraries as bad base camps** — Tying back to the navigation analogy.
12. **Can it be fixed?** — Yes: measure real-world costs, demand evidence, refuse rituals.
13. **Outro** — Q&A teaser and Kickstarter wrap-up.
