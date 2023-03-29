---
layout: figure-side
figureCaption: An example of table structure recognition
figureUrl: assets/example1.png
figureFootnoteNumber: 1
---

## 1. Background

TSR (table structure recognition) task is recognizing the physical and logical structure of tables which are usually represented by image. 

The conventional digital table image recognition has been relatively mature.Recent years, some researchers have focused on more challenging table structure recognition tasks, such as **recognizing the distortion table**.

<Footnotes separator>
  <Footnote :number=1><a href="https://arxiv.org/abs/2111.13359" rel="noreferrer" target="_blank">Neural Collaborative Graph Machines for Table Structure Recognition</a></Footnote>
</Footnotes>

---
layout: figure-side
figureCaption: An example of physical structure and logical structure
figureUrl: assets/example2.svg
---

## Logical and Physical Position

The smallest unit in table recognition is text segment bounding box, and the task is to predict the position of each bounding box, in which the logical position refers to the row position (start (end) row, start (end) column), and the physical position refers to the coordinate position $(x, y, w, h)$.

---
layout: figure
figureCaption: Distorted vs Regular Table
figureUrl: assets/example3.jpg
figureFootnoteNumber: 1
---

## Distorted Table and Regular Table

<Footnotes separator>
  <Footnote :number=1><a href="https://arxiv.org/abs/2208.04921" rel="noreferrer" target="_blank">TSRFormer: Table Structure Recognition with Transformers</a></Footnote>
</Footnotes>

---
src: ./related-work.md
---

---

## Motivation

In table recognition, inductive biases of different modalities may affect the performance of the modality. 

For example, when identifying regular tables, the coordinates of tables will dominate, but when dealing with distorted tables, they will become unreliable.


---
layout: figure-side
figureCaption: Intra-modality and Inter-modality.
figureUrl: assets/intra-inter.svg
---

## Hetero-TSR Problem

Can different modalities **collaborate** with each other rather than **interfering** with each other?

Tow aspects to utilize the modalities.

- **Intra-Modality** (Among the modality)

- **Inter-Modality** (Between the modalities)