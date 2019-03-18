# Molecular_Generating_RNN-LSTM
Created a RNN with LSTM cells to learn patterns from SMILES Strings, and use them to generate new molecular structures. 

The design of the architecture I built is based off the research paper “Generative Recurrent Networks for De Novo Drug Design” by Gupta et al. It consists of two LSTM layers, each with a hidden state vector H passed through cell to cell with previous information the RNN has never seen before. More recurrent connections like this allow for the network to understand far more complex dependancies of the SMILES sequences. I also used a dropout regularization of 0.25 on these layers, followed by a dense output layer consisting of a neutron unit using the softmax activation function. Softmax is a function that takes as input a vector of K real numbers (in our case the output vector Y), and normalizes it into a probability distribution consisting of K probabilities. If you’d like to understand more about this activation function, I’d recommend the wiki page for the softmax function.

# Future Improvements and Goals
The goal of this project was to train a generative recurrent neural network to create new molecules which are similar to those presented in the given dataset. However, we do not know the validity of these molecules, so in the future I hope to address this and also design molecules with certain properties using data from certain inhibitors, a process known as Fragment-Based Drug Discovery.

This method of generating molecular designs in silico represents a way to build tailor-made molecules for specific purposes, and could potientially save millions and years of time as it becomes better developed! I'm excited to see how these method of using generative networks for molecular design continues to improve!

