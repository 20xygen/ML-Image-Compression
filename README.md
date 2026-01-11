# ML Image Compression

This repository contains a machine learning project focused on **neural network–based image compression**.  
The project explores convolutional autoencoder architectures, architectural design choices, and evaluation metrics for image reconstruction quality.

The main research and experiments are presented in [ImageCompression_part_1.ipynb](ImageCompression_part_1.ipynb) and [ImageCompression_part_2.ipynb](ImageCompression_part_2.ipynb).
The final model architecture is separated into [Tenet.ipynb](Tenet.ipynb) for clarity and reuse.

---

## Project Structure

```
├── ImageCompression.ipynb # Main research notebook
├── Tenet.ipynb # Core model architecture
├── data/ # Dataset
├── models/ # Saved models, weights, training statistics
├── results/ # Benchmarks, metrics, and visual results
└── README.md
```

---

## Frameworks

- PyTorch  
- Torchvision
- Optuna
- Pandas
- Numpy
- TorchMetrics

---

## Dataset

The project uses the **Flickr Image Dataset** from Kaggle:

https://www.kaggle.com/datasets/hsankesara/flickr-image-dataset

---

## Results Summary

- Simple CNN autoencoders achieve acceptable MSE (and thus PSNR) but suffer from visual artifacts.
- Batch Normalization improve training stability.
- Residual Blocks significantly reduce artifacts.
- Tone correction mechanism based on skip-connections improves color accuracy.
- The family of SSIM metrics provide more informative quality assessment than MSE alone.

The final model achieves a reasonable trade-off between compression rate and visual quality.
