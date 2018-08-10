# GSoC2018: Rational Point on Varieties
### Mentors: [Benjamin Hutz](https://sites.google.com/a/slu.edu/benjamin-hutz/), [Travis Scrimshaw](https://sites.google.com/view/tscrim/home)
### Organization: [SageMath](http://www.sagemath.org/)
Hi, my name is [Raghukul Raman](https://raghukul01.github.io/) and I have been working on implementing rational 
point algorithms for Schemes, in Google Summer of Code 2018. 
This gist describes all the work that I have done during this period.

### Trac Tickets
SageMath uses the [Trac](trac.sagemath.org) issue tracking system for development, 
each ticket has a unique ticket number. These ticket contain all the important discussion 
regarding that issue, it also contain links to the commit. Apart from coding, I also reviewed 
some ticket of other sage developers. For convenience I have provides
link to my commits, also current status of each ticket (including reviewed tickets) in following section.

## Summary

Status of ticket which I commited to:


| Ticket No | Ticket Summary | Squashed Commit | Status |
|:---------:|:----------------:|:-----------------:|:--------:|
| #22771 | [Numerical Precision for Heights in Number Fields](https://trac.sagemath.org/ticket/22771) | [f88426b](https://git.sagemath.org/sage.git/commit?id=219661892657e535333c4131126bbb6213948cf9) | **Merged** |
| #23627 | [Update points() in projective_homset.py and affine_homset.py to work over CC and CDF](https://trac.sagemath.org/ticket/23627) | [c6f8d4f](https://git.sagemath.org/sage.git/diff?id=81260999f8edb4a778c5a6ae8fe9e149ba799bcf) | **Merged**|
| #23807 | [Different affine patches are the same object in memory](https://trac.sagemath.org/ticket/23807) | [affine_patch_23807](https://git.sagemath.org/sage.git/diff?id2=ada43b34b3b0fdf4ff6cb6a24468565fafbe09ac&id=820be598eae1c1556a89bf473f1f9719465fd9d5) | **Needs Work** |
| #25529 | [Implement Sieving to replace search enumeration](https://trac.sagemath.org/ticket/25529) | [e4a4340](https://git.sagemath.org/sage.git/commit?id=1a81fa568af10a31103895bc793b0495dd530bc9) | **Merged** |
| #25564 | [Implement hash for affine_point](https://trac.sagemath.org/ticket/25564) | [1b0ab74](https://git.sagemath.org/sage.git/commit?id=eeec88a6534be601e4d172990ce537f123db9b4d) | **Merged** |
| #25592 | [enum_affine_rational_field function is missing points](https://trac.sagemath.org/ticket/25592) | [6ec7a09](https://git.sagemath.org/sage.git/commit?id=5ab17cff2b52030f5b20351c589f4772edab37be) | **Merged** |
| #25697 | [Implement enumeration over QQ for product projective schemes](https://trac.sagemath.org/ticket/25697) | [f9cb450](https://git.sagemath.org/sage.git/diff?id=cb8d60aa438013f020622dabfaf95318e96d1c39) | **Merged** |
| #25701 | [Implement Sieve algorithm for product_projective space](https://trac.sagemath.org/ticket/25701) | [product_sieve_23701](https://git.sagemath.org/sage.git/diff?id=75dd2f607b8cac270eb81a3607b5b0690e59d379) | **Needs Work** |
| #25780 | [Normalize bound checking in points function](https://trac.sagemath.org/ticket/25780) | [b9266c6](https://git.sagemath.org/sage.git/commit?id=bcd7cca671f2525bfc4981b73507583244893645) | **Merged** |
| #25781 | [Add Comparison operator for morphism between product](https://trac.sagemath.org/ticket/25781) | [3ffc28c](https://git.sagemath.org/sage.git/diff?id=bfbabe6ffc6f836c96b073071475dbee240e42d6) | **Merged** |
| #25792 | [Add dehomogenize function for product projective point](https://trac.sagemath.org/ticket/25792) | [f073039](https://git.sagemath.org/sage.git/diff?id=01e44a172ded787428f0df2d86d52c56b5197125) | **Merged** |
| #25795 | [Minor optimization in comparison between morphisms](https://trac.sagemath.org/ticket/25795) | [25795](https://git.sagemath.org/sage.git/diff?id=b15b1f28afe99cdf75f1d6cc7335c9bbb75bc8cb) | **Positive Reviewed** |
| #25821 | [Implement height functions for product points](https://trac.sagemath.org/ticket/25821) | [af73f9](https://git.sagemath.org/sage.git/diff?id=31f7661bb4023498e1be80522a94b5a6f69d4d41) | **Merged** |
| #25878 | [Implement Height function for product morphism](https://trac.sagemath.org/ticket/25878) | [bbadcc6](https://git.sagemath.org/sage.git/commit?id=47959c3f7d057c17aab504f505dd1a2bbcd7c4cf) | **Merged** |
| #25897 | [Incorrect Comparison of embedding index in projective_embedding](https://trac.sagemath.org/ticket/25897) | [5652a9d](https://git.sagemath.org/sage.git/commit?id=5a9630a763f614f324e84251bf1d4c27a1311cd2) | **Merged** |

<br/>

Status of tickets which I reviewed:

| Ticket No | Ticket Summary | Ticket Author/s | Status |
|:---------:|:--------------:|:-------------:|:------:|
| #23627 | [Update points() in projective_homset.py and affine_homset.py to work over CC and CDF](https://trac.sagemath.org/ticket/23627) | Rebecca Lauren Miller, Raghukul Raman, Ben Hutz | **Merged** |
| #25156 | [multivariate power series rings don't always format latex properly](https://trac.sagemath.org/ticket/25156) | Brent Baccala, Raghukul Raman | **Merged** |
| #25242 | [is_polynomial fails when multiple roots](https://trac.sagemath.org/ticket/25242) | Ben Hutz | **Merged** |
| #25877 | [dehomogenize for projective morphism failure in number field order](https://trac.sagemath.org/ticket/25877) | Ben Hutz | **Positive Reviewed** |
| #25795 | [minor optimization in comparison between morphisms](https://trac.sagemath.org/ticket/25795)  | Raghukul Raman, Travis Scrimshaw | **Positive Reviewed** |

## Detailed version


Now lets discuss each of the Ticket which I have worked on in detail:

### [#22771 Numerical Precision for Heights in Number Fields](https://trac.sagemath.org/ticket/22771)
First part of my project was to implement [Doyle-Krumm Algorithm-4](https://arxiv.org/abs/1403.6501). 
This algorithm provides an efficient method to compute all elements of a 
number field (K) having realtive height at most B. 
Initially in **sage** Algorithm-3 was implemented. So why implement algorithm-4?
<br/>
A computer has a limited memory, hence there is a limit of storing data. 
Issues are due to the fact that in a computer we cannot work exactly with the
 real numbers that appear in the algorithm (heights of algebraic numbers, 
 logarithms of real numbers, absolute values of algebraic numbers), 
 so we must make do with rational approximations of them. Consider the following example:

```python
sage: from sage.rings.number_field.bdd_height import bdd_height
sage: K.<v> = NumberField(x^3 + x + 1)
sage: bound = 3
sage: list(bdd_height(K,bound))
sage: for x in T:
....    print x, e**(K(x).global_height()*K.degree())
0 1.00000000000000
-v^2 + v - 1 2.14789903570479
v^2 - v + 1 2.14789903570479
v^2 + 1 1.46557123187677
-v^2 - 1 1.46557123187677
-1 1.00000000000000
1 1.00000000000000
-v 1.46557123187677
v 1.46557123187677
-v^2 2.14789903570479
v^2 2.14789903570479
```
If we change the bound to just 3.1 we get:

```python
sage: from sage.rings.number_field.bdd_height import bdd_height
sage: K.<v> = NumberField(x^3 + x + 1)
sage: bound = 3.1
sage: list(bdd_height(K,bound))
sage: for x in T:
....    print x, e**(K(x).global_height()*K.degree())
0 1.00000000000000
-v^2 + v - 1 2.14789903570479
v^2 - v + 1 2.14789903570479
v^2 + 1 1.46557123187677
-v^2 - 1 1.46557123187677
-1 1.00000000000000
1 1.00000000000000
-v 1.46557123187677
v 1.46557123187677
-v^2 2.14789903570479
v^2 2.14789903570479
-2/3*v^2 + 1/3*v - 1/3 3.00000000000000
-v^2 + v 3.00000000000000
2/3*v^2 - 1/3*v + 1/3 3.00000000000000
v^2 - v 3.00000000000000
1/3*v^2 + 1/3*v + 2/3 3.00000000000000
-v + 1 3.00000000000000
-1/3*v^2 - 1/3*v - 2/3 3.00000000000000
v - 1 3.00000000000000
1/3*v^2 + 1/3*v - 1/3 3.00000000000000
-v^2 - 2 3.00000000000000
-1/3*v^2 - 1/3*v + 1/3 3.00000000000000
v^2 + 2 3.00000000000000
```
So with example above it is clear that we were missing points whose height were 
exactly 3 (due to approximation of real numbers). Algorithm-4 provides a convinent
way of finding approximations that are good enough to gurantee correct results.
To see my raw implementation click [here](https://paste.ubuntu.com/p/nwtzHqG696/).

### [#23627 Update points() in projective_homset.py and affine_homset.py to work over CC and CDF](https://trac.sagemath.org/ticket/23627)
Most of the work in this ticket was done by [Rebecca Miller](https://www.linkedin.com/in/rebecca-lauren-miller-a4ba9b64/)
and [Prof. Ben](https://sites.google.com/a/slu.edu/benjamin-hutz/). 
My work was to review this ticket and the only contribution I did was to remove duplicate points.
Due to inaccurate results of groebner basis calculation, same projective points we treated different. So I added a tolerance 
parameter, if distance between any 2 points is less that tolerance, they are considered same.

```python
dupl_points = list(rat_points) # rat_points is list of points containing duplicates
for i in range(len(dupl_points)):
    u = dupl_points[i]
    for j in range(i+1, len(dupl_points)):
        v = dupl_points[j]
        if all([(u[k]-v[k]).abs() < 2**(-tol) for k in range(len(u))]):
            rat_points.remove(u)
            break 
```
rat_points is a set, so complexity of this algorithm is O(n^2log(n)).


### [#23807 Different affine patches are the same object in memory](https://trac.sagemath.org/ticket/23807)


### [#25529 Implement Sieving to replace search enumeration](https://trac.sagemath.org/ticket/25529)


### [#25564 Implement hash for affine_point](https://trac.sagemath.org/ticket/25564)


### [#25592 enum_affine_rational_field function is missing points](https://trac.sagemath.org/ticket/25592)


### [#25697 Implement enumeration over QQ for product projective schemes](https://trac.sagemath.org/ticket/25697)


### [#25701 Implement Sieve algorithm for product_projective space](https://trac.sagemath.org/ticket/25701)


### [#25780 Normalize bound checking in points function](https://trac.sagemath.org/ticket/25780)


### [#25781 Add Comparison operator for morphism between product](https://trac.sagemath.org/ticket/25781)


### [#25792 Add dehomogenize function for product projective point](https://trac.sagemath.org/ticket/25792)


### [#25795 Minor optimization in comparison between morphisms](https://trac.sagemath.org/ticket/25795)


### [#25821 Implement height functions for product points](https://trac.sagemath.org/ticket/25821)


### [#25878 Implement Height function for product morphism](https://trac.sagemath.org/ticket/25878)


### [#25897 Incorrect Comparison of embedding index in projective_embedding](https://trac.sagemath.org/ticket/25897)


