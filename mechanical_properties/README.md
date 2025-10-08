# Mechanical properties predictions

The predictions of mechanical properties in this work were performed via predictions of the Voigt-Reuss-Hill averages of the bulk (K_VRH) and shear moduli (G_VRH). The predictions of both potentials were performed using the regression method. The training dataset is adapted from Sun et al.<sup>1</sup>. and contains 16503 materials from the Materials Project<sup>2</sup>. The validation dataset contains a total of 4743 materials that contain any of the 7 elements with the most negative standard reduction potentials (Li, Na, K, Ca, Mg, Al, Ba)<sup>3</sup>.

Shortlisted materials from the validation datasets are those predicted to have G_VRH ≥ 8.5 GPa and Pugh Ratio ≥ 1.75 (Pugh Ratio = K_VRH/G_VRH)


## References

(1) Sun, J.; Kang, S.; Kim, J.; Min, K. Accelerated Discovery of Novel Garnet-Type Solid-State Electrolyte Candidates via Machine Learning. ACS Appl. Mater. Interfaces 2023, 15 (4), 5049–5057. https://doi.org/10.1021/acsami.2c15980.


(2) Jain, A.; Ong, S. P.; Hautier, G.; Chen, W.; Richards, W. D.; Dacek, S.; Cholia, S.; Gunter, D.; Skinner, D.; Ceder, G.; Persson, K. A. Commentary: The Materials Project: A Materials Genome Approach to Accelerating Materials Innovation. APL Materials 2013, 1 (1). https://doi.org/10.1063/1.4812323.


(3) Flinn Scientific. Standard Reduction Potential Chart. www.flinnsci.com. https://www.flinnsci.com/standard-reduction-potential-chart/ap7041/ (accessed 2024-06-13).
