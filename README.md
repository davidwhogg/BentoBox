KitchenSink
===========

Authors
-------

* Dan Foreman-Mackey (NYU)
* Jonathan Goodman (NYU)
* David W. Hogg (NYU)
* Fengji Hou (NYU)

License
-------

This is **an academic project which includes software that doesn't even work**.
Use at your own risk.
Copyright 2013 the Authors.

Abstract
--------

Most MCMC methods perform very badly when the density function being sampled is
multi-modal, especially when the modes are separated by large regions of small or
vanishing density; this is generic in many data-analysis problems of interest
to scientists.  Here we propose a sampler that solves this problem by recursively
splitting the parameter space until each sub-space contains at most one mode, or at
least some easy-to-sample distribution.  The modes are founded by initializing
standard samplers at prior samplings; we use the housekeeping data from an ensemble
sampler to provide mode (or cluster) label information. Each parameter sub-space 
split is performed by a support vector machine.  The (now easy-to-make)
sub-space samplings are recombined into a complete
sampling by importance sampling on the total posterior integral within each
sub-space; this requires computation of the marginalized likelihood (or Bayes
factor) in every sub-space; we propose a simple method for this that works well
for uni-modal density functions (which we have, by construction).  In its naivest
form, the method requires proper priors, and is faster if the prior PDF can be
sampled quickly or simply; again this is common for many data-analysis problems
of interest in scientific applications.  We demonstrate the value of the method
on a data-analysis problem in exoplanet astronomy.  It outperforms [which other
methods] by [how much].
