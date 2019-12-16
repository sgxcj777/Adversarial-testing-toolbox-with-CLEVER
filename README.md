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

### CLEVER metric in ART library
Using the CLEVER metric function in ART library requires a few predetermined parameters that we need to set to sample points and estimate the CLEVER metric. In order to use the function, the model has to be wrapped in a classifier provided by ART library. Details on how to wrap the model for each model framework is explained in the example folders.

### Computing of CLEVER score
```metrics.clever_u``` is used to evaluate CLEVER score for untargetted attacks.
```metrics.clever_t``` is used to evaluate CLEVER score for targetted attacks.
#### Usage
##### official documentation: <a href="https://adversarial-robustness-toolbox.readthedocs.io/en/latest/modules/metrics.html">click here</a> or <a href="https://arxiv.org/pdf/1807.01069.pdf"> click here</a>

```metrics.clever_u(classifier, x, nb_batches, batch_size, radius, norm, c_init=1, pool_factor=10)```

<ul>
    <li><b>classifier</b> (classifier) - classifier object we wrapped above</li>
    <li><b>x</b> (np.ndarray) - input sample (typically use x_test)</li>
    <li><b>nb_batches</b> (int) - Number of repetitions to estimate CLEVER</li>
    <li><b>batch_size</b> (int) - Number of random examples to sample per batch</li>
    <li><b>radius</b> (float) - ball of radius of the maximum perturbation</li>
    <li><b>norm</b> (int) - norm of gradient x (current support by ART: 1,2,np.inf</li>
    <li><b>c_init</b> (float) – initialization of Weibull distribution (default=1)</li>
    <li><b>pool_factor</b> (int) – The factor to create a pool of random samples with size pool_factor x n_s (default=10)</li>
</ul>

#### Predetermined parameters
Using the authors' predetermined values, we will use the following parameters:
- nb_batches = 50
- batch_size = 10
- radius = 5
- norm = 1

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

