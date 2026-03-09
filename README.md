# 🩺 DiffusionTBAD: Synthetic CTA Images for Type B Aortic Dissection

**DiffusionTBAD** is a curated dataset of *synthetic* CT angiography (CTA) images focused on **Type B Aortic Dissection (TBAD)**. All images are generated using **text-to-image diffusion models**, providing a resource for advancing research in medical imaging, anomaly detection, and synthetic data augmentation.

---

## 📋 Table of Contents

- [🧠 About the Data](#-about-the-data)
- [📦 Model Download](#-model-download)
- [🚀 How to Use the Tuned DreamBooth Model](#-how-to-use-the-tuned-dreambooth-model)
- [📌 Citing this Dataset](#-citing-this-dataset)
- [🙌 Acknowledgements](#-acknowledgements)
- [📫 Contact](#-contact)

---

## 🧠 About the Data

- **Image Size**: 512 × 512 pixels  
- **Sampling Methods**: Euler, Euler A  
- **Image Count**: 1600 per class  
- **Modality**: Synthetic CT Angiography  
- **Condition**: Type B Aortic Dissection (TBAD)

This dataset is best suited for:
- Training and evaluating deep learning models for TBAD
- Exploring generative diffusion models in radiology
- Augmenting real-world CTA datasets with rare pathological examples

---

## 📦 Model Download

You can download the fine-tuned DreamBooth model and example data here:

- 🔗 [**Download DreamBooth Model (HuggingFace)**](https://huggingface.co/your-model-link)  
- 📁 [**Sample Dataset (ZIP)**](https://yourwebsite.com/download/diffusion_tbad_sample.zip)

---

## 🚀 How to Use the Tuned DreamBooth Model

To replicate or extend the dataset generation, follow these steps:

### 🔧 1. Install Requirements

```bash
git clone https://github.com/huggingface/diffusers
cd diffusers
pip install -e .
pip install transformers accelerate xformers safetensors
💡 It's recommended to use a virtual environment and a CUDA-compatible GPU for faster inference.

🧪 2. Load the Fine-Tuned DreamBooth Model
python
Copy
Edit
from diffusers import StableDiffusionPipeline
import torch

pipe = StableDiffusionPipeline.from_pretrained(
    "your-hf-username/tbad-dreambooth-model",
    torch_dtype=torch.float16
).to("cuda")

prompt = "Computed Tomography Angiography Type-B aortic dissection data with true lumen"
image = pipe(prompt).images[0]
image.save("tbad_sample.png")
⚙️ 3. Run Batch Generation (Optional)
To generate a large number of CTA images, you can loop through a list of prompts or metadata tags.

python
Copy
Edit
prompts = [
    "CTA of Type B Aortic Dissection, sagittal view, high contrast",
    "Aortic dissection with true and false lumen clearly visible",
    "Synthetic angiogram of TBAD with contrast dye"
]

for idx, p in enumerate(prompts):
    image = pipe(p).images[0]
    image.save(f"tbad_sample_{idx}.png")

---

## 📌 Citing this Dataset
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
@INPROCEEDINGS{10782969,
  author={Abaid, Ayman and Ali Farooq, Muhammad and Hynes, Niamh and Corcoran, Peter and Ullah, Ihsan},
  booktitle={2024 46th Annual International Conference of the IEEE Engineering in Medicine and Biology Society (EMBC)}, 
  title={Synthesizing CTA Image Data for Type-B Aortic Dissection using Stable Diffusion Models},
  doi={10.1109/EMBC53108.2024.10782969}}



🙌 Acknowledgements
""
📫 Contact
For questions, dataset access, or collaborations, please contact:
a.abaid1@universityofgalway.ie
muhammadali.farooq@universityofgalway.ie






