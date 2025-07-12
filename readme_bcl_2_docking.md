# BCL2 Docking Project

## 🔬 Overview

This project involves molecular docking of three natural ligands — **Curcumin**, **Berberine**, and **Quercetin** — against the mutated **BCL2 (G101V)** protein using **AutoDock Vina** and visualized with **PyMOL**.

The goal is to evaluate and compare the binding affinities and docking poses of these phytochemicals as potential inhibitors of the anti-apoptotic protein BCL2, commonly implicated in cancer cell survival.

---

## 🧪 Methodology

### 1. Ligand Preparation

- Ligands: `curcumin.pdbqt`, `berberine.pdbqt`, `quercetin.pdbqt`
- Prepared and converted to `.pdbqt` format using **Open Babel**

### 2. Receptor Preparation

- Receptor: `BCL2_G101V.pdbqt`
- Mutation G101V introduced manually
- Converted to `.pdbqt` format with polar hydrogens and charges using **AutoDock Tools**

### 3. Docking Configuration

Grid box:

- Center: `X=3.664`, `Y=-4.153`, `Z=2.012`
- Size: `X=40`, `Y=40`, `Z=40`
- Exhaustiveness: `8`

Each ligand used a custom Vina config:

- `vina_config_curcumin.txt`
- `vina_config_berberine.txt`
- `vina_config_quercetin.txt`

### 4. Docking Execution

Run using **AutoDock Vina v1.2.7** via command line. Output files are saved as:

- `curcumin_out.pdbqt`
- `berberine_out.pdbqt`
- `quercetin_out.pdbqt`

### 5. Visualization

- Visualized using **PyMOL**
- PyMOL sessions saved: `.pse`
- High-resolution images saved: `.png`

---

## 📁 Folder Structure

```
Day2_Ligands/
├── receptor/
│   └── BCL2_G101V.pdbqt
├── ligands/
│   ├── curcumin.pdbqt
│   ├── berberine.pdbqt
│   └── quercetin.pdbqt
├── configs/
│   ├── vina_config_curcumin.txt
│   ├── vina_config_berberine.txt
│   └── vina_config_quercetin.txt
├── results/
│   ├── curcumin_out.pdbqt
│   ├── berberine_out.pdbqt
│   └── quercetin_out.pdbqt
├── pymol_sessions/
│   ├── curcumin_docking.pse
│   ├── berberine_docking.pse
│   └── quercetin_docking.pse
├── images/
│   ├── curcumin_docking.png
│   ├── berberine_docking.png
│   └── quercetin_docking.png
```

---

## 📊 Results Summary

| Ligand    | Best Binding Affinity (kcal/mol) |
| --------- | -------------------------------- |
| Curcumin  | -7.184                           |
| Berberine | -7.753                           |
| Quercetin | -7.574                           |

**Berberine** showed the strongest binding affinity among the three.

---

## 📌 Tools Used

- AutoDock Tools 1.5.7
- AutoDock Vina 1.2.7
- Open Babel
- PyMOL
- GitHub for version control

---

## 📚 References

- Trott, O., & Olson, A. J. (2010). AutoDock Vina: improving the speed and accuracy of docking. *J Comput Chem*, 31(2), 455-461.
- Eberhardt, J., et al. (2021). AutoDock Vina 1.2.0: New Docking Methods, Expanded Force Field, and Python Bindings. *J Chem Inf Model.*

---

## 🙋‍♂️ Author

**Sayak Ghosh**\
M.Sc. Biotechnology\
GitHub: [Sayak1007](https://github.com/Sayak1007)

---

## 📌 Note

This repository is for academic and educational purposes. Further refinement and validation may be required for publication or drug discovery pipelines.

