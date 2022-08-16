<img width="1600" alt="Statistical Python" src="https://user-images.githubusercontent.com/103318089/184670711-6febc08c-5cfc-46a5-bfb3-a13bf46a5bc6.png">

# Table of Contents
* [Intro to Scipy](#bookmark-introduction-to-scipy)
* [Why Scipy](#gem-why-scipy)
* [Getting Start](#wrench-getting-start)
* [About Scipy Docstring](#page_facing_up-about-scipy-docstring)
* [Acknowledgements](#acknowledgements)


# :bookmark: Introduction to Scipy

[SciPy](https://scipy.org/), is a fantastic library in Python (it is short for Scientific Python and is pronounced "Sigh Pi,"). This libriry simplifies the process of doing mathematical, scientific and engineering computations as it offers a variety of user-friendly and effective numerical techniques, such as routines for numerical integration and optimization. It is designed to interact with NumPy arrays. Together, they are quick to install, free, and compatible with all common operating systems. Some of the top scientists and engineers in the world depend on NumPy and SciPy because they are simple to use but have sufficient power. It is not only about less code, but is also about an efficient way to takle processes and applicatons. Scipy is a very popular library that has a wide variaty of applications, and it is extremly popular for statistical analysis.  

The scipy.stats is the SciPy sub-package. It is mainly used for probabilistic distributions and statistical operations. There is a wide range of probability functions. The statistical functionality is expanding as the library is open-source.

We have functions for both continuous and discrete variables and can work with different types of distributions like the binomial, uniform, and continuous. We can also perform the T-test and determine the T-score. Let us learn more about [SciPy Stats](https://docs.scipy.org/doc/scipy/reference/stats.html). Below a few of the modeling that can be done with SciPy Stats

- Generate random variables from a wide choice of discrete and continuous statistical distributions – binomial, normal, beta, gamma, student’s t, etc.
- Compute frequency and summary statistics of multi-dimensional datasets
- Run popular statistical tests such as t-test, chi-square, Kolmogorov-Smirnov, Mann-Whitney rank test, Wilcoxon rank-sum, etc.
- Perform correlation computations such as Pearson’s coefficient, ANOVA, Theil-Sen estimation, etc.
- Compute statistical distance measures such as Wasserstein distance and energy distance.


# :gem: Why Scipy

- SciPy contains varieties of sub packages which help to solve the most common issue related to Scientific Computation.
- Easy to use and understand as well as fast computational power.
- It can operate on an array of NumPy library

# :wrench: Getting Start

## Installation

To use pip can use the below command to install Scipy package:

    pip install scipy

After that you can import the stats modules:

    import numpy as np
    from scipy import stats

# :page_facing_up: About Scipy Docstring

A Python docstring is a string used to document a Python module, class, function or method, so programmers can understand what it does without having to read the details of the implementation.
Some standards exist about docstrings, so they are easier to read, and they can be exported to other formats such as html or pdf, including:

- [PEP-8 Style](https://www.python.org/dev/peps/pep-0008) Guide for Python Code
- [PEP-257](https://www.python.org/dev/peps/pep-0257) Docstring Conventions
- [NumPy](https://numpydoc.readthedocs.io/en/latest/format.html) docstring standard

The [Zen of Python](https://peps.python.org/pep-0020/#the-zen-of-python) tells us that "Readability counts" and "Explicit is better than implicit." These are necessary characteristics of Python. When we write code, we do it for end-users, developers, and ourselves.

[NumPy/SciPy docstrings](https://numpydoc.readthedocs.io/en/latest/format.html) is one of the four primary types of docstrings avalable.

For instance after importing the stats module you can run the following code:

    help(scipy.stats.bayes_mvs)

getting the following outcome
```
Help on function bayes_mvs in module scipy.stats.morestats:

bayes_mvs(data, alpha=0.9)
    Bayesian confidence intervals for the mean, var, and std.
    
    Parameters
    ----------
    data : array_like
        Input data, if multi-dimensional it is flattened to 1-D by `bayes_mvs`.
        Requires 2 or more data points.
    alpha : float, optional
        Probability that the returned confidence interval contains
        the true parameter.
    
    Returns
    -------
    mean_cntr, var_cntr, std_cntr : tuple
        The three results are for the mean, variance and standard deviation,
        respectively.  Each result is a tuple of the form::
    
            (center, (lower, upper))
    
        with `center` the mean of the conditional pdf of the value given the
        data, and `(lower, upper)` a confidence interval, centered on the
        median, containing the estimate to a probability `alpha`.
    
    Notes
    -----
    Each tuple of mean, variance, and standard deviation estimates represent
    the (center, (lower, upper)) with center the mean of the conditional pdf
    of the value given the data and (lower, upper) is a confidence interval
    centered on the median, containing the estimate to a probability
    `alpha`.
    
    Converts data to 1-D and assumes all data has the same mean and variance.
    Uses Jeffrey's prior for variance and std.
    
    Equivalent to tuple((x.mean(), x.interval(alpha)) for x in mvsdist(dat))
    
    References
    ----------
    T.E. Oliphant, "A Bayesian perspective on estimating mean, variance, and
    standard-deviation from data", http://hdl.handle.net/1877/438, 2006.
```

https://github.com/Pegah-Ardehkhani/Statistics-and-Probability-in-Python.git


# Acknowledgements
This project was based on 
- [A Comprehensive Guide on using Flask for Data Science](https://www.analyticsvidhya.com/blog/2021/10/a-comprehensive-guide-on-using-flask-for-data-science/#:~:text=Flask%20provides%20different%20libraries%2C%20tools,or%20any%20commercial%20website%2C%20etc)
- [Flask SQLAlchemy](https://pythonbasics.org/flask-sqlalchemy/)
- [Flask in Production: Minimal Web APIs](https://towardsdatascience.com/flask-in-production-minimal-web-apis-2e0859736df)
- [Rendering Pages in Flask Using Jinja](https://hackersandslackers.com/flask-jinja-templates/)

