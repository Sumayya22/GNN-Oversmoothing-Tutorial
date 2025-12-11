# Understanding Oversmoothing in Graph Neural Networks  
### Tutorial and Experimental Demonstration Using a Manual PyTorch GCN

**Author:** Sumayya  
**Course:** 7PAM2021-0901-2025 - Machine Learning and Neural Networks 
**Student ID:** 24069633
**Year:** 2025  
**Assessment:** Individual Assignment: Machine Learning Tutorial  

---

## Overview

This repository contains the code, figures, and supporting documentation for the tutorial titled:

**“Understanding Oversmoothing in Graph Neural Networks: A Visual and Intuitive Tutorial.”**

The tutorial investigates the oversmoothing phenomenon in Graph Neural Networks (GNNs) using a controlled synthetic dataset and a manually implemented Graph Convolutional Network (GCN) in PyTorch.  
The aim is to provide a clear, visual explanation of how node representations evolve as message-passing depth increases, and why oversmoothing causes embeddings to collapse in deep GNNs.

The accompanying PDF tutorial, located in the `tutorial/` folder, provides a comprehensive written explanation of concepts, methodology, and results.

---

## Repository Structure

```
GNN-Oversmoothing-Tutorial/
│── gnn_oversmoothing_tutorial.ipynb      # Main notebook (full experiment)
│── requirements.txt                       # Python environment dependencies
│── README.md                              # Project documentation
│── LICENSE                                # MIT License
│── .gitignore                             # Files to be excluded from Git
│
│── figures/                               # Generated visual outputs
│     ├── graph_structure.png
│     ├── embeddings_layer1.png
│     ├── embeddings_layer2.png
│     ├── embeddings_layer4.png
│     ├── embeddings_layer8.png
│     ├── embeddings_layer16.png
│     └── embeddings_layer32.png
│
│── tutorial/
│     └── GNN_Oversmoothing_Tutorial.pdf   # Final written tutorial
```

---

## Running the Project

### 1. Install Dependencies

Run the following command:

```bash
pip install -r requirements.txt
```

The environment uses only CPU-compatible libraries (PyTorch, NumPy, NetworkX, Matplotlib, Scikit-learn).

### 2. Launch the Notebook

Start Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```
gnn_oversmoothing_tutorial.ipynb
```

Execute all cells in sequence.  
All figures will be displayed inline and saved to the `figures/` folder.

---

## Methodology Summary

### 1. Synthetic Graph Construction
A Stochastic Block Model (SBM) generates a graph with four distinct communities, enabling clear observation of how message passing affects node embeddings.

### 2. Manual GCN Implementation
A Graph Convolutional Network is implemented manually in PyTorch, without using external GNN libraries. This highlights the underlying mechanics of graph convolution, neighborhood aggregation, and feature propagation.

### 3. Depth-Based Embedding Visualisation
Node features are propagated across multiple GCN layers (1, 2, 4, 8, 16, 32).  
PCA is used to project embeddings into two dimensions for visualization.

### 4. Oversmoothing Demonstration
At shallow depths, communities remain separable.  
At greater depths, embeddings converge toward similar values, demonstrating oversmoothing.

---

## Reproducibility

The notebook fixes all relevant random seeds:

- Python `random`
- NumPy
- PyTorch (CPU/GPU where applicable)

PyTorch deterministic backend options are also enabled to ensure consistent results when re-running the notebook.

---

## Accessibility Considerations

The project includes several accessibility-oriented design decisions:

- Colorblind-friendly visual palette  
- Distinct marker shapes in PCA plots  
- High-contrast styling  
- Readable font sizes  
- Structured PDF headings supporting screen-reader navigation  

These decisions align with accessibility guidelines in the assignment rubric.

---

## License

This project is released under the **MIT License**, allowing reuse for educational and research purposes.  
See the `LICENSE` file for full terms.

---

## Contact

For project inquiries:

Name: Sumayya
Your University: University Of Hertfordshire 
Email: sum90285@gmail.com
