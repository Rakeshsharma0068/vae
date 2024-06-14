# Variational Autoencoder (VAE) for Breast Cancer Histopathology Slides

This project is part of CSE 5370: Bioinformatics coursework. It involves training a variational autoencoder (VAE) on breast cancer histopathology (H&E) slides using PyTorch.

## Table of Contents

- [Introduction](#introduction)
- [Requirements](#requirements)
- [Project Structure](#project-structure)
- [Setup](#setup)
- [Usage](#usage)
- [Extra Credit](#extra-credit)
- [References](#references)

## Introduction

Variational Autoencoders (VAEs) are a class of generative models that combine deep learning and probabilistic graphical models. In this project, we train a VAE to compress and reconstruct breast cancer histopathology slides.

## Requirements

- Python 3.7+
- PyTorch
- PyTorch Lightning
- Google Colab (optional, for GPU usage)
- Other dependencies are listed in `requirements.txt`

## Project Structure

The project directory is organized as follows:

vae/
├── data/
├── general/
│ ├── init.py
│ ├── datamodule.py
│ ├── dataset.py
│ ├── task.py
│ ├── train.py
├── layers/
│ ├── init.py
│ ├── components.py
├── utils/
│ ├── init.py
│ ├── download_tools.py
│ ├── image_tools.py
│ ├── os_tools.py
│ ├── stats_tools.py
├── logs/
├── main.ipynb
└── README.md

## Setup

1. **Clone the repository**:

    ```sh
    git clone https://github.com/Rakeshsharma0068/vae.git
    cd vae
    ```

2. **Install the required packages**:

    ```sh
    pip install -r requirements.txt
    ```

3. **Set up the framework**:

    - Download the `vae.zip` file provided in the coursework.
    - Unzip the file and place the contents in the `vae` directory.
    - Ensure your directory structure matches the one described above.

4. **Prepare the dataset**:

    - Open `main.ipynb` in Google Colab.
    - Change the runtime to GPU (`Runtime > Change runtime type > Hardware Accelerator > GPU`).
    - Run the notebook cells to download and prepare the dataset.

## Usage

1. **Training the VAE**:

    - Open `main.ipynb` in Google Colab.
    - Run the notebook cells to train the VAE model.
    - Adjust hyperparameters as needed and rerun the training cells.

2. **Running Scripts**:

    - You can run individual scripts using the command line or within Colab.
    - Example to run `train.py`:

      ```sh
      python general/train.py --epochs 20 --batch_size 64
      ```

## Extra Credit

For extra credit, a downstream task using the latent variables learned from the VAE can be developed and implemented. The implementation should be fully functional and generate preliminary results on a prototype dataset.

## References

- D. P. Kingma and M. Welling, “Auto-encoding variational bayes,” arXiv preprint arXiv:1312.6114, 2013.
- M. S. Nasr, A. Hajighasemi, et al., “Clinically relevant latent space embedding of cancer histopathology slides through variational autoencoder based image compression,” 2023.
