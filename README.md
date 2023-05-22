# Resilient Federated-Learning

This repo implements constrained and resilient federated learning under heterogenous local distributions generated by class imbalance. It is based on [the official implementation](https://github.com/shenzebang/Federated-Learning-Pytorch.git) of [An Agnostic Approach to Federated Learning with Class Imbalance](https://scholar.google.com/scholar_url?url=https://openreview.net/pdf?id=Xo0lbDt975&hl=en&sa=X&ei=3GtrZNG1IqqSy9YPk7-DqA8&scisig=AGlGAw8Hf-y-Jo4Xga6-OhQK4V5t&oi=scholarr) (Shen et al., ICLR 2022).

By default, all results are logged to weights and biases.

  ## Installation

To create a new environment and install dependencies using conda, run
```
conda create -f environment.yaml
```
Additional requirements can be installed with pip by running:
```
pip install -r requirements.txt
```
## Running experiments

```
python -m run_PD_FL.py <arguments>
```
Tu run the constrained algorithm use `--formulation 'imbalance-fl'` and `--formulation 'imbalance-fl-res'` to run the resilient one.

All other arguments can be found in `config.py`, or by running
```
python -m run_PD_FL.py --help
```

We have added the following hyperparameters for our algorithm:

 - `perturbation_lr`: Learning rate for the relaxation u.
 - `perturbation_penalty`: Coefficient alpha in the quadratic relaxation cost.

  
## Paper experiments
### Bash Scripts
Bash scripts for reproducing all experiments on the paper can be found on the folder `scripts`.

### Plots
In the folder `plots`, we include Jupyter notebooks that pull the results from W&B and make the plots included in the paper.