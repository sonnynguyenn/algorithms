# Dot product
**Dot product** is the product of two vectors that result in the *scalar* that is related to one of them. The *scalar* when used to scale (or multiply) one of the vectors, has resulted in a new vector that is perpendicular to the other vector at the base of that vector. For example, we take the dot product between **a** and **b** vector which results in *c*, a scalar number. Scaling **a** with *c* will result in a vector *A*, which is coincident to a, the result of *b* - *A* will be a vector that is perpendicular to *a* and *A*, if we add that to *a* vector, we will get *B*. The result is the same as doing this with vector *b* as being scaled.<br>
<img src="./images/Screenshot 2023-08-11 132027.png">
## Formula
For a vector of **any dimension**, the formula will be `scalar = a.x*b.x + a.y*b.y + a.z*b.z + ...`, or also it can be performed by multiplying two matrices, in which the first line-up on the first row and the second matrix are values of vector lining up in the first column. <br>
```
[ v1.x v1.y v1.z ...] x [ v2.x ]
                        [ v2.y ]
                        [ v2.z ]
                        ...
```
