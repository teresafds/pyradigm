# Pyradigm: PYthon based data structure to improve Dataset's InteGrity in Machine learning workflows

[![status](http://joss.theoj.org/papers/c5c231486d699bca982ca7ebd9cf32d2/status.svg)](http://joss.theoj.org/papers/c5c231486d699bca982ca7ebd9cf32d2)
[![travis](https://travis-ci.org/raamana/pyradigm.svg?branch=master)](https://travis-ci.org/raamana/pyradigm.svg?branch=master)
[![Codacy Badge](https://api.codacy.com/project/badge/Grade/cffd80f290544e2e824011bfccf35ff8)](https://www.codacy.com/app/raamana/pyradigm?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=raamana/pyradigm&amp;utm_campaign=Badge_Grade)
[![PyPI version](https://badge.fury.io/py/pyradigm.svg)](https://badge.fury.io/py/pyradigm)
[![Python versions](https://img.shields.io/badge/python-3.5%2C%203.6-blue.svg)]
[![codecov](https://codecov.io/gh/raamana/pyradigm/branch/master/graph/badge.svg)](https://codecov.io/gh/raamana/pyradigm)



## Upgrade your life with pyradigm

Pyradigm is an open source data structure for biomedical data and features, designed to link multiple tables of mixed data types to improve dataset integrity and ease of use.


The illustration below describes the full functionality of `pyradigm` in the latest version `0.6`, for which docs will be updated shortly (see below illustration for docs):

![flyer.png](docs/flyer.png)

The value of pyradigm is even more appreciated in the management of multi-modal feature sets, which becomes more efficient and easier to manage.

![multimodalflyer.png](docs/flyer_multimodal.png)

## Installation

Install pyradigm in a local environment executing:

`pip install pyradigm`


## Getting Started

First import the pyradigm class

```python
from pyradigm import ClassificationDataset as ClfDataset
dataset = ClfDataset()
dataset.description = 'Iris data'
```

Then, load the dataset using iris data in ARFF format.

```python
from scipy.io import arff
data = arff.loadarff(‘example_datasets/iris.arff')
for id, sample in enumerate(data[0]):
	dataset.add_samplet(id,sample[1], sample[4])
```


## Usage and more examples

Usage notebook (no setup required): [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/raamana/pyradigm/master?filepath=docs%2Fusage.ipynb)

Check more about Pyradigm on the [documentation](http://pyradigm.readthedocs.io),
and for more details in [usage](http://pyradigm.readthedocs.io/docs/usage.html)

## Contributing
Contributions are welcome! Please refer to [CONTRIBUTING.md](./CONTRIBUTING.md) for more details.

## License
MIT

[![saythanks](https://img.shields.io/badge/say-thanks-ff69b4.svg)](https://saythanks.io/to/raamana)
