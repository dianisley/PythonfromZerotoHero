<img width="1600" alt="Statistical Python" src="https://user-images.githubusercontent.com/103318089/184670711-6febc08c-5cfc-46a5-bfb3-a13bf46a5bc6.png">

# Table of Contents
* [Intro to Scipy](#bookmark-introduction-to-scipy)
* [Why Scipy](#gem-why-scipy)
* [Getting Start](#wrench-getting-start)
* [About Scipy Docstring](#page_facing_up-about-scipy-docstring)
* [Scipy in Action](#books_scipy_in_action)
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

## Documenting Functions and Methods

Using this syntax, a `numpydoc` style docstring for a function or method is made up of the following elements:

- A short description of what the function or class does
- A section named `Parameters` that explains the object’s input parameters
- A section named `Returns` that explains that function’s output
- Any of the following “optional sections”:
  - `Examples`: This section is optional, but strongly recommended and encouraged. Within the section we would include one or more examples for how to use the object.
  - `Notes`: This section provides additional details that help the user understand the function, but were not included in the short description at the beginning. This might include a description of the algorithm or mathematics underlying the function.
  - `References : If any journal articles, books, or other publications or 3rd party code were consulted when writing the function, this should be documented in this section.
  - `Raises`: if the function/class might raise an exception when called, the exception along with cases under which the exception is raised should be documented. 
  - `See Also`: if the function/class is related to another object, we should specify this relation in a See Also section.

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
## Documenting Classes

The `numpydoc` standard for documenting classes is very similar. The key components are (this all goes the first line of the docstring that is below the line containing the `class` keyword)

- A short description of what the class does
- A `Parameters` section that describes the parameters for the class’s `__init__` function
- An `Attributes` section that describes all the attributes of the class. This replaces the `Returns` section we saw above for functions and methods.
- Any of the optional sections outlined above in addition to an optional section describing the `Methods` that are implemented specifically for this class.

# :books: Scipy in Action

The following repository contains extended applications of the Scipy.Stats library:

https://github.com/dianisley/Statistics-and-Probability-in-Python.git




# Acknowledgements
This project was based on:
- https://github.com/Pegah-Ardehkhani/Statistics-and-Probability-in-Python.git


