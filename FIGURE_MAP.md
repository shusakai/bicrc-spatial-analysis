# Figure-to-Code Mapping

Mapping between manuscript figures and the notebook code that generates each panel.

> **Notation**: `NB07:cell-35` = notebook `07_caf_trajectory.ipynb`, cell index 35

---

## Main Figures

### Fig. 1 — Overview of study design, sampling time points, and multi-modal dataset compositions
| Panel | Description | Notebook | Cell | Notes |
|-------|-------------|----------|------|-------|
| a | Study design schematic | — | — | Illustrative (PowerPoint/Illustrator) |
| b | Sampling timepoints diagram | — | — | Illustrative |
| c | Multi-modal dataset composition | — | — | Illustrative |

### Fig. 2 — Clustering and annotation of spatial transcriptomic cell populations
| Panel | Description | Notebook | Cell | Notes |
|-------|-------------|----------|------|-------|
| a | UMAP colored by Major_cluster | `01_major_cluster_annotation` | cell-10 | Saves `01_umap_major_clusters.png` |
| b | Spatial scatter (whole section, NR/MPR/pCR) | `01_major_cluster_annotation` | cell-10 | Spatial embedding at 500μm scale |
| c | Cell composition stacked bar per sample | `01_major_cluster_annotation` | cell-14 | Saves `01_composition_major_cluster_pathol.png` |
| d | UMAP colored by Major_cluster_pathol (Tumor/Normal) | `01_major_cluster_annotation` | cell-10 | Second panel of the 2-panel UMAP |
| e | Spatial scatter zoom (100μm, NR) | `01_major_cluster_annotation` | cell-10 | Zoomed spatial view |
| f | Spatial scatter zoom (100μm, MPR/pCR) | `01_major_cluster_annotation` | cell-10 | Zoomed spatial view |

### Fig. 3 — Identification of treatment-associated T cells, CAFs, and myeloid subclusters
| Panel | Description | Notebook | Cell | Notes |
|-------|-------------|----------|------|-------|
| a | Subcluster UMAP — T cell (11 clusters) | `02_subcluster_annotation` | cell-22 | `02_umap_tcell_subclusters.png` |
| a | Subcluster UMAP — Stromal/CAF (17 clusters) | `02_subcluster_annotation` | cell-22 | `02_umap_stromal_subclusters.png` |
| a | Subcluster UMAP — Myeloid (13 clusters) | `02_subcluster_annotation` | cell-22 | `02_umap_myeloid_subclusters.png` |
| b | Dot plot — Stromal marker genes | `02_subcluster_annotation` | cell-24 | `02_dotplot_stromal_markers.png` |
| b | Dot plot — T cell marker genes | `02_subcluster_annotation` | cell-25 | `02_dotplot_tcell_markers.png` |
| b | Dot plot — Myeloid marker genes | `02_subcluster_annotation` | cell-26 | `02_dotplot_myeloid_markers.png` |
| c | Cell composition bar per subcluster | `05_temporal_dynamics` | cell-8 | Major cluster composition stacked bar |
| d | Spatial scatter of subclusters (Pre/Resection, NR/pCR) | `02_subcluster_annotation` | cell-22 | Spatial embedding colored by subcluster |

### Fig. 4 — Treatment-resistant CAFs and myeloids enriched adjacent to residual tumor
| Panel | Description | Notebook | Cell | Notes |
|-------|-------------|----------|------|-------|
| a | SKNY gridding & distance from tumor surface | `09_skny_gridding` | cell-10 | Per-sample gridding + `calculate_distance()` |
| a | Spatial scatter: cell types near tumor | `04_spatial_neighborhood_analysis` | cell-13 | SKNY distance distributions |
| b | Neighborhood enrichment heatmap | `04_spatial_neighborhood_analysis` | cell-10 | Delaunay-based z-score heatmap |
| b | Average number of cells adjacent to tumor | `04_spatial_neighborhood_analysis` | cell-10 | Enrichment score bar |
| c | PhenoCycler: DAPI, EPCAM, αSMA, CD68, PDPN | — | — | Experimental imaging (not code) |
| d | PhenoCycler: αSMA, COL1, Galectin, Vimentin, etc. | — | — | Experimental imaging (not code) |
| e | PhenoCycler merge (IDO1, CD68, αSMA, EPCAM, PDPN) | — | — | Experimental imaging (not code) |

### Fig. 5 — Molecular characteristics and targetable pathways of NR CAFs
| Panel | Description | Notebook | Cell | Notes |
|-------|-------------|----------|------|-------|
| a | Spatial scatter: NR CAF, pCR CAF, Fibroblast, Tumor | `10_caf_spatial_distribution` | cell-49 | `sq.pl.spatial_scatter` for Pt-7 |
| b | NR CAF density: peri-tumor vs peri-normal (violin) | `10_caf_spatial_distribution` | cell-19 | Wilcoxon test, `NR_CAF_tumor_normal.png` |
| c | NR CAF vs Fibroblast DEG (volcano) | `10_caf_spatial_distribution` | cell-26 | Red=up in NR CAF, Blue=up in Fibroblast |
| d | Reactome pathway enrichment (up in NR CAF) | `10_caf_spatial_distribution` | cell-30 | Top 15 terms, red bars |
| e | UMAP colored by CAF subtype (NR/pCR) | `02_subcluster_annotation` | cell-22 | Stromal UMAP with annotations |
| f | POSTN spatial expression | `07_caf_trajectory` | cell-62 | Isomap scatter colored by POSTN |
| g | POSTN expression across conditions | `07_caf_trajectory` | cell-78 | Embedding colored by POSTN |
| h | RNA ISH: SFRP1, WNT5A, MMP11 | — | — | Experimental (RNAscope/ISH) |
| i | Kaplan-Meier DFS curves | `06_survival_analysis` | cell-8, cell-12 | KM by response group / spatial features |
| j | TCGA validation (POSTN, KRAS) | `06_survival_analysis` | cell-18, cell-19 | POSTN boxplot + KM curve |

### Fig. 6 — Trajectory inference reveals bifurcation of CAFs into NR and pCR branches
| Panel | Description | Notebook | Cell | Notes |
|-------|-------------|----------|------|-------|
| a | Isomap embedding with STORIES potential & velocity | `07_caf_trajectory` | cell-23, cell-48 | Potential on isomap + velocity stream |
| b | Fate probability: NR CAF & pCR CAF on embedding | `07_caf_trajectory` | cell-33, cell-35 | Isomap + spatial scatter of fate probs |
| c | Violin: Pre Other CAF fate prob by Response | `07_caf_trajectory` | cell-37 | Mann-Whitney U test, NR vs CR |
| d | Per-patient spatial fate maps (5 patients) | `07_caf_trajectory` | cell-42, cell-43 | `fate_prob_NR_CAF` on spatial coords |
| e | Driver gene trends (NR & CR branches) | `07_caf_trajectory` | cell-65–68 | `stories.tools.plot_gene_trends` |

### Fig. 7 — Molecular function of tumor interacting with NR CAF
| Panel | Description | Notebook | Cell | Notes |
|-------|-------------|----------|------|-------|
| a | Spatial scatter: NR CAF Neighbor vs Non-neighbor tumor | `11_tumor_neighbor_analysis` | cell-26 | Delaunay-based neighbor identification |
| b | DEG volcano: Neighbor vs Non-neighbor tumor | `11_tumor_neighbor_analysis` | cell-36 | `Neighbor_NR_CAF_neighbor_volcano_integrate.png` |
| c | Per-patient pathway enrichment heatmap | `11_tumor_neighbor_analysis` | cell-41 | Hallmark pathway heatmap |
| d | Per-patient LR interaction heatmap | `12_ligand_receptor_analysis` | cell-40, cell-41 | Curated LR (WNT, TGF-β, TNF, Notch, etc.) |
| e | LR significant spots spatial visualization | `12_ligand_receptor_analysis` | cell-31 | `st.pl.ccinet_plot` per-patient |
| f | LR network diagram | `12_ligand_receptor_analysis` | cell-20 | `st.pl.ccinet_plot` network |

---

## Supplementary Figures

### Suppl. Fig. 1 — Marker genes and inter-patient variability
| Panel | Description | Notebook | Cell | Notes |
|-------|-------------|----------|------|-------|
| a–b | UMAP by Sample/Timepoint | `01_major_cluster_annotation` | cell-11 | `01_umap_sample_timepoint.png` |
| c–e | Major cluster marker gene expression | `01_major_cluster_annotation` | cell-10 | Feature plots |

### Suppl. Fig. 2 — Subclusters and annotations
| Panel | Description | Notebook | Cell | Notes |
|-------|-------------|----------|------|-------|
| a | Stromal/CAF subcluster dot plot (top DEGs + markers) | `02_subcluster_annotation` | cell-24 | `02_dotplot_stromal_markers.png` |
| b | T cell subcluster dot plot | `02_subcluster_annotation` | cell-25 | `02_dotplot_tcell_markers.png` |
| c | Myeloid subcluster dot plot | `02_subcluster_annotation` | cell-26 | `02_dotplot_myeloid_markers.png` |
| d–e | Tumor subcluster dot plot + pathway UMAPs | `03_tumor_analysis` | cell-7, cell-12 | Marker genes + Hallmark pathways |

### Suppl. Fig. 3 — Normalized abundance of subclusters across response groups and timepoints
| Panel | Description | Notebook | Cell | Notes |
|-------|-------------|----------|------|-------|
| a | Density (cells/μm²) line plots: Stromal, T cell, Myeloid | `05_temporal_dynamics` | cell-22, cell-18, cell-20 | Per-subcluster temporal dynamics |
| b | Proportion (fraction) line plots: Stromal, T cell, Myeloid | `05_temporal_dynamics` | cell-22, cell-18, cell-20 | Same cells, proportion metric |

### Suppl. Fig. 4 — Spatial distribution and LR interactions among NR CAFs, myeloid, and tumor
| Panel | Description | Notebook | Cell | Notes |
|-------|-------------|----------|------|-------|
| a | SKNY distance-from-tumor distributions (KDE) | `04_spatial_neighborhood_analysis` | cell-13 | `04_skny_distance_distributions.png` |
| b | LIANA LR dot plot | `04_spatial_neighborhood_analysis` | cell-18 | `04_liana_lr_dotplot.png` |
| c | Longitudinal neighborhood enrichment | `04_spatial_neighborhood_analysis` | cell-21 | `04_longitudinal_nhood_dynamics.png` |
| d | Per-patient LR heatmap (all pairs) | `12_ligand_receptor_analysis` | cell-38, cell-39 | Raw + normalized counts |

### Suppl. Fig. 5 — Identification of NR CAFs and fibroblast, and molecular function of pCR CAFs
| Panel | Description | Notebook | Cell | Notes |
|-------|-------------|----------|------|-------|
| a | Reactome enrichment (down in NR CAF / up in Fibroblast) | `10_caf_spatial_distribution` | cell-34 | Blue bars, top 15 terms |
| a | CR CAF neighbor DEG volcano (NR patients) | `11_tumor_neighbor_analysis` | cell-53 | CR CAF neighbor analysis |
| a | CR CAF neighbor DEG volcano (MPR patients) | `11_tumor_neighbor_analysis` | cell-61 | MPR CR CAF neighbor analysis |

### Suppl. Fig. 6 — Additional trajectory analyses of CAF bifurcation
| Panel | Description | Notebook | Cell | Notes |
|-------|-------------|----------|------|-------|
| a | Velocity stream colored by Timepoint_Response | `07_caf_trajectory` | cell-49 | Pre_NR, Pre_CR, Resection_NR, Resection_CR |
| b | Branch assignment on isomap | `07_caf_trajectory` | cell-59 | NR_branch vs CR_branch velocity |
| c | TF enrichment (TRRUST) for NR and CR branches | `07_caf_trajectory` | cell-74–75 | Transcription factor analysis |

### Suppl. Fig. 7 — Identification of tumor cells interacting with NR CAFs and associated signaling
| Panel | Description | Notebook | Cell | Notes |
|-------|-------------|----------|------|-------|
| a | Per-patient spatial scatter of NR CAF neighbors | `11_tumor_neighbor_analysis` | cell-22 | Loop over samples |
| b | Per-cell pathway enrichment spatial maps | `11_tumor_neighbor_analysis` | cell-32 | EMT, Hypoxia, etc. on spatial |
| c | Non-canonical WNT pathway bubble plot | `11_tumor_neighbor_analysis` | cell-45 | Per-patient enrichment |

### Suppl. Fig. 8 — Graphical summary
| Panel | Description | Notebook | Cell | Notes |
|-------|-------------|----------|------|-------|
| — | Graphical abstract | — | — | Illustrative (PowerPoint/Illustrator) |

---

## Notebooks Not Directly Producing Main Figure Panels

| Notebook | Role |
|----------|------|
| `03_tumor_analysis` | Suppl. Fig. 2d–e (tumor subclusters, pathway scoring) |
| `09_skny_gridding` | Preprocessing (gridding); outputs used by notebooks 10, 11, 12 |
