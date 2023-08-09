# Vector
## Definition
**Vector** is a type of storing decimal like a *List* with fixed dimension like 2D, 3D, 4D, ... For *n*D dimension, a vector can store up to *n* decimals
<br>
## XYZ and so on
Vector acts like a list with a fixed length, which we can call an element by `vec[n]` with `n <= vec.length-1`. However, as a protocol, vector element can also be called with *x*,*y*,*z*,*w*,*t*,... equivalent to *vec[0]*,*vec[1]*,*vec[2]*,*vec[3]*,*vec[4]*, respectively
<br>
## Basic math operation on a vector
Vectors with the same dimension can operate subtraction or addition together. <br>
<br>
+ For example:
Given two 3D vector, **u** and **v**, adding **u** and **v** will be: <br>
```
u+v = [ u.x + v.x, u.y + v.y, u.z + v.z]
      [<x>       , <y>,       <z>      ]
```
As well as other operations: <br>
**Subtracting:** <br>
```
u-v = [ u.x - v.x, u.y - v.y, u.z - v.z]
```
**Multiplying:** <br>
```
u*v = [ u.x * v.x, u.y * v.y, u.z * v.z]
```
**Dividing:** <br>
```
u/v = [ u.x / v.x, u.y / v.y, u.z / v.z]
```
