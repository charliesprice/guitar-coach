# Ingesting a lesson transcript

Input: a transcript file in `inbox/lessons/` (any text format; .vtt/.srt fine). Optional screenshots for anything visual (chord shapes, tab on screen).

## Steps
1. Read the whole transcript. Identify the date (filename or ask).
2. Extract, quoting the teacher briefly where it helps:
   - **Assignments** — what to practise before next lesson, with any tempo targets.
   - **Corrections** — technique problems the teacher noticed (these are gold: the user can't see them alone).
   - **New techniques / concepts** — each becomes a drill if it can be practised.
   - **Songs** discussed — map to existing `songs` ids; new ones become suggestions or (if assigned) a song in Learning *after asking*.
   - **Teacher's opinion on stage/readiness** — becomes a suggested stage move, not an applied one.
3. Write `lessons/<date>`.
4. For each affected song/drill: set `lessonNote` (≤ 140 chars, the specific thing to work on) and `lessonUntil` (next lesson date; default +10 days).
5. Create new `drills` for new techniques with concrete `task` text and skill tags.
6. Append any musical ideas worth stealing to the song's `notes` (append-only, marked).
7. Report back: a short summary, what you changed in the app, and suggested stage moves for the user to make.

## Don'ts
- Don't change stages. Don't overwrite notes. Don't invent assignments the teacher didn't give.
