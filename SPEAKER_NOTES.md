# Speaker Notes — CiteX 2026

**Stackable Citation Knowledge: Building on Nanopublications for Climate and Biodiversity Research**

Anne Fouilloux (LifeWatch ERIC, Spain) · Jean Iaquinta (Vitenhub AS, Norway)

CiteX 2026 · Frankfurt · 28 May 2026 · *remote*

---

**Total time budget:** 30 min
- ~14 min live slides (9 slides)
- ~5 min pre-recorded demo (embedded at slide 7; Wernberg → Poloczanska 2013 annotation, citesAsAuthority)
- ~10 min live Q&A and discussion

**Delivery format:** live slides via Zoom screen-share. Demo segment plays from a pre-recorded mp4 embedded at slide 7. Live Q&A retains room presence.

**Pre-talk checklist:** see README.md. **Demo:** demo-script.md. **Q&A:** qa-prep.md.

---

## Slide 1 · Stackable Citation Knowledge

Opening line (≈20 s):
"Hi everyone. I'm Anne Fouilloux,
joining remotely from LifeWatch ERIC in Spain. This is joint work with
Jean Iaquinta at Vitenhub. We want to argue that citation extraction is
only half of what open citations need — the other half is making the
extracted thing addressable and stackable. We'll show what that means
with a worked example you can click into during this talk."

## Slide 2 · Citation data has two jobs

Beat (~2 min):
- On the left: "you've all seen this. A 4-line reference list entry. Excellent for credit, opaque for building-upon."
- On the right: "this is the same citation in our stackable form. The URI in the middle is a click-resolvable signed nanopub. The reader doesn't have to read the body to learn what was qualified — they click."
- Punchline: "OpenCitations and WikiCite already build the left-hand side beautifully. What's missing is a citable target on the right — and that's what the rest of this talk is about."

## Slide 3 · Stackable architecture

Beat (~3 min):
- Point at the diagram (left). "Three named graphs in one nanopub. Top: the assertion — the actual claim. Middle: provenance — how the claim was derived. Bottom: publication info — who, when, under what licence."
- "The URI itself contains a hash of the assertion. You cannot quietly rewrite a published nanopub. Cryptographic immutability is built into the identifier."
- Right column: "And because each nanopub has its own URI, you can build chains where each step cites a specific upstream nanopub. The next slide shows what that looks like in practice."
- Land the "stackable" word here, not earlier.

## Slide 4 · Stackable in practice — a FORRT replication chain

Beat (~2 min) — "show, don't tell" of stackable:
- Don't read the diagram. Point: "every node is its own nanopub with its own URI"
- Say: "Soroye 2020 on the left — what we replicated. Three coloured branches: two
  flavours of the thermal-niche claim plus a cross-substrate replication. Each ends in a CiTO
  citation back to the original paper — two 'confirms', one 'qualifies'."
- Punchline (point at magenta apex on the right): "Synthesis on the right is one URI. Cite that
  one URI and you've cited the full constellation. That's what stackable means."
- Every box is a clickable hyperlink to the published nanopub on Science Live. Useful in Q&A:
  if anyone asks "what does an actual Outcome nanopub look like?" — click `05 Outcome Validated`.
- Research Software nanopubs (used for tooling reuse) are omitted from the diagram for clarity —
  mention only if asked. They cite the Claim one-way and live off-chain.
- This slide is the *concrete* version of slide 3. Slide 5 is how you build one.

## Slide 5 · Three production paths to a signed nanopub

Beat (~3 min):
- OPEN with the analogy (it's printed but say it out loud, slowly): "Self-driving cars will drive themselves — but humans still choose the destination. LLM extraction is the same. The model can do the driving — the author still chooses the citation intent."
- LEFT (Extract): "this is where most of you live. GROBID / CEC / GRAPHIA — extract intent retroactively. We're additive, not competing — the extracted intent becomes a signed nanopub on the network."
- Limit: "but extraction has an accuracy ceiling because intent is partially implicit in prose"
- RIGHT (Author): point at the worked example. "The Zotero plugin lets the author declare intent at write time, from the source that knows best. Highlight the quote. Comment. Pick the CiTO type. Sign and publish. That's a Quote-with-comment nanopub — the first step of every FORRT chain you saw on slide 4."
- Closing technical bridge: "LLM extraction lands you in a FORRT chain via the replication template. Zotero authoring lands you at chain step 01."
- BEFORE DELIVERY: replace the "…" in the Quote field with the actual verbatim sentence from the Soroye 2020 paper used in the RAErLL… nanopub.

## Slide 6 · Three worked domains

Beat (~3 min):
- Point at the left first: "the chain you saw on slide 4 — its apex is RA5TJVZ0. Click that URI and you reach all 18 nanopubs."
- "The quantum-biodiversity PRISMA review contributes 238 more nanopubs on the same network — different domain question, same architecture."
- Middle (Climate change → EarthCARE → DGGS): "we built the full software pipeline to convert EarthCARE EO data to HEALPix-geo. The CiTO chain ties the new data to the upstream literature. Click the URI to see the chain."
- Right (Cross-discipline → FIESTA plankton): "scattering transforms — a method from astrophysics — applied to plankton classification. Same nanopub carries three CiTO predicates simultaneously: extends the original plankton paper, uses the astrophysics method, cites our reproduction as a data source. This is what cross-disciplinary citation looks like when it's machine-readable."
- Three URIs all resolve today; nothing is forthcoming.

## Slide 7 · Demo · annotate while reading

Demo (~5 min, pre-recorded — annotation-while-reading workflow):
- Open Wernberg et al. 2016 in Zotero, find ref 11 (Poloczanska et al. 2013)
- Science Live Zotero plugin → Citation with CiTO template
- Citing: doi.org/10.1126/science.aad8745 (Wernberg)
- Cited:  doi.org/10.1038/nclimate1958 (Poloczanska — Global imprint of climate change on marine life)
- Relation: citesAsAuthority
- Comment: "Wernberg cites Poloczanska as the global authority for climate-driven marine species redistribution; WA kelp is one regional manifestation, Mediterranean Iberian is another"
- Generate Nanopublication → signed + published to the open network
- Verify on Science Live viewer → three graphs visible
- Punchline: third production path = expert reader, neither LLM nor citing-author

See demo-script.md for full beat-by-beat narration.

Fallback if the embedded mp4 fails:
- Open platform.sciencelive4all.org and resolve a freshly published CiTO URI
- ~90s manual walkthrough, return to slide 9 (Atomicity)

The mp4 is committed at recordings/demo.mp4 and served by GitHub Pages, so
no external network dependency at delivery time.

## Slide 8 · Atomicity enables claim-level verification

Beat (~3 min):
- The trust gradient is the honest answer to "how do you know an LLM didn't hallucinate this?"
- The FORRT layer is the differentiating move — we publish the verification chain alongside the original claim
- Acknowledge limitations openly — this audience will trust the work more for it

## Slide 9 · Try it · Cite it · Extend it

Beat (~2 min):
- Hold this slide as long as possible during Q&A
- The audience needs URLs visible while asking questions
- If asked "where do I go to try this" — point and read out the URL
