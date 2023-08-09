*If you did not know the essential of **Vector** concept, [click here](../../vital-concepts/vector/README.md)* 
<br/>
# Vector in linear algebra
In linear algebra, a vector can store information about a point (position) or a direction. Overall, whatever information is stored inside a vector, the number always could be understood as an offset from the origin. Additionally, the elements of the vector can also be represented as how it moves along that axis, then move along another axis base on that element, and so on. For example, `v = [ 0.5 0.5 ]`, the vector v move along x axis 0.5 unit, and along x 0.5 unit. For visualization [Image of vector](./README.md?plain=1#L7)  <br>
Let's say, we are working in 2D of linear algebra in default, we have two axes, `Y = [ 0 1 ]`  and `X = [ 1 0 ]`.
<img src="./images/Screenshot 2023-08-09 165557.png"><br>
And if we add a point `B = [0.5 0.5]` which says point B at x 0.5 and y 0.5 <br>
<img src="./images/Screenshot 2023-08-09 170339.png">

## Vector addition and subtraction
In [Essential of vector](../../vital-concepts/vector/README.md), adding vectors results in a new vector in which each element is the sum of the corresponding element of participating vectors. Vectors in linear algebra behave the same way as well. Moreover, the operation when visualized in graphs shows that the resultant vector is the offset from v<sub>1</sub> as v<sub>2</sub> offset from the origin.<br>
For example we take `v = [ 0.5 0.5 ]` + `u = [ 0.2 0.1 ]`, as calculation, the result vector is `r = [ 0.7 0.6]`<br><br>
<img src="./images/Screenshot 2023-08-09 174943.png"><br>
*We can see that the `R` offset from `V` is the same as the `U` offset from `O` (which is the origin point)*. We also see that the gray ray represents a direction, so how we can calculate that? The answer is using subtraction. As same in basic subtraction, a+b=c, so c-a=b or c-b=a, the subtraction from *v2* to *v1* resulting the offset vector, which is offset-based from the origin point. `R-V = U` or <br>
`[0.7 0.6] - [0.5 0.5] = [0.2 0.1]`

Next: [*Linear transformation*](../linear-transformation/README.md)
