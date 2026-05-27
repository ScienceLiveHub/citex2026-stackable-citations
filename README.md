# Stackable Citation Knowledge — CiteX 2026 talk

Slidev deck + pre-recorded demo for the talk *"Stackable Citation Knowledge:
Building on Nanopublications for Climate and Biodiversity Research"* by Anne
Fouilloux (LifeWatch ERIC) and Jean Iaquinta (Vitenhub AS), given remotely at
**CiteX 2026** (Frankfurt, 28 May 2026, 16:10 CET).

The extended abstract (camera-ready) is on the CiteX 2026 Zenodo community.

## Live preview

```bash
npm install
npm run dev
```

Opens at `http://localhost:3030`.

## Build static site

```bash
npm run build         # output in dist/
npm run export-pdf    # PDF fallback for offline delivery
```

## Files

| Path | Purpose |
|---|---|
| `slides.md` | Slidev source — 9 slides (one is a demo cue), with speaker notes |
| `demo-script.md` | Click-by-click script for the ~4-5 min pre-recorded demo segment |
| `qa-prep.md` | Anticipated Q&A from the programme committee + one-line answer cards |
| `recordings/demo.mp4` | Final demo recording (committed at v0.1.0) |
| `CITATION.cff` | Citation metadata — gets a Zenodo concept DOI at first release |
| `LICENSE` | MIT |

## Format

- Live slides (~17–18 min)
- Pre-recorded demo segment (~5 min) embedded at slide 7
- Live Q&A (~8 min)
- Total slot: 30 min

## Pre-talk checklist

- [ ] All 21 nanopubs in the extended abstract resolve via `platform.sciencelive4all.org/np/?uri=…`
- [ ] Demo recording shot, edited (re-shoot rather than edit), exported as 1080p mp4
- [ ] Slide deck dry-run with timing — under 18 min for the live portion
- [ ] Jean reviewed deck + demo (May 27)
- [ ] PDF export saved locally as offline fallback
- [ ] Zoom screen-share rehearsed with the demo recording (audio + video share)
- [ ] v0.1.0 GitHub release tagged → Zenodo concept DOI minted → updated in CITATION.cff

## After the talk

- Push the recording to Zenodo as a separate citable artifact
- Mirror to YouTube (Science Live channel) for discoverability
- Add the Zenodo DOI to the platform's `/about` page
- Decide whether to write a post-workshop follow-up paper (Special Issue possible if indicated to Tamara after the talk)
