---
layout: figure-side
figureCaption: ICDAR 2013 Partial and ICDAR 2019
figureUrl: images/result1.png
---
## 3. Result

Evaluation setting: Different methods utilize different information. Some methods use the cell/text bounding box, while others do not. Therefore, they design two different steps:
   
- **Step A**: Only with table image
- **Step B**: Along with the cell/text segment bounding box and text content

<Footnotes separator>
  <Footnote>P: Precision, R: Recall, F1: F1 score. Metric: IoU(Coincidence ratio between the predicted area and the target area)</Footnote>
</Footnotes>

---
layout: figure
figureCaption: SciTSR and SciTSR-COMP
figureUrl: images/result2.png
---
## 3. Result

<Footnotes separator>
  <Footnote>P: Precision, R: Recall, F1: F1 score. Metric: IoU(Coincidence ratio between the predicted area and the target area)</Footnote>
</Footnotes>
---
layout: figure-side
figureCaption: Logical structure recognition
figureUrl: images/result3.png
---
## Result

$$
\operatorname{TEDS}\left(T_a, T_b\right)=1-\frac{\operatorname{EditDist}\left(T_a, T_b\right)}{\max \left(\left|T_a\right|,\left|T_b\right|\right)}
$$

where $EditDist$ denotes tree-edit distance, and $|T|$ is the number of nodes in $T$. The table recognition performance of a method on a set of test samples is defined as the mean of the TEDS score between the recognition result and ground truth of each sample.$^{[1]}$

<Footnotes separator>
  <Footnote :number=1><a href="https://arxiv.org/pdf/1911.10683">Image-based table recognition: data, model, and evaluation</a></Footnote>
</Footnotes>