**Diffusion-Based Generation of Novel Linkers for Antibody-Drug Conjugates (ADCs)**
This repository contains the code, data, and supplementary materials for the research paper:

**Generating Novel Linker Structures in Antibody-Drug Conjugates with Diffusion Models**  
*April Cao and Jake Y. Chen*  
[Western Canada High School, University of Alabama at Birmingham]

## 🧪 Overview

Antibody-drug conjugates (ADCs) are next-generation cancer therapeutics. A critical yet challenging component of ADC design is the *linker*, which determines payload release, stability, and systemic toxicity.

We introduce a **conditional diffusion model** that learns to generate *novel linker SMILES strings* optimized for a given antibody and payload context. Our framework outperforms baseline generative models in multiple pharmacological properties including predicted **toxicity (LD50)**, **bioavailability**, and **synthetic accessibility**.

## 🚀 Features

- ✅ Diffusion-based conditional generation of ADC linkers
- ✅ High-dimensional featurization using:
  - ESM-2 for antibody sequences
  - NLP-based n-gram encoding for SMILES
- ✅ Decoder trained to ensure SMILES validity (RDKit validation)
- ✅ Benchmarking against GPT-2 baseline and FDA-approved linkers
- ✅ Molecular property evaluation via ProTox-3.0 and SwissADME

## 📁 Repository Structure

```
.
├── data/           # Preprocessed dataset and sample embeddings
├── model/          # Diffusion model training scripts and checkpoints
├── decoder/        # SMILES decoder and tokenization logic
├── evaluation/     # Property evaluation and visualization scripts
├── figures/        # Figures used in the manuscript
├── notebooks/      # Jupyter notebooks for analysis and prototyping
├── utils/          # Helper functions and preprocessing utilities
├── README.md       # Project overview (this file)
└── requirements.txt # Python package requirements
```

---

## ⚙️ Setup Instructions

### 1. Clone the repository

```bash
git clone https://github.com/your-username/adc-diffusion-linkers.git
cd adc-diffusion-linkers
```

### 2. Create and activate a virtual environment

```bash
python -m venv venv
source venv/bin/activate        # macOS/Linux
# OR
.\venv\Scripts\activate         # Windows
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```
### 4. Download datasets and pretrained models

To replicate our results or run inference, download the processed ADC dataset and model weights from:  
📎 [Insert Zenodo or Google Drive link here]

---

## 🔄 Reproducing Our Results

### Generate a novel linker for an antibody + payload pair:

```bash
python model/inference.py --antibody heavy_chain.fasta light_chain.fasta \
                          --payload payload.smiles \
                          --output output_linker.smiles
```
### Evaluation
To evaluate generated linker structures, copy and paste the SMILES strings into ProTox-3.0 (https://tox.charite.de/protox3/) and SwissADME (https://www.swissadme.ch/)

## 📄 Paper

The preprint version of the paper is available at:  
📄 [Insert bioRxiv link here]

### Citation

```bibtex
@misc{cao2025adc,
  author = {Cao, April and Chen, Jake Y.},
  title = {Generating Novel Linker Structures in Antibody-Drug Conjugates with Diffusion Models},
  year = {2025},
  howpublished = {arXiv preprint arXiv:XXXX.XXXXX}
}
```

---

## 🤝 Acknowledgments

Supported by **NIH UM1TR004771** and the **UAB Systems Pharmacology AI Research Center (SPARC)**.  
Special thanks to the **AlphaMind Club** for supporting student-led research in biomedical AI.

---

## 📬 Contact

**April Cao (student researcher):** aprilcao3@gmail.com 
**Prof. Jake Y. Chen (PI, UAB DBIDS):** jakechen@uab.edu
---

## 📜 License

MIT License  
*Last updated: April 2025*
