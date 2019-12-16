# Making use of Adverserial Robustness Toolbox (ART) from IBM

This is a library is to provide a toolbox for adversarial testing. It mainly focuses on using CLEVER score as a metric to evaluate a model's robustness.

IBM's ART library is used to provide frameworks for popular Machine Learning Libraries, types of attacks, defences, metrics and verifications (including the use of CLEVER).

Documentation of ART: https://adversarial-robustness-toolbox.readthedocs.io

Details on which Machine Learning Libraries and types of attacks, defences and metrics are documented in the IBM ART github.


## Required packages

- IBM ART package: we are making use of this package to conduct testing
-

## Setup of IBM ART

### Installation with `pip`

The toolbox is designed and tested to run with Python 3. 
ART can be installed from the PyPi repository using `pip`:

```bash
pip install adversarial-robustness-toolbox
```

### Manual installation

The most recent version of ART can be downloaded or cloned from this repository:

```bash
git clone https://github.com/IBM/adversarial-robustness-toolbox
```

Install ART with the following command from the project folder `art`:
```bash
pip install .
```

ART provides unit tests that can be run with the following command:

```bash
bash run_tests.sh
```

## Citing ART

If you use ART for research, please consider citing the following reference paper:
```
@article{art2018,
    title = {Adversarial Robustness Toolbox v1.0.1},
    author = {Nicolae, Maria-Irina and Sinn, Mathieu and Tran, Minh~Ngoc and Buesser, Beat and Rawat, Ambrish and Wistuba, Martin and Zantedeschi, Valentina and Baracaldo, Nathalie and Chen, Bryant and Ludwig, Heiko and Molloy, Ian and Edwards, Ben},
    journal = {CoRR},
    volume = {1807.01069},
    year = {2018},
    url = {https://arxiv.org/pdf/1807.01069}
}
```

