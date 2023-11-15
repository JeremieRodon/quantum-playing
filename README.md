# Quantum Playing

The repository contains several Jupyter Notebooks playing with two well-know library for Quantum Computing:
- Qiskit - https://github.com/Qiskit/qiskit
- Braket - https://github.com/amazon-braket/amazon-braket-sdk-python

Qiskit is mostly used to display quantum circuits and results, while Braket is used to perform tests both with Cloud simulators and Cloud QPUs on AWS.

## Installation
In order to use those notebooks, you need to have:
- Qiskit (I'm using v0.45)
- Braket SDK (I'm using v1.61.0)

```
pip install qiskit
pip install amazon-braket-sdk
```

The `quantum_adder.ipynb` notebook, an old (and wrong) one dating from my early experiments also make use of the `qiskit-braket-provider`
```
pip install qiskit-braket-provider
```

Of course, if you plan to use AWS simulations or access real QPUs, you will also need to have programmatic access to an AWS account and provide it to the notebook.

Personally I use a cell to export environnement variables with the AK/SK/ST into the notebook Python kernel because that's practical for my situation, but that's up to you to choose any method that suits you.
