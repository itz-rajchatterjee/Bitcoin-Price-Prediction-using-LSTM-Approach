LSTM basically solves the problem of Short Term Memory.
Its is a special type of RNN approach.
As in case of simple RNN approach the hidden states are passed with vectors and sigma operation is performed with the weighed sum of the vectors and tanh operation is done,
which gives us a new hidden state.
When the LSTM approach is implemented a few extra steps are performed in each cell states among them the first is "Forget Gate" and before passing to teh forget gate here
sigmoid function is applied and it basically converts all the values to either 0 or 1 and thus to discard the previous memory if a vector containing all zeros is encountered
it takes in the new input and discards the previous one.
Now to add more inputs to the cell a concept of input gate comes which implements both sigmoid and tanh (+ bias factor if present) functions to add new inputs in 
the memory from the weighted vectors that are passed to the cell state.
Then finally comes the output gate where weighted sum of the vectors from the hidden state and new input vectors is done and sigmoid function is applied and whatever
output is obtained it is multiplied with the long term memory value after applying tanh to it.
Thus we obtain a new hidden state.
If we want to take out the output of the current timestamp then we need to apply Softmax activation on the obtained hidden state.

