# 🧬 AI-Accelerated Molecular Docking with DiffDock — NVIDIA NIM Microservices

> A curated collection of Jupyter notebooks demonstrating end-to-end drug discovery and biomolecular workflows powered by **NVIDIA NIM Microservices**.

---

## 📖 Overview

This repository provides example workflows for AI-accelerated computational biology, spanning **protein structure prediction**, **molecular docking**, **molecule generation**, and **guided optimization** — all using NVIDIA's NIM (NVIDIA Inference Microservices) APIs.

Whether you're a researcher, bioinformatician, or ML engineer, these notebooks offer a hands-on starting point for integrating state-of-the-art AI models into your drug discovery pipeline.

---

## 📂 Notebooks

| # | Notebook | Description |
|---|----------|-------------|
| 1 | **Boltz-2 NIM** | Biomolecular structure prediction using the Boltz-2 model |
| 2 | **GenMol NIM** | Fragment-based molecule generation |
| 3 | **AlphaFold2 NIM** | Predict 3D protein structure with AlphaFold2 |
| 4 | **DiffDock NIM** | Predict protein-ligand 3D interactions using DiffDock |
| 5 | **MolMIM NIM (Notebook)** | Guided molecule generation with custom oracles |
| 6 | **MolMIM NIM Client** | Client-side guided molecule generation with custom oracles |
| 7 | **MolMIM Guided Optimization API** | Advanced guided optimization via the MolMIM API |

---

## 🚀 Getting Started

### Installation

```bash
# Clone the repository
git clone https://github.com/<your-username>/ai-molecular-docking-nim.git
cd ai-molecular-docking-nim

# Install dependencies
pip install -r requirements.txt

# Launch Jupyter
jupyter notebook
```

### API Key Setup

Set your NVIDIA NIM API key as an environment variable before running any notebook:

```bash
export NVIDIA_API_KEY="your_api_key_here"
```

Or add it directly in the notebook where prompted.

---

## 🧪 Workflow Summary

```
Input Protein/Ligand
        │
        ▼
┌───────────────────┐
│  Structure        │  ← AlphaFold2 NIM / Boltz-2 NIM
│  Prediction       │
└────────┬──────────┘
         │
         ▼
┌───────────────────┐
│  Molecule         │  ← GenMol NIM / MolMIM NIM
│  Generation       │
└────────┬──────────┘
         │
         ▼
┌───────────────────┐
│  Molecular        │  ← DiffDock NIM
│  Docking          │
└────────┬──────────┘
         │
         ▼
┌───────────────────┐
│  Guided           │  ← MolMIM Guided Optimization API
│  Optimization     │
└───────────────────┘
```

---

## 📋 Notebook Details

### 1. 🔬 Biomolecular Structure Prediction — Boltz-2 NIM
Predict the 3D structure of proteins and biomolecular complexes using the Boltz-2 model via NIM API. Ideal for understanding binding sites and preparing inputs for docking.

### 2. 🧩 Fragment-based Molecule Generation — GenMol NIM
Generate novel small molecules using fragment-based approaches. Useful for hit identification and scaffold hopping in early drug discovery.

### 3. 🏗️ 3D Protein Structure Prediction — AlphaFold2 NIM
Leverage AlphaFold2 through NVIDIA NIM to predict high-accuracy 3D protein structures from amino acid sequences.

### 4. ⚗️ Protein-Ligand Docking — DiffDock NIM
Use the DiffDock diffusion model to predict 3D binding poses of small molecule ligands to target proteins — the core workflow of this repository.

### 5 & 6. 🎯 Guided Molecule Generation — MolMIM NIM
Generate molecules guided by custom oracle functions (e.g., docking scores, ADMET properties). Available as both a standalone notebook and a client implementation.

### 7. 🔄 MolMIM Guided Optimization API
Advanced molecule optimization using the MolMIM API with custom scoring functions for property-guided molecular design.

---

## 📁 Repository Structure

```
├── notebooks/
│   ├── 01_boltz2_structure_prediction.ipynb
│   ├── 02_genmol_fragment_generation.ipynb
│   ├── 03_alphafold2_protein_structure.ipynb
│   ├── 04_diffdock_protein_ligand.ipynb
│   ├── 05_molmim_guided_generation.ipynb
│   ├── 06_molmim_nim_client.ipynb
│   └── 07_molmim_guided_optimization_api.ipynb
├── utils/
│   └── helpers.py
├── requirements.txt
├── LICENSE
└── README.md
```

---

## 🛠️ Dependencies

Key Python packages used across notebooks:

```
nvidia-nim-client
biopython
rdkit
py3dmol
matplotlib
pandas
requests
```

See `requirements.txt` for the full list.

---

## 🤝 Contributing

Contributions are welcome! Please open an issue or submit a pull request for:
- Bug fixes
- New workflow notebooks
- Documentation improvements

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

## 🔗 References & Resources

- [NVIDIA NIM Documentation](https://docs.nvidia.com/nim/)
- [NVIDIA BioNemo](https://www.nvidia.com/en-us/clara/bionemo/)
- [DiffDock Paper (arXiv)](https://arxiv.org/abs/2210.01776)
- [AlphaFold2 Paper](https://www.nature.com/articles/s41586-021-03819-2)
- [MolMIM Paper](https://arxiv.org/abs/2208.09016)

---

<div align="center">
  <sub>Built with ❤️ using NVIDIA NIM Microservices</sub>
</div>
