# Forging new worlds (GANaxies)
### High-resolution synthetic galaxies with chained generative adversarial networks

<img src="/images/logo.png" alt="logo" width="200px"/>

This repository contains supplementary code for the paper _Forging new worlds: high-resolution synthetic galaxies with chained generative adversarial networks_ published in [MNRAS](https://doi.org/10.1093/mnras/stz602), a preprint version of which can be found on [arXiv](https://arxiv.org/abs/1811.03081).

For an easily accessible application, this repository provides the trained models for generating galaxies using our chained GAN model. Please note that you will need a functioning [PyTorch](https://pytorch.org/) installation to make use of the code.

### File description

* `generate_galaxies.py`: The user-facing Python file to create synthetic galaxy samples

* `models.py`: The DCGAN and StackGAN models used in the corresponding research and paper

* `dcgan_G.pth`: The pre-trained DCGAN generator used to create synthetic 64x64 pixel galaxy images

* `stackgan_G.pth`: The pre-trained StackGan generator used to upscale the DCGAN generator output

### Quickstart guide

Generating galaxies with the provided pretrained models works in both Python 2 and Python 3. In order to create one synthetic galaxy image, you can simply use the following command:

```shell
python generate_galaxies.py
```

If you want to create a specific number of synthetic samples, modify the `batchSize` parameter with that number:

```shell
python generate_galaxies.py --batchSize 42
```

Below, you can see a few examples of galaxy images created with the pretrained models.

<img src="/images/examples.png" alt="examples" width="600px"/>
