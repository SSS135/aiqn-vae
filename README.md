# VAE + (Conditioned) Quantile Networks for MNIST
PyTorch VAE example extended with Autoregressive Quantile Networks (though, they aren't autoregressive when applied to VAE) https://arxiv.org/abs/1806.05575

By default, writes tensorboard logs to `./tensorboard`, change with `--log-folder /log/path`. Saving just png images without tensorboard is not implemented.

With `--conditioned` argument AIQN network also receives class labels as inputs. VAE encoder / decoder does not have access to class labels.

## Requirements
PyTorch 0.4.0

tensorboard-pytorch https://github.com/lanpa/tensorboard-pytorch

## Running
Conditioned AIQN with KL regularizer `main.py --conditioned --kl-scale 1 --log-folder ./tensorboard`

No AIQN with KL regularizer (same as PyTorch example) `main.py --no-aiqn --kl-scale 1 --log-folder ./tensorboard`

## Examples

#### AIQN / no AIQN with KL regularizer. AIQN gives some improvements.
<img src="images/mnist_aiqn_kl1.png" width="300"> <img src="images/mnist_noaiqn_kl1.png" width="300"> 

#### AIQN / no AIQN without KL regularizer. Without AIQN and KL penalty generated images are mess. AIQN gives noticible improvement.
<img src="images/mnist_aiqn_kl0.png" width="300"> <img src="images/mnist_noaiqn_kl0.png" width="300"> 

#### Conditioned AIQN with / without KL regularizer.
<img src="images/mnist_aiqn_kl1_cond.png" width="300"> <img src="images/mnist_aiqn_kl0_cond.png" width="300"> 
