*FunGen_Final* 
**Functional Genomics Final Project (BIOL 5850/6850)**
## Individual Component – Samira Salimiyan

## Project Overview

This final project focuses on RNA-seq differential gene expression and enrichment analysis in testicular tissue across dog breeds of varying sizes. My individual component specifically investigates the differential expression of genes involved in metabolic regulation and energy homeostasis between large and small dog breeds.

## Data

Raw single-end RNAseq data from testicular tissue were retrieved from the NCBI Sequence Read Archive (SRA) under BioProject PRJNA69086. A total of 12 datasets from 12 different dog breeds were selected. These datasets were divided into two size groups based on breed size according to the [American Kennel Club's](https://www.akc.org/) definitions. Samples used are listed in the table below:

| SRR ID       | Breed              | Size Group |
|--------------|-------------------|------------|
| SRR13389818  | Havanese           | Small      |
| SRR13389805  | Papillon           | Small      |
| SRR13389807  | Bichon Frise       | Small      |
| SRR13389809  | Maltese            | Small      |
| SRR13389841  | Border Terrier     | Small      |
| SRR13389834  | Yorkshire Terrier  | Small      |
| SRR13389820  | Golden Retriever   | Large      |
| SRR13389817  | Irish Wolfhound    | Large      |
| SRR13389815  | Labrador Retriever | Large      |
| SRR13389849  | Rottweiler         | Large      |
| SRR13389840  | Weimaraner         | Large      |
| SRR13389824  | German Shepherd    | Large      |

## Research Hypothesis

Are genes involved in metabolic regulation and energy homeostasis differentially expressed between large and small dog breeds?
I hypothesize that key metabolic genes (PPARGC1A, SIRT1, AMPK, MTOR, UCP1) will show differential expression reflective of breed size-related metabolic adaptations.

## Methodological Approach

Gene Selection:
Identified metabolic genes involved in mitochondrial function, energy expenditure, nutrient sensing, thermogenesis, and the AMPK/mTOR/SIRT1 pathways.

Differential Expression Analysis:
Used DESeq2 in RStudio (v4.4.1) to compare metabolic gene expression between small and large breed groups. Generated volcano plots and heatmaps to visualize DEGs.

Pathway Enrichment:
Performed GSEA using the Hallmark (h.all.v2024.1.Hs.symbols.gmt) and KEGG pathway gene sets to examine enrichment of metabolic and energy-related pathways.

Correlation with IIS:
Cross-referenced metabolic gene expression with IIS components (IGF1, AKT, FOXO3) to explore co-regulatory patterns.

Tools & Software

DESeq2 for differential gene expression
GSEA (Broad Institute) for enrichment analysis
R (v4.4.1) for statistical analyses
Cytoscape for enrichment network visualization

## Key Results

Upregulation of PPARGC1A and SIRT1 in small breeds suggests enhanced mitochondrial biogenesis and energy efficiency.
GSEA showed enrichment of fatty acid oxidation and oxidative phosphorylation pathways in small breeds.
Co-expression analysis indicated regulatory links between PPARGC1A and IIS genes, such as IGF1 and AKT1.

*Potential Pitfalls and Solutions*

Age-related effects:
Age was not included in the metadata. Results were interpreted in light of the literature on age-related metabolic changes.

Size classification:
Only distinctly small (<10kg) and large (>25kg) breeds were included to avoid ambiguity.

Tissue heterogeneity:
Analysis was constrained to testis tissue and cross-validated with tissue-specific gene expression databases.

Interpretation complexity:
All findings were reviewed in conjunction with existing literature on mammalian metabolic regulation.

## Output Files

DEG_results_padj_0.05.csv – Significant DEGs (padj < 0.05)

DGErank_Feline.rnk – Ranked gene list for GSEA PreRanked

MA_plot.png, Heatmap_Top50Genes.png, PCA_Plot.png – Visualizations of DE and sample clustering

TopGene_expression.png – Normalized counts of top metabolic gene

NormTransExpIDs.txt – Expression matrix for Cytoscape

## Conclusion

This project supports the hypothesis that small dog breeds exhibit higher expression of key metabolic regulators related to energy efficiency and thermogenesis. These findings highlight how gene expression linked to energy balance and size may be evolutionarily regulated across breed phenotypes.
