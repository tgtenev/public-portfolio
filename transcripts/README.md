# Audio transcripts

Listening editions of the papers in this repository. Each `.txt` file here is a plain-prose adaptation of
one Markdown source in the parent directory, written to be played through a text-to-speech app rather than
read on screen.

**The Markdown originals are the documents of record.** A transcript is an adaptation, never a citable
source. Cite the published version via its DOI, exactly as the [repository README](../README.md) directs.

## What "adapted" means

A transcript is sentence-for-sentence faithful to its source. Nothing is summarized, reordered, or
explained. Only mechanical adaptations are applied, so that a document written for the eye can be followed
by the ear:

- Mathematics is read out in words, the way you would dictate it to a colleague over the phone. Greek
  letters go by name, with phonetic spellings where a speech engine mispronounces the standard
  romanization — `myu`, `nyu`, `ksai`, `kai`, `fai`.
- Acronyms that are not pronounceable as words are expanded. Ones that are — MOND, SPARC, JADES — are
  kept and expanded once at first use.
- Figures are described in words, then their captions read. Tables are read as lists, every row.
- Code listings become structured verbal walkthroughs, grouped the way the code is grouped.
- Links, DOIs, and file paths are never read aloud; destinations are named descriptively instead.
- Reference lists are not read. Each transcript closes by saying so.

Markup is stripped entirely: no headings, emphasis, brackets, pipes, or math delimiters survive into the
spoken text.

Where a source contains an error, the transcript reproduces it. If the source is unclear, the transcript is
equally unclear. That is deliberate — a listening edition that quietly corrects its source would diverge
from the document of record.

## The transcripts

### Journal papers

| Paper | Transcript |
|---|---|
| [The Mechanics of Spacetime](../tenev2018-mechanics-spacetime.md) | [tenev2018-mechanics-spacetime.txt](tenev2018-mechanics-spacetime.txt) |
| [Recovering the Principle of Relativity](../tenev2018-recovering-relativity.md) | [tenev2018-recovering-relativity.txt](tenev2018-recovering-relativity.txt) |
| [The Spacetime Metric of a Spherically Symmetric Deformation](../tenev2019-spacetime-metric.md) | [tenev2019-spacetime-metric.txt](tenev2019-spacetime-metric.txt) |
| [Dark Matter Effect Attributed to the Inherent Structure of Cosmic Space](../tenev2019-dark-matter-effect.md) | [tenev2019-dark-matter-effect.txt](tenev2019-dark-matter-effect.txt) |

### Conference and magazine papers

| Paper | Transcript |
|---|---|
| [A Solution for the Distant Starlight Problem](../tenev2018-starlight.md) | [tenev2018-starlight.txt](tenev2018-starlight.txt) |
| [A 'creationeering' Perspective on Dark Matter](../tenev2025-creationeering-dark-matter.md) | [tenev2025-creationeering-dark-matter.txt](tenev2025-creationeering-dark-matter.txt) |
| [A Non-Expansionary Mechanism for Galactic Redshift](../tenev2026-non-expansionary-redshift.md) | [tenev2026-non-expansionary-redshift.txt](tenev2026-non-expansionary-redshift.txt) |

### Preprints

| Paper | Transcript |
|---|---|
| [Emergent de Sitter Expansion and Closed Topology](../tenev2026-emergent-de-sitter.md) | [tenev2026-emergent-de-sitter.txt](tenev2026-emergent-de-sitter.txt) |
| [Modified Newtonian Dynamics after Four Decades](../tenev2026-mond-review.md) | [tenev2026-mond-review.txt](tenev2026-mond-review.txt) |
| [How Dennis's Young-Earth Cosmology Works](../tenev2026-dennis-cosmology.md) | [tenev2026-dennis-cosmology.txt](tenev2026-dennis-cosmology.txt) |
| [The Aether Lineage](../tenev2026-aether-lineage.md) | [tenev2026-aether-lineage.txt](tenev2026-aether-lineage.txt) |
| [Crystal Growth by Steps and Spirals](../tenev2026-bcf-review.md) | [tenev2026-bcf-review.txt](tenev2026-bcf-review.txt) |
| [Avalanches and Self-Organized Criticality](../tenev2026-soc-review.md) | [tenev2026-soc-review.txt](tenev2026-soc-review.txt) |

### Dissertation

| Document | Transcript |
|---|---|
| [Landing page — abstract, errata, contents](../tenev2018-dissertation.md) | [tenev2018-dissertation.txt](tenev2018-dissertation.txt) |
| [Condensed digest](../tenev2018-dissertation-digest.md) | [tenev2018-dissertation-digest.txt](tenev2018-dissertation-digest.txt) |
| [Ch. 1 — Introduction](../tenev2018-dissertation/ch1-introduction.md) | [ch1-introduction.txt](tenev2018-dissertation/ch1-introduction.txt) |
| [Ch. 2 — Background](../tenev2018-dissertation/ch2-background.md) | [ch2-background.txt](tenev2018-dissertation/ch2-background.txt) |
| [Ch. 3 — The Cosmic Fabric Model](../tenev2018-dissertation/ch3-cosmic-fabric-model.md) | [ch3-cosmic-fabric-model.txt](tenev2018-dissertation/ch3-cosmic-fabric-model.txt) |
| [Ch. 4 — Recovering Relativity](../tenev2018-dissertation/ch4-recovering-relativity.md) | [ch4-recovering-relativity.txt](tenev2018-dissertation/ch4-recovering-relativity.txt) |
| [Ch. 5 — The Spacetime Metric](../tenev2018-dissertation/ch5-spacetime-metric.md) | [ch5-spacetime-metric.txt](tenev2018-dissertation/ch5-spacetime-metric.txt) |
| [Ch. 6 — The Dark Matter Effect](../tenev2018-dissertation/ch6-dark-matter-effect.md) | [ch6-dark-matter-effect.txt](tenev2018-dissertation/ch6-dark-matter-effect.txt) |
| [Ch. 7 — Numerical Framework](../tenev2018-dissertation/ch7-numerical-framework.md) | [ch7-numerical-framework.txt](tenev2018-dissertation/ch7-numerical-framework.txt) |
| [Ch. 8 — Conclusions](../tenev2018-dissertation/ch8-conclusions.md) | [ch8-conclusions.txt](tenev2018-dissertation/ch8-conclusions.txt) |
| [Ch. 9 — Future Research](../tenev2018-dissertation/ch9-future-research.md) | [ch9-future-research.txt](tenev2018-dissertation/ch9-future-research.txt) |

The dissertation's [references.md](../tenev2018-dissertation/references.md) has no transcript. Reference
lists are not read in a listening edition, so a transcript of a file that is nothing but a reference list
would be a recitation of bibliographic entries and DOIs. The dissertation's front matter — abstract,
errata, and contents — is covered by the landing-page transcript.

## Keeping them current

**A transcript must be regenerated whenever its source document changes.** It is regenerated whole, never
patched, because the adaptation decisions run through the entire text. There is no automation watching for
this; it is a manual step that belongs with the commit that changes the source.

## Notes and known limits

**Figures are described from words, not from pictures.** Figures are served from a CDN and are not
committed to this repository, so the figure descriptions are built from each figure's alt text, its
caption, and the surrounding body prose. They describe what the source says the figure shows. If a
description and the actual artwork ever disagree, the artwork is right.

**Equation cross-references are handled two ways.** Some transcripts keep audible "Equation N" labels;
others replace every cross-reference with a description of the equation's content. Documents that
cross-reference their equations dozens of times generally keep the numbers, since descriptive glosses stop
being followable at that density. Both readings are faithful to the source; neither changes any content.

**Numbers are formatted per document, not across the corpus.** Within any one transcript the convention is
consistent — either digits or fully spelled-out words — but it varies between documents, following what
suits each source.

**These files live in a subfolder.** The house convention elsewhere places a `.txt` audio edition directly
beside its `.md` source. Here they are gathered into `transcripts/` instead, at the author's direction, so
that the repository root stays a clean list of papers. Basenames are unchanged, and the chapter transcripts
mirror the chapter folder.
