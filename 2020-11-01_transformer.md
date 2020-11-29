# Attention is all you need

## Abstract
- propose a new simple network architecture, the Transformer
- experiments show these models to be superior in quality while being more parallelizable and requiring significantly less time to train
- the Transformer generalizes well

## Model Architecture
![](figs/2020-11-01_transformertrpmn18for310r_20-18-11-12.png)

- Input Embedding, Output Embeding has the same embeding layer.
- Positional Encoding
  - no convolution, no recurrence, so no use of sequence order
  ![](figs/2020-11-01_transformertrpmn44for380r_20-18-11-02.png)
- multi-head attention 
![](figs/2020-11-01_transformertrpmn26for430r_20-18-11-59.png)
![](figs/2020-11-01_transformertrpmn55for420r_20-18-11-48.png)

    > the authors suspect that for large values of $d_k$, the dot products grow large in magtitude, pushing the softmax function into regions where it has extremely gradients. To counteract this effect, they scale the dot products by $\frac{1}{\sqrt{d_k}}$

    >  In "encoder-decoder attention" layers, the queries come from the previous decoder layer, and the memory keys and values come from the output of the encoder.

## Why self-attention
![](figs/2020-11-01_transformertrpmn20for170r_20-19-11-56.png)