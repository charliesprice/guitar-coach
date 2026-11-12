# Finding new material

Goal: the user always has songs they like, at the right level, that train their weak skills.

## Inputs
- Playlist exports in `inbox/playlists/` (Exportify CSV for Spotify, or a pasted list).
- Songs the user or teacher names.
- Current board (`songs`) and past `suggestions` (skip anything added or dismissed).

## Rating a song
For each candidate, judge from what you actually know about the guitar part (say "unsure" rather than guessing):
- **Guitar role** — is there a learnable guitar part? (Skip songs that are mostly synth/piano unless the user wants an arrangement.)
- **Skills** it trains, using skill ids from the `skills` collection.
- **Tier** relative to the current board:
  - `ready` — comparable to songs now in Stitching/Up to tempo.
  - `step` — one clear new demand (faster tempo, new technique, alternate tuning, barre-heavy).
  - `reach` — several new demands; a 1–3 month project.
- **Ideas worth stealing** — the voicing, riff shape, rhythm feel or progression that would feed their songwriting.
- **Verify** — tuning, capo, or arrangement details you're unsure of.

## Picking which to write
- Weight toward the least-practised skills (from the last 28 days of sessions) and the focus skills: rhythm, ear, melody + chords.
- Mix tiers: roughly 3 ready, 3 step, 2 reach per batch.
- For ear training, flag songs simple enough to work out by ear first (riff-based, few chords) and say so in `why`.
- Max ~8 new suggestions per run; quality over volume.

## TrueFire
If a weak skill needs structured instruction rather than a song, recommend a TrueFire course *from `references/resources.md`'s catalog* (don't invent course names). If the catalog is empty, suggest the user search TrueFire for the skill and add what they like to the catalog.
