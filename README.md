# INFO-H512 — Counterfactual Fairness

Reproduction of [Kusner et al.](https://arxiv.org/abs/1703.06856) (2017), *Counterfactual Fairness*, on the Law School dataset.

## Reproducing the results

Everything runs from a single notebook: [src/main.ipynb](src/main.ipynb).

1. Clone the repo.
2. Install the dependencies:

   ```bash
   pip install pandas numpy scikit-learn matplotlib seaborn pymc
   ```

3. Open [src/main.ipynb](src/main.ipynb) and run the cells top to bottom.

The notebook loads the dataset from [Data/law_data.csv](Data/law_data.csv), trains the four models (Full, Unaware, FairAdd, FairK) and produces the RMSE table and density plots from the report.

The FairK cell uses MCMC sampling with PyMC and takes a few minutes on a laptop. The other models run in seconds.
