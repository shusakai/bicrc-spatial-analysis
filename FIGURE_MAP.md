# Figure-to-Code Mapping

Mapping between manuscript figures and the notebooks that generate each panel.
Panels not listed are experimental images (PhenoCycler, RNAscope, H&E) or illustrative diagrams not produced by code.

---

## Main Figures

### Fig. 1 — Overview of study design, sampling time points, and multi-modal dataset compositions
Illustrative figure (PowerPoint/Illustrator). No code.

### Fig. 2 — Clustering and annotation of spatial transcriptomic cell populations
| Panel | Description | Notebook |
|-------|-------------|----------|
| a | UMAP colored by Major_cluster | `01_major_cluster_annotation` |
| c | Cell composition stacked bar per sample | `01_major_cluster_annotation` |
| d | UMAP colored by Major_cluster_pathol (Tumor/Normal) | `01_major_cluster_annotation` |
| e, f | Spatial scatter zoom (100μm scale) | `01_major_cluster_annotation` |

### Fig. 3 — Identification of treatment-associated T cells, CAFs, and myeloid subclusters
| Panel | Description | Notebook |
|-------|-------------|----------|
| a | Subcluster UMAPs (T cell, Stromal, Myeloid) | `02_subcluster_annotation` |
| b | Dot plots of marker genes | `02_subcluster_annotation` |
| c | Cell composition bar per subcluster | `05_temporal_dynamics` |

### Fig. 4 — Treatment-resistant CAFs and myeloids enriched adjacent to residual tumor
| Panel | Description | Notebook |
|-------|-------------|----------|
| a | SKNY gridding & distance from tumor surface | `09_skny_gridding`, `04_spatial_neighborhood_analysis` |
| c–e | PhenoCycler protein imaging | — (experimental) |

### Fig. 5 — Molecular characteristics and targetable pathways of NR CAFs
| Panel | Description | Notebook |
|-------|-------------|----------|
| a | Spatial scatter: NR CAF, pCR CAF, Fibroblast, Tumor | `10_caf_spatial_distribution` |
| b | NR CAF density: peri-tumor vs peri-normal (violin) | `10_caf_spatial_distribution` |
| e | UMAP colored by CAF subtype | `02_subcluster_annotation` |
| h | RNA ISH (SFRP1, WNT5A, MMP11) | — (experimental) |
| i | Kaplan-Meier DFS curves | `06_survival_analysis` |
| j | TCGA validation (POSTN, KRAS) | `06_survival_analysis` |

### Fig. 6 — Trajectory inference reveals bifurcation of CAFs into NR and pCR branches
| Panel | Description | Notebook |
|-------|-------------|----------|
| a | Isomap embedding with STORIES potential & velocity | `07_caf_trajectory` |
| c | Violin: Pre Other CAF fate probability by Response | `07_caf_trajectory` |
| d | Per-patient spatial fate maps | `07_caf_trajectory` |
| e | Driver gene trends (NR & CR branches) | `07_caf_trajectory` |

### Fig. 7 — Molecular function of tumor interacting with NR CAF
| Panel | Description | Notebook |
|-------|-------------|----------|
| c | Per-patient pathway enrichment heatmap | `11_tumor_neighbor_analysis` |
| e | LR significant spots spatial visualization | `12_ligand_receptor_analysis` |
| f | LR network diagram | `12_ligand_receptor_analysis` |

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
| `01_major_cluster_annotation` | Fig. 2a,c–f; SFig. 1 |
| `02_subcluster_annotation` | Fig. 3a,b; Fig. 5e; SFig. 2 |
| `03_tumor_analysis` | SFig. 2 |
| `04_spatial_neighborhood_analysis` | Fig. 4a; SFig. 4 |
| `05_temporal_dynamics` | Fig. 3c; SFig. 3 |
| `06_survival_analysis` | Fig. 5i,j |
| `07_caf_trajectory` | Fig. 6a,c–e; SFig. 6 |
| `09_skny_gridding` | Fig. 4a (preprocessing) |
| `10_caf_spatial_distribution` | Fig. 5a,b; SFig. 5 |
| `11_tumor_neighbor_analysis` | Fig. 7c; SFig. 5, 7 |
| `12_ligand_receptor_analysis` | Fig. 7e,f; SFig. 4 |
