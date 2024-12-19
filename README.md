# IMDDiffusion
### Abstract

The most popular metrics for evaluation of generative models in computer vision are Fréchet Inception Distance (FID) and Kernel Inception Distance (KID). However, these metrics only capture the first two or three moments of the distribution and can be insensitive to more complex structural issues. In the paper ["The Shape of Data: A Multi-Scale Intrinsic Distance"](https://arxiv.org/pdf/1905.11141), a new method - Intrinsic Multi-scale Distance (IMD) for characterizing and comparing data manifolds is proposed. This method uses SLQ estimator to calculate the Laplacian of a KNN graph to find lower bound of the spectral Gromov-Wasserstein inter-manifold distance to evaluate GAN models. We will show that this metric can be used to evaluate the quality of diffusion models. We compared the KID, FID, and Intrinsic Manifold Distance (IMD) metrics for diffusion models on the MNIST and CIFAR-10 datasets, and found that IMD agreed with KID and FID across them. In addition, we assessed the stability and scalability of these metrics by examining their behavior with different sample sizes on the CIFAR-10 dataset.

### Usage examples and experiements
During our work we used the [pid](https://github.com/photosynthesis-team/piq) library, as well as the [open-source code](https://github.com/xgfs/imd) from the authors of the article, to calculate the aforementioned generation quality metrics (FID, KID and IMD). You can learn more about the features of metric calculation by using the demos.ipynb notebook.
1. Robustness to Gaussian Blur
  IMDDiffusion_GBlur.ipynb notebooks presents the results of an experiment to determine the stability of metrics for data noise using Gaussian noise.
2. Stability and scalability w.r.t. sample size
  IMDDiffusion_stability.ipynb demostrates the results of an experiment to determine the stability and scalability of metrics w.r.t. sample size.

### DreamFusers Team
1. Alexander Zaytsev
2. Yurii Melnik
3. Ivan Listopadov
4. Vasiliy Kakurin
5. Roman Dyachenko
