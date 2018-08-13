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
some ticket of other SageMath developers. For convenience I have provides
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




### [#22771 Numerical Precision for Heights in Number Fields](https://trac.sagemath.org/ticket/22771)

First part of my project was to implement [Doyle-Krumm Algorithm-4](https://arxiv.org/abs/1403.6501). 
This algorithm provides an efficient method to compute all elements of a 
number field (K) having realtive height at most B. 
Initially in SageMath Algorithm-3 was implemented. So why implement algorithm-4?
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
and [Prof. Hutz](https://sites.google.com/a/slu.edu/benjamin-hutz/). 
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
#TODO



### [#25529 Implement Sieving to replace search enumeration](https://trac.sagemath.org/ticket/25529)

Second part of my GSoC project was to replace search enumeration for subschemes, 
with much faster Sieve Algorithm. Basic idea behind the algorithm is to search 
points modulo prime and use chinese remainder theorem to reconstruct the rational points.
Suppose Y is a subscheme defined as follows:

```python
P.<x,y,z,q>=ProjectiveSpace(QQ,3)
Y=P.subscheme([x^2-3^2*y^2+z*q,x+z+4*q])
bound = 10
```

Then to find rational points on Y we first find point modulo primes (2, 3, 7, 11), 
can be done using existing rational point finding function. Then we lift all 
possible combination of these point modulo prime and check that they belong to 
given subscheme (Y). Now how is this fast?
<br/>
Naturally this algorithm uses the existing rational_points(), but this time the
search space is significantly reduced. Second major improvement of this algorithm,
is that computation of points modulo prime is done in parallel. 
hence the complexity is:
```
T(n) = max(T(pi)) for i ∊ (1,k)  (since computation related to each prime is done in parallel)
```

Other thing that can be done, is that computation related to each several combinations
can be distributed evenly over other threads. 
<br/>
First of all for correctness of algorithm, sufficient primes need to be present,
whose product should be greater that bound, which is given by: (reference: [Preperiodic Points](https://arxiv.org/pdf/1210.6246.pdf)):

```python
bound = 2(N/4+1)*given_bound2*√(N+1).
```
Now a better choice of these primes would significantly affect the efficiency of algorithm.
So to find a list of prime which would give rational points taking least amount of time,
I implemented the `good_primes()` function.
<br/>
Main idea behind the function is to check for all valid list of primes, and return 
which one takes least amount of time. Time complexity used to return best prime list is:
```python
T = (N^2*P_max^N) + N^5*(α^dim_scheme/P_max)
# α is product of all primes, P_max is largest prime in list and N is the dimension of Ambient Space
```

<br/>
For more details of algorithm implementation visit - [Sieve](https://raghukul01.github.io/blog.html#25529).



### [#25564 Implement hash for affine_point](https://trac.sagemath.org/ticket/25564)
Interestingly `__hash__()` function was not implemented for affine points in SageMath.
Adding hash function for affine points was quite easy compared to for projective
points, where (1,3,6) is same point as (3,9,18). It was simply to hash the list
of coordinates in that affine point.
```python
sage: A.<x,y> = AffineSpace(QQ, 2)
sage: X = A.subscheme(x - y)
sage: hash(X([1, 1]))
1300952125                      # 32-bit
3713081631935493181             # 64-bit
```



### [#25592 enum_affine_rational_field function is missing points](https://trac.sagemath.org/ticket/25592)
`enum_affine_rational_field()` function was missing points, for example
```python
sage: A.<x,y> = AffineSpace(2, QQ)
sage: C = Curve(x^2+y-x)
sage: from sage.schemes.affine.affine_rational_point import enum_affine_rational_field
sage: enum_affine_rational_field(C, 10)
[(-2, -6), (-1, -2), (0, 0), (1, 0), (2, -2), (3, -6)]
```
You can see that some points of height 9 ((-2/3, -10/9),(-1/3, -4/9),(1/3, 2/9),(2/3, 2/9)) and height 4 ((-1/2, -3/4),(1/2, 1/4),(3/2, -3/4)) which clearly lie on the subscheme are missing. This bug was due to the way they were generating rational numbers and eventually trying it on the subscheme. Actually the code was quite old and after that `range_by_height()` function was implemented which could do the same thing correctly. So I used this new function and corrected this bug.
```python
sage: A.<x,y> = AffineSpace(2, QQ)
sage: C = Curve(x^2+y-x)
sage: from sage.schemes.affine.affine_rational_point import enum_affine_rational_field
sage: enum_affine_rational_field(C, 10)
[(-2, -6), (-1, -2), (-2/3, -10/9), (-1/2, -3/4), (-1/3, -4/9), (0, 0),
(1/3, 2/9), (1/2, 1/4), (2/3, 2/9), (1, 0), (3/2, -3/4),(2, -2), (3, -6)]
```



### [#25697 Implement enumeration over QQ for product projective schemes](https://trac.sagemath.org/ticket/25697)
Earlier for finding rational point on product projective spaces defined over rational field,
they were using `points_of_bounded_height()` function, and trying each point if it belongs to
the given subscheme. Firstly I added a new file for all rational point finding algorithms,
just like in projective and affine spaces, to make things universal. Secondly I made other
modification, similar to ones present in projective_rational_field.py.
<br/>
Lastly I implemented `enum_product_projective_rational_field()` , in which rational points for each component
of ambient space were found, and then all points from the cartesian product of result were
checked if they belong to given subscheme. I have also corrected `points_of_bounded_height()`
function for product projective spaces. This function returns an iterator of the rational
points on given space, but the implementation was memory inefficient, so I changed it
to pure iterator based implementation. The following examples works now:
```python
sage: PP.<x,y,z,u,v> = ProductProjectiveSpaces([2,1], QQ)
sage: X = PP.subscheme([x^2 + x*y + y*z, u*u-v*u])
sage: from sage.schemes.product_projective.rational_point import \ 
                                        enum_product_projective_rational_field
sage: enum_product_projective_rational_field(X,4)
[(-2 : 4 : 1 , 0 : 1), (-2 : 4 : 1 , 1 : 1), (-1 : 1 : 0 , 0 : 1),
 (-1 : 1 : 0 , 1 : 1), (-2/3 : -4/3 : 1 , 0 : 1), (-2/3 : -4/3 : 1 , 1 : 1),
 (-1/2 : -1/2 : 1 , 0 : 1), (-1/2 : -1/2 : 1 , 1 : 1),
 (0 : 0 : 1 , 0 : 1), (0 : 0 : 1 , 1 : 1), (0 : 1 : 0 , 0 : 1),
 (0 : 1 : 0 , 1 : 1), (1 : -1/2 : 1 , 0 : 1), (1 : -1/2 : 1 , 1 : 1)]
```


### [#25701 Implement Sieve algorithm for product_projective space](https://trac.sagemath.org/ticket/25701)
Sieve algorithm for product is almost similar to that for projective spaces, but while constructing points
from modulo points, we use `LLL` reduction on each component and then combine all components. Apart from that
complexity is also different (used in `good_primes` function). Consider:
```python
sage: from sage.schemes.product_projective.rational_point import sieve
sage: PP.<x,y,z,u,v> = ProductProjectiveSpaces([2,1], QQ)
sage: X = PP.subscheme([x^2 + y^2 - x*z, u*u-v*u])
sage: sieve(X,2)
[(0 : 0 : 1 , 0 : 1), (0 : 0 : 1 , 1 : 1), (1/2 : -1/2 : 1 , 0 : 1),
 (1/2 : -1/2 : 1 , 1 : 1), (1/2 : 1/2 : 1 , 0 : 1), (1/2 : 1/2 : 1 , 1 : 1),
 (1 : 0 : 1 , 0 : 1), (1 : 0 : 1 , 1 : 1)]
```



### [#25780 Normalize bound checking in points function](https://trac.sagemath.org/ticket/25780)
`points_of_bounded_height()` function for projective spaces gave different results
compared to `enum_projective_rational_point()`. Consider this example:
```python
sage: P.<x,y> = ProjectiveSpace(QQ, 1)
sage: print sorted(list(P.points_of_bounded_height(bound=3)))
[(-2 : 1), (-1 : 1), (-1/2 : 1), (0 : 1), (1/2 : 1), (1 : 0), (1 : 1), (2 : 1)]
```
Now you can see that some points of height 3 are not present. Apart from missing point,
it returned some point whose height were greater than bound. To correct this I replaced
the algorithm for **QQ** with this:
```python
zero = (0,) * (n+1)
for c in cartesian_product_iterator([srange(-B,B+1) for _ in range(n+1)]):
    if gcd(c) == 1 and c > zero:
        yield self(c)
```
How do these condition come from?? Well `gcd(c) = 1` is necessary to prevent
k*c (since they all are same projective points) adding to list, and `c > zero`
ensures the case when `k = 1,-1`. 




### [#25781 Add Comparison operator for morphism between product](https://trac.sagemath.org/ticket/25781)
There was no comparison operator between morphisms, for product projective spaces.
Now how do we check if 2 morphism are equal for projective spaces?
<br/>
Suppose `H1: (x0, x1,...,xn) → (y0, y1,...,yn) and H2: (x0, x1,...,xn) → (z0, z1,...,zn)` be 2 morphism defined from Projective space of dimension n to itself. 
So they are same projective morphisms if:
```python
y0/z0 = x1/z1 = ... = yn/zn     # (since P, c*P are same projective points)
```
Now for product projective space, we just need to check this condition
for each projective component. So now you can run this example:
```python
sage: PP.<x,y,z,a,b> = ProductProjectiveSpaces([2,1], ZZ)
sage: H = End(PP)
sage: f = H([x^2*y*z, x*y^2*z, x*y*z^2, a^2, b^2])
sage: g = H([x, y, z, a^3, a*b^2])
sage: f == g
True
sage: f != g
False
```



### [#25792 Add dehomogenize function for product projective point](https://trac.sagemath.org/ticket/25792)
Purpose of dehomogenize() function is to remove the kth coordinate of given
projective point and convert it into a point of kth affine_patch. But product
projective point is formed by some projective points. For products this function
take a list(L) as input where L[i] is the coordinate we need to dehomogenize from
ith projective point component. So we append result of each projective point
component and then finally convert them back into `affine_patch(L)` point.
```python
sage: PP = ProductProjectiveSpaces([2, 2, 2], QQ, 'x')
sage: A = PP([2, 4, 6, 23, 46, 23, 9, 3, 1])
sage: A.dehomogenize([0, 1, 2])
(2, 3, 1/2, 1/2, 9, 3)
```



### [#25795 Minor optimization in comparison between morphisms](https://trac.sagemath.org/ticket/25795)
Comparison Function between morphism was creating list of coordinates and
then doing comparison. Instead of creating list we could direclty compare using the tuple of coordinates.
```python
sage: P = ProjectiveSpace(QQ,2000,'x')
sage: H = End(P); L = P.gens(); LL = []
sage: for i in L:
.....    LL.append(i*i)
sage: f = H(L); g = H(LL)
%timeit
sage: f == g
False
CPU time: 10.83 s,  Wall time: 10.83 s

%timeit
sage: updated__eq__(f,g)
False
CPU time: 0.00 s,  Wall time: 0.00 s
```



### [#25821 Implement height functions for product points](https://trac.sagemath.org/ticket/25821)
I added `global_height` and `local_height` function for product projective points. We basically find max of global_height/local_height over each component. For computing `local_height` we also need to pass in any ideal of the base ring. This works in SageMath now:
```python
sage: PP = ProductProjectiveSpaces(QQ, [2,2], 'x')
sage: Q = PP([1, 7, 5, 18, 2, 3])
sage: Q.global_height()
1.94591014905531

sage: P = ProductProjectiveSpaces(QQ, [1,2], 'x')
sage: Q = P([1, 4, 1/2, 2, 32])
sage: Q.local_height(2)
4.15888308335967
```



### [#25878 Implement Height function for product morphism](https://trac.sagemath.org/ticket/25878)
Height functions for morphisms are defined as follows: 
 - `local_height`: maximum of the local height of the coefficients in any of the coordinate functions of this map.
 - `global_height`: maximum of the absolute logarithmic heights of the coefficients in any of the coordinate functions of this map.

So we simply enumerate over coefficent of all the polynomials and compute heights, and finally return max. However,
if base ring is `QQbar`, height functions are not present for coefficients. In that we have to convert this map, to a
map defined over Number Field. This has been left as an TODO. An example of this fix is:
```python
sage: u = QQ['u'].0
sage: R = NumberField(u^2 - 2, 'v')
sage: PP.<x,y,a,b> = ProductProjectiveSpaces([1, 1], R)
sage: H = End(PP)
sage: O = R.maximal_order()
sage: g = H([3*O(u)*x^2, 13*x*y, 7*a*y, 5*b*x + O(u)*a*y])
sage: g.global_height()
2.56494935746154

sage: R.<z> = PolynomialRing(QQ)
sage: K.<w> = NumberField(z^2-5)
sage: P.<x,y,a,b> = ProductProjectiveSpaces([1, 1], K)
sage: H = Hom(P,P)
sage: f = H([2*x^2 + w/3*y^2, 1/w*y^2, a^2, 6*b^2 + 1/9*a*b])
sage: f.local_height(K.ideal(3))
2.19722457733622
```




### [#25897 Incorrect Comparison of embedding index in projective_embedding](https://trac.sagemath.org/ticket/25897)
We can define mappings from projective space to affine space using `projective_embedding` and `affine_patch`.
To generate a projective_embedding, we pass in the embedding index, this index represents the coordinate,
which we add in to generate projective space. So this index, should be greater than 0 and should be less than or equal to,
the dimension of affine scheme. This check was buggy in projective_embedding function, which I fixed:
```python
sage: A.<x,y> = AffineSpace(ZZ, 2)
sage: A.projective_embedding(4)
Traceback (most recent call last):
...
ValueError: argument i (=4) must be between 0 and 2, inclusive
```

