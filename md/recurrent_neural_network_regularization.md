# Recurrent Neural Network Regularization
## Abstract
- We present a simple regularization technique for Recurrent Neural Networks(RNNs) with Long-Short Term Memory(LSTM) units - Dropout.
## Introduction
- The Recurrent Neural Network(RNN) is **neural sequence model** that achieves state of the art performance on import tasks that include **language modeling, speech recognition, and matchine translation**.
## Related Work
- Conventional dropout does not work well with RNNs because the recurrence amplifies(扩大) noise, which in turn hurts learning.
## Regularizing RNNs with LSTM Cell
- The LSTM has complicated dynamics that allow it to easily "memorize" information for an extended number of timesteps. The "long term" memory is stored in a vector of `memory cell`.
- The main idea is to apply the dropout operator only to the non-recurrent connections.
- The dropout operator corrupts the information carried by the units, forcing them to perform their intermediate computations more robustly. At the same time, we do not want to erase all the information from the units. It is especially important that the units remember events that occurred many timesteps in the past.