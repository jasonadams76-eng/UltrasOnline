# Adding an adventure

1. Copy `TEMPLATE.json` to a new file, e.g. `my_adventure.json`, and fill it in.
2. Add the file name to the list in `index.json`, e.g. `"my_adventure.json"`.
3. Optional chapter pictures go in `/images/` named after the chapter id (e.g. `ma1.jpg`). Cover = first chapter's image.
4. Commit and push. No other changes are needed.

## Rules
- `id` (adventure and chapter): lowercase letters, numbers, underscores only; unique across ALL adventures. Never change an id after players have saves.
- Each chapter needs `id`, `title`, `eyebrow`, `opening`, `gmInstructions`. `imagePrompt` is optional.
- `escalations` is optional: a list of `{"after": N, "text": "..."}`. On the player's Nth turn in that chapter the narrator is told to make that thing visibly happen (a closing hazard, a ticking clock). Use it so a chapter has real pressure even when the player takes a slow, careful approach.
- Adventure-level `facts` (a line or a list of lines, next to `title` and `blurb`) is optional but recommended: story facts that must never change (a headcount, a character's name and look, where the safe place is). The narrator is reminded of them on every turn, even in a long chapter.
- `notYet` is optional but strongly recommended: a line (or lines) naming story beats that belong to LATER chapters and must not be played out in this one (for example "the missing train is not found here", or a fixed headcount). The game also automatically tells the narrator the titles of all later chapters so it does not jump ahead.
- `opening` and `gmInstructions` are arrays of lines (or one string). Empty string = blank line.
- Chapters play in the order listed. Each `gmInstructions` should end the chapter via the game's standard completion marker rules (the global GM rules already handle this).
- A file with a mistake is skipped and the others still load; the admin account sees a notice on the adventure screen.

## Knockouts (all adventures)
When the hero is beaten (Health 0), ORACLE pulls him out, he wakes at half Health, a Public Defeat Karma penalty is recorded, and the SAME chapter carries on. This is built into the game, so it applies to every adventure, including new ones. A chapter never ends because the hero lost a fight, so write each chapter's `gmInstructions` and `notYet` so that the chapter's goal can still be reached after a rescue.
