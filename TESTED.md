# What was tested

2026-11-25, version 0.1.0.

**Tested**

- **Claude Code CLI 2.1.332, macOS 15.3.1, project install, from a FRESH CLONE of this repository.** The skill folder was copied into a new, empty project's `.claude/skills/`, with only project settings loaded (`--setting-sources project`) and only the Read tool allowed. Invoked headless as `/hooks-for-your-trade` with `examples/before/transcript.md` (a made-up plumber).
  - It gave three hooks of three different kinds, each with the phrase it was built from, plus a pick, three captions and four hashtags.
  - It added no numbers. It left out a "call us" ending because no phone number was given, and said so.
  - The output is `examples/after/hooks-and-captions.md`, unedited.
- **Unit tests** (`python3 -m unittest discover -s tests`): 11 pass, from the fresh clone. The invented-proof check fails on a known-bad line ("Rated 5 stars by 200 owners").

**Not tested**

- Input as a `.srt` or `.vtt` caption file (only pasted text was run).
- A personal install in `~/.claude/skills/` (same mechanism as the project install, but not run).
- The Claude Code desktop app, web app and IDE extensions; the Claude apps' skill upload; the Agent SDK.
- Windows and Linux.
- Other businesses and trades, and more than one run. One run on one made-up business is not evidence that every output will be this good. Read what it gives you.
- Whether its output gets more views or customers. Nothing here measures that.
