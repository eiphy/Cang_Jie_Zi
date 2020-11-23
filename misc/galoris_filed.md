# Galoris Filed

A finite filed or Galoris filed is a filed that contains a **finite number of elements** with defined addition, subtraction, multiplication and divition [wiki](https://en.wikipedia.org/wiki/Finite_field#:~:text=In%20mathematics%2C%20a%20finite%20field,and%20satisfy%20certain%20basic%20rules.).
The addition identity element, multiplication identity element, and inverse should also be defined.
One application scenario is when you want to implement RAID-6. 
The **P** and **Q** could be a number bigger the 255 if Galoris Filed is not applied.

### GF(2)

This is the smallest Galoris Filed which only contains 2 numbers 0 and 1. 
This is also the foundation of larger filed like commonly used GF(8).

Addition operation is defined as exclusive OR and so do the subtraction operation.
Thus, addition and subtraction is identical in GF(2).
Addition identity element is 0 in this filed.
This definition is basically a modulos:

$$0+0=0$$
$$0+1=1$$
$$1+0=1$$
$$1+1=0$$

Multiplication operation on GF(2) is identical to AND operation:

$$0*0=0$$
$$1*0=0$$
$$0*1=0$$
$$1*1=1$$

The inverse of 1 is 1 itself. 
According to definition, 1 does not have a inverse.

### Extension of GF(2)

Like how we extend the number in binary, we use polynominal to extend to a larger filed.
A exteneded GF(2) number $A$ could have following expression:
$$A = a_nx^n+\cdots +a_0$$
, where $a_i \in GF(2)=\{0, 1\}$ and $x=2$ for $GF(2^n)$ filed.
The calculation of $a_i$ obey to the GF(2) operation and the calculation of polynomial obey the rule of polynomial calculation.

A python implementation of GF{2^8} could be found in [raid-6](https://github.com/eiphy/RAID-6-project)