# Demo script — meta-demonstration

**Length target:** 4–5 min · **Recording:** OBS Studio or QuickTime · **Output:** `recordings/demo.mp4` (1080p)

This script drives the pre-recorded demo segment embedded in slide 9. The audience has just seen slide 8 ("This paper *is* 21 nanopubs") and is primed for proof. The recording's job: show that every citation in the extended abstract resolves to a live, signed, click-through nanopub on Science Live.

**No live narration over the recording at delivery time** — voice-over baked into the mp4. Anne's live voice resumes at slide 10 (Atomicity / Trust gradient).

---

## Pre-recording setup

- [ ] Browser: fresh window, no extensions visible, tabs closed except the ones used in the demo
- [ ] Browser zoom: 110-125% so text reads clearly in 1080p capture
- [ ] Logged-out of Science Live (audience sees the public read-only view)
- [ ] Network: confirm `platform.sciencelive4all.org` resolves and is fast
- [ ] All 21 nanopub URIs verified resolvable beforehand (see `qa-prep.md` URI verification checklist)
- [ ] OBS: 1080p, 30fps, single-monitor screen capture, mic level checked
- [ ] Quiet room, do-not-disturb on, phone silenced

## Recording target

A clean ~4-minute take. **Re-shoot rather than edit.** Do not stitch multiple clips — keep going from the top until one take is good. Edit only to trim silence at the start/end.

---

## Beat sheet (with timing)

### 0:00 — 0:20 · Open the extended abstract

**Show:** Browser tab open to the Zenodo community page for CiteX 2026, abstract "Stackable Citation Knowledge…" by Fouilloux & Iaquinta.

**Voice-over:**
> "This is our extended abstract on the CiteX 2026 Zenodo community. Standard PDF, looks like any other workshop paper. But look at the references."

Scroll to the references section. Pause briefly.

### 0:20 — 0:50 · Reveal: every citation is a clickable nanopub

**Show:** Cursor hover over the first reference (Fouilloux 2025) — the inline `[citesAsDataSource]` label is highlighted next to the Zenodo URL.

**Voice-over:**
> "Each reference carries an inline CiTO type — `citesAsDataSource`, `citesAsAuthority`, `usesMethodIn` — and a link in the bibliography to the corresponding nanopublication on the open network. The CiTO type isn't decorative metadata. Watch."

### 0:50 — 1:45 · Click into Groth 2010 [citesAsAuthority]

**Show:** Click the nanopub URI under Groth 2010 (`w3id.org/np/RA4h2w5UImaqgF84fPfqy_lkjhgXZCAIae3Onh9_6G83o`). Lands on `platform.sciencelive4all.org/np/?uri=…` viewer.

**Voice-over:**
> "This is a signed nanopublication. Three named graphs: the Assertion — that we cite Groth 2010 as the foundational definition of nanopublication structure. The Provenance — when we made the claim, with which method. And the Publication Info — our ORCIDs, the timestamp, the CC-BY licence. The Trusty URI in the address bar contains a hash of the assertion. It is content-addressable. We cannot quietly rewrite this claim after the fact."

Pan slowly through the three graphs in the viewer. ~30 seconds on this page.

### 1:45 — 2:30 · Show a different CiTO type: Kuhn 2021 [usesMethodIn]

**Show:** Browser back. Click the Kuhn 2021 nanopub link (`w3id.org/np/RAgBSZ6agwJr9eWvxRTZQqo_dfa1Xmvx3i1-t5t8hxpQ4`).

**Voice-over:**
> "Same paper, different citation. Where Groth was an *authority* citation — we depend on the concept — Kuhn is a *usesMethodIn*: we actively use their Trusty URI scheme and decentralised network. Two different relationships, two different nanopubs, two different URIs. A future paper can cite either one specifically — not just 'Fouilloux cites Kuhn.'"

### 2:30 — 3:15 · Show the Wikidata concept link

**Show:** From the Kuhn 2021 page, click through to a Wikidata Q-ID linked in the assertion (e.g. `wd:Q22683756` for "nanopublication" if exposed; if not, fall back to a Q-ID from a different nanopub).

**Voice-over:**
> "Concepts in the assertion link to Wikidata Q-IDs — so the same machinery that Scholia and the Open Citations community already query can index these claims directly. We don't ask the CiteX community to adopt new vocabulary. We ride on CiTO, FaBiO, PROV-O, Wikidata — the stack that already exists."

### 3:15 — 4:00 · Step back to the abstract; close

**Show:** Browser back to the extended abstract references section. Scroll quickly past the remaining citations.

**Voice-over:**
> "Twenty-one nanopubs in total for this paper: seven AIDA cited claims, six CiTO citation relations, eight Wikidata concept definitions. Each one signed. Each one click-resolvable. Each one citable individually by future work. This is what stackable citation knowledge looks like once it exists on the network. Back to Anne."

(Stop recording.)

---

## Fallback if a URI doesn't resolve during recording

KP outages can take down nanopub-network endpoints intermittently. If any URI fails during a recording session:

1. **First**: try `platform.sciencelive4all.org/np/?uri=<URI>` directly — Science Live serves from its own DB and is independent of KP availability
2. **Second**: pick a different URI from the references — all 21 are independently resolvable; you don't need to demo all six CiTO types, two-or-three different ones is enough
3. **Last resort**: record a still-image walkthrough using screenshots captured during a known-good window — same voice-over, slower pacing on each frame

## Live-demo fallback (if the recording itself fails to play during delivery)

If the embedded mp4 fails to play during the talk (Zoom audio share refuses, file corrupt, network glitch on remote-shared content):

1. Pause, say "let me show you live" — do not apologise extensively
2. Switch to browser, open `platform.sciencelive4all.org`
3. Show **one** nanopub — the Groth 2010 [citesAsAuthority] one is the cleanest visual
4. Keep it to 90 seconds maximum, then return to slide 10
5. Apologise once afterwards, briefly, and move on

The live-demo skill is the recording's content squeezed to one third of the time. Rehearse this once before May 28 even if the recording is perfect.

---

## After recording

- [ ] Watch the mp4 end-to-end at delivery scale
- [ ] Trim silence with QuickTime (no other edits)
- [ ] Export 1080p H.264, target ~50 MB
- [ ] Move to `recordings/demo.mp4`
- [ ] Test embedding in Slidev: edit slide 9 to add `<video src="./recordings/demo.mp4" controls />` (or play it via Zoom screen-share window adjacent to slides — simpler)
- [ ] Test Zoom audio-share with the mp4 (Zoom can be finicky with embedded video audio over screen-share — *test this end-to-end before May 28*)
