# CS6910 - DL_Assignment 3
***
Name -  Raj Mahajan 


Roll Number -  CS22M067
***

## Instruction for Assignment 3

### Objective -

The objective is to create a feedforward neural network structure that includes backpropagation and allows for the selection of available optimizers, activation functions, and loss functions. The model will be tested on the Fashion-MNIST dataset.

### Report link -  https://api.wandb.ai/links/rajmahajan24/qrl098dt

### Model parameters - 
# default parameters with attention and without attention
cell_type = "GRU" | "GRU"

bidirectional = True | False

enc_layers = 1 | 5

dec_layers = 1 | 5

batch_size = 256 | 256

embedding_size = 384 | 256

hidden_size = 384 | 512
 
enc_dropout = 0 | 0

dec_dropout = 0 | 0

attention = True | False


### Model functions -

#### run_NN()
```
def run_NN():
```
This function takes the pareameters from user or sweep_config and then calls the function neural_network() with that parameters.

#### neural_network()
```
neural_network(cell_type, bidirectional, enc_layers, dec_layers, batch_size, embedding_size, hidden_size, enc_dropout, dec_dropout, attention)
```
This function takes the parameters and calls the appropriate intitlizer then optimizer on which neural network is trained. Finally computers accuracy on test data. 

#### Accuracy()
```
Accuracy(model, english_matrix, marathi_matrix, epoch, batch_size)
```
Computes the accuracy of predicted words with respect to ground truth (If whole word is matched then only it is considerd as correct)


#### Seq2Seq()
```
class Seq2Seq(nn.Module)
```
Creates seq2seq model with given configuration.

#### Encoder()
```
class Encoder(nn.Module)
```
Calls the encoder with given configuration

#### Decoder()
```
class Decoder(nn.Module)
```
Calls the decoder without attention with given configuration

#### Atten_decoder()
```
class Atten_decoder(nn.Module)
```
Calls the decoder with attention and with given configuration

#### matrix_to_words()
```
matrix_to_words(model, english_matrix, marathi_matrix, batch_size, data_type)
```
Converts predicted output vector to actual readable words.

#### word2vec()
```
word2vec(word, lang)
```
Takes actual word and type of language as input and converts it into matrix of words.
