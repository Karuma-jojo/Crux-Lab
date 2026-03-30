# Euler 9 — Reducing the triplet search to one parameter

## Problem
Find natural numbers `a < b < c` such that:

- `a^2 + b^2 = c^2`
- `a + b + c = 1000`

Compute `abc`.

## Key idea
I started by looking at small Pythagorean triples and noticed I could rewrite the product in the form `abc = (a+b+c)cx`.
That turns the problem into a one-parameter search instead of a 3-variable search.

## Reduction
From the setup:

- `ab = 1000x`
- `c = 500 - x`
- `a + b = 500 + x`

So `a` and `b` must be roots of:

`t^2 - (500 + x)t + 1000x = 0`

For integer roots, the discriminant must be a perfect square.

## Working value
The valid value is `x = 75`.

So:

- `c = 425`
- `a + b = 575`
- `ab = 75000`

which gives:

- `a = 200`
- `b = 375`

Hence:

`(a,b,c) = (200,375,425)`

and

`abc = 31875000`

## What I learned
The main missing idea was using Vieta’s formulas plus the discriminant condition:

If two integers have sum `M` and product `N`, then they are roots of  
`t^2 - Mt + N = 0`.

So integer-root constraints can finish a problem after algebraic reduction.

## Checker
```python
for x in range(1, 500):
    s = 500 + x
    p = 1000 * x
    D = s*s - 4*p
    r = int(D**0.5)
    if r*r == D:
        a = (s - r) // 2
        b = (s + r) // 2
        c = 500 - x
        if a > 0 and b > 0 and a < b < c:
            print(x, a, b, c, a*b*c)
            break