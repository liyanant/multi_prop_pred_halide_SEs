# Multi-property predictions and verifications of novel halide solid electrolytes (SEs)
Repository for multi-property predictions and verifications of novel halide SEs. Properties predicted include ionic conudctivity, bulk modulus (K_VRH), shear modulus (G_VRH), and electrochemical stability window (ESW) via the redox potentials.


## Key requirements
The codes in this work were mainly prepared using Jupyter Notebook and/or Google Colab. Users intending to replicate this work would need to install several packages and libraries to do so. These can be installed using pip or conda.


For model developments, Pycaret, Pytorch, and Skorch should be installed.


The training and validation datasets used in this work were prepared with the matminer library, pymatgen, and Materials Project API. The ionic conductivity training dataset is identical to the one used by Kang et al. The mechanical properties training dataset is based off the one by Sun et al. The ESW training dataset is based off the work by Wang et al.


## Authors
This repository and codes under it are maintained by

- Li Yan Anthony Choong (LIYANANT001@e.ntu.edu.sg)

## Key References
(1) Jain, A.; Ong, S. P.; Hautier, G.; Chen, W.; Richards, W. D.; Dacek, S.; Cholia, S.; Gunter, D.; Skinner, D.; Ceder, G.; Persson, K. A. Commentary: The Materials Project: A Materials Genome Approach to Accelerating Materials Innovation. APL Materials 2013, 1 (1). https://doi.org/10.1063/1.4812323.


(2) Kang, S.; Kim, M.; Min, K. Discovery of Superionic Solid-State Electrolyte for Li-Ion Batteries via Machine Learning. J. Phys. Chem. C 2023, 127 (39), 19335–19343. https://doi.org/10.1021/acs.jpcc.3c02908.


(3) Sun, J.; Kang, S.; Kim, J.; Min, K. Accelerated Discovery of Novel Garnet-Type Solid-State Electrolyte Candidates via Machine Learning. ACS Appl. Mater. Interfaces 2023, 15 (4), 5049–5057. https://doi.org/10.1021/acsami.2c15980.


(4) Wang, X.; He, B.; Liu, B.; Avdeev, M.; Shi, S. A Database of Electrochemical Stability Windows Containing over 1500 Solid‐State Inorganic Compounds. Adv Funct Materials 2024, 2406146. https://doi.org/10.1002/adfm.202406146.


