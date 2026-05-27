# Demo script — full author workflow

**Length target:** ~4:30–5:00 · **Recording:** QuickTime Player (macOS-native) or OBS · **Output:** `recordings/demo.mp4` (1080p H.264)

Replaces the earlier meta-only script. Now the demo walks the *full pipeline*: a researcher reads a paper, annotates a citation in Zotero, publishes the resulting nanopublication to the open network, and shows how another paper can reuse it by URI. The narrative answers the audience's "what does this look like for me?" question end-to-end.

The demo plays in **slide 9**. The live voice resumes at slide 10 (Atomicity).

---

## Demo paper

**Wernberg, T., Bennett, S., Babcock, R.C., et al. (2016).** *Climate-driven regime shift of a temperate marine ecosystem.* **Science**, 353(6295), 169–172. DOI `10.1126/science.aad8745`.

**Template**: **Comment on Paper** (paper-level commentary + a CiTO relation dropdown — *not* Quote-with-comment, which has no CiTO field)

**Intent**: `cito:citesAsPotentialSolution` — Wernberg's mechanism offers a candidate solution to the question of what marine-biodiversity regime shifts may occur in **Mediterranean Iberian marine systems** under projected SSP3-7.0 ocean warming. The resulting nanopub becomes the first reading-trace of a future FORRT replication chain.

**Draft Comment**:
> *"Wernberg et al.'s 2011 Ningaloo-Niño event offers a candidate mechanism (extreme marine heatwaves → kelp range contraction + community-wide tropicalization) for what may happen in Mediterranean Iberian marine systems under DestinE Climate DT SSP3-7.0 projections. Open question: does the same tropicalization signature emerge in a warmer baseline ocean basin, or does the higher thermal floor mute the regime-shift threshold?"*

**CiTO relation**: `citesAsPotentialSolution`

---

## Pre-recording setup

- [ ] **Zotero** — Wernberg et al. 2016 open in the library, PDF viewer pane visible
- [ ] **Zotero plugin** — logged in, ORCID linked, tested today, ready to publish to the network
- [ ] **Browser** — fresh window, no extensions visible, two tabs prepared:
  - Tab 1: Science Live viewer base (`platform.sciencelive4all.org`)
  - Tab 2: CiteX 2026 abstract PDF on the Zenodo community
- [ ] **Browser zoom** — 110–125% so text reads at 1080p capture
- [ ] **Mic** — built-in MacBook mic is fine; do a 10-sec test recording first
- [ ] **Quiet room** — phone silenced, DND on, no notifications visible
- [ ] **QuickTime** — `Cmd-Space → QuickTime Player → File → New Screen Recording`. Click the arrow next to the record button to select microphone (built-in or external) and ensure system audio is OFF unless you specifically need it. Click *Record Entire Screen* or drag-select the area
- [ ] **One full dry-run** of the click path with no recording, to confirm all clicks land

## Recording target

A clean ~4:30–5:00 take. **Re-shoot rather than edit.** Don't try to splice clips — go from the top until one take is clean. Trim leading/trailing silence with QuickTime's `Edit → Trim` after.

---

## Beat sheet (with timing)

### 0:00 — 0:30 · Read the paper

**Show:** Zotero open, Wernberg et al. 2016 visible in the library, PDF reader open at the abstract or page 1.

**Voice-over:**
> "I'm reading Wernberg et al.'s 2016 paper in Science — a regime-shift in Western Australian kelp forests after the 2011 marine heatwave. I'm reading it because we plan to test whether this regime-shift mechanism reproduces in the Mediterranean Iberian marine systems under SSP3-7.0. Normal Zotero workflow — paper's in my library, PDF open."

### 0:30 — 1:30 · Annotate the citation (Comment on Paper)

**Show:** Open the Science Live Zotero plugin. Select the **Comment on Paper** template (not Quote-with-comment — that one has no CiTO field). The paper identifier auto-populates from the Zotero record (DOI 10.1126/science.aad8745).

Type the personal comment into the plugin's *Comment* field:

> *"Wernberg et al.'s 2011 Ningaloo-Niño event offers a candidate mechanism (extreme marine heatwaves → kelp range contraction + community-wide tropicalization) for what may happen in Mediterranean Iberian marine systems under DestinE Climate DT SSP3-7.0 projections. Open question: does the same tropicalization signature emerge in a warmer baseline ocean basin, or does the higher thermal floor mute the regime-shift threshold?"*

Select **`citesAsPotentialSolution`** from the CiTO relation dropdown.

**Voice-over:**
> "Here's the Science Live plugin. I'm using the *Comment on Paper* template — it lets me write a paper-level commentary in my own words, on *why* I'm citing this work and what I plan to test next. And I pick the CiTO relation — `citesAsPotentialSolution` — declaring that Wernberg's mechanism is a candidate solution to the marine-biodiversity question I'm investigating. The intent is declared at write time, from the source that knows best. No retrospective inference needed."

**Pacing note:** Don't rush. This beat is the heart of the demo. The Comment field should be visible long enough for the audience to read it, and the CiTO dropdown selection should be deliberate and clear.

### 1:30 — 2:00 · Publish

**Show:** Click *Generate Nanopublication* (or equivalent button in the plugin). Plugin signs and pushes to the network. The resulting URI appears in the plugin panel.

**Voice-over:**
> "Click *Generate Nanopublication*. The plugin signs the assertion, signs the provenance graph, signs the publication info, and pushes the three-graph nanopub to the open network. Decentralised, content-addressable, Trusty URI. About one second."

### 2:00 — 2:45 · Verify on the network

**Show:** Click the resulting URI (or copy → paste into browser). Land on the Science Live viewer for the just-published nanopub. Slowly pan through the three graphs: Assertion, Provenance, Publication info.

**Voice-over:**
> "Here it is on the network. The Assertion graph — what I just claimed, my quote and CiTO type, linked to Wikidata. The Provenance graph — who I am (ORCID), when, with what method. The Publication info graph — the licence, the timestamp, the cryptographic hash. Anyone can now cite this URI as a typed, machine-readable reference. Including future papers that build on, dispute, or extend it."

### 2:45 — 3:30 · Reuse

**Show:** Switch to the CiteX abstract PDF tab. Scroll to the reference list. Hover over one of the inline CiTO-typed citations. Click into it — lands on another Science Live viewer.

**Voice-over:**
> "And here's reuse. This is our extended abstract for *this* talk. Every citation in the reference list has the same shape as what I just published — a CiTO type, a click-resolvable URI on the network. Twenty-one nanopubs from this paper alone. Each one independently citable by future work. That's stackable."

### 3:30 — 4:30 · Land the punchline

**Show:** Switch back to the Slidev deck and navigate to slide 4 (the Bombus FORRT chain). Brief pan over the 16 nodes.

**Voice-over:**
> "What I just authored — a Comment-on-Paper with `citesAsPotentialSolution` — is the reading-trace at the top of a future chain. Slide 4's Bombus chain started with its own paper-rooted nanopub: a Quote-with-comment on Soroye 2020. Different templates, same architecture: paper → typed citation → claim → study → outcome → CiTO. When this Wernberg chain runs to completion, it'll look like this — eighteen nanopubs, the pink node on the right is the apex Research Synthesis, one URI that wraps the whole verified replication. Back to Anne."

(Stop recording.)

---

## Fallbacks

### Zotero plugin glitches mid-recording

1. Calmly say nothing, stop recording, re-shoot from the top
2. If glitching persists: skip beats 1–3 entirely, jump straight to the meta-demo of pre-published nanopubs (beats 4–5 of *this* script with the substrate-sensitivity `RAumfa30…` URI as the worked example)

### Science Live viewer fails to load a URI

All 12 demo-path URIs confirmed 200 OK from Science Live's resolver as of pre-recording smoke test. If one fails during recording, the others remain — swap to a different URI from the abstract bibliography (the 9 in `qa-prep.md` "URI verification checklist") and continue.

### KP outage during recording

Science Live's `/np/?uri=…` viewer serves from its own DB, independent of KP. If KP is down, the demo still works.

## Live-demo backup (if the embedded mp4 fails to play during delivery)

If the recording fails to play during the talk (Zoom audio-share refuses, file corrupt, network glitch):

1. Pause — say "let me show you live" — don't apologise extensively
2. Switch to browser, open the substrate-sensitivity CiTO `RAumfa30…` directly
3. Walk through *one* nanopub: assertion → provenance → publication info
4. Keep it to 90 seconds maximum, then return to slide 10
5. Brief one-line apology afterwards, move on

The live-demo skill is this script's beats 4–5 squeezed to one third of the time. Rehearse this even if the recording is perfect.

---

## After recording

- [ ] Watch the mp4 end-to-end at delivery scale (full-screen, headphones)
- [ ] Trim leading/trailing silence in QuickTime (no other edits — re-shoot before editing splice)
- [ ] Export 1080p H.264, target ~50–80 MB
- [ ] Move to `recordings/demo.mp4`
- [ ] Add to slide 9: replace the `[ Demo ]` placeholder with `<video src="./recordings/demo.mp4" controls autoplay class="mx-auto" style="max-height: 480px;" />` (or play it via Zoom screen-share window adjacent to slides — simpler if embed misbehaves)
- [ ] Test Zoom audio-share with the mp4 (Zoom can be finicky with embedded video audio over screen-share — **test this end-to-end before May 28**)
- [ ] Commit + push; the GitHub Action redeploys the deck with the video baked in
