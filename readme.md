I had to learn about a kind of prefix codes called entropy codes while working on the implementation of Lisp in Lisp.  This project taught me enough to write an entropy code that encoded positive integers about as effectively as elias delta.  The positive integer n will be expressed in about logn+2loglogn bits, but the exact closed-form formula is somewhat more complex.

Elias delta is not used in industry and this is code is hardly different, so it's really nothing more than a toy.  What I like most about it is that it has sweet spots, so to speak: there is a set of integers roughly represented by 2^2^n, i.e. 3, 18, 273, 65808, that take 4, 6, 8, and 10 bits respectively, so you can essentially cheat binary if you want to express a very large number and only care about its rough order of magnitude.