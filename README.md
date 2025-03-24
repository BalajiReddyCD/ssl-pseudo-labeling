# Semi-Supervised Learning with Pseudo-Labeling

This repository contains the code, tutorial, and resources for implementing a **Semi-Supervised Learning** approach using **Pseudo-Labeling** on the **CIFAR-10** dataset in PyTorch.

## 📌 Project Overview

In many real-world scenarios, labeled data is scarce while unlabeled data is abundant. This project demonstrates how to leverage both using a simple yet powerful method — **pseudo-labeling**.

We simulate a semi-supervised environment:
- Use only 1,000 labeled CIFAR-10 images (100 per class)
- Treat the remaining 49,000 images as unlabeled
- Train a baseline CNN model
- Generate pseudo-labels with high-confidence predictions
- Retrain with combined labeled + pseudo-labeled data

## 📂 Files Included

- `pseudo_labeling_cifar10.ipynb`: Final Colab-ready notebook with all code and fixes
- `semi_supervised_learning_tutorial.html`: HTML version of the tutorial
- `README.md`: Project overview and instructions
- `LICENSE`: Open-source license (MIT)

## 📊 Results

| Model                  | Test Accuracy |
|------------------------|----------------|
| Supervised (1000 labels) | ~45–50%        |
| With Pseudo-Labeling     | ~60–65%        |

## 🚀 Run This Notebook in Google Colab

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/BalajiReddyCD/ssl-pseudo-labeling/blob/main/pseudo_labeling_cifar10.ipynb)

## 📚 References

- Oliver et al. (2018). [Realistic Evaluation of Deep Semi-Supervised Learning Algorithms](https://arxiv.org/abs/1804.09170)
- Berthelot et al. (2019). [MixMatch](https://arxiv.org/abs/1905.02249)
- Sohn et al. (2020). [FixMatch](https://arxiv.org/abs/2001.07685)
- Miyato et al. (2018). [Virtual Adversarial Training](https://arxiv.org/abs/1704.03976)
- PyTorch CIFAR-10 Tutorial: [Link](https://pytorch.org/tutorials/beginner/blitz/cifar10_tutorial.html)

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).

## 🙋‍♂️ Personal Reflection

Creating this project helped me move beyond the theory of semi-supervised learning into hands-on practice.
Implementing pseudo-labeling taught me how models can learn effectively from confident predictions on unlabeled data.
I also learned the importance of thresholding, balanced datasets, and careful combination of data sources.
Debugging the training loop and fixing type errors was challenging but rewarding. I now feel better prepared
to apply SSL methods in real-world scenarios where labeled data is scarce.
