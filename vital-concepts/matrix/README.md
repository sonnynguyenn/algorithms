# Matrix
## Definition
**Matrix** is used to store decimals in two-dimensional (two-dimensional in the scope of this repo), it is as same as 2D *List* with **columns** and **rows**. Matrix can be *4x4*, *3x3*, *2x3*, ... In the format of ***n***x***m***, the ***n*** is number of rows and ***m*** is number of columns <br>
+ For example, a 3x2 matrix is: <br>
```
    C  C
R [ 10 12 ]
R [ 3  4  ]
R [ 4  4  ]
```
## Matrix addition and subtraction
 Matrices that have **same number of columns and rows** can perform addition or subtraction operations. Each element at the same position will perform the operation together, resulting in the same matrices with the same number of columns and rows. To visualize:
```
[ 4 3 ]   [ 3 0 ]   [ 4+3 3+0 ]   [ 7  3  ]
[ 0 5 ] + [ 9 8 ] = [ 0+9 8+5 ] = [ 9  13 ]
[ 1 4 ]   [ 2 1 ]   [ 1+2 4+1 ]   [ 3  5  ]
```
As well as subtraction:
```
[ 4 3 ]   [ 3 0 ]   [ 4-3 3-0 ]   [  1  3  ]
[ 0 5 ] - [ 9 8 ] = [ 0-9 8-5 ] = [ -9  3  ]
[ 1 4 ]   [ 2 1 ]   [ 1-2 4-1 ]   [ -1  3  ]
```

## Matrix multiplication
When it comes to matrix multiplication, it doesn't work as same as addition or subtraction, instead, it will perform [Dot-product](../../linear-algebra/dot-product/README.md)-like calculation, which is the sum of all products of elements with similar position. Additionally, this operation only requires the first's columns number to match the second's rows number To visualize:
```
[ a b c ]   [ g h i]   [ a*g+b*j+c*m a*h+b*k+c*n a*i+b*l+c*o ]
[ d e f ] x [ j k l] = [ d*g+e*j+f*m d*h+e*k+f*n d*i+e*l+f*o ]
            [ m n o]
```
or <b>
```
[ 3 1 6 ]   [ 1 8 4 ]   [ 3*1+1*4+6*5 3*8+1*7+6*5 3*4+1*6+6*0 ]   [ 37 42 18 ]
[ 0 8 4 ] x [ 4 7 6 ] = [ 0*1+8*4+4*5 0*8+8*7+4*5 0*4+8*6+4*0] =  [ 52 76 48 ] 
            [ 5 5 0 ]
```
As we can see, the matrix multiplication resulted in a new matrix with the rows number of the first matrix and the columns number of the second matrix. Each resultant element is the sum of products from an *n*th element from that row of the first matrix with the *n*th element from that column of the second matrix. 
