# be7d_reaction_rate

In this repository are the data files associated with the reaciont rate described in
the article "Measurement of near-threshold resonances in 9B for big bang nucleosynthesis"
by McCann et al. ([DOI link](https://doi.org/10.1103/37y9-m3yb)).

## Reaction rate data

The reaction rate data files are stored as CSV files. The first column is the
temperature in units of GK. The second column is the reaction rate in units of cm^3/(mol*s).

There are six data files. Each reaction channel of interest has its own nominal value file,
as well as upper and lower limits (labeled hi and lo respectively). The channels are

- 7Be(d,alpha)5Li
- 7Be(d,p0)8Be (or 7Be(d,p)8Be(g.s.))
- 7Be(d,p1)8Be (or 7Be(d,p)8Be(2+))

## Reaclib Parameters

A fit of the total nominal reaction rate was performed with a two part Reaclib parameterization.
The function is as follows:

$$
\lambda = exp\left[a0 + \sum^{5}_{i=1}ai T_9^{\frac{2i-5}{3}} + a6ln(T_9)\right] + 
exp\left[a7 + \sum^{12}_{i=8}ai T_9^{\frac{2(i-7)-5}{3}} + a13ln(T_9)\right]
$$

The values of the $ai$ constants are given in the file reaclib.txt with uncertainties
from the least-squares fit.

## Contact

If you have questions or would like to discuss please reach out to:

- Ingo Wiedenhoever - email: iwiedenhoever@fsu.edu
- Gordon McCann - email: gordonmccann215@gmail.com
