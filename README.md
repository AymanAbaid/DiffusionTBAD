# 🩺 DiffusionTBAD: Synthetic CTA Images for Type B Aortic Dissection

**DiffusionTBAD**, a curated dataset of *synthetic* CT angiography (CTA) images for **Type B Aortic Dissection (TBAD)**. All images are generated using **text-to-image diffusion models**, aimed at enhancing research in medical imaging, anomaly detection, and synthetic data evaluation.

---

## 📋 Table of Contents

- [🧠 About the Data](#-about-the-data)
- [📦 Model Download](#-model-download)
- [🚀 How to Use the Tuned DreamBooth Model](#-how-to-use-the-tuned-dreambooth-model)
- [📌 Citing this Dataset](#-citing-this-dataset)

---

## 🧠 About the Data

- **Image Size**: 512 × 512 pixels  
- **Sampling Methods**: Euler, Euler A  
- **Image Count**: 1600 per class  
- **Modality**: Synthetic CT Angiography  
- **Condition**: Type B Aortic Dissection (TBAD)

This dataset is best suited for:
- Training and evaluating deep learning models for TBAD
- Exploring generative models in radiology
- Augmenting real-world CTA datasets

---

## 📦 Model Download

You can download the fine-tuned DreamBooth model used to generate this dataset here:

🔗 [Download DreamBooth Model (HuggingFace)](https://huggingface.co/your-model-link)  
🔗 [Sample Dataset (ZIP)](https://yourwebsite.com/download/diffusion_tbad_sample.zip)

---

## 🚀 How to Use the Tuned DreamBooth Model

To replicate or extend the dataset generation, follow the steps below to install DreamBooth and run inference using the tuned model.

### 🔧 1. Install Requirements

```bash
git clone https://github.com/huggingface/diffusers
cd diffusers
pip install -e .
pip install transformers accelerate xformers safetensors






# DiffusionTBAD

This dataset contains synthetic CT angiography (CTA) images of Type B Aortic Dissection (TBAD). All the images in this dataset are generated using a Diffusion Model.

## Table of Contents

- [About the Data](#about-the-data)
- [Citing this Dataset](#citing-this-dataset)
## About the Data

- **Image Size:** 512 x 512 pixels
- **Sampling Methods:** Euler, Euler A
- **Number of Images per Class:** 1600

This dataset is intended for research and development in the field of medical imaging, specifically for the detection and analysis of Type B Aortic Dissection.


## Citing this Dataset

If you use this dataset in your research, please cite the following paper:

> **Paper Title:** [Title of the Paper]  
> **Authors:** [Author Names]  
> **Journal/Conference:** [Journal/Conference Name]  
> **Year:** [Year]  
> **DOI:** [DOI]

Here’s the BibTeX entry for your convenience:

```bibtex
@article{your_paper,
  title={Title of the Paper},
  author={Author Names},
  journal={Journal/Conference Name},
  year={Year},
  publisher={Publisher},
  doi={DOI}
}

