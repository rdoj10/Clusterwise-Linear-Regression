# Article Repository

This repository contains the source code and real-world datasets used in the experimental evaluation presented in the article. It includes implementations of classical and adaptive clusterwise linear regression algorithms for interval-valued data, together with the complete procedures for model fitting, hyperparameter selection, and experimental evaluation.

---

# Repository Structure

The repository is organized as follows:

```text
├── Algorithm - Clusterwise Linear Regression For Interval-Valued Data.ipynb
└── Real Datasets/
    ├── Cardio.csv
    ├── Dog Breeds.csv
    ├── Unemployment.csv
    ├── ...
    └── (Toral: 16 real-world datasets)
```

* **Algorithm - Clusterwise Linear Regression For Interval-Valued Data.ipynb** contains the complete implementation of all algorithms evaluated in the article.
* **Real Datasets** contains the sixteen real-world datasets used in the experimental evaluation.

---

# Notebook Organization

The notebook is divided into three main sections.

## 1. Model Fitting

This section contains the implementations of the optimization procedures for each algorithm.

Implemented algorithms:

* **$\boldsymbol{J}_{CLRi}$**
* **$\boldsymbol{J}_{WCLRi-ED}$**
* **Adaptive variants of $\boldsymbol{J}_{WCLRi-ED}$**

Each subsection implements the corresponding model fitting algorithm described in the article.

---

## 2. Parameter Selection

This section implements the hyperparameter selection procedures.

Two validation strategies are available.

### Cross-Validation

* Parameter Selection ($\boldsymbol{J}_{CLRi}$)
* Parameter Selection ($\boldsymbol{J}_{WCLRi}$ and Variants)

### Bootstrap .632+

* Parameter Selection ($\boldsymbol{J}_{CLRi}$)
* Parameter Selection ($\boldsymbol{J}_{WCLRi}$ and Variants)

These procedures automatically select the optimal values of the hyperparameters according to the validation criterion adopted in the article.

---

## 3. Overall Algorithm

This section combines model fitting and hyperparameter selection into a complete execution pipeline.

### Cross-Validation

* Overall $\boldsymbol{J}_{CLRi}$
* Overall $\boldsymbol{J}_{WCLRi}$ and Variants

### Bootstrap .632+

* Overall $\boldsymbol{J}_{CLRi}$
* Overall $\boldsymbol{J}_{WCLRi}$ and Variants

These functions perform the complete workflow, including hyperparameter selection, model fitting, prediction, and computation of the evaluation metrics.

---

# Running the Real-World Experiments

Choose one of the datasets contained in the **Real Datasets** directory.

The validation procedure depends on the selected dataset.

### Cross-Validation

Use the **Cross-Validation** implementation for:

* Cardio
* Dog Breeds
* Unemployment

For these datasets, execute the corresponding code contained in:

* Parameter Selection → Cross-Validation
* Overall Algorithm → Cross-Validation

### Bootstrap .632+

Use the **Bootstrap .632+** implementation for all remaining real-world datasets.

For these datasets, execute the corresponding code contained in:

* Parameter Selection → Bootstrap .632+
* Overall Algorithm → Bootstrap .632+

---

# Synthetic Data Generation

Although this repository contains only the real-world datasets, the synthetic datasets used in the article can be generated directly from the notebook.

Generation procedures are provided in:

* **Section 3.2 – Synthetic Experiment 1** (Datasets 1–3)
* **Section 3.3 – Synthetic Experiment 2** (Datasets 4–7)

The notebook contains the complete code required to reproduce all synthetic datasets described in the article.

---

# Hyperparameter Configuration

Before executing the algorithms, users must specify the candidate values for:

* Number of clusters ($K$);
* Number of nearest neighbors ($k_{nn}$);
* Weighting parameter ($\alpha$).

The choice of these candidate values depends on the dataset under analysis.

To exactly reproduce the experimental results reported in the article, users should adopt the hyperparameter configurations specified in **Section 3 – Experimental Evaluation**.

---

# Implemented Algorithms

The notebook includes implementations of:

* CLRi
* WCLRi-ED
* WCLRi-ED-LC1
* WCLRi-ED-LC2
* WCLRi-ED-LC3
* WCLRi-ED-GL1
* WCLRi-ED-GL2
* WCLRi-ED-GL3

---

# Reproducing the Experiments

To reproduce the experiments presented in the article:

1. Select the dataset.
2. Define the candidate values for $K$, $k_{nn}$, and $\alpha$.
3. Choose the appropriate validation strategy (Cross-Validation or Bootstrap .632+).
4. Execute the corresponding **Overall Algorithm**.
5. Analyze the evaluation metrics produced by the notebook.

---

# Notes

* All algorithms are implemented in Python.
* The notebook contains the complete implementation of all methods evaluated in the article.
* All datasets follow a common input format compatible with every implemented algorithm.
* The notebook automatically performs model fitting, hyperparameter selection, prediction, and computation of the evaluation metrics.
* For mathematical details, optimization criteria, evaluation metrics, and the complete experimental design, please refer to the associated article.

# License

The source code contained in this repository is released under the MIT License.

The datasets included in the Real Datasets directory are not covered by the MIT License.

Datasets obtained from external sources remain subject to the licenses, terms of use, and copyright policies established by their respective original authors or data providers.

The synthetic datasets and any real-world datasets originally created by the authors of this repository are provided solely for the purpose of reproducing the experimental results presented in the associated article.

Users are responsible for verifying and complying with the licensing conditions of each dataset before using or redistributing them.
