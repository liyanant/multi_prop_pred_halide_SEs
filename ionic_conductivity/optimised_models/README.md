# Optimised ionic conductivity classifier models

## Key information
The optimised models prepared can be used directly for the model training step. The models can be loaded using pycaret's `load_model` function. For the Skorch Neural Networks, the model architecture needs to be defined and initialised first before the model can be loaded. Users may refer to lines 14-15 of this code (Link: https://github.com/pranaymodukuru/pycaret-with-skorch/blob/main/pycaret-skorch-example.ipynb). The only difference to be made is changing the value of `num_inputs` in line 14 to `len(X.columns)`.
