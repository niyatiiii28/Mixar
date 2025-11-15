# Mixar


# README – Mesh Normalization, Quantization & Reconstruction

## Overview
This project implements:
1. Task 1 – Extract mesh statistics (min/max/mean/std).
2. Task 2 – Normalize (Min–Max and Unit Sphere), Quantize (1024 bins), 
   and save processed meshes.
3. Task 3 – Dequantize, Denormalize, Reconstruct meshes and compute 
   reconstruction error (MSE, MAE).
4. Visualization – Using Matplotlib point clouds (.xyz converted).

All code is executed inside a single Kaggle notebook.

---

## How to Run the Code
1. Upload the notebook (.ipynb) and the input OBJ files to Kaggle.
2. Run the notebook top to bottom.
3. Outputs will be generated automatically in:
   - task2_normalized/
   - task2_quantized/
   - task3_reconstructed/
   - xyz_visuals/
   - task3_errors.csv
   - *_mse_plot.png files

4. Visualizations are generated using:
   - Matplotlib 3D scatter plots
   - XYZ files (converted from OBJ/PLY for stable Kaggle rendering)

---

## Output Files
### Meshes
- <name>_minmax.ply (Min–Max Normalized)
- <name>_unitsphere.ply (Unit Sphere Normalized)
- <name>_minmax_quantized.ply
- <name>_unitsphere_quantized.ply
- <name>_minmax_reconstructed.ply
- <name>_unitsphere_reconstructed.ply

### Plots
- <name>_mse_plot.png (per-axis MSE)
- task3_errors.csv

---

## Observations (Summary)
1. **Unit Sphere normalization preserves the mesh structure best**, due to uniform scaling.
2. **Min–Max distorts the mesh more**, especially if ranges differ across axes.
3. Quantization introduces small but visible reconstruction error.
4. Reconstruction under Unit Sphere is significantly closer to the original mesh.
5. Per-axis MSE shows Unit Sphere has balanced, lower error compared to Min–Max.

---

## Requirements
- Python 3
- numpy
- trimesh
- open3d
- matplotlib
- pandas

---

## Folder Structure (Final Submission)
submission/
│── notebook.ipynb  
│── README.txt  
│── Final_Report.pdf  
│── task2_normalized/  
│── task2_quantized/  
│── task3_reconstructed/  
│── xyz_visuals/  
│── task3_errors.csv  
│── all plots (.png)  

---

## Author
Niyati Siju  
IIT Gandhinagar
