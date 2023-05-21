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
Seq2Seq(nn.Module)
```
Creates seq2seq model with given configuration.
