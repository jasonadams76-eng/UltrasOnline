# Adding an adventure

1. Copy `TEMPLATE.json` to a new file, e.g. `my_adventure.json`, and fill it in.
2. Add the file name to the list in `index.json`, e.g. `"my_adventure.json"`.
3. Optional chapter pictures go in `/images/` named after the chapter id (e.g. `ma1.jpg`). Cover = first chapter's image.
4. Commit and push. No other changes are needed.

## Rules
- `id` (adventure and chapter): lowercase letters, numbers, underscores only; unique across ALL adventures. Never change an id after players have saves.
- Each chapter needs `id`, `title`, `eyebrow`, `opening`, `gmInstructions`. `imagePrompt` is optional.
- `opening` and `gmInstructions` are arrays of lines (or one string). Empty string = blank line.
- Chapters play in the order listed. Each `gmInstructions` should end the chapter via the game's standard completion marker rules (the global GM rules already handle this).
- A file with a mistake is skipped and the others still load; the admin account sees a notice on the adventure screen.
