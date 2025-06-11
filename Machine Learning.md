

Neural Networks

RandomForestRegressors

## Time-Series Modelling:


- **Order matters**: Today’s price depends on yesterday’s.
    
- **Observations are not independent**: Unlike regular ML tasks, each row depends on past rows.
    
- **We often care about future prediction**: Forecasting is the goal, not just classification

When it comes to Deep Learning for Time Series we can use:

#### Recurrent Neural Networks (RNN)

- Designed to handle sequences of data
    
- Can learn temporal relationships

RNNs process a **sequence of data one step at a time**, and **remember information** from previous steps through a hidden state.

- Input: a sequence
    
- At each time step, it processes one value and updates an internal memory ("hidden state")
    
- The same weights are reused at each time step


- **Vanishing gradients**: As sequences get long (e.g. 30+ days), the memory of early inputs fades — training becomes unstable
    
- **Short memory**: Not great at remembering long-term dependencies

#### LSTM (Long Short-Term Memory)

- A special kind of RNN that remembers long-term dependencies
    
- Perfect for stock trends, sensor readings, etc.

LSTM is a **special kind of RNN** designed to fix the short memory problem.

- **Input gate**: Decides what new info to store
    
- **Forget gate**: Decides what old info to drop
    
- **Output gate**: What to pass forward

#### Transformer Models

- State-of-the-art in NLP and now time-series
    
- Better at long sequences, parallelisable

Instead of processing data step-by-step like RNNs, Transformers **look at the entire sequence at once** using **self-attention**.

Each time step can "pay attention" to all other steps — the model learns **which points in the past matter most**.

- **Encoder** (for understanding the input sequence)
    
- **Self-Attention Layers**
    
- **Positional Encoding** (so it knows the order of the sequence)