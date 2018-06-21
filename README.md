# AIQN-VAE
PyTorch VAE example extended with Autoregressive Quantile Networks

#### No AIQN, 1 KL penalty (same as PyTorch example)
`main.py --no-aiqn --kl-scale 1`
<img src="images/mnist_noaiqn_kl1.png" width="500">

#### AIQN, 1 KL penalty
`main.py --kl-scale 1`
<img src="images/mnist_aiqn_kl1.png" width="500">


#### No AIQN, 0 KL penalty
`main.py --no-aiqn --kl-scale 0`
<img src="images/mnist_noaiqn_kl0.png" width="500">


#### AIQN, 0 KL penalty
`main.py ---kl-scale 0`
<img src="images/mnist_aiqn_kl0.png" width="500">