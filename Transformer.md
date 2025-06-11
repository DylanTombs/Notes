


## Attention

![[Screenshot 2025-06-11 at 20.30.31.png]]

## Positional Encoding

It injects **sequence order information** using a deterministic function (usually sine & cosine) into the embeddings, so the model can differentiate position `1` from position `50`

![[Screenshot 2025-06-11 at 20.44.19.png]]

## Encoder Layer

Initially it computes attention scores for the input sequence (`Q=K=V=x`). Applying a `mask` (optional): Prevents attending to future tokens (for decoders) or padding. It then applies a dropout which randomly zeros out activations to prevent overfitting. It applies this to the original input and then normalises the result. 

For the next stage that result is passed into the forward feed which non-linear transforms each token independently. This is then applied similarly, dropout and then normalising with the dropout. 

### Dropout

Randomly masks activations during training (scaled to preserve expected magnitude) where it scales according to the rate given. This prevents overfitting. 

## Input Embedding

The embedding matrix is created, taking random variables from a normal distribution. These are scaled to prevent large variance in initial embeddings, which can destabilise training. 

The forward pass takes a batch of input tokens with each value being the token ID. Each ID retrieves the corresponding dimensional row in the embedded matrix
