# warmed-skills

A work-in-progress repo for distilling Claude Code skills from [Casey Muratori](https://caseymuratori.com/)'s talks — starting with **"Where Does Bad Code Come From?"** (invited lecture to infura.io, [YouTube `7YpFGkG-u1w`](https://www.youtube.com/watch?v=7YpFGkG-u1w)).

The repo name nods to Casey's **WARMED** acronym from that talk — a deliberately measurable counter to SOLID.

Sister project to [`yegor-pm-skills`](../yegor): same general shape (skills + research + talk source material), different philosophy lineage.

## Goal

Read Casey's talks closely, extract the durable principles (e.g. the **WARMED** acronym, the *generator/filter* model of learning, training instincts on measurable costs rather than rituals), and turn each into a Claude Code skill that an AI agent can apply to real work.

For now this repo is the *raw material* stage — the talk summary lives on `main`, with the bulky transcript and captions on the `talks` branch for cite-and-quote work. Skill folders and research write-ups will be added as they're produced.

## Branch layout

This repo uses two long-lived branches so you can decide whether you want the bulky raw talk media when you clone:

| Branch | Contents |
|---|---|
| `main` | README, LICENSE, .gitignore, `bad_code_talk/talk_summary.md` — and (as they're written) the `skills/` and `research/` folders. Lean. |
| `talks` | Everything on `main` **plus** the raw talk media in `bad_code_talk/`: `captions.SRT` and `transcript.txt`. |

The hand-curated summary is small and lives on `main` because the skills will quote it directly. The transcript and SRT are bulky and recoverable from YouTube via `yt-dlp`, so they live on a side branch — keeping the default clone small while still making the raw source material easy to grab when you need it.

### Clone just the lean main branch

```bash
git clone --single-branch --branch main <repo-url> warmed-skills
```

### Clone and check out the talks branch instead

```bash
git clone <repo-url> warmed-skills
cd warmed-skills
git checkout talks
```

### Already cloned? Switch between them

```bash
git fetch origin
git checkout talks   # transcript.txt + captions.SRT appear
git checkout main    # transcript.txt + captions.SRT disappear
```

Git itself manages the raw files appearing/disappearing as you switch — nothing is lost, both branches stay in sync with the remote.

## Status

Very early. The talk has been transcribed and summarised; no skills have been written yet. See [`bad_code_talk/talk_summary.md`](./bad_code_talk/talk_summary.md) for the current distillation of the talk's salient points.

## License

MIT — see [LICENSE](./LICENSE). Talk content (transcript, captions, summary) is derivative of Casey Muratori's lecture and remains his intellectual property; it is included here for study and citation, not redistribution.
