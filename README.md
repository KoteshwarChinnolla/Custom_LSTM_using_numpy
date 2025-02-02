So here we go, 

Adjusting weights has proven to be effective in all deep-learning neural network architectures. So, I believe Adjusting weights has always been a key to good accuracy and greater functioning. basically, every architecture differs from each other by the way they have been assigned weights and the way these weights are changed. 

Starting from a basic Neural network architecture like a perceptron to complex architectures like Transformers. there have always been weights and biases. Being able to understand any NN architecture is not that complex when we look at it from the perspective of adjusting weights and the way these weights have been assigned. 

So coming to LSTM which is applicable for time series data or continuous data flows. it might be NLP understanding a continuous series of words(sentence) or any IOT time serious sensor data. Before understanding LSTM let's look at the RNNs. So RNNs don't have the concept of memory and basically, it's a block where a time series data is processed.

Here is an example "YouTube is a great source of learning"

As I mentioned RNN is a block so in this block we have a number of RNNs (same as sentence length) each RRN is capable of of processing one input. so first RNN cell process the input be "YouTube" and then the next RNN input be "is" and then "a" and so on until the last word. 

Let's understand what's inside one RNN block. this block takes two inputs they are current time stamp input and the output of the previous RNN block. so every RNN block can process a single input that input is first added to the previous state output and both together will be passed through an activation function and the result from the activation function will be then sent as an output for the next state. this process continues until the last word of the sentence. 

**How RNNs learn?** Until now we just looked at the forward pass. so before knowing how it learns let's understand **what actually it learns**. so this basically let's look at the human perspective. someone reading the sentence he/she can only understand the next words when he/she remembers the context of previous words. RNNs need to learn how to remember these and understand the whole sentence. to make this learn we must focus more on the previous context and present context. so basically the weights that must be focused here are one from the previous layer and one from the current layer. Previous layer weights are adjusted to make it pass maximum information to the next layer and present layer weights are adjusted to make it understand the importance of the current word. 

![RNN image](https://images.datacamp.com/image/upload/v1647442110/image6_f6vds6.png)

LSTM is a kind of RNN architecture. let us understand **what makes it different from RRN?** . when we certainly test the RNNs it might not be that accurate in remembering the context of the previous word. because if we consider a long sentence it will be very difficult to remember what is the relation between the first and last word is just because there is no separate memory cell assigned to it. How can someone remember if there is no memory valid right. to solve this case the LSTM comes into the picture.

![LSTM](https://github.com/KoteshwarChinnolla/Custom_LSTM_using_numpy/blob/main/images/lstn.png?raw=true)

The LSTMs outperform RNNs when it comes to remembering the previous context. this is majorly due to the addition of memory cell C(t). important information from every cell will be stored or added to it and retrieved when processing for oputputs.

Like RNNs it is all similar that how the sentence or time series data will be sent to this LSTM block. the difference comes in the architecture of the cell. we have three gates. this discribed as forget gate, Input gate and output gate. where each has its own supperate functionality's. comming to memory LSTM have cell state which differentiate it from RNN.

![lstm basic](https://github.com/KoteshwarChinnolla/Custom_LSTM_using_numpy/blob/main/images/Lstm-Basic.png?raw=true)

![lstm basic](https://github.com/KoteshwarChinnolla/Custom_LSTM_using_numpy/blob/main/images/forget_gate.png?raw=true)

![lstm basic](https://github.com/KoteshwarChinnolla/Custom_LSTM_using_numpy/blob/main/images/input_gate.png?raw=true)

![lstm basic](https://github.com/KoteshwarChinnolla/Custom_LSTM_using_numpy/blob/main/images/output_gate.png?raw=true)
