# CS6910-Deep-Learning-3

## Overview:

In this assignment I have made a model sequence2sequence learning problems using Reccurent Neural Networks. Then I also have compared different cells such as RNN, LSTM and GRU. I also worked with attention and understood the working and also observed that attention netwroks generally overcomes effeciently the limitations of vanilla sequence2sequence models. For this assignment I have used Aksharantar Dataset which contains a word in native script and it's corresponding transliteration in the Latin script. I have used Python for my implementation and have used the required packages from PyTorch and also used several required libraries. I ran my code on kaggle.

## Working:

I have built the RNN based seq2seq model which contains the input layer, one encoder, one decoder which takes the last state of the encoder as input and produces one output character at a time. This code is flexible for RNN, LSTM and GRU. Then I trained my model using hindi language from Aksharantar Dataset and for good accuracy I ran over the sweep feature in wandb which are given as follows:

### Hyperparameters:

1. Epochs: [5,10,15]
2. Batch Size: [64,128,256]
3. Embedding Size: [16, 32, 64, 256]
4. Hidden Size: [16, 32, 64, 256]
5. Encoder Layers: [1,2,3],
6. Decoder Layers: [1,2,3],
7. Cell Type: ["LSTM","RNN","GRU"],
8. Bi-Directional: ["Yes"],
9. Dropout: [0.2,0.3],
10. Attention: ["No"]

I also used unique strategy to save my time which I already discussed in report and after that I got the best configuration which is given as follows:

### Best Configuration:

1. Epochs: [15]
2. Batch Size: [128]
3. Embedding Size: [64]
4. Hidden Size: [256]
5. Encoder Layers: [3],
6. Decoder Layers: [3],
7. Cell Type: ["GRU"],
8. Bi-Directional: ["Yes"],
9. Dropout: [0.3],
10. Attention: ["No"]

After that I have calculated the test accuracy using my best model and I was getting that above 30 which can be considered as good one. Then I used attention which I have not used earlier. By doing I enhanced the effeciency of model and it started giving better result.
