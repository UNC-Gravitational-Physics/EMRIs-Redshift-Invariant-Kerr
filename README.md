# Redshift-Invariant
High-order post-Newtonian expansion of the generalized redshift invariant for eccentric-orbit, equatorial extreme-mass-ratio inspirals with a spinning primary (2023)

This repository contains the expansion of the redshift invariant for equatorial Kerr EMRIs to 8PN order (in v), as a supplement to the paper arXiv:2203.13832.  In general, each PN term is given to e^16 through 6PN and e^10 through 8PN, though various lower-order terms are found in closed or compact form.  The series is contained within the text file "vSeries8PN."  The series can be loaded by using Mathematica’s Get[] function, for example Get[“<file-path>/vSeries8PN”].

A few PN terms contain special functions that can be expanded separately.  These are defined at the beginning of the file.  Upon inputting the series with Get[], Mathematica will load all such functions, so that each can be called in straightforward fashion.  The following functions are currently included: 

1) g[n,e,highestPower], which is the e-expansion of nth-harmonic of the Newtonian mass quadrupole power spectrum to the order “highestPower.”  The g function can be expanded to arbitrary order in e, and sums of g over n are used to compute subsequent functions.

2) chi4PNConv[e,highestPower], which is the convergent (as e->1) part of the chi-like function appearing in the spin-independent portion of the 4PN redshift correction, expanded to “highestPower” in e.  See the paper for more details.  This function can be expanded to arbitrary order. 

3) chi5PNConv[e,highestPower], which is the convergent part of the chi-like function appearing in the spin-independent portion of the 5PN redshift correction, expanded to “highestPower” in e.  See the paper for more details.  This function can be only be expanded to e^20.

4) fiveP5PNConv[e,highestPower], which is the spin-independent portion of the 5.5PN redshift correction, but with powers of (1-e^2) removed to make the remaining series minimally convergent, expanded to “highestPower” in e.  This series is the same as the convergent portion of the 1.5PN energy flux and can be expanded to arbitrary order in e.



