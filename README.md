# Dataset & Supplementary Material: Influence of Burn Severity on Avifaunal Communities in Southern Tropical Dry Deciduous Forest, Western Ghats

[![DOI](https://img.shields.io/badge/DOI-10.1002%2Fece3.74098-blue.svg)](https://doi.org/10.1002/ece3.74098)
[![License: CC BY 4.0](https://img.shields.io/badge/Data_License-CC_BY_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

## Overview

This repository contains the dataset and supplementary material for the research article:

> **Influence of Burn Severity on Avifaunal Communities in Southern Tropical Dry Deciduous Forest, Western Ghats**  
> **Authors:** Rajagopal James Pradeeshwar, Kumar Parthasarathy Ramesh, Tharmalingam Ramesh, and Riddhika Kalle  
> **Journal:** *Ecology and Evolution* (2026), Vol. 16, Issue 8, e74098  
> **DOI:** [10.1002/ece3.74098](https://doi.org/10.1002/ece3.74098)



---

## Repository Contents

* **`README.md`**: Repository documentation and complete data dictionary (this file).
* **`LICENSE`**: Open-access license terms ([Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/)).
* **`Dataset.xlsx`**: Primary Excel workbook containing 7 sheets of processed species abundance, environmental covariates, guild classifications, and diversity indices.
* **`Supplementary.docx`**: Supplementary figures, diagnostic plots, model summaries, and methodological documentation referenced in the paper.

---

## Dataset Overview (`dataset.xlsx`)

The dataset comprises 120 point-count sampling stations equally distributed across four burn severity classes:
* **`H`**: High Burn Severity ($n = 30$)
* **`M`**: Moderate Burn Severity ($n = 30$)
* **`L`**: Low Burn Severity ($n = 30$)
* **`U` / `UB`**: Unburned Control ($n = 30$)

**Key Dataset Statistics:**
* **Total Bird Count:** 1,616 individuals
* **Total Species Recorded:** 56 avian species across 8 orders and 30 families

---

## Data Dictionary

`Dataset.xlsx` is structured into 7 worksheets:

### Sheet 1: `general` (Species Trait Mastersheet)
*56 rows × 9 columns — Contains taxonomic classification and ecological functional traits for all recorded species.*

| Column Name | Data Type | Example | Description |
| :--- | :--- | :--- | :--- |
| `S.No` | Integer | `1` | Serial index (1 to 56) |
| `Abbr.` | Character | `AGBE` | 4-letter standardized species code |
| `Common Name` | Character | `Asian Green Bee-eater` | English vernacular name |
| `Scientific Name` | Character | `Merops orientalis` | Taxonomic binomial name |
| `Order` | Character | `Coraciiformes` | Taxonomic order |
| `Family` | Character | `Meropidae` | Taxonomic family |
| `Feeding Substrate` | Categorical | `air` | Primary foraging stratum (`air`, `ground-vegetation`, `upper canopy`, etc.) |
| `Feeding Technique` | Categorical | `sallier` | Primary foraging maneuver (`sallier`, `gleaner`, `frugivore-granivore`, etc.) |
| `Nesting Location` | Categorical | `cavity` | Preferred nesting substrate (`cavity`, `shrub`, `canopy`, etc.) |

---

### Sheet 2: `species` (Site × Species Abundance Matrix)
*120 rows × 58 columns — Community matrix used for multivariate community analysis (NMDS, PERMANOVA).*

| Column Name | Data Type | Range / Options | Description |
| :--- | :--- | :--- | :--- |
| `Point_ID` | Character | `H01` – `U30` | Unique sampling station code |
| `Severity` | Categorical | `H`, `M`, `L`, `U` | Burn severity classes  |
| `AGBE` ... `YEBA` | Integer | $0 – 12$ | Individual abundance count for each of the 56 species across 120 stations |

---

### Sheet 3: `lm` (Linear Modeling Predictors and Covariates )
*120 rows × 16 columns — Contains point-count level biodiversity metrics and environmental predictors.*

| Column Name | Data Type | Units / Range | Description |
| :--- | :--- | :--- | :--- |
| `Point_ID` | Character | `H01` – `U30` | Unique sampling station code |
| `Severity` | Categorical | `H`, `M`, `L`, `U` | Burn severity classification |
| `Totalindividuals` | Integer | $3 – 25$ | Total avian abundance recorded per station |
| `Richness` | Integer | $3 – 18$ | Total species richness per station |
| `Shannon` | Numeric | $1.099 – 2.810$ | Shannon-Wiener diversity index ($H'$) |
| `Simpson` | Numeric | $0.600 – 0.934$ | Simpson’s diversity index ($D$) |
| `Evenness` | Numeric | $0.763 – 1.000$ | Pielou’s species evenness index ($J'$) |
| `dnbr` | Numeric | Standardized | Continuous Difference Normalized Burn Ratio (dNBR) index |
| `stdev_sev` | Numeric | Standardized | Spatial standard deviation of burn severity within grid cell |
| `Visibility` | Ordinal | $1 – 4$ | Field visibility score during sampling |
| `Weather` | Ordinal | $1 – 6$ | Weather condition score during sampling |
| `Elevation` | Numeric | $929 – 1143$ meters | Elevation above sea level |
| `Slope` | Numeric | Standardized | Terrain slope gradient |
| `Aspect` | Numeric | Standardized | Terrain aspect angle |
| `mean_ndvi_grid` | Numeric | Standardized | Mean NDVI within a grid|
| `stdev_ndvi_grid` | Numeric | Standardized | Standard deviation of NDVI within a grid|

---

### Sheets 4–7: Guild Subsets
*Contain aggregated abundance data per sampling station for specific functional guilds.*

* **`foraging_substrate-ground`** (119 stations): Abundance of ground-foraging substrate users.
* **`foraging_substrate-shrub-lower`** (109 stations): Abundance of shrub and lower-canopy foraging substrate users.
* **`foraging_substrate-generalist`** (29 stations): Abundance of generalist substrate foraging users.
* **`foraging_technique-probing`** (86 stations): Abundance of probing species.

Each guild sheet contains three columns:
1. `Point_ID`: Station code.
2. `abundance`: Total bird count within the specified guild.
3. `Severity`: Burn severity stratum (`H`, `M`, `L`, `U`/`UB`).

---

## License

This dataset and all supplementary materials are shared under the **Creative Commons Attribution 4.0 International License (CC BY 4.0)**. You are free to copy, distribute, transform, and build upon this data for any purpose, provided appropriate credit is given to the original authors and publication.

---

## Citation

If you utilize this dataset, please cite the published article:

```Standard Citation:

Pradeeshwar, R. J., K. P. Ramesh, T. Ramesh, and R. Kalle. 2026. “Influence of Burn Severity on Avifaunal Communities in Southern Tropical Dry Deciduous Forest, Western Ghats.” Ecology and Evolution 16, no. 8: e74098. https://doi.org/10.1002/ece3.74098.

```
```bibtex
@article{https://doi.org/10.1002/ece3.74098,
author = {Pradeeshwar, Rajagopal James and Ramesh, Kumar Parthasarathy and Ramesh, Tharmalingam and Kalle, Riddhika},
title = {Influence of Burn Severity on Avifaunal Communities in Southern Tropical Dry Deciduous Forest, Western Ghats},
journal = {Ecology and Evolution},
volume = {16},
number = {8},
pages = {e74098},
keywords = {burn severity, community ecology, ornithology, pyrodiversity, Western Ghats, wildfire},
doi = {https://doi.org/10.1002/ece3.74098},
url = {https://onlinelibrary.wiley.com/doi/abs/10.1002/ece3.74098},
eprint = {https://onlinelibrary.wiley.com/doi/pdf/10.1002/ece3.74098},
note = {e74098 ECE-2026-01-00008.R1},
abstract = {ABSTRACT Climate change has exacerbated the extent and severity of forest fire in biodiversity hotspots. The variation in fire regime attributes creates diverse successional stages and structures, thus offering ecological niches for species occupancy and increasing the biodiversity, thereby supporting the pyrodiversity-biodiversity hypothesis. Understanding the effects of postfire burn severity and landscape heterogeneity on bird communities is essential for developing forest fire mitigation measures in tropical protected areas. We systematically surveyed birds in 120 point counts, 5 years postfire, to represent burn severity classes (unburned, low, moderate, and high severity). We assessed the influence of burn severity (a single-fire component of pyrodiversity) on bird communities in a southern tropical dry deciduous forest of Bandipur Tiger Reserve, Nilgiri Biosphere Reserve in the Western Ghats. We calculated delta normalized burn ratio (dNBR) to classify burn severity using Landsat data. Richness, evenness, and Simpson diversity were not significant across burn severity. While Shannon diversity was marginally significant before testing the Bonferroni's correction, no individual burn severity class showed a significant difference in Shannon diversity after applying the correction. Bird community composition was significantly dissimilar between all burn severity classes (F = 4.52, p = 0.001). Among the foraging substrate guild, abundance of ground and generalist species was significantly higher in high burn severity than that of unburned. We found a significant positive relationship between burn severity (dNBR) and abundance (β = 1.41, p = 0.009) corroborating with the pyrodiversity-biodiversity hypothesis. Forest fire management should account for the landscape heterogeneity created by fire. Implementing prescribed fires in highly vulnerable areas reduces fuel loads and prevents large, high burn severity areas within the reserve. In tropical environments, this study establishes a foundational understanding of the pyrodiversity-avian diversity relationship, underscoring the necessity for future investigations employing multi-taxa and multi-scale approaches to discern underlying patterns for improving forest fire management.},
year = {2026}
}

```

---

## Contact & Inquiries

* **Rajagopal James Pradeeshwar** (First Author) — Sálim Ali Centre for Ornithology and Natural History (SACON) / Central University of Tamil Nadu
*Email:* [pradeeshwarrj@gmail.com](mailto:pradeeshwarrj@gmail.com)
* **Riddhika Kalle** (Corresponding Author) — Sálim Ali Centre for Ornithology and Natural History (SACON) / University of KwaZulu-Natal
*Email:* [riddhikalle@gmail.com](mailto:riddhikalle@gmail.com)

```

```
