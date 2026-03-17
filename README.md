# Al-Ti Alloy Molecular Dynamics Simulation

This project performs a Molecular Dynamics (MD) simulation to calculate and visualize the initial atomic positions and acceleration vectors of an Aluminum-Titanium (Al-Ti) alloy. The simulation is powered by **LAMMPS** and analyzed using **Python**.

## 🚀 Features
- **Crystal Structure:** FCC lattice modeling with a lattice constant of 4.05 Å.
- **Interatomic Potential:** Modified Embedded Atom Method (MEAM) for accurate Al-Ti interactions.
- **Data Processing:** Automated calculation of acceleration matrices from force outputs ($a = F/m$).
- **Visualization:** 3D plotting of atomic species with superimposed force/acceleration vectors.

## 📁 File Structure
- `in.proje`: LAMMPS input script.
- `library.meam` & `TiAl.meam`: MEAM potential parameter files. (Obtained from this link:https://www.ctcms.nist.gov/potentials/entry/2025--Sharifi-H-Wick-C-D--Ti-Al/2025--Sharifi-H--Ti-Al--LAMMPS--ipr1.html)
- `lmp.exe`: LAMMPS executable engine.
- `output.txt`: Raw simulation data (positions and forces).
- `analysis.ipynb`: Jupyter Notebook for processing and visualization.

## 🛠️ Usage

1. **Run Simulation:**
   Open your terminal in the project directory and run:
   ```bash
   lmp.exe -in in.proje

   and you will get the output.txt file

## 📊 Results

First 5 atoms - Position values:
[[0.    0.    0.   ]
 [2.025 2.025 0.   ]
 [2.025 0.    2.025]
 [0.    2.025 2.025]
 [4.05  0.    0.   ]]
First 5 atoms - Acceleration values:
[[-0.00219766  0.00059033 -0.00039789]
 [-0.00468484 -0.00142876  0.00444855]
 [-0.0023286  -0.00114793 -0.00139445]
 [ 0.00284902 -0.00144748  0.00011059]
 [-0.00249599 -0.00036669  0.00163101]]


![3D Atomic Positions and Acceleration Vectors of Al-Ti Alloy (t=0)](image.png)
