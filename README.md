# Tool Sensei 🥷

A Claude Code skill that acts as your creative studio concierge.

**Describe what you want to make → it scans your installed skills and tells you exactly which one to use.**

Works for any setup. No assumptions. No hardcoded tool lists.

---

## What it does

On invoke, Tool Sensei scans your `~/.claude/skills/` folder to see what you actually have installed. Then you describe what you want to make — it picks the best match from *your* skills, not a generic list.

You say: *"I want to make a product reel"*  
Tool Sensei checks your skills → says: **Use → /launch-film** · invoke it with `/launch-film` · beat-synced brand reel, zero cost.

You say: *"I want to study this competitor reel"*  
Tool Sensei checks your skills → says: **Use → rea-video** · then chain with ReelMimic if you have it.

It routes from reality, not assumptions.

---

## Install

1. Copy `SKILL.md` into your Claude Code skills folder:

**Mac / Linux:**
```bash
mkdir -p ~/.claude/skills/tool-sensei
cp SKILL.md ~/.claude/skills/tool-sensei/SKILL.md
```

**Windows:**
```powershell
New-Item -ItemType Directory -Path "$env:USERPROFILE\.claude\skills\tool-sensei" -Force
Copy-Item SKILL.md "$env:USERPROFILE\.claude\skills\tool-sensei\SKILL.md"
```

2. Restart Claude Code (or reload skills).

3. Invoke with:
```
/tool-sensei
```

---

## Usage

Just describe the job:

> "I want to make a product launch reel with voiceover"  
> "I want to turn this PDF into a video lesson"  
> "I want to record a walkthrough of my app"  
> "I want captions synced word by word"

Tool Sensei scans your installed skills automatically, picks the best fit, and suggests combos when two skills together beat one.

If nothing you have covers the job, it says so and recommends what to install — free options first.

---

## Rules it follows

- Scans your actual installed skills first — never assumes
- Never suggests paid if free covers it
- Never suggests installing something new if something you have already fits
- Max 5 lines per answer
- Suggests combos when two skills together are better than one

---

## Also by maisonlumiere

- [launch-film](https://github.com/maisonlumiere/launch-film) — turn brand photos into a beat-synced launch reel, zero cost

---

MIT License
