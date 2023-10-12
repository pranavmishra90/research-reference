# ANOVA in Python
Pranav Mishra
Thursday, October 12, 2023

## Pre-ANOVA testing

### Levene test

A test which sees if the variance found in each group / sample is equal
to that of the other ones.

Input: quantitative variables - 2+

Which test(s) are we hoping to perform later:

- One-way ANOVA
- T-test for independent samples

Why is the Levene test important?

If the each group / sample has a large difference in their sample sizes,
you need to make sure that the varience in each group are roughly the
same. This is called *homogeneity*. Without homogeneous variances
between groups of different sizes, the ANOVA could give you a false
result of significance<sup>1</sup>.

------------------------------------------------------------------------

**References**

<div id="refs" class="references csl-bib-body">

<div id="ref-van_den_berg_levenes_2023" class="csl-entry">

<span class="csl-left-margin">1.
</span><span class="csl-right-inline">Berg RG van den. Levene’s test
(statistics) - the ultimate guide. SPSS tutorials. Published 2023.
<https://www.spss-tutorials.com/levenes-test-in-spss/></span>

</div>

</div>
