<div align="justify">

# Butterfly Similarity Network Analysis

This repository contains the complete workflow for analyzing the Leeds
Butterfly Dataset similarity network using community detection algorithms
(Louvain, Infomap, SBM). The project explores the relationship between visual
phenotype (computer vision similarity) and biological genotype (species
taxonomy), investigating how algorithms group species based on shared visual
features like texture, color, and shape.

## 🚀 Setup

1.  **Clone the repository**

    ```bash
    git clone https://github.com/RahulSandhu/butterfly-network
    cd butterfly-network
    ```

2.  **Create and activate a virtual environment**

    ```bash
    python3 -m venv .venv
    source .venv/bin/activate
    ```

3.  **Install dependencies**

    ```bash
    pip install -r requirements.txt
    ```

    _Note: This project requires `graph-tool` for SBM analysis, which may need
    specific installation steps depending on your OS._

## 📁 Dataset

The project utilizes the **Leeds Butterfly Dataset**, which comprises 832
high-resolution images covering 10 distinct butterfly species (55 to 100 images
per category). The analysis is performed on a pre-computed similarity network
where:

- **Nodes** represent individual butterfly images.
- **Edges** represent the visual similarity weight between images, calculated
  based on color, shape, and texture features.
- **Labels** correspond to the biological scientific names (e.g., _Danaus
  plexippus_, _Vanessa cardui_).

## 📊 Key Findings

Our analysis of the network structure yielded the following insights regarding
visual vs. biological classification:

- **Visual Phenotype over Genotype:** Louvain identified 7 communities based on
  visual traits rather than strict biology. For example, "Orange/Spotted" species
  (_Lycaena phlaeas_ and _Vanessa cardui_) were grouped together due to shared
  patterns, while "Dark/Velvet" species formed a separate cluster.
- **Geometric Distinctiveness:** Species defined by unique shapes, such as the
  stripes of _Heliconius charitonius_ or circular eyespots of _Junonia coenia_,
  formed the most isolated and pure communities.
- **Hierarchical Structure of "Noise":** Dendrogram analysis of the most
  heterogeneous community (Community 2) revealed a structured "High Luminance"
  group rather than random noise. The algorithm successfully distinguished a
  sub-group of faded/overexposed _Danaus plexippus_ and clustered them with
  naturally white _Pieris rapae_ based on shared brightness.

## 🎓 Acknowledgements

- Leeds Butterfly Dataset (Josiah Wang, Katja Markert, and Mark Everingham)
- Developed as part of the Complex Networks course at Universitat Rovira i
  Virgili (URV)

</div>
