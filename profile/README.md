# FAIR bioHeaders

We build metadata specifications and tools that keep provenance with biological
data, lowering the barriers to making those data **Findable, Accessible,
Interoperable, and Reusable (FAIR)**.

Our core standard, **FHR (FAIR Header Reference genome)**, records who created a
reference genome, how it was assembled, and how it can be identified and reused.
The metadata can travel with FASTA and GFA files or be shared separately in
machine-readable formats. We also work on reference transcriptome metadata,
GFF3 annotation validation, and workflow integration.

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
| [FAIR-bioHeaders-Specification](https://github.com/FAIR-bioHeaders/FAIR-bioHeaders-Specification) | Released specifications for every header type (FHR, FHP, FHGFF3): schemas, shared core, format rules, examples, and conformance suite. Formerly FHR-Specification. |
| [FHR-Specification](https://github.com/FAIR-bioHeaders/FHR-Specification) | Development of the FHR reference genome header; released work moves to FAIR-bioHeaders-Specification. |
| [FHP-Specification](https://github.com/FAIR-bioHeaders/FHP-Specification) | Development of the FHP protein FASTA header (draft). |
| [FAIR-bioHeaders-Tools](https://github.com/FAIR-bioHeaders/FAIR-bioHeaders-Tools) | Metadata conversion and validation, sequence header tools, and checksum verification. Formerly FHR-File-Converter. |
| [gff3-validator](https://github.com/FAIR-bioHeaders/gff3-validator) | GFF3 syntax, structure, and Sequence Ontology checks through a web interface, CLI, and library. Early release. |
| [FAIR-bioHeaders-Nextflow](https://github.com/FAIR-bioHeaders/FAIR-bioHeaders-Nextflow) | Nextflow DSL2 modules and Dockstore workflow for FHR, FHP and FHGFF3 headers (formerly FHR-Nextflow); first release v0.1.0. |
| [FHT-Specification](https://github.com/FAIR-bioHeaders/FHT-Specification) | Reference transcriptome metadata specification. Work in progress. |
| [FHGFF3](https://github.com/FAIR-bioHeaders/FHGFF3) | Draft computable GFF3 schema, based on biodatamodels/gff-schema. |
| [FHR-Citation](https://github.com/FAIR-bioHeaders/FHR-Citation) | Citation information and BibTeX entries for FHR resources. |
| [fair-bioheaders.github.io](https://github.com/FAIR-bioHeaders/fair-bioheaders.github.io) | Source for the project website at fhref.org. |

See each repository for its supported formats, installation instructions,
development status, and licensing.

## Cite our work

For an introduction to FHR, see the published paper,
[“FAIR Header Reference Genome: A TRUSTworthy Standard”](https://doi.org/10.1093/bib/bbae122)
(*Briefings in Bioinformatics*, 2024).

When using a specific resource, cite the
[FHR specification](https://doi.org/10.5281/zenodo.6762549) or
[converter software](https://doi.org/10.5281/zenodo.6762547), using the version DOI
for the release you used where available. These are FHR resource DOIs;
they are not FHT-specific citations. [FHR-Citation](https://github.com/FAIR-bioHeaders/FHR-Citation)
maintains machine-readable citation entries.

## Get involved

Report problems, suggest metadata improvements, or contribute examples and code
in the relevant project's issue tracker or pull requests. Check that repository's
contribution guidance before submitting changes.

For general enquiries, email [info@fhref.org](mailto:info@fhref.org).
