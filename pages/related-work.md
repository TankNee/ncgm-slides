---
layout: figure-side
figureCaption: Early (Late) fusion-based method with NCGM.
figureUrl: images/structure1.svg
---

## Comparison

Traditional multi-modal fusion methods lack of attention to modal collaboration, so they do not perform well on distorted tables.

NCGM utilize **graph** to construct different modality relationship, and achieves good performance on the **distorted tables**.

---
layout: figure-side
figureCaption: Early (Late) fusion-based method with NCGM.
figureUrl: images/structure1.svg
---
## Related Work

After entering the era of deep learning, there are several main ways to identify table structure:

### Boundary extraction-based

Based on the boundary extraction technology, the table structure is identified by detecting the **horizontal and vertical separator** in the table.

### Generative model-based

This method uses the **encoder-decoder** schema to generate HTML text to represent the table structure.

---

## Related Work

After entering the era of deep learning, there are several main ways to identify table structure:

### Graph-based

This method is mainly based on the **graph** model, and describes the table structure by representing the table elements as nodes and the relationship between them as edges.

### Transformer-based multimodal

Use early fused embedding as input (VLBERT, LayoutLM etc.), and the method of using two modalities to do co-attentional fusion (ViLBERT).