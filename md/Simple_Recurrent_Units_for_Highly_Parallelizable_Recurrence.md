# Simple_Recurrent_Units_for_Highly_Parallelizable_Recurrence
## Questions
- TODO
## Abstract
- Common recurrent neural architectures scale poorly due to the `intrinsic difficulty in parallelizing their state computations`.
- SRU is designed to provide expressive recurrence, enable highly parallelized implementation, and comes with `careful initialization` to facilitate training of deep models.
- SRU achieves 5-9x speed-up over cuDNN-optimized LSTM on clasification and question answering datasets, and delivers stronger results than LSTM and convolutional models.
## Introduction
- The difficulty of scaling recurrent networks arises from the time dependence of state computation.
- The design of SRU is inspired by previous efforts, such as Quasi-RNN and Kernel NN.
- SRU benefits
    - SRU exhibits the same level of parallelism as convolution and feed-forward nets.
    - SRU replaces the use of convolutions, as in QRNN and KNN, with more recurrent connections.
    - SRU improves the training of deep recurrent models by employing highway connections and a parameter initialization scheme tailored for gradient propagation in deep architectures.
## Simple Recurrent Unit
- The complete architecture decomposes to two sub-components: `a light recurrence` and `a highway network`.