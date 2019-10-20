A copy of Bindsnet for Minibatch Processing in Spiking Neural Networks.

The updates to Bindsnet for enabling minibatch processing are found in a couple key sections:

```
bindsnet/datasets
```
The datasets module provides all of the data loading mechanics including the managment of the temporal dimension in a custom batch collate function.

```
bindsnet/learning/learning.py
```
The learning module includes changes to enable the reduction across the batch dimension and minor modifications to account for the batch dimension.

```
bindsnet/network/network.py
```
Additions were made to enable management of the batch dimension in a standard way as we abstract that component of the state away from the underlying nodes themselves.

```
examples/mnist/batch_eth_mnist.py
```
Extends an example from Bindsnet to show how to utilize the changes without any of the managment layers.
