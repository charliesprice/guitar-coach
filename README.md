# guitar-coach

A Claude skill plus a practice app ("Fretwork") for structured guitar learning aimed at songwriting.

- **`SKILL.md`** — the skill: weekly reviews, new-song suggestions from playlists, lesson-transcript ingestion, song cards.
- **`references/`** — practice research, data model, and workflow guides the skill reads.
- **`app/fretwork.html`** — the practice app, published as a private claude.ai artifact with a shared database. It builds a daily plan from the time you have (and from earlier sessions that day), tracks minutes, BPM and cleanliness, and shows the song stage board, skill balance and tempo progress.
- **`inbox/`** — drop lesson transcripts (`inbox/lessons/`) and playlist exports (`inbox/playlists/`) here. Their contents are git-ignored.

## Install the skill

Copy or symlink this folder to `~/.claude/skills/guitar-coach` so Claude Code can use it.

## Update the app

Edit `app/fretwork.html` and republish it to the same artifact URL listed in `SKILL.md`. Your practice data lives in the artifact's database, not in this repo.
