# Figure-to-Code Mapping

Mapping between manuscript figures and the notebooks that generate each panel.
Panels not listed are experimental images (PhenoCycler, RNAscope, H&E) or illustrative diagrams not produced by code.

---

## Main Figures

### Fig. 1 — Overview of study design, sampling time points, and multi-modal dataset compositions
Illustrative figure (PowerPoint/Illustrator). No code.

### Fig. 2 — Clustering and annotation of spatial transcriptomic cell populations
`01_major_cluster_annotation` — UMAP by Major_cluster/Major_cluster_pathol, cell composition stacked bar, spatial scatter

### Fig. 3 — Identification of treatment-associated T cells, CAFs, and myeloid subclusters
- `02_subcluster_annotation` — Subcluster UMAPs, marker gene dot plots
- `05_temporal_dynamics` — Cell composition bar per subcluster

### Fig. 4 — Treatment-resistant CAFs and myeloids enriched adjacent to residual tumor
- `09_skny_gridding` — SKNY gridding & distance from tumor surface
- `04_spatial_neighborhood_analysis` — SKNY distance distributions

### Fig. 5 — Molecular characteristics and targetable pathways of NR CAFs
- `10_caf_spatial_distribution` — NR CAF spatial scatter, peri-tumor vs peri-normal violin
- `02_subcluster_annotation` — UMAP colored by CAF subtype
- `06_survival_analysis` — KM DFS curves, TCGA validation (POSTN, KRAS)

### Fig. 6 — Trajectory inference reveals bifurcation of CAFs into NR and pCR branches
`07_caf_trajectory` — STORIES potential & velocity on isomap, fate probability violin, per-patient spatial fate maps, driver gene trends

### Fig. 7 — Molecular function of tumor interacting with NR CAF
- `11_tumor_neighbor_analysis` — Per-patient pathway enrichment heatmap
- `12_ligand_receptor_analysis` — LR spatial visualization, LR network diagram

---

## Supplementary Figures

### Suppl. Fig. 1 — Marker genes and inter-patient variability
`01_major_cluster_annotation` — UMAP by Sample/Timepoint, marker gene expression

### Suppl. Fig. 2 — Subclusters and annotations
- `02_subcluster_annotation` — Subcluster dot plots (Stromal, T cell, Myeloid)
- `03_tumor_analysis` — Tumor subcluster markers, Hallmark pathway UMAPs

### Suppl. Fig. 3 — Normalized abundance of subclusters across response groups and timepoints
`05_temporal_dynamics` — Per-subcluster density and proportion line plots

### Suppl. Fig. 4 — Spatial distribution and LR interactions among NR CAFs, myeloid, and tumor
- `04_spatial_neighborhood_analysis` — SKNY distance distributions, LIANA LR dot plot, longitudinal neighborhood enrichment
- `12_ligand_receptor_analysis` — Per-patient LR heatmaps

### Suppl. Fig. 5 — Identification of NR CAFs and fibroblast, and molecular function of pCR CAFs
- `10_caf_spatial_distribution` — Reactome enrichment (Fibroblast)
- `11_tumor_neighbor_analysis` — CR CAF neighbor DEG (NR and MPR patients)

### Suppl. Fig. 6 — Additional trajectory analyses of CAF bifurcation
`07_caf_trajectory` — Velocity streams, branch assignment, TF enrichment (TRRUST)

### Suppl. Fig. 7 — Identification of tumor cells interacting with NR CAFs and associated signaling
`11_tumor_neighbor_analysis` — Per-patient spatial scatter, per-cell pathway enrichment, non-canonical WNT analysis

### Suppl. Fig. 8 — Graphical summary
Illustrative figure (PowerPoint/Illustrator). No code.

---

## Notebook Summary

| Notebook | Figures |
|----------|---------|
| `01_major_cluster_annotation` | Fig. 2; SFig. 1 |
| `02_subcluster_annotation` | Fig. 3; Fig. 5; SFig. 2 |
| `03_tumor_analysis` | SFig. 2 |
| `04_spatial_neighborhood_analysis` | Fig. 4; SFig. 4 |
| `05_temporal_dynamics` | Fig. 3; SFig. 3 |
| `06_survival_analysis` | Fig. 5 |
| `07_caf_trajectory` | Fig. 6; SFig. 6 |
| `09_skny_gridding` | Fig. 4 (preprocessing) |
| `10_caf_spatial_distribution` | Fig. 5; SFig. 5 |
| `11_tumor_neighbor_analysis` | Fig. 7; SFig. 5, 7 |
| `12_ligand_receptor_analysis` | Fig. 7; SFig. 4 |
