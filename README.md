# hooks-for-your-trade

**Three first lines that make people keep watching, built from what you actually said.** A free Claude skill from Terramore.

- **What you give it:** the words from your video (pasted, or a caption file), and your trade.
- **What you get back:** three opening lines to pick from, a caption each for Instagram, TikTok and YouTube Shorts, and three to five hashtags.
- **What it never does:** post for you, promise views, or make up facts and numbers.

## What it does

Paste what you said in a video, or give it the caption file. It finds the strongest moments: a sign the viewer can spot, a common mistake, or a question customers ask. From those it writes three opening lines, each a different kind, so you have a real choice. Each hook shows the exact phrase it was **built from**, so you can see it came from you. It says which one it would pick and why.

Then it writes one caption per platform from the same words, each ending in one action, and a few hashtags that fit the post (your town only if you give it).

## Requirements

- Claude Code (tested with 2.1.332 on macOS).
- Nothing else to install. No scripts.

## Install

Ask Claude: "Install the hooks-for-your-trade skill from github.com/adam-moreno/hooks-for-your-trade."

Or by hand. **For you, on every project:**

```sh
git clone https://github.com/adam-moreno/hooks-for-your-trade.git
mkdir -p ~/.claude/skills
cp -R hooks-for-your-trade/skills/hooks-for-your-trade ~/.claude/skills/
```

**For one project:** copy `skills/hooks-for-your-trade` into that project's `.claude/skills/` folder.

Start a new Claude Code session afterwards so the skill is picked up.

## Use

Type `/hooks-for-your-trade`, or ask: "give me a hook for this video", "write a caption for my reel", "how should I start this video?". Then paste what you said.

Pairs with **edit-talking-head**: make the first cut, then get hooks for it.

## Example: before and after

Real input and output from `examples/`. Made-up businesses only, never a real client.

- `examples/before/transcript.md`: a made-up plumber (Tidewell Plumbing) on why a water heater pops.
- `examples/after/hooks-and-captions.md`: what the skill gave back in one real run.

The three hooks from that run:

1. "Water heater making a popping sound?" (built from: "If your water heater makes a popping sound")
2. "A lot of people never drain their water heater." (built from: "A lot of people never drain theirs.")
3. "Why's your water heater popping? Usually it's sediment at the bottom of the tank."

It left "Call us" out of the captions because no phone number or website was given, and said so.

## Limitations

- **It writes words; it can't tell you what will get views.** Nothing here is a promise of reach.
- **Only as good as what you said.** If your video has one point, the three hooks will circle that one point.
- **It doesn't watch your video.** It works from the words.
- **Platform rules change.** The one hard limit it uses is YouTube's 100-character title. Check your app if a caption gets cut off.
- **Tested once on one made-up business** (see `TESTED.md`).

## Privacy

No telemetry. Nothing leaves your computer except what Claude Code itself sends to Claude. It writes no files.

## Credits

None: written by Terramore.

## Tests

`python3 -m unittest discover -s tests`

## License

MIT. Made by Terramore (terramore.io). Want the video side done for you? Terramore Studio: terramore.io/studio
