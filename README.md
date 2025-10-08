# Multi-property predictions and verifications of novel halide solid electrolytes (SEs)
This is a repository for multi-property predictions and verifications of novel halide SEs. Properties predicted include ionic conudctivity, bulk modulus (K_VRH), shear modulus (G_VRH), and electrochemical stability window (ESW) via the redox potentials.


## Key information
The codes in this work were mainly prepared and run using either Jupyter Notebook or Google Colab. Users intending to replicate this work would need to install several packages and libraries to do so. These can be installed using pip or conda.


For model developments, Pycaret, Pytorch, and Skorch should be installed<sup>1-3</sup>. For Pycaret installation, users may want to attempt doing so with `pip install pycaret[full]` first. If installation issues are encountered with regards to compatibility with Python versions starting from 3.12, users may want to use this command instead `pip install git+https://github.com/pycaret/pycaret.git@master` as a possible solution.


The training and validation datasets used in this work were prepared with the matminer library, pymatgen, and Materials Project API<sup>4-6</sup>. All the training and validation datasets used in this work contain 145 compositional attributes extracted using Matminer. Users may refer to the matminer documentation as a guide (Link: https://hackingmaterials.lbl.gov/matminer/index.html) The chemical composition is used as the required input to extract the aforementioned features. It is recommended that users prepare the training and validation datasets directly from the respective sources mentioned below:

The validation datasets are prepared and extracted from the Materials Project API<sup>4</sup>. The general screening criteria used to prepare the validation datasets are as follows:

1. Theoretical lithium-based halides
2. Band gap ≥ 1.0 eV
3. No d-block and f-block elements except Zn and Cd
4. Negative Formation Energy
5. Energy above hull ≤ 50 meV/atom
6. No Cs-containing compounds


The ionic conductivity training dataset is identical to the one used by Kang et al.<sup>7</sup>.  The mechanical properties training dataset is based off the one by Sun et al.<sup>8</sup>. The ESW training dataset is based off the work by Wang et al.<sup>9</sup>.

The optimised models for machine learning predictions and model training have been uploaded for ease of replication of this work. They can be found in the `ionic_conductivity/optimised_models`, `mechanical_properties/optimised_models`, and `ESW/optimised_models` subdirectories. To avoid issues with loading the Skorch NN ionic conductivity classification models, PyTorch versions beyond 2.5.1 should not be installed.

The main code to perform model training for predictions of the properties mentioned earlier is adapted from that by Kang et al.<sup>7</sup>. Users may refer to the original code provided in their GitHub repository.<sup>7</sup>. Link: https://github.com/kminmin/LiSSE-MP.

The main differences to the roiginal code are the addition of lines of code to perform z-score scaling of the training and validation datasets before feeding them to the models, and saving the average training performance metrics of the models besides the average test performance metrics. For Skorch NNs, the training loop is performed 3 times. Both classification and regression metrics are compatible with the main code, depending on the property being predicted (classification for ionic conductivity, and regression for ESW and mechanical properties). Users are advised to save the average training and test performance metrics in csv files (e.g. `Skorch_NN/TRAIN_ACCURACIES.csv` for classification or `Trad_ML/Reduction_potential/RED_POT_HOLDOUT_R2.csv` for regression) to produce the training and test box plots for comparison.

The snippet of code used to generate the Shapley feature importance plots is also similar to that by Kang et al. and available from their same repository<sup>7</sup>. Alternatively, users may refer to the Shapley official documentation (https://shap.readthedocs.io/en/latest/index.html) to assist with preparation of the plots.


## Authors
This repository is maintained by

- Li Yan Anthony Choong (LIYANANT001@e.ntu.edu.sg)


## References
(1) Ali, M. PyCaret: An Open Source, Low-Code Machine Learning Library in Python; 2020.

(2) Tietz, M.; Fan, T. J.; Nouri, D.; Bossan, B.; skorch Developers. Skorch: A Scikit-Learn Compatible Neural Network Library That Wraps PyTorch; 2017.

(3) Paszke, A.; Gross, S.; Massa, F.; Lerer, A.; Bradbury, J.; Chanan, G.; Killeen, T.; Lin, Z.; Gimelshein, N.; Antiga, L.; Desmaison, A.; Köpf, A.; Yang, E.; DeVito, Z.; Raison, M.; Tejani, A.; Chilamkurthy, S.; Steiner, B.; Fang, L.; Bai, J.; Chintala, S. PyTorch: An Imperative Style, High-Performance Deep Learning Library. arXiv December 3, 2019. http://arxiv.org/abs/1912.01703 (accessed 2024-09-18).

(4) Ward, L.; Dunn, A.; Faghaninia, A.; Zimmermann, N. E. R.; Bajaj, S.; Wang, Q.; Montoya, J.; Chen, J.; Bystrom, K.; Dylla, M.; Chard, K.; Asta, M.; Persson, K. A.; Snyder, G. J.; Foster, I.; Jain, A. Matminer: An Open Source Toolkit for Materials Data Mining. Computational Materials Science 2018, 152, 60–69. https://doi.org/10.1016/j.commatsci.2018.05.018.

(5) Ong, S. P.; Richards, W. D.; Jain, A.; Hautier, G.; Kocher, M.; Cholia, S.; Gunter, D.; Chevrier, V. L.; Persson, K. A.; Ceder, G. Python Materials Genomics (Pymatgen): A Robust, Open-Source Python Library for Materials Analysis. Computational Materials Science 2013, 68, 314–319. https://doi.org/10.1016/j.commatsci.2012.10.028.

(6) Jain, A.; Ong, S. P.; Hautier, G.; Chen, W.; Richards, W. D.; Dacek, S.; Cholia, S.; Gunter, D.; Skinner, D.; Ceder, G.; Persson, K. A. Commentary: The Materials Project: A Materials Genome Approach to Accelerating Materials Innovation. APL Materials 2013, 1 (1). https://doi.org/10.1063/1.4812323.

(7) Kang, S.; Kim, M.; Min, K. Discovery of Superionic Solid-State Electrolyte for Li-Ion Batteries via Machine Learning. J. Phys. Chem. C 2023, 127 (39), 19335–19343. https://doi.org/10.1021/acs.jpcc.3c02908.

(8) Sun, J.; Kang, S.; Kim, J.; Min, K. Accelerated Discovery of Novel Garnet-Type Solid-State Electrolyte Candidates via Machine Learning. ACS Appl. Mater. Interfaces 2023, 15 (4), 5049–5057. https://doi.org/10.1021/acsami.2c15980.

(9) Wang, X.; He, B.; Liu, B.; Avdeev, M.; Shi, S. A Database of Electrochemical Stability Windows Containing over 1500 Solid‐State Inorganic Compounds. Adv Funct Materials 2024, 2406146. https://doi.org/10.1002/adfm.202406146.


