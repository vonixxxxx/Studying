# Obsidian Vault Starter — STEM / Curriculum Edition

This is a ready-to-open Obsidian vault skeleton built for the note-taking stack recommended in `curriculum-scratch-to-expert.md`: Obsidian as the commonplace book, LaTeX for math, Excalidraw for sketching, Zotero for papers, and Anki for spaced repetition. It ships as folders and templates only — no personal notes, no plugin binaries — so it's safe to keep in a shared repo and drop straight into your own Obsidian.

**Important:** Obsidian is a local desktop/mobile app; nothing in this remote session can install it on your machine. What's here is the vault structure and templates — you do the one-time setup below yourself, in your own Obsidian, on your own computer (5-10 minutes now — see "What's already pre-configured" below for why it's shorter than it used to be).

## 0. Install Obsidian and open this vault

1. Download Obsidian free from **obsidian.md** (Mac/Windows/Linux/iOS/Android).
2. On first launch, choose **"Open folder as vault"** and select this `obsidian-vault-starter` folder (or wherever you've unzipped/cloned it).
3. That's it — you now have a working vault with the folder structure below, and (see next section) most of the configuration already done.

## What's already pre-configured, and the one thing that deliberately isn't

I went as far as this sandbox honestly allows, and stopped at a real boundary rather than fake the rest. Here's exactly what that means:

**Already done for you, in this vault:**
- `.obsidian/app.json` — new notes default to `00-Inbox`, attachments default to `Attachments`, wikilinks are on.
- `.obsidian/community-plugins.json` — Templater, Excalidraw, LaTeX Suite, Dataview, Zotero Integration, and Obsidian Git are pre-listed as enabled, so the moment you install each one below, it's already switched on — no extra toggle.
- `.obsidian/plugins/templater-obsidian/data.json` — Templater is pre-configured to point at the `Templates` folder *and* to auto-apply the right template by folder (a new note in `02-Math` already opens as a Concept Note, `06-Papers` as a Paper Note, `07-Projects` as a Project Log, etc. — no manual "create from template" step per note).
- Two fully filled example notes are already in the vault so you can see the system working before you write anything yourself: `02-Math/Example - Eigenvectors.md` (a complete Concept Note, Anki blocks included) and `01-Commonplace-Book/Example Daily Note.md` (a complete Daily Note).

**What I deliberately did not do, and why:** I tried to fetch and pre-install the actual plugin code so you'd never need to touch the Community Plugins browser at all. That failed for a good reason, not a lazy one: this sandbox's GitHub access is scoped to your own repo, so it can't reach third-party plugin authors' release binaries — and honestly, even if it could, downloading and running someone else's compiled JavaScript from outside Obsidian's own verified plugin channel is a worse security posture than the alternative. The one-click **Install** button in Obsidian's Community Plugins browser is exactly that verified channel. So that one step — clicking Install on 5-6 plugins — is the one piece of this setup that stays manual, on purpose, and it takes about 60 seconds per plugin.

## Folder structure

| Folder | What goes here |
|---|---|
| `00-Inbox` | Quick capture — anything you haven't filed yet. Set this as your default "new note" location (Settings → Files & Links → Default location for new notes). |
| `01-Commonplace-Book` | Your running Track-0 journal: questions, half-formed connections, things that surprised you. This is the folder you re-read monthly. |
| `02-Math`, `03-Physics`, `04-CS-and-AI`, `05-Robotics-and-Infra` | One folder per subject area from the curriculum stages — use the **Concept Note** and **Theorem Note** templates inside each. |
| `06-Papers` | One note per paper you read, using the **Paper Note** template — this is your literature-note layer, feeds from Zotero. |
| `07-Projects` | One note per hands-on project (Stage 6 robots, OSS contributions, hackathon builds), using the **Project Log** template. |
| `08-Handwritten-Scans` | Where scanned/exported handwritten pages land (from GoodNotes, reMarkable, or a photo of paper) before being embedded into the relevant concept/theorem note. |
| `Attachments` | Images, diagrams, PDFs. |
| `Templates` | The six templates below. |

## 1. Turn on Community Plugins, then install Templater (30 seconds)

1. Settings → Community plugins → **Turn on community plugins** (Obsidian shows a safety warning the first time — this is normal, it's the same warning for every vault).
2. Browse → search **"Templater"** → Install → Enable. Because of the pre-filled config above, it's already pointed at the `Templates` folder and already wired to auto-apply the right template per folder — nothing left to configure.
3. Test it: create a new note inside `02-Math` — it should open already formatted as a Concept Note. If you'd rather trigger a template manually instead (e.g. for Daily Note or Weekly Review, which aren't tied to a single folder), use the command palette (`Ctrl/Cmd+P`) → **"Templater: Create new note from template"**.
4. Optional: bind a hotkey to your most-used templates in Settings → Hotkeys.

## 2. Install the rest of the plugin stack (about a minute each)

All via Settings → Community plugins → Browse → search the name → Install → Enable:

| Plugin | Why | Setup note |
|---|---|---|
| **Excalidraw** | Sketching/diagrams embedded directly in notes — this is your Track-0 "sketch it" habit. Draw the picture, save, it embeds inline. | Nothing extra needed. |
| **LaTeX Suite** | Snippet expansion for math — type shortcuts (e.g. `dm` → display math block, `//` → fraction) instead of typing raw LaTeX every time. The single biggest speed-up for STEM note-taking in Obsidian. | Turn on the default snippet set in its settings; math itself renders via Obsidian's built-in MathJax, no separate plugin needed for that part. |
| **Dataview** | Query your vault like a database — e.g. list every paper tagged `to-read`, or every concept note still `status: seed`. | Optional at first; adopt once you have 30+ notes and want to query them. |
| **Zotero Integration** | Pulls a paper's metadata (and PDF annotations) from your Zotero library straight into a new note. | Requires **Zotero** desktop (free, zotero.org) installed and running, plus its **Better BibTeX** add-on. Point the plugin at your Zotero library in its settings, then create Paper Notes with it instead of typing metadata by hand. |
| **Obsidian_to_Anki** | Turns the `START ... END` flashcard blocks already in the Concept/Theorem templates into real cards in real Anki decks. | Requires **Anki** desktop (free, apps.ankiweb.net) installed, plus the **AnkiConnect** add-on inside Anki (Tools → Add-ons → Get Add-ons → code `2055492159`). Run the command **"Obsidian_to_Anki: Scan Notes"** whenever you want to sync. |
| **Obsidian Git** (optional) | Auto-commits/pushes your vault to a git remote for backup and version history. | **Use a separate private repo for your actual notes** — don't point this at the public `Studying` repo, since your real commonplace book will contain a lot of personal in-progress thinking you don't want public. |
| **reMarkable Sync** or **Scrybble** (optional, only if you own a reMarkable tablet) | Pulls your handwritten pages in automatically as images into `08-Handwritten-Scans`. | Connect it to your reMarkable Cloud account in its settings. If you don't have a reMarkable, skip this — see the manual workflow below. |

## 3. The handwritten-notes workflow

Obsidian is a text tool, not an inking app — the actual math/derivation-by-hand work happens in GoodNotes (iPad) or on a reMarkable, and then flows *into* Obsidian as an embed:

1. **Write by hand** in GoodNotes or on your reMarkable, same as always.
2. **Export the page** as a PDF or PNG:
   - GoodNotes: Share → Export → PDF/Image, save to a synced folder (iCloud Drive/Dropbox) that also syncs to wherever this vault lives, or AirDrop it in.
   - reMarkable: either the auto-sync plugin above, or manually email/export the page as PDF from the reMarkable app.
3. **Drop the file into `08-Handwritten-Scans`.**
4. **Embed it** in the relevant Concept or Theorem note using `![[filename.pdf]]` (or `.png`) in the "Handwritten work" section already present in both templates.
5. **Always write one typed sentence above the embed summarizing what's on the page.** This is the single fix for the fact that handwriting isn't searchable text — the typed sentence is what Dataview/search will actually find later.

## 4. Daily habit checklist (ties directly back to Track 0)

- [ ] Create/open today's **Daily Note**, fill in all five sections.
- [ ] For any genuinely new idea today, make a **Concept Note** or **Theorem Note**, do the Feynman explanation, and add the Anki block.
- [ ] Read one thing from the Inventor's Library or a technical source; log it in the Daily Note.
- [ ] Once a week: fill in **Weekly Review**, actually publish the post draft somewhere public.
- [ ] Once a month: re-read the whole `01-Commonplace-Book` folder start to finish, looking for old entries that now connect to something new.

## A note on privacy

This starter — folders and templates, no content — is fine to keep in the shared `Studying` repo. Once you start filling it with your real notes, move the vault (or point Obsidian Git) at a **separate private repo**, iCloud, or Obsidian Sync instead. A commonplace book is supposed to contain half-formed, embarrassing, wrong-turn thinking — that's what makes it useful later — and that's exactly the content you don't want sitting in a repo other people can read.
