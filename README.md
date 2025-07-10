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


💡 It's recommended to use a virtual environment and a CUDA-compatible GPU for faster inference.

---

🧪 2. Load the Fine-Tuned DreamBooth Model

from diffusers import StableDiffusionPipeline
import torch

pipe = StableDiffusionPipeline.from_pretrained(
    "your-hf-username/tbad-dreambooth-model",
    torch_dtype=torch.float16
).to("cuda")

prompt = "Computed Tomography Angiography Type-B aortic dissection data with true Lumen"
image = pipe(prompt).images[0]
image.save("tbad_sample.png")

---

⚙️ 3. Run Batch Generation (Optional)
You can loop over a set of prompts to generate large-scale datasets.

---

📌 Citing this Dataset
If you use DiffusionTBAD in your research, please cite the following:

Paper Title: [Title of the Paper]
Authors: [Author Names]
Conference: [Conference or Journal Name]
Year: [Year]
DOI: [DOI]

📚 BibTeX
bibtex
Copy
Edit
@article{your_paper,
  title={Title of the Paper},
  author={Author Names},
  journal={Conference or Journal Name},
  year={2025},
  publisher={Publisher},
  doi={DOI}
}


