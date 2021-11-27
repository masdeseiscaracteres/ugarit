# Neural networks
## Educational resources
- Coursera Deep Learning Course by Andrew Ng: [website](https://www.coursera.org/learn/neural-networks-deep-learning) | [weekly videos compilation](https://www.youtube.com/playlist?list=PLkRLdi-c79HKEWoi4oryj-Cx-e47y_NcM)


## Network types
- Feedforward network

### Sequence models
- RNN (Recurrent Neural Network):  
  Pros:
  - Due to their design, parameters are reused in all layers. Less parameters -> easier to train.
  - Can handle arbitrarily long sequences.

  Cons:
  - Suffer from the **vanishing gradients** problem
  - May also suffer from the **exploding gradients** problem. Dealt with via **gradient clipping**.
  
  Particular cases:
  - GRU (Gated Recurrent Unit): RNN whose cells are able to decide what must be memorized and for how long via a memory gate.  
    Pros:
    - ...
  - Full GRU: includes and additional *relevance* gate.
  - LSTM (Long Short-Term Memory)
  
  - ESN (Echo State Network)
- BRNN (Birectional Neural Network)
