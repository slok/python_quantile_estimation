python_quantile_estimation
==========================

Python Implementation of Graham Cormode and S. Muthukrishnan's Effective Computation of Biased Quantiles over Data Streams in ICDE’05

    $ python setup.py install

or

     $ pip install git+https://github.com/slok/python_quantile_estimation

Example of how to use it:

    data = [3, 5.2, 13, 4]

    invariants = [(0.50, 0.05), (0.90, 0.01), (0.99, 0.001)]
    estimator = quantile.Estimator(*invariants)
    [estimator.observe(float(i)) for i in data2]

    for i in estimator._invariants:
        q = i._quantile
        print("{0}: {1}".format(q, estimator.query(q)))
