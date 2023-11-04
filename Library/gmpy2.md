# GMPY2

gmpy2 it's library python use to manipule big number in memory, like bin int, big float

doc : https://gmpy2.readthedocs.io/en/latest/mpfr.html

## installation

```
pip install gmpy2
```

## cheat sheet

### Incrase precision

Default precision : 53

```python

gmpy2.gmpy2.get_context().precision=10000
```

### Data in memory

The number 194844 in memory

```python
gmpy2.mpz(194844)
```

For higher precision provided the mpfr type, always pass constants as strings
```python
mpfr('1.2')
#>>> mpfr('1.2000000000000000000000000000006',100)
```

### Usefull function

Addition (a + b)
```python
gmpy2.add(a, b)
```

Multiplication (a * b)
```python
gmpy2.mul(a,b)
```

Square root of a
```python
gmpy2.root(a)
```

Cubic root of a
```python
gmpy2.cbrt(a)
```

exponent th root of a
```python
gmpy2.iroot(a, exponent)

gmpy2.iroot(9, 2)
#>>> 3
```

Perform a modulo (a % b)
```python
gmpy2.mpz_mod(a, b)
```

```python
gmpy2.gcd(a, n)
```
