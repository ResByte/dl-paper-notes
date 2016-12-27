# Batch Normalization

paper: https://arxiv.org/abs/1502.03167

Title: "Batch Normalization: Accelerating Deep Network Training by Reducing Internal Covariate Shift"

During learning of a deep neural network using mini-batches of inputs, the parameters of each layer are updated after a batch. This update in parameters results into change in the distribution of inputs to each further layers and is termed as 'Internal Covariate Shift'.(Changing distribution of inputs of learning system results in 'Covariate Shift').  As a result of this, convergence rate of training slows down and it tends to saturate.
Sergey et al. proposed "Batch Normalization" method to reduce this internal covariate shift by normalizing and fixing mean and variance of layer inputs. This normalization results into independence from gradients scale or initializations. Some of the additional modification to accelerate network are increasing learning rate, remove dropout, reduce the L2 weight regularization, accelerate learning rate decay, shuffle training examples, reduce photo metric distortion.

Finally, some advantages of BatchNorm
- adds 2 extra parameters per activation.
- networks can be trained with saturating non-linearities.
- more tolerant to increasing learning rates. 
- do not require dropout for regularization.    
