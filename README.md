# HPV Alignment Dashboard

The HPV Alignment Dashboard is a single, self-contained web page for exploring the evolutionary and sequence relationships among human papillomavirus (HPV) types. It packages MAFFT protein alignments of 28 HPV genotypes across all eight viral proteins (E1, E1^E4, E2, E5, E6, E7, L1, L2) into an interactive tool that runs entirely in the browser — no server, install, or internet connection required.

## Views

It has three linked views. The **Between HPV types** view shows a heatmap comparing every HPV type against every other for a chosen protein (or a "Combined" whole-proteome supermatrix), colored by percent identity, percent similarity, bit score, or E-value; clicking any tile opens the full pairwise alignment with color-coded residues and statistics. The **Within one HPV type** view flips this around, comparing a single type's own proteins against each other. The **Phylogenetic trees** view renders distance trees for each protein or the combined proteome, in phylogram, cladogram, or radial layouts. Throughout, HPV types are grouped and color-cued by clinical risk (high-risk, possible high-risk, low-risk), and a download bar exports the current selection as reference FASTA, MAFFT alignment FASTA, an Excel summary, or a Newick tree.

## Use

Its main use is to let researchers quickly answer questions like "how conserved is E7 across the high-risk types?", "which types cluster together phylogenetically?", or "where exactly do HPV16 and HPV18 differ in a given protein?" — without running command-line alignment tools. Practically, it supports comparative genomics and evolutionary analysis of HPV, identification of conserved regions for vaccine and diagnostic target design (e.g. cross-type epitope selection), and teaching or presentation of HPV sequence relationships. Because it's a portable HTML file, it also serves as a shareable, citable companion resource for a paper or lab website.

## Methods

BLOSUM62 scoring with gap penalties (existence 11, extension 1) and Karlin–Altschul statistics (λ = 0.267, K = 0.041). Between-type metrics come from the global MAFFT alignment, while within-type protein comparisons use local alignment.

## Contact

Keshav Saini, Ph.D. · ICGEB–Emory Vaccine Program
