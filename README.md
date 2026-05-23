# casey-muratori-skills

A work-in-progress repo for distilling Claude Code skills from [Casey Muratori](https://caseymuratori.com/)'s talks — starting with **"Where Does Bad Code Come From?"** (invited lecture to infura.io, [YouTube `7YpFGkG-u1w`](https://www.youtube.com/watch?v=7YpFGkG-u1w)).

Sister project to [`yegor-pm-skills`](../yegor): same general shape (skills + research + talk source material), different philosophy lineage.

## Goal

Read Casey's talks closely, extract the durable principles (e.g. the **WARMED** acronym, the *generator/filter* model of learning, training instincts on measurable costs rather than rituals), and turn each into a Claude Code skill that an AI agent can apply to real work.

For now this repo is the *raw material* stage — the talk transcripts and summaries are checked in so we have a stable basis to quote and cite while drafting skills. Skill folders and research write-ups will be added as they're produced.

## Branch layout

This repo uses two long-lived branches so you can decide whether you want the bulky talk media when you clone:

| Branch | Contents |
|---|---|
| `main` | README, LICENSE, .gitignore — and (as they're written) the `skills/` and `research/` folders. Lean. |
| `talks` | Everything on `main` **plus** the `bad_code_comes_from_youtube_talk/` folder with `captions.SRT`, `transcript.txt`, and `talk_summary.md`. |

The talk transcript and SRT are recoverable from YouTube via `yt-dlp`, so keeping them on a side branch (rather than `main`) keeps the default clone small while still making the source material easy to grab when you need it.

### Clone just the lean main branch

```bash
git clone --single-branch --branch main <repo-url> casey-muratori-skills
```

### Clone and check out the talks branch instead

```bash
git clone <repo-url> casey-muratori-skills
cd casey-muratori-skills
git checkout talks
```

### Already cloned? Switch between them

```bash
git fetch origin
git checkout talks   # talk folder appears
git checkout main    # talk folder disappears
```

Git itself manages the folder appearing/disappearing as you switch — nothing is lost, both branches stay in sync with the remote.

## Status

Very early. The talk has been transcribed and summarised; no skills have been written yet. See [`bad_code_comes_from_youtube_talk/talk_summary.md`](./bad_code_comes_from_youtube_talk/talk_summary.md) on the `talks` branch for the current distillation of the talk's salient points.

## License

MIT — see [LICENSE](./LICENSE). Talk content (transcript, captions, summary) on the `talks` branch is derivative of Casey Muratori's lecture and remains his intellectual property; it is included here for study and citation, not redistribution.
