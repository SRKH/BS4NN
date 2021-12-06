# BS4NN

The implementation of BS4NN presented in "Kheradpisheh, S.R., Mirsadeghi, M. & Masquelier, T. BS4NN: Binarized Spiking Neural Networks with Temporal Coding and Learning. Neural Processing Letters (2021). https://doi.org/10.1007/s11063-021-10680-x", availbale at: https://link.springer.com/article/10.1007/s11063-021-10680-x. it is also available on arXiv at https://arxiv.org/abs/2007.04039.
  
You need to install Cupy package to work with GPU. You can install it on your own machine by the following command:

`$ sudo pip install cupy`

## Pretrained on MNIST
The pre-trained wight matrices of the first and second layers are respectively available in W0_binary.npy and W1_binary.npy files. 

## Paper abstract
We recently proposed the S4NN algorithm, essentially an adaptation of backpropagation to multilayer spiking neural networks that use simple non-leaky integrate-and-fire neurons and a form of temporal coding known as time-to-first-spike coding. With this coding scheme, neurons fire at most once per stimulus, but the firing order carries information. Here, we introduce BS4NN, a modification of S4NN in which the synaptic weights are constrained to be binary (+1 or -1), in order to decrease memory (ideally, one bit per synapse) and computation footprints. This was done using two sets of weights: firstly, real-valued weights, updated by gradient descent, and used in the backward pass of backpropagation, and secondly, their signs, used in the forward pass. Similar strategies have been used to train (non-spiking) binarized neural networks. The main difference is that BS4NN operates in the time domain: spikes are propagated sequentially, and different neurons may reach their threshold at different times, which increases computational power. We validated BS4NN on two popular benchmarks, MNIST and Fashion-MNIST, and obtained reasonable accuracies for this sort of network (97.0% and 87.3% respectively) with a  negligible accuracy drop with respect to real-valued weights  (0.4% and 0.7%, respectively). We also demonstrated that BS4NN outperforms a simple BNN with the same architectures on those two datasets (by 0.2% and 0.9% respectively), presumably because it leverages the temporal dimension. 
