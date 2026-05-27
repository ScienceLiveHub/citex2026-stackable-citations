# Demo script — full author workflow

**Length target:** ~4:30–5:00 · **Recording:** QuickTime Player (macOS-native) or OBS · **Output:** `recordings/demo.mp4` (1080p H.264)

Replaces the earlier meta-only script. Now the demo walks the *full pipeline*: a researcher reads a paper, annotates a citation in Zotero, publishes the resulting nanopublication to the open network, and shows how another paper can reuse it by URI. The narrative answers the audience's "what does this look like for me?" question end-to-end.

The demo plays in **slide 7**. The live voice resumes at slide 8 (Atomicity).

---

## Demo target — annotate while reading

The demo authors **one** CiTO citation nanopub that declares the reader's inferred citation intent for one of Wernberg's *own* references. This is the **third production path** named on slide 5 (Annotate) — distinct from Extract (LLM) and Author (the citing author themselves). Effectively: crowd-sourced citation typing, signed and contestable.

**Paper being annotated**:
Wernberg, T., Bennett, S., Babcock, R.C., et al. (2016). *Climate-driven regime shift of a temperate marine ecosystem.* **Science**, 353(6295), 169–172. DOI `10.1126/science.aad8745`.

**Reference inside Wernberg to be typed**: **Poloczanska et al. (2013)** (Wernberg's ref 11) — *Global imprint of climate change on marine life*. **Nature Climate Change 3, 919–925**. DOI **`10.1038/nclimate1958`**.

Wernberg cites Poloczanska in the body (p.169 right column): *"These processes culminate in novel ecosystems where tropical and temperate species interact, with unknown implications (11, 12)."* That's a textbook `citesAsAuthority` — Poloczanska 2013 is the global meta-analytic authority for climate-driven marine species redistribution, and Wernberg's WA kelp case study sits inside that global pattern.

### Draft CiTO citation fields (nanopub #1)

| Field | Content |
|---|---|
| Citing entity | `https://doi.org/10.1126/science.aad8745` (Wernberg et al. 2016) |
| Cited entity | `https://doi.org/10.1038/nclimate1958` (Poloczanska et al. 2013) |
| Relation | **`citesAsAuthority`** |
| Comment | *"Wernberg cites Poloczanska et al. 2013 as the global authority for the climate-driven redistribution of marine life. Wernberg's WA kelp case study is one regional manifestation of this global pattern, and the Mediterranean Iberian marine systems we plan to investigate next are another."* |

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

## Setup

I opened my Zotero Application on my laptop. I have different collections and before we start, let's check the Science Live plugin and settings.

The ScienceLive Plugin is installed

Now the settings, where I see that my ScienceLive key is setup. This enables me to create Nanopublications with Science Live in Zotero.


### 0:00 — 0:30 · Read the paper, find the reference

**Show:** Zotero open, Wernberg et al. 2016 visible in the library, PDF reader open at page 169 (right column). Highlight or point at the sentence: *"These processes culminate in novel ecosystems where tropical and temperate species interact, with unknown implications (11, 12)."*

**Voice-over:**
> "I'm reading Wernberg et al.'s 2016 paper. It is about a marine heatwave in Western Australia.  While reading, I notice Wernberg cites reference 11 — Poloczanska et al. 2013 in Nature Climate Change — as the global authority for the climate-driven redistribution of marine life. The intent is clear from context: Poloczanska is being used as the global-scale authority that Wernberg's regional case study sits inside."

### 0:30 — 1:30 · Annotate the citation (Citation with CiTO)

**Show:** Open the Science Live Zotero plugin. Select the **Citation with CiTO** template. Fill in:

- **Citing entity**: `https://doi.org/10.1126/science.aad8745` (Wernberg et al. 2016)
- **Cited entity**: `https://doi.org/10.1038/nclimate1958` (Poloczanska et al. 2013, *Global imprint of climate change on marine life*)
- **CiTO relation**: `citesAsAuthority`
- **Comment**: *"Wernberg cites Poloczanska et al. 2013 as the global authority for the climate-driven redistribution of marine life. Wernberg's WA kelp case study is one regional manifestation of this global pattern, and the Mediterranean Iberian marine systems we plan to investigate next are another."*

**Voice-over:**
> "I'm not the author of Wernberg's paper. I'm not the author of Poloczanska's paper. I'm an expert reader, and I'm typing a citation that neither author explicitly declared. The plugin lets me capture my reading: Wernberg cites Poloczanska as the global authority for the climate-driven redistribution of marine life, my inferred CiTO relation is `citesAsAuthority`, and I add a one-sentence comment explaining why. My ORCID signs the assertion. Anyone disagreeing can publish a counter-CiTO. This is the alternative to LLM-extracted citation typing: same downstream nanopub, human reader instead of language model in the loop."

**Pacing note:** Don't rush. The Citing/Cited DOIs should be readable. Pause briefly when selecting `citesAsAuthority` in the dropdown — that's the load-bearing moment.

### 1:30 — 2:00 · Publish

**Show:** Click *Generate Nanopublication*. Plugin signs and pushes to the network. The resulting URI appears in the plugin panel.

**Voice-over:**
> "Click *Generate Nanopublication*. The plugin signs the assertion, signs the provenance graph (timestamp + my ORCID + the inference method), signs the publication info, and pushes the three-graph nanopub to the open network. Decentralised, content-addressable, Trusty URI. About one second."

### 2:00 — 2:45 · Verify on the network

**Show:** Click the resulting URI (or copy → paste into browser). Land on the Science Live viewer. Slowly pan through the three graphs.

**Voice-over:**
> "Here it is on the network. The Assertion graph — Wernberg cites Burrows, relation `citesAsAuthority`. The Provenance graph — *I* authored this inference, my ORCID, timestamp, the method. The Publication info graph — CC-BY 4.0 licence, cryptographic hash. Critically: the Assertion is about Wernberg's citation behaviour; the Provenance says *I* read it that way. Transparently third-party. Anyone can publish a counter-CiTO with a different inferred relation; that's how the network learns."

### 2:45 — 3:30 · Reuse — pre-existing typed citations

**Show:** Switch to the CiteX abstract PDF tab. Scroll to its reference list. Hover over one of the inline CiTO-typed citations. Click into it — lands on another Science Live viewer.

**Voice-over:**
> "And reuse. Our extended abstract for this conference has severak citations like the one I just published — every one a click-resolvable, CiTO-typed nanopub. I know why I am citing this paper and I inform the readers about it. "

### 3:30 — 4:30 · Land the punchline

**Show:** Switch back to the Slidev deck and navigate to slide 4 (the Bombus FORRT chain). Brief pan over the 16 nodes.

**Voice-over:**
> "What I just authored is a single typed citation — the third production path from slide 5: annotation while reading. Now imagine this scaled. Every expert reader who works through a paper can type its citations as they go. Slide 4's Bombus chain is what stackable looks like when this happens systematically: eighteen nanopubs, the pink node on the right is the apex Research Synthesis, one URI that wraps the whole verified replication. The CiTO citations there are signed by the replication's authors — author-validated, top tier of the trust gradient on slide 8. The one I just published is reader-validated — mid-tier of the gradient. Same architecture, different signers, different epistemic weights. Both atomic. Both citable. Both on the open network. Back to Anne."

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
4. Keep it to 90 seconds maximum, then return to slide 8
5. Brief one-line apology afterwards, move on

The live-demo skill is this script's beats 4–5 squeezed to one third of the time. Rehearse this even if the recording is perfect.

---

## After recording

- [ ] Watch the mp4 end-to-end at delivery scale (full-screen, headphones)
- [ ] Trim leading/trailing silence in QuickTime (no other edits — re-shoot before editing splice)
- [ ] Export 1080p H.264, target ~50–80 MB
- [ ] Move to `recordings/demo.mp4`
- [x] Embedded in slide 7 with `<video src="./recordings/demo.mp4" controls />`. Play it via Zoom screen-share window adjacent to slides if the inline embed misbehaves.
- [ ] Test Zoom audio-share with the mp4 (Zoom can be finicky with embedded video audio over screen-share — **test this end-to-end before May 28**)
- [ ] Commit + push; the GitHub Action redeploys the deck with the video baked in
