# Estimating Heterogeneous Agent Models With Neural Networks
Example code for the simple 3 equation New Keynesian model with analytical solution from "Estimating Heterogeneous Agent Models With Neural Networks" by H. Kase, L. Melosi, and M. Rottner

Github Repo: https://github.com/tseep/estimating-hank-nn

**Modified by Qingyuan Fang (JHU) on Nov 20, 2024**

**In preparation for JHU Economics Machine Learning Reading Group meeting on Nov 22, 2024**

1. ''pyproject.toml'': add dependencies, delete license
   *Reference* : https://packaging.python.org/en/latest/guides/writing-pyproject-toml/
2. "solution_QY.ipynb": add more comments to the first part of the authors' notebook ("Extended Model Solution with Neural Network Approach"), and delete the second part ("Particle Filters")
   Ideal for individuals with a basic understanding of neural networks (like stochastic gradient descend) who are interested in training one using PyTorch.

# Structure of the folder

* ./examples
  * ./save
    * ./authors_backup: include the two networks trained by the authors
  * analytical.ipynb: notebook by the authors
  * solution_QY.ipynb: modified notebook by Qingyuan, focusing on using the extended NN to solve the model
* ./src/estimating_hank_nn
  * the source code (with some helper functions) by the authors

# Create a virtual environment and install the packages

After cloning the repo
```bash
git clone https://github.com/QingyuanFang/KMR22_JHUML_20241122.git
```

**Mac**

```bash
cd [your path]/KMR22_JHUML_20241122

python -m venv .venv
source .venv/bin/activate
pip install --upgrade pip
pip install .
deactivate
```

**Windows**

```bash
cd [your path]\KMR22_JHUML_20241122

python -m venv .venv
.venv\Scripts\activate
pip install --upgrade pip
pip install .
deactivate
```

***What does the code above do?***

1. First, it creates a virtual environment, named ".venv", inside the "KMR22_JHUML_20241122" folder.
   Note: on Mac, press "command+shift+." to make it visible in Finder.
2. Then, it activates that environment and installs all python packages the project requires. See the "dependencies" section in pyproject.toml. 

```
numpy
scipy
matplotlib
torch
tqdm
```

3. It also installs the package "estimating_hank_nn". It is inside the ./src folder and has some helper functions written by the authors.
4. Finally, It deactivates the environment.

# To proceed

Open solution_QY.ipynb in your favorite code editor, choose ./venv as the kernel, and you are ready to go!

# Reference
Kase, Hanno, Leonardo Melosi, and Matthias Rottner. Estimating nonlinear heterogeneous agents models with neural networks. Centre for Economic Policy Research, 2022.
