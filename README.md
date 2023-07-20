# Redshift-Invariant
High-order PN expansion of the redshift invariant for eccentric-orbit EMRIs (2022)

This repository contains different forms for the expansion of the redshift invariant for Schwarzschild EMRIs to 10PN, as a supplement to the paper arXiv:2203.13832.  In general, each PN term is given as an expansion in eccentricity to e^20, though various lower-order terms are found in closed or compact form.  The series are contained within text files, with the files “pSeries” and “ySeries” showing expansions in 1/p and y, respectively.  The series can be loaded by using Mathematica’s Get[] function, for example Get[“<file-path>/pSeries10PNe20”].

A few PN terms contain special functions that can be expanded separately.  These are defined at the beginning of the file.  Upon inputting the series with Get[], Mathematica will load all such functions, so that each can be called in straightforward fashion.  The following functions are currently included: 

1) g[n,e,highestPower], which is the e-expansion of nth-harmonic of the Newtonian mass quadrupole power spectrum to the order “highestPower.”  The g function can be expanded to arbitrary order in e, and sums of g over n are used to compute subsequent functions.

2) chi4PNConv[e,highestPower], which is the convergent (as e->1) part of the chi-like function appearing in the 4PN redshift correction, expanded to “highestPower” in e.  See the paper for more details.  This function can be expanded to arbitrary order. 

3) chi5PNConv[e,highestPower], which is the convergent part of the chi-like function appearing in the 4PN redshift correction, expanded to “highestPower” in e.  See the paper for more details.  This function can be only be expanded to e^20.

4) fiveP5PNConv[e,highestPower], which is the 5.5PN redshift correction, but with powers of (1-e^2) removed to make the remaining series minimally convergent, expanded to “highestPower” in e.  This series is the same as the convergent portion of the 1.5PN energy flux and can be expanded to arbitrary order in e.



