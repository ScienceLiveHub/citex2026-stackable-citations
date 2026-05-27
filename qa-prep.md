# Q&A prep — anticipated questions + answer cards

CiteX 2026 · 30-min slot · 8-min Q&A window.

The room contains the people who *built* the open-citations stack you extend (Silvio Peroni, Daniel Mietchen, Bianca Kramer, Tamara Heck, Angelo Di Iorio, Matteo Romanello) plus the people building the *next* extraction pipelines (CEC, GRAPHIA, the OFFZIB educational-research group). Two distinct registers in the same room.

**Answer discipline:**
- Lead with the 1-line answer
- Add one concrete example or URI
- Stop. Don't volunteer additional content the questioner didn't ask for.
- If unsure, say "I don't know — happy to follow up after the workshop." Better than over-claiming.

---

## Hard questions from the programme committee

### Silvio Peroni — *How does this compose with OpenCitations / OCI?*

**1-line:** CiTO IS what we use; OpenCitations COCI is the citation-edge layer; we add a citable *target* at the citing-side content (the AIDA/Claim nanopub) so that OCI's edges can point at structured units rather than at paper-level DOIs.

**Concrete:** an OCI triple `Fouilloux-2026-citex cito:citesAsAuthority Groth-2010` can now point to a Trusty URI for the *specific claim* we cite Groth for, not just to the Groth-2010 paper DOI.

**Don't say:** that we replace OpenCitations. We don't.

---

### Bianca Kramer — *Alignment with Barcelona Declaration on Open Research Information?*

**1-line:** Direct alignment — open, machine-readable, openly-licensed (CC-BY 4.0), no authentication barriers, decentralised infrastructure. The Trusty URI gives the "open" component a persistence guarantee the DOI ecosystem doesn't provide for individual claims.

**Concrete:** every nanopub on our worked examples carries CC-BY 4.0; the network has no single owner; the assertion is content-addressable.

---

### Daniel Mietchen — *Wikidata / Scholia pathway? Has the data flowed in?*

**1-line:** Each nanopub assertion links concepts to Wikidata Q-IDs at creation time; Egon Willighagen's pipeline can ingest these for Scholia visualisation. We've mapped Q-numbers for the FORRT chain types; the Scholia integration is feasible but not yet at production scale.

**Concrete:** the WeatherXBio Bombus chain has every species linked to its taxonomic Wikidata Q-ID; the citation graph could be Scholia-renderable today.

**Honest:** the Wikidata side of the loop is the work that hasn't fully landed yet.

---

### Matteo Romanello / GRAPHIA team — *How does this compare with our LLM citation-context extraction?*

**1-line:** Complementary, not competing. You extract; we make the extracted thing citable. GRAPHIA's output could be the *input* to our nanopub-generation pipeline — every (citation, intent, context) triple GRAPHIA produces is a candidate nanopub.

**Concrete:** if GRAPHIA classifies a citation as `disputes`, that's a CiTO predicate; we'd publish it as a signed nanopub with the extracted context as the comment, the cited claim's URI as the target.

**Opportunity:** floats the possibility of a downstream integration without committing to one.

---

### Angelo Di Iorio / Ivan Heibi — *Your CEC tool also does context-aware extraction + intent classification. Overlap?*

**1-line:** Same upstream goal (machine-readable citation intent), different layers — CEC is the *extractor*, Science Live is the *publisher of the result*. CEC output could feed our nanopub-generation pipeline directly.

**Concrete:** CEC's intent labels map onto CiTO predicates; the pipeline we showed in slide 5 abstracts over which extractor produced the (intent, context) pair.

---

### Tamara Heck / OFFZIB — *Does this transfer to educational research?*

**1-line:** The template is currently focused on **computational reproducibility** — Docker, conda, Snakemake, notebooks. The chain pattern itself (Quote → AIDA → Claim → Study → Outcome → CiTO) is field-agnostic, and the `DOMAIN.md` mechanism adapts the tooling defaults to your field. Non-computational replications would need adapting the bundled tools.

**Concrete:** point to `ScienceLiveHub/forrt-replication-template` and the `docs/domain-flavours/` directory. Happy to co-develop a domain flavour for educational research as a follow-up.

**Door-opener:** sets up potential post-workshop collaboration with the OFFZIB project, which is the workshop's host. *Don't oversell — be honest the current template runs code; non-computational replication workflows would need additional adaptation.*

---

### Christian Boulanger — *We're doing law and humanities with Grobid. Different citation styles, monographs, footnotes. Does this work?*

**1-line:** The publishing layer is style-agnostic — once your Grobid pipeline extracts (citing-context, cited-target, intent), we publish the result as a nanopub regardless of whether the source was a footnoted monograph or an APA journal article. Where it gets harder is the cited-target side: monographs less often have DOIs.

**Concrete:** the FaBiO / SPAR ontologies (which we use) handle the bibliographic-type variation; the nanopub doesn't care about citation style.

---

## Likely general-audience questions

### Scalability — *238 nanopubs is small. What about 10M references?*

**1-line:** 238 is the human-validated number; the LLM-assisted pipeline scales linearly with compute, and the decentralised network is designed for population scale (current network has ≈10M+ published nanopubs across all domains).

**Honest:** we haven't run a 10M-reference batch ourselves; we've validated the pipeline up to a PRISMA-systematic-review scale.

---

### Adoption — *Who actually publishes nanopubs and reads them?*

**1-line:** Today: a few hundred publishers across the nanopub network (DisGeNET, LinkedSPL, FAIR Workbench community, our work). Reading happens through the resolvers + SPARQL endpoints + Scholia. The honest answer: nascent. The Zotero plugin is our adoption-ramp bet.

---

### Trust in LLM-extracted CiTO types — *How do you know an LLM didn't hallucinate the intent?*

**1-line:** We don't, at the LLM-output stage. That's why the trust gradient exists: LLM-extracted is the *lowest* tier; author-validated and FORRT-replicated sit above. The recommendation is to treat LLM output as a draft that the author signs off on before it becomes a signed nanopub.

**Reference:** point at slide 8.

---

### *Why bother with the Zotero plugin — can't LLMs eventually do citation intent end-to-end?*

**1-line (use the analogy):** Self-driving cars *will* drive themselves — but humans still choose the destination. LLM extraction will keep improving, but choosing the citation *intent* is the high-stakes meta-decision that the human, not the system, should make. The plugin makes that decision easy to record at write time.

**Concrete:** the author already knows whether they're citing Soroye to use the method, qualify a finding, or dispute a claim. The plugin captures it as a signed nanopub in the second the author would have moved on. Asking an LLM to recover that later is doing the harder problem for no good reason.

**Don't say:** that LLMs can't do this. They can, with imperfect accuracy. The question is whether you want imperfect-retroactive or perfect-write-time. We support both, with the trust gradient labelling them.

---

### Format choice — *Why nanopubs rather than JSON-LD / schema.org / [other]?*

**1-line:** Nanopubs *are* RDF/JSON-LD-serialisable — they're not a competing format, they're a *packaging* convention. The three-graph structure + Trusty URI gives you content-addressability and provenance separation that flat JSON-LD doesn't enforce. Use the JSON-LD output if your tooling prefers it.

---

### Network reliability — *KP went down last week. What happens to citations when the registry is offline?*

**1-line:** Two answers. (1) Resolvable Trusty URIs are *content-addressable* — any server holding a copy can serve it; the network is supposed to be decentralised, though in practice KP runs most of it. (2) Science Live's own API resolves from its own DB, independent of KP availability.

**Honest:** the de-facto centralisation on KP is a real risk; the protocol's decentralisation goal isn't fully realised yet. We mirror locally for our own production work.

---

### Citation gaming — *What stops a malicious actor publishing wrong CiTO types?*

**1-line:** Nothing prevents publishing it. The trust gradient (slide 8) is the *signal*, not a gate. The atomic structure makes a wrong CiTO type easy to dispute via a counter-nanopub. We don't enforce truth at publish time; we make truth easier to *verify* and *contest* at read time.

---

### Cost / infrastructure — *Who pays for the publishing infrastructure?*

**1-line:** Today: the nanopub network is run by Knowledge Pixels (operationally) and the FAIR Workbench community (financially, in part). Science Live's platform is funded through LifeWatch ERIC and Horizon Europe (FAIR2Adapt). The Vitenhub AS commercial arm is exploring sustainable hosting models for production deployments.

---

## URI verification checklist

Before recording the demo, confirm each of these resolves via `platform.sciencelive4all.org/np/?uri=…` (Science Live's resolver, independent of KP):

- [ ] Fouilloux 2025 [citesAsDataSource] — `RA-NA9GylGUn4P1AFm20txzBCZlFGaMFtPbkR7CFSWzs`
- [ ] Groth 2010 [usesMethodIn] — `RAZ1sRo-ei2f52bEiuXlAoVyny1V9vpeSxN69avod14sM`
- [ ] Groth 2010 [citesAsAuthority] — `RA4h2w5UImaqgF84fPfqy_lkjhgXZCAIae3Onh9_6G83o`
- [ ] Kuhn 2021 [usesMethodIn] — `RAgBSZ6agwJr9eWvxRTZQqo_dfa1Xmvx3i1-t5t8hxpQ4`
- [ ] Kuhn 2021 [citesAsPotentialSolution] — `RAh0rL16HvIf_1WxlxkHjvsIdEyrxKQtWaZb0CLRKpS5U`
- [ ] Page 2021 [usesMethodIn] — `RAbESIdEoD2BawGtL8fOi5M_0-vyl3uZMKHbIaa2JG7qo`
- [ ] Röseler 2025 [citesAsRecommendedReading] — `RALQHC6aQXDr2rGbWwbqFPEYjo3o9-8MB4SVx6rhZqw8I`
- [ ] Peroni & Shotton 2012 [usesMethodIn] — `RAohoa4RPbFENR_YxWx9UiSRILD303Zw0RAh7v0prwSDM`
- [ ] Shotton 2010 [usesMethodIn] — `RAu1zPQntKRYXS9womcgIXSNAPFt53Y3LiFLi885aJFFo`

If any fail (KP outage), fall back to other URIs from your existing chains — the WeatherXBio Bombus chain (19 nanopubs) and the SDM resolution scaffold (8 Quote-with-comment) are alternatives.

---

## During Q&A — discipline

- **Listen to the full question** before answering. Two heartbeats of silence before the answer is fine.
- **Repeat the question** in your own words if it was long — gives you 5 seconds to think and confirms you heard right.
- **If you don't know**, say so. The audience trusts the work more when you don't bluff. Offer to follow up after the workshop and exchange contact.
- **Don't get drawn into a long back-and-forth** with one questioner. Tamara (chair) will move on. If a question is generating real engagement, offer "let's continue this in the community discussion tomorrow."
- **Take notes** during Q&A — every question is a data point for the post-workshop follow-up paper, if you decide to write one.
