Version 0.5.8 (2017-05-13)
++++++++++++++++++++++++++

Fixed
-----

* Implement random sampling for Poisson

* Update some old licensing information


Version 0.5.7 (2016-11-15)
++++++++++++++++++++++++++

Fixed
-----

* Fix deterministic mappings in Mixture, which caused NaNs in results


Version 0.5.6 (2016-11-08)
++++++++++++++++++++++++++

Fixed
-----

* Remove significant reshaping overhead in Cholesky computations in linalg
  module

* Fix minor plate multiplier issues


Version 0.5.5 (2016-11-04)
++++++++++++++++++++++++++

Fixed
-----

* Fix critical plate multiplier bug in Take node. The bug caused basically all
  models with Take node to be incorrect.

* Fix ndim handling in GaussianGamma and Wishart

* Support lists and other array-convertible formats in several nodes


Version 0.5.4 (2016-10-27)
++++++++++++++++++++++++++

Added
-----

* Add conversion from Gamma to scalar Wishart

* Implement message from GaussianMarkovChain to its input parent node

* Add generic unit test functions for messages and moments

Changed
-------

* Require NumPy 1.10 or greater


Version 0.5.3 (2016-08-17)
++++++++++++++++++++++++++

Fixed
-----

* Fix package metadata handling

* Fix Travis test errors


Version 0.5.2 (2016-08-17)
++++++++++++++++++++++++++

Added
-----

* Add a node method to obtain the VB lower bound terms that contain the node

Fixed
-----

* Handle empty CLI argument lists in CLI argument parsing

* Fix handling of the two variables (Gaussian and Gamma) in GaussianGamma
  methods

* Fix minor bugs, including CGF in GaussianMarkovChain with inputs


Version 0.5.1 (2016-05-17)
++++++++++++++++++++++++++

Fixed
.....

* Accept lists as number of multinomial trials

* Fix typo in handling concentration regularization shape


Version 0.5.0 (2016-05-04)
++++++++++++++++++++++++++

Added
.....

* Implement the following new nodes:

  - Take
  - MultiMixture
  - ConcatGaussian
  - GaussianWishart
  - GaussianGamma
  - Choose
  - Concentration
  - MaximumLikelihood
  - Function

* Add preliminary support for maximum likelihood estimation (implemented only
  for Wishart moments now)

* Support multiplying Wishart variable by a gamma variable (scale method in
  Wishart class)

* Support GaussianWishart and GaussianGamma in GaussianMarkovChain

* Support 1-p operation (complement) for beta variables

* Implement random sampling for Multinomial node

* Support ndim in many linalg functions and Gaussian-related nodes

* Add conjugate gradient support for Multinomial and Mixture

* Support monitoring of only some nodes when learning

* Add diag() method to Gamma node

* Add some examples as Jupyter notebooks

Changed
.......

* Simplify GaussianARD mean parent handling

* Move documentation to Read the Docs

Fixed
.....

* Fix an axis mapping bug in Mixture (#39)

* Fix NaN issue in Mixture with deterministic mappings (#66)

* Fix Dirichlet node parent validation

* Fix VB iteration when no data given (#67)

* Fix axis label support in Hinton plots (#64)

* Fix recursive node deletion

Version 0.4.1 (2015-11-02)
++++++++++++++++++++++++++

* Define extra dependencies needed to build the documentation

Version 0.4.0 (2015-11-02)
+++++++++++++++++++++++++++

* Implement Add node for Gaussian nodes

* Raise error if attempting to install on Python 2

* Return both relative and absolute errors from numerical gradient checking

* Add nose plugin to filter unit test warnings appropriately

Version 0.3.9 (2015-10-16)
++++++++++++++++++++++++++

* Fix Gaussian ARD node sampling

Version 0.3.8 (2015-10-16)
++++++++++++++++++++++++++

* Fix Gaussian node sampling

Version 0.3.7 (2015-09-23)
++++++++++++++++++++++++++

* Enable keyword arguments when plotting via the inference engine

* Add initial support for logging

Version 0.3.6 (2015-08-12)
++++++++++++++++++++++++++

* Add maximum likelihood node for the shape parameter of Gamma

* Fix Hinton diagrams for 1-D and 0-D Gaussians

* Fix autosave interval counter

* Fix bugs in constant nodes

Version 0.3.5 (2015-06-09)
++++++++++++++++++++++++++

* Fix indexing bug in VB optimization (not VB-EM)

* Fix demos

Version 0.3.4 (2015-06-09)
++++++++++++++++++++++++++

* Fix computation of probability density of Dirichlet nodes

* Use unit tests for all code snippets in docstrings and documentation

Version 0.3.3 (2015-06-05)
++++++++++++++++++++++++++

* Change license to the MIT license

* Improve SumMultiply efficiency

* Hinton diagrams for gamma variables

* Possible to load only nodes from HDF5 results

Version 0.3.2 (2015-03-16)
++++++++++++++++++++++++++

* Concatenate node added

* Unit tests for plotting fixed

Version 0.3.1 (2015-03-12)
++++++++++++++++++++++++++

* Gaussian mixture 2D plotting improvements

* Covariance matrix sampling improvements

* Minor documentation fixes

Version 0.3 (2015-03-05)
++++++++++++++++++++++++

* Add gradient-based optimization methods (Riemannian/natural gradient or normal)

* Add collapsed inference

* Add the pattern search method

* Add deterministic annealing

* Add stochastic variational inference

* Add optional input signals to Gaussian Markov chains

* Add unit tests for plotting functions (by Hannu Hartikainen)

* Add printing support to nodes

* Drop Python 3.2 support

Version 0.2.3 (2014-12-03)
++++++++++++++++++++++++++

* Fix matplotlib compatibility broken by recent changes in matplotlib

* Add random sampling for Binomial and Bernoulli nodes

* Fix minor bugs, for instance, in plot module

Version 0.2.2 (2014-11-01)
++++++++++++++++++++++++++

* Fix normalization of categorical Markov chain probabilities (fixes HMM demo)

* Fix initialization from parameter values

Version 0.2.1 (2014-09-30)
++++++++++++++++++++++++++

* Add workaround for matplotlib 1.4.0 bug related to interactive mode which
  affected monitoring

* Fix bugs in Hinton diagrams for Gaussian variables

Version 0.2 (2014-08-06)
++++++++++++++++++++++++

* Added all remaining common distributions: Bernoulli, binomial, multinomial,
  Poisson, beta, exponential.

* Added Gaussian arrays (not just scalars or vectors).

* Added Gaussian Markov chains with time-varying or swithing dynamics.

* Added discrete Markov chains (enabling hidden Markov models).

* Added joint Gaussian-Wishart and Gaussian-gamma nodes.

* Added deterministic gating node.

* Added deterministic general sum-product node.

* Added parameter expansion for Gaussian arrays and time-varying/switching
  Gaussian Markov chains.

* Added new plotting functions: pdf, Hinton diagram.

* Added monitoring of posterior distributions during iteration.

* Finished documentation and added API.

Version 0.1 (2013-07-25)
++++++++++++++++++++++++

* Added variational message passing inference engine.

* Added the following common distributions: Gaussian vector, gamma, Wishart,
  Dirichlet, categorical.

* Added Gaussian Markov chain.

* Added parameter expansion for Gaussian vectors and Gaussian Markov chain.

* Added stochastic mixture node.

* Added deterministic dot product node.

* Created preliminary version of the documentation.
