# Weekly review

Run when the user asks for a review (or weekly if scheduled).

1. Read `config/profile`, `skills`, `songs`, `drills`, and `sessions` from the last 28 days.
2. Compute:
   - Minutes this week vs `dailyGoal × 7`; days practised; average session length.
   - Minutes per skill (7 and 28 days) vs an even share (focus skills ×1.3). Name the most under-fed skill.
   - Per song: minutes this week, BPM change (first vs last `bpmHistory` entry this week), weeks in current stage.
   - Repetition check: share of time on the top 3 songs. Over ~50% → flag it.
   - Learning column size. Under 2 → material warning.
   - Don't flag items that ran past their planned minutes. The user does that on purpose when they want more time on something. Count actual minutes, and mention long stays only as "what you leaned into this week".
3. Write the review as a short report:
   - **The week in one line.**
   - **What moved** (BPM gains, stage moves the user made).
   - **What stalled** (same stage 3+ weeks with flat BPM) and a specific diagnosis — usually transitions (stitching) or no performance-mode runs.
   - **Balance** — skill minutes vs targets.
   - **Suggested stage moves** — with evidence; the user decides.
   - **3 changes for next week** — concrete (a new drill, a lesson flag, a new song from suggestions, a lower/higher BPM target).
4. Ask which changes to apply; then write them via ArtifactData.
