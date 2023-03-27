---
layout: figure
figureCaption: Modality Fusion Abalation Study
figureUrl: assets/ablation1.png
---
## Ablation Study of Modality Fusion

<Footnotes separator>
  <Footnote>P: Precision, R: Recall, F1: F1 score. Metric: IoU(Coincidence ratio between the predicted area and the target area)</Footnote>
</Footnotes>

---
layout: figure
figureCaption: Modality Fusion Abalation Study
figureUrl: assets/ablation2.png
---
## Ablation Study of Multi-Modality

<Footnotes separator>
  <Footnote>P: Precision, R: Recall, F1: F1 score. Metric: IoU(Coincidence ratio between the predicted area and the target area)</Footnote>
</Footnotes>

---

## Thinking about modalities collaboration

- What does ECE learn from the intra-modality?

Separate attention heads may learn to look for various relationships between inputs and introducing more sparsity and diversity for attention may improve performance and interpretability$^1$.

- How do different modalities collaborate with each other?

Multi-head Attention.

<Footnotes separator>
  <Footnote :number=1><a href="" rel="noreferrer" target="_blank">Sparse and constrained attention for neural machine translation.</a></Footnote>
</Footnotes>