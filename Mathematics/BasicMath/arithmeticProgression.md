# Arithmetic Progression

A sequence of numbers is called "Arithmetic Progression" if the difference between any two consecutive terms is always the same.

* * *

### Every A.P. must have

- **Initial Term** is the first number in the sequence

- **Common difference** is the value by which consecutive terms increase or decrease:

    * positive, then the terms will grow towards positive infinity
        * negative, then the terms will grow towards negative infinity

**Example**

1 --> 4 --> --> 7 --> 10

```
initial term = 1
common difference = 3
positive
```

### Formulas and algorithm

**N<sup>th</sup> term of an A.P**

```
a = sequence
n = position of the nth number
d = common difference
```

![](https://quicklatex.com/cache3/8f/ql_89dcd7a990b276e5a1d440c87234fe8f_l3.png)

```
integer array = [2, 4, 6, 8, 10]
sort(array)
integer d = array[1] - array[0]

write(array[0] + (n - 1) * d)
```

**Sum of first N<sup>th</sup> terms of an A.P.**

```
S = sum
n = position of the nth number
d = common difference
n = range of sum
```

![](https://quicklatex.com/cache3/a8/ql_2a3915e3cac774ac037f59909ceca8a8_l3.png)

```
integer array = [2, 4, 6, 8, 10]
sort(array)
integer d = array[1] - array[0]

write((n / 2) * (2 * array[0] + (n - 1) * d))
```
