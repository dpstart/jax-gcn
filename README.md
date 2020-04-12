# Graph Convolutional Networks in JAX

This repository implements GCNs in JAX (check it out on [github](https://github.com/google/jax)). The code contains the model definition of a Graph Convolutional Network with two graph convolutional layers, following the model used in the paper [Semi-Supervised Classification with Graph Convolutional Networks](https://arxiv.org/abs/1609.02907).

## Usage
Run 

```python train.py```

to train a model on the Cora dataset.

## Good to know
Sparse matrix multiplication is not supported by JAX at the moment. This means that this implementation is currently using a standard matrix multiplication by the adjacency matrix to propagate the nodes' features. A sparse version of this operation would likely speed things up and reduce the amount of memory used.