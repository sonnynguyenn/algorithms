# Vector
## Definition
**Vector** is a type of storing decimal like a *List* with fixed dimension like 2D, 3D, 4D, ... For *n*D dimension, a vector can store up to *n* decimals
<br>
## XYZ and so on
Vector acts like a list with a fixed length, which we can call an element by `vec[n]` with `n <= vec.length-1`. However, as a protocol, vector element can also be called with *x*,*y*,*z*,*w*,*t*,... equivalent to *vec[0]*,*vec[1]*,*vec[2]*,*vec[3]*,*vec[4]*, ... respectively
<br>
## Basic math operation on a vector
Vectors with the same dimension can operate subtraction or addition together. <br>
<br>
For example:
Given two 3D vector, **u** and **v**, adding **u** and **v** will be: <br>
```
u+v = [ u.x + v.x, u.y + v.y, u.z + v.z]
      [<x>       , <y>,       <z>      ]
```
or subtraction: 
```
u-v = [ u.x - v.x, u.y - v.y, u.z - v.z]
```
As well as other operations: <br>
**Multiplying:** <br>
+ Multiplying a vector with another vector with the same dimension 
```
u*v = [ u.x * v.x, u.y * v.y, u.z * v.z]
```
+ Multiplying a vector another vector has the behavior of scaling the vector.
 ```
v*n = [ v.x * n, v.y * n, v.z * n ] 
```
**Dividing:** <br>
+ Dividing a vector with the same dimension
```
u/v = [ u.x / v.x, u.y / v.y, u.z / v.z]
```
+ Diving a vector with a number. It behaves similarly to scaling or multiplying a vector
```
v/n = [ v.x / n, v.y / n, v.z / n ] 
```
## Normalized vector
A **normalized vector** is a vector that has a magnitude of 1. The magnitude can be calculate by this formula : *mag* = sqrt(v.x<sup>2</sup>+v.y<sup>2</sup>+v.z<sup>2</sup>+... ). By dividing the vector by its *mag*, we will have a **normalized vector**
