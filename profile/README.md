# FAIR bioHeaders

We build metadata specifications and tools that keep provenance with biological
data, lowering the barriers to making those data **Findable, Accessible,
Interoperable, and Reusable (FAIR)**.

Our core standard, **FHR (FAIR Header Reference genome)**, records who created a
reference genome, how it was assembled, and how it can be identified and reused.
The metadata can travel with FASTA and GFA files or be shared separately in
machine-readable formats. The family also covers proteins (FHP), transcriptomes (FHT), GFF3 annotations
(FHGFF3), and native gene models (FHGM). Each implementation has its own
support matrix; a published schema does not imply support in every tool.

## Get started

1. Visit [fhref.org](https://fhref.org/) for project documentation and web tools.
2. Explore the [FAIR-bioHeaders specifications](https://github.com/FAIR-bioHeaders/FAIR-bioHeaders-Specification),
   including its [field reference](https://github.com/FAIR-bioHeaders/FAIR-bioHeaders-Specification/blob/main/docs/FORMAT.md)
   and [minimal metadata example](https://github.com/FAIR-bioHeaders/FAIR-bioHeaders-Specification/blob/main/examples/minimal.fhr.json).
3. Use [FAIR-bioHeaders Tools](https://github.com/FAIR-bioHeaders/FAIR-bioHeaders-Tools)
   to convert and validate metadata, attach it to sequence files, and verify file
   checksums. The package is called `fair-bioheaders` and the CLI is `bioheaders`:

   ```bash
   python -m pip install fair-bioheaders
   bioheaders --help
   ```

For annotation files, try the [GFF3 validator](https://fhref.org/gff3-validator/)
in your browser or use its [CLI and Python library](https://github.com/FAIR-bioHeaders/gff3-validator).
It is an early release; its rule catalogue is under review.

## Projects

| Project | Purpose |
| --- | --- |
| [FAIR-bioHeaders-Specification](https://github.com/FAIR-bioHeaders/FAIR-bioHeaders-Specification) | Publication authority for FHR, FHP, FHT, FHGFF3 and native FHGM: schemas, shared core, format rules, examples, and conformance suite. Formerly FHR-Specification. |
| [FHR-Specification](https://github.com/FAIR-bioHeaders/FHR-Specification) | Development of the FHR reference genome header; released work moves to FAIR-bioHeaders-Specification. |
| [FHP-Specification](https://github.com/FAIR-bioHeaders/FHP-Specification) | Development of the FHP protein FASTA header. |
| [FAIR-bioHeaders-Tools](https://github.com/FAIR-bioHeaders/FAIR-bioHeaders-Tools) | Metadata conversion and validation, sequence header tools, and checksum verification. Formerly FHR-File-Converter. |
| [gff3-validator](https://github.com/FAIR-bioHeaders/gff3-validator) | GFF3 syntax, structure, and Sequence Ontology checks through a web interface, CLI, and library. Early release. |
| [FAIR-bioHeaders-Nextflow](https://github.com/FAIR-bioHeaders/FAIR-bioHeaders-Nextflow) | Nextflow DSL2 modules and workflow examples; consult its tested support matrix and pinned dependencies. |
| [FHT-Specification](https://github.com/FAIR-bioHeaders/FHT-Specification) | Development of the FHT transcriptome header; released contracts live in the shared specification. |
| [FHGFF3](https://github.com/FAIR-bioHeaders/FHGFF3) | Development of the FHGFF3 header. Its inherited GFF feature-model tree has separate provenance and reuse restrictions. |
| [FHGM-Specification](https://github.com/FAIR-bioHeaders/FHGM-Specification) | Development of native gene-model metadata; distinct from the GFF3 header. |
| [Tools-R](https://github.com/FAIR-bioHeaders/FAIR-bioHeaders-Tools-R), [Tools-JavaScript](https://github.com/FAIR-bioHeaders/FAIR-bioHeaders-Tools-JavaScript), [Tools-Java](https://github.com/FAIR-bioHeaders/FAIR-bioHeaders-Tools-Java), [Tools-Julia](https://github.com/FAIR-bioHeaders/FAIR-bioHeaders-Tools-Julia) | Language-specific libraries; use each repository’s installation instructions and supported operations. |
| [FHR-Citation](https://github.com/FAIR-bioHeaders/FHR-Citation) | Citation information and BibTeX entries for FHR resources. |
| [fair-bioheaders.github.io](https://github.com/FAIR-bioHeaders/fair-bioheaders.github.io) | Source for the project website at fhref.org. |

See each repository for its supported formats, installation instructions,
development status, and licensing.

## Cite our work

For an introduction to FHR, see the published paper,
[“FAIR Header Reference Genome: A TRUSTworthy Standard”](https://doi.org/10.1093/bib/bbae122)
(*Briefings in Bioinformatics*, 2024).

When using a specific resource, cite the
[shared specification](https://doi.org/10.5281/zenodo.6762549) or
[Tools software](https://doi.org/10.5281/zenodo.6762547), using the version DOI
for the release you used where available. These links identify software/specification concepts across versions. Preserve
the registered title and license of the particular record you cite. [FHR-Citation](https://github.com/FAIR-bioHeaders/FHR-Citation)
maintains machine-readable citation entries.

## Get involved

Report problems, suggest metadata improvements, or contribute examples and code
in the relevant project's issue tracker or pull requests. Check that repository's
contribution guidance before submitting changes. Another model reviews every
agent-authored PR; humans perform merges. Agents address review findings and CI
failures before handing over the current commit and validation evidence.

For general enquiries, email [info@fhref.org](mailto:info@fhref.org).
