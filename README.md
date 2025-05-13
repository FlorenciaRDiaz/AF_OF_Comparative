# AF_OF_Comparative – Figures for Manuscript

**Repository for the manuscript:**  
**"Comprehensive evaluation of AlphaFold/OpenFold prediction of experimentally unresolved proteins through novel metrics"**

---

## 🧬 Authors

Florencia R. Díaz<sup>1</sup>, Juan F. Folco<sup>2</sup>, Juana Espain Ceci<sup>1</sup>, Veronica Baronetto<sup>3,4</sup>, Guadalupe Nibeyro<sup>3,4</sup>, Daniela Orschansky<sup>3,4</sup>, Juan P. Nicola<sup>5,6</sup>, Elmer A. Fernández<sup>*1,3,4,7</sup>  
<sup>*</sup>Corresponding author: [elmer.fernandez@scirelab.org](mailto:elmer.fernandez@scirelab.org)

### 📬 Contact

For questions or further information, please contact:

Florencia R. Díaz<sup>1</sup> ([florencia_diaz@mi.unc.edu.ar](mailto:florencia_diaz@mi.unc.edu.ar))

---

## 🧪 Abstract

Accurate protein 3D structure prediction is crucial for understanding diseases and drug discovery. AlphaFold has revolutionized the field, improving prediction accuracy and inspiring new methods. However, current evaluation metrics, like average iLDDT and template matching scores, may overlook critical differences between predictions, leading to potential misinterpretations.

In this study, we compared four AlphaFold 2 implementations, two OpenFold variants, and AlphaFold 3, using both conventional methods and per-residue profiles (PRPs) to perform an in-depth analysis. PRPs were generated from 239 protein sequences, including both wild-type and single amino acid variants, and examined through Bland-Altman plots and dimensionality reduction techniques.

Our findings show that generalized metrics can be misleading, while PRPs reveal variations across sequences and specific structural regions. Using AlphaFold 2 with full homology data as a reference, we demonstrate that alternative methods produce significantly different structures. Notably, Intrinsically Disordered Regions (IDR) exhibit high sensitivity, with substantial Cα positional variability due to single amino acid variants or predictor choice.

These variations impact global assessment metrics, highlighting the need for refined evaluation strategies. Our approach provides deeper insights for researchers selecting prediction methods based on available resources and intended structural applications.

---

## 📁 Repository Content

| File | Description |
|------|-------------|
| `Figures.ipynb` | Generates Figures 1–7 of the main manuscript. It compares structural models predicted by different algorithms, using both confidence and structural metrics. |
| `Suplementary_Figures.ipynb` | Contains the code to generate Supplementary Figures, expanding the main analysis. |
| `DataSource_Fig1.xlsx` to `DataSource_Fig7.xlsx` | Data files used to generate the main manuscript figures. Each corresponds to one figure. |
| `DataSource_SupFig.xlsx` | Contains the data used for supplementary figures. |
| `requirements.txt` | Python dependencies for reproducing the figures. |

---
## 📊 Notebooks for Figures and Supplementary Figures

To reproduce the plots and analysis shown in the main and supplementary figures of the manuscript, you can open the following Google Colab notebooks:


## 📊 Figures Explained

- **Figures.ipynb:**  
  Generates all main figures using prediction confidence matrices (Mx) and atomic distance matrices to compare different prediction algorithms. Data analyzed includes:
  - NIS (n = 181)
  - SGLT1 (n = 29)
  - SGLT2 (n = 29)
    
  👉 [Open in Google Colab](https://colab.research.google.com/drive/1_cmLlHairPWm_cYjn8b8csEK_BHOP_3D?usp=chrome_ntp)

- **Suplementary_Figures.ipynb:**  
  Includes figures that support the main results using the same metrics and visualizations.
  
  👉 [Open in Google Colab](https://colab.research.google.com/drive/1KavQ-f8PxlCaKXeIHLgoP1KQ4LQNN2-R?usp=chrome_ntp)

---

## 📚 Data Sources

- Wild-type sequences for human **NIS**, **SGLT1**, and **SGLT2** were obtained from **UniProt**:  
  - Q92911 (NIS)  
  - P13866 (SGLT1)  
  - P31639 (SGLT2)  

- Benign/pathogenic variants:  
  - NIS variants: compiled from Ravera *et al.* [15]  
  - SGLT1 and SGLT2 variants: manually curated from Martín, M., & Nicola, J.P. *et. al* [18]

---

## 🧩 Custom Code

For metric calculations, this repository uses the companion repository:  
👉 [`FoldComparative`](https://github.com/FlorenciaRDiaz/FoldComparative.git)

Please clone or install it as a dependency if metric computation is required.

---

## 🔁 Reproducibility

### 1. Clone the repository

```bash
git clone https://github.com/FlorenciaRDiaz/AF_OF_Comparative.git
cd AF_OF_Comparative

pip install -r requirements.txt
