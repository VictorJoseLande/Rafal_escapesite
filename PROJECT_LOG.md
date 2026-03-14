# Project Log: The Legend of Sir Rafal — Escape Site

## Overview

A birthday gift for Rafal's 40th birthday: a 10-level interactive "escape room" webpage themed as a medieval tale of a Polish craftsman-knight journeying north to Norway to seek treasures. Built and deployed on 2026-03-14.

**Live URL:** https://victorjoselande.github.io/Rafal_escapesite/
**Repository:** https://github.com/VictorJoseLande/Rafal_escapesite

---

## Concept

- **Theme:** "A Polish craftsman-knight leaves his homeland and family to journey north to Norway in search of new treasures"
- **Recipient:** Rafal Wojcikiewicz — Maria's partner, turning 40. A Polish man living in Arendal, Norway. Known for talking endlessly ("Podcast"), being incredibly handy, working on ferries, making beautiful furniture, being a fitness machine, cooking amazing (but catastrophically messy) food, watching insect documentaries at midnight, and being a loyal, principled, honest man with a heart of gold.
- **Tone:** Medieval narrator voice with modern humor. The comedy comes from casting Rafal's real-life traits as legendary knight abilities.
- **Gift:** Bungee jumping experience from Telemark Opplevelser (KR 1,590), given by Maria. Gift card message: "Panda er endelig 40 ar — hopp inn i din nye epoke. Elsker deg fra Maria"

---

## Tech Stack

- **Single HTML file** (`index.html`) — no framework, no build step, no dependencies
- **Embedded CSS + JavaScript** — everything self-contained
- **Fonts:** Google Fonts (MedievalSharp for titles, Cinzel for headers, Lora for story text, Inter for UI)
- **Hosting:** GitHub Pages (free, permanent, instant deploy)

### Why this approach?
Same proven approach as the Bianca escape site — maximum speed with a single HTML file and GitHub Pages. Based directly on the Bianca site architecture with a new theme and story.

---

## Story Arc — 10 Levels

| Level | Title | Story Beat | Puzzle Type |
|-------|-------|-----------|-------------|
| 1 | The Craftsman's Calling | A raven brings a scroll summoning Rafal to the Northern Kingdom | Unscramble "NORWAY" |
| 2 | Farewell to the Brotherhood | Saying goodbye to childhood friend Arthur (endless conversation) | Multiple choice (his nickname: The Podcast) |
| 3 | The Craftsman's Arsenal | Packing tools and his entire Garmin collection | Multiple choice (what he does on the ferries) |
| 4 | Crossing the Baltic Sea | Sailing north while watching insect documentaries | Multiple choice (what he watches on YouTube) |
| 5 | The Viking's Test of Strength | A Viking chieftain challenges him — he's terrifyingly fit | Matching puzzle (Garmin gear to purpose) |
| 6 | The Feast of Chaos | Cooking a legendary feast in a catastrophically messy kitchen | Multiple choice (the cooking paradox) |
| 7 | The Language Riddle | Revealing he secretly understood Norwegian all along | Riddle (answer: Norwegian) |
| 8 | The Great Outdoors Trial | Hiking, fishing, camping — fitter than knights half his age | Multiple choice (which is NOT his passion) |
| 9 | The Panda's Heart | The mirror of truth reveals who he really is | Multiple choice (Maria's name for him: Panda) |
| 10 | The Greatest Treasure | The vault opens only once every 40 years | Text input (answer: birthday) |

### Post-Level 10: Two-Stage Finale

1. **Birthday message screen** — heartfelt message with confetti, "PODCAST MODE: FOREVER!", and the reveal that "The greatest treasure is the life you've built, Panda"
2. **Gift card reveal** — "But wait... claim your royal reward!" button leads to the bungee jumping gift card with Maria's personal message

---

## Visual Design

- **Color palette:** Dark brown/black background (medieval stone), warm gold accents, cream text
- **Background:** Floating ember/torch particles instead of stars (medieval atmosphere)
- **Fonts:** MedievalSharp for titles (medieval feel), Cinzel for headers, Lora for story text, Inter for UI
- **Progress bar:** Brown-to-gold gradient bar at the top

### Animations
- **Floating embers** — warm torch-like particles with drift animation
- **Torch glow** — pulsing gold text-shadow on titles
- **Floating emojis** — level icons bob up and down
- **"PODCAST MODE" pulse** — text scales up and down for emphasis
- **Running knight** — `⚔️🏃💨` runs across the screen between levels
- **Correct/wrong feedback** — green pulse for correct, red shake for wrong
- **Confetti** — 60 multicolored pieces rain down on the finale
- **Gift card reveal** — 3D flip animation with golden shimmer border
- **Sparkles** — floating emoji sparkles during gift reveal

---

## Puzzle Types Implemented

1. **Unscramble** — click letters to build a word, with clear/reset
2. **Multiple choice** — 4 options in a grid, visual correct/wrong feedback
3. **Text input** — type answer, accepts multiple valid answers (e.g., "NORWEGIAN", "NORSK", "NORSE")
4. **Matching** — click left item then right item to pair them
5. **Riddle** — riddle text + text input for the answer

---

## Features

### Progress Saving
- Current level saved to `localStorage` on every navigation action
- Refreshing the page resumes at the exact level/page you were on
- "Play Again" button clears saved progress

### Secret Password Fast-Track
- Password field on the title screen (subtle, below the start button)
- Entering `PANDA40` skips directly to the gift card reward page
- Password is only revealed at the bottom of the reward page after completing the quest

### Back Button Navigation
- "Go Back" button appears at the top of every chapter
- Chapter 1 goes back to the title screen
- Going back saves progress so refreshing stays on the current page

### Feedback Fix
- When selecting the correct answer, the response message and the success message are shown stacked (appended), not replacing each other
- Prevents the jarring experience of text being yanked away mid-read

### Gift Card Preview
- Reward page shows a screenshot preview image instead of an embedded PDF
- Price is not revealed on the page — Rafal can download the full PDF himself
- Download button provides the full PDF gift card

---

## Files

| File | Purpose |
|------|---------|
| `index.html` | The entire escape site — HTML, CSS, and JS |
| `giftcard.pdf` | Telemark Opplevelser bungee jumping gift card (the prize) |
| `giftcard-preview.jpeg` | Screenshot preview of the gift card (shown on reward page) |
| `PROJECT_LOG.md` | This file |

---

## Git History

| Commit | Description |
|--------|-------------|
| `deda43d` | Initial build — all 10 levels, medieval theme, animations, puzzles, birthday finale, gift card reveal |
| `4263b81` | Added progress saving (localStorage) and secret password fast-track (PANDA40) |
| `250b2b7` | Fixed success message replacing response mid-read (now appends) |
| `bbd643d` | Added Go Back button to return to previous level |
| `0f1e9fe` | Moved Go Back button to top of level screen, always visible on levels 2+ |
| `ea21e34` | Added Go Back button on chapter 1 (returns to title screen) |
| `d2dd42e` | Fixed progress saving when navigating back so refresh stays on current page |
| `24a7af7` | Replaced PDF iframe with preview image, removed price from page |

---

## Deployment

1. Repository created on GitHub: `VictorJoseLande/Rafal_escapesite`
2. GitHub Pages enabled — source: `main` branch, root folder
3. Site live at: https://victorjoselande.github.io/Rafal_escapesite/
4. Hosting is free and permanent (until repo is deleted or Pages disabled)

---

## Personal Details Woven Into the Story

- "Podcast" — Maria's nickname for Rafal because he never stops talking (recurring theme)
- "Panda" — Maria's loving nickname, revealed as the emotional climax in level 9
- Arthur — childhood best friend from Poland, equally talkative
- Ferry work in Arendal — fixes engines and maintains the ferries (level 3)
- Incredible craftsman — builds his own furniture, referenced throughout
- Garmin obsession — watch, scale, chest strap, macro tracking (level 5)
- Insect YouTube at midnight — watches wildlife/insect docs while Maria sleeps (level 4)
- Fitness machine — bulking/cutting, in better shape than people half his age (levels 5, 8)
- Amazing chef, catastrophic kitchen — the legendary cooking paradox (level 6)
- Secret Norwegian skills — understood more than he let on for years (level 7)
- Outdoor adventurer — hiking, fishing, camping, tent sleeping (level 8)
- Strong principles — honest, says what he thinks, stands by his beliefs (level 9)
- Maria's safety — drives her everywhere, takes her on vacations, provides calm (level 9)
- Turning 40 — the milestone that opens the treasure vault (level 10)
- Polish-Norwegian journey — the overarching narrative from Poland to Arendal

---

## Process

1. Used Bianca's escape site as the architectural reference
2. Read the about_rafal_wojcikiewicz.txt file and the gift card PDF for context
3. Designed a medieval-themed 10-level story arc weaving in Rafal's personality
4. Built the entire site in a single HTML file write
5. Connected to GitHub repo and deployed via GitHub Pages
6. Iteratively added features: progress saving, password, back button, feedback fix, image preview
7. Applied the same improvements back to Bianca's escape site
