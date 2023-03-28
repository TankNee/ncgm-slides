---
layout: figure
figureCaption: The architecture of NCGM.
figureUrl: assets/structure2.png
figureFootnoteNumber: 1
---

## 2. Model Architecture

1. Three modalities: **Geometry**, **Appearance** and **Content**
2. Collaborative block: **ECE** (Intra modality) and **CCS** (Inter modality)
3. Structure prediction: **Fully connected layers**

<Footnotes separator>
  <Footnote :number=1><a href="https://arxiv.org/abs/2111.13359" rel="noreferrer" target="_blank">Neural Collaborative Graph Machines for Table Structure Recognition</a></Footnote>
</Footnotes>

---

## Feature Extraction

Three different modalities are used in the NCGM model, namely **Geometry**, **Appearance** and **Content**.

### Geometry

$\mathbf{F}^{\mathrm{G}} \in \mathbb{R}^{N \times d}$, Geometry modality mainly uses the **spatial information** of the cell.

### Appearance

$\mathbf{F}^{\mathrm{A}} \in \mathbb{R}^{N \times d}$, Appearance modality mainly uses cell **visual information**, background color, pixel information and so on.

<Footnotes separator>
  <Footnote><span class="katex mord mathnormal" style="margin-right: 0.10903em;">N</span> denotes the number of text segment bounding boxes.</Footnote>
</Footnotes>

---

## Feature Extraction

Three different modalities are used in the NCGM model, namely **Geometry**, **Appearance** and **Content**.

### Content

$\mathbf{F}^{\mathrm{C}} \in$ $\mathbb{R}^{N \times d}$, The Content modality mainly uses the **text content** of the cell.

<Footnotes separator>
  <Footnote><span class="katex mord mathnormal" style="margin-right: 0.10903em;">N</span> denotes the number of text segment bounding boxes.</Footnote>
</Footnotes>

---
layout: figure
figureCaption: Three modalities
figureUrl: assets/modality1.svg
---

## Feature Extraction

---
src: ./ece.md
---

---
src: ./ccs.md
---

---
layout: figure-side
figureCaption: Predicting the structure of the table.
figureUrl: assets/prediction1.png
---

## Structure Prediction

Based on the output embeddings 

$$
\mathbf{E}=\left\{\mathbf{e}_1, \mathbf{e}_2, \ldots, \mathbf{e}_N\right\} \in \mathbb{R}^{N \times d_e}
$$

a set of node pairs is constructed, where each element is a vector formed by two node vectors concatenate, and then predicted by the full connection layer.

$$
\mathbf{U}=\left\{\mathbf{u}_{1,1}, \mathbf{u}_{1,2}, \ldots, \mathbf{u}_{i, j}, \ldots, \mathbf{u}_{N, N}\right\} \in \mathbb{R}^{N^2 \times 2 d_e}
$$

Is to predict whether two nodes (cell) are in the same row, the same column, and to restore the table structure.

---
layout: figure
figureCaption: Post processing. Convert adjacency matrix containing relationships to spanning information.
figureUrl: assets/prediction2.png
---

## Structure Prediction