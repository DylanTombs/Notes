


## Attention

![[Screenshot 2025-06-11 at 20.30.31.png]]

## Positional Encoding

It injects **sequence order information** using a deterministic function (usually sine & cosine) into the embeddings, so the model can differentiate position `1` from position `50`

![[Screenshot 2025-06-11 at 20.44.19.png]]

## Encoder Layer

Initially it computes attention scores for the input sequence (`Q=K=V=x`). Applying a `mask` (optional): Prevents attending to future tokens (for decoders) or padding. It then applies a dropout which randomly zeros out activations to prevent overfitting. It applies this to the original input and then normalises the result. 

For the next stage that result is passed into the forward feed which non-linear transforms each token independently. This is then applied similarly, dropout and then normalising with the dropout. 

### Dropout
![[Screenshot 2025-06-11 at 20.44.19.png]]
Randomly masks activations during training (scaled to preserve expected magnitude) where it scales according to the rate given. This prevents overfitting. 

## Input Embedding

The embedding matrix is created, taking random variables from a normal distribution. These are scaled to prevent large variance in initial embeddings, which can destabilise training. 

The forward pass takes a batch of input tokens with each value being the token ID. Each ID retrieves the corresponding dimensional row in the embedded matrix. This is then scaled to counteract the reduction in magnitude when these embeddings are later added to positional encodings. It also preserves the relative importance of the embedding vs. positional information.

## Multi-head Attention

### Scaled Dot Product Attention

Initially the depth of each attention head is abstracted and we get the raw attention scores. This is calculated by for each sequence, multiplying q with transposed k. This produces how much each token should attend to another. This is scaled to prevent the products growing too large

A mask is applied to mask out positions (future tokens in the decoder). A value near negative infinity will give near 0 after softmax which is applied to the results of the masked values. 

These returned values are then multiplied with v, as each token becomes a weighted combination of all the other token's values. 


## Positional Encoding

Firstly, a column vector of positions of the given sequence are created, which is converted into (max_len, 1) for broadcasting. 

The div term is then created using the frequency term calculation for wavelength control that only computes for even integers and uses log-space for numerical stability. The outputted shape is now (d_model//2,)

An empty matrix is intialised of size (max_len, d_model)

We apply sine/cosine encoding to the div_terms

![[Screenshot 2025-06-11 at 20.44.19.png]]