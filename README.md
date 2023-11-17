# Quantum Playing

The repository contains several Jupyter Notebooks playing with two well-know library for Quantum Computing:
- Qiskit - https://github.com/Qiskit/qiskit
- Braket - https://github.com/amazon-braket/amazon-braket-sdk-python

Qiskit is mostly used to display quantum circuits and results, while Braket is used to perform tests both with Cloud simulators and Cloud QPUs on AWS.

## Installation & prerequisites
In order to use those notebooks, you need to have:
- Qiskit (I'm using v0.45)
- Braket SDK (I'm using v1.61.0)
- qiskit_qasm3_import (allows Qiskit to read OpenQASM3 programs, I use that to convert Braket circuits to Qiskit circuits)
```
pip install qiskit
pip install amazon-braket-sdk
pip install qiskit_qasm3_import
```

The `quantum_adder.ipynb` notebook, an old (and wrong) one dating from my early experiments, also make use of the `qiskit-braket-provider`
```
pip install qiskit-braket-provider
```

### Simulations and tests in the Cloud
Of course, if you plan to use AWS simulations or access real QPUs, you will also need to have programmatic access to an AWS account and provide it to the notebook.

Personally I use a cell to export environnement variables with the AK/SK/ST into the notebook Python kernel because it is a sensible approach for my situation, but that's up to you to choose any method that suits you.

## Content

- `presentation.ipynb` un notebook en français qui contient tout ce que j'ai utiliser pour générer les tests et les illustrations de la présentation faite aux GSDays 2023
- `shors-1-7n+2.ipynb` a notebook featuring a detailled explanation and construction of the famous Shor's algorithm. The circuit constructed is far from optimal but has the advantage of being easier to understand
- `shors-2-4n+3.ipynb` a notebook featuring a detailled explanation and construction of the famous Shor's algorithm. The circuit constructed is optimal given what is possible with Braket or Qiskit. It is more advanced than the other notebook but you should definitly check it out if you are interested in understanding how Shor's algorithm really works.
- `test-aria1.ipynb` a notebook featuring increasingly difficult addition circuit tested on the real-world QPU Aria (IONQ). I made these tests following the discovery that Aria was performing extremely well with a ~70 depth circuit, which was certainly a big surprise for me.
- `schemas.drawio` les quelques schémas que j'ai fait pour la présentation aux GSDays 2023.
- `qiskit/*.ipynb` notebook that where directly copied from the qiskit repository. You can find them and more at https://github.com/Qiskit/textbook/tree/main/notebooks


### Happy quantum playing!
