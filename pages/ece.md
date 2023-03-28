---
layout: figure-side
figureCaption: ECE Module Architecture
figureUrl: images/ece1.png
---

## ECE Module

Ego Context Extractor module (ECE) is used to extract the context information of intra modality. The feature of modality that input ECE will be constructed as a graph.

This input $\mathbf{C}_{(l-1)}^{\sim}$ is copied into two copies, one as the **Query** input to CMHA and the other into the Graph building module to model the intra-modality context which is taken as Keys $\mathbf{K}$ and values $\mathbf{V}$.

---
layout: figure
figureCaption: Graph Building Module
figureUrl: images/build-graph1.svg
---

## ECE Module

$\mathbf{G}^{\sim}=$ $\{\mathcal{V}, \mathcal{E}\} \in\left\{\mathbf{G}^{\mathrm{G}}, \mathbf{G}^{\mathrm{A}}, \mathbf{G}^{\mathrm{C}}\right\}$. The nodes in $\mathcal{V}$ is the node (cell) feature set, and $\mathcal{E}$ is the full connected graph edge set.

---
layout: figure
figureUrl: images/build-graph1.svg
---

## ECE Module

Authors adopt the following asymmetric edge function to combine graph edge features to each node.


<Footnotes separator>
  <Footnote :number=1><a href="https://zh.wikipedia.org/wiki/%E5%85%8B%E7%BD%97%E5%86%85%E5%85%8B%E7%A7%AF" rel="noreferrer" target="_blank">Kronecker product operator</a></Footnote>
</Footnotes>

---
layout: figure-side
figureCaption: Compressed Multi-head Attention Module
figureUrl: images/cmha1.png
---

## CMHA Module

Compressed Multi-Head Attention (CMHA) module which has been verified that it makes few assumptions about inputs and can learn to combine local behavior and global behavior on input stream.

---
layout: figure-side
figureCaption: Compressed Multi-head Attention Module
figureUrl: images/cmha1.png
---

## CMHA Module

In order to reduce the amount of computation caused by too many dimensions, we introduce a memory compression module. In addition, we also introduce residual links to make the query information ﬂow unimpeded.

$$
\begin{aligned}
& \mathbf{Y}=A d d \& \operatorname{Norm}(F F N(\widetilde{\mathbf{P}}), \widetilde{\mathbf{P}}) \\
& \widetilde{\mathbf{P}}=A d d \& \operatorname{Norm}(\mathbf{Q}, \mathbf{P}) \text {, } \\
& \mathbf{P}=M H A(\mathbf{Q}, M C(\mathbf{K}), M C(\mathbf{V})) \text {, } \\
&
\end{aligned}
$$