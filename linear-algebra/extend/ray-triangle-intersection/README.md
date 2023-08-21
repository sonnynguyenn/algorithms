# Ray triangle intersection (3D)
To know whether a ray is projecting at a triangle (created from 3 points $\(x,y,z)\$ ), we can scale the ray to land on the plane of the triangle and check the landing point whether is inside the triangle.
## Finding the point landing on the plane of the triangle
We have *O(R)*, *R* represents origin and ray respectively and 3 points *p<sub>1</sub>*, *p<sub>2</sub>*, *p<sub>3</sub>* of the triangle. If the dot product between any coordination (that is related to the normal vector of the plane's origin ) with the normal vector of the plane equal 0, then that point land on the plane. Through this we have:
<br>*n is the scalar of the R vector and N is the normal vector and O(N)
$$(O(R)+Rn-O(N))⋅N = 0$$
$${O(R)_x}{N_x}+{R_x}{N_x}n-{O(N)_x}{N_x}+
{O(R)_y}{N_y}+{R_y}{N_y}n-{O(N)_y}{N_y}+
{O(R)_z}{N_z}+{R_z}{N_z}n-{O(N)_z}{N_z}=0$$
$${R_x}{N_x}n+{R_y}{N_y}n+{R_z}{N_z}n = {O(N)_x}{N_x} + {O(N)_y}{N_y} + {O(N)_z}{N_z}
-{O(R)_x}{N_x} -{O(R)_y}{N_y} -{O(R)_z}{N_z}$$
$$n = { {O(N)_x}{N_x} + {O(N)_y}{N_y} + {O(N)_z}{N_z}
-{O(R)_x}{N_x} -{O(R)_y}{N_y} -{O(R)_z}{N_z} \over {R_x}{N_x}+{R_y}{N_y}+{R_z}{N_z}}$$
The *O(N)* can be any point of the triangle *p<sub>1</sub>* or *p<sub>2</sub>* or *p<sub>3</sub>* 
and the N is the cross-product of a segment from other points to the chosen point. For example, the chosen origin is 
*p<sub>1</sub>*, then $\ O(N) = {p_1}\$ and $\ N = ({p_2}-{p_1})×({p_3}-{p_1})\$
## Check if the point is inside the triangle
To check if the point is inside, we need to check if the point is a line inside the rectangular space of the line. This rectangular space has a horizontal expand along the segment and a vertical expand infinitely on both sides of the segment
For each line, we have this algorithm (*w* is the point; *s* and *e* is the start and end of the segment, based on the example above, we chose the *p<sub>1</sub>* as the origin of the normal vector, so we make $\ s = {p_1}\$ and $\ e = {p_2}\$):
$$d = ((w-s) ÷ |(ê-ŝ)|) ⋅ ((e-s) ÷ |(ê-ŝ)|)$$
$$d = ((w-s)÷\sqrt{({e_x}-{s_x})^2+({e_y}-{s_y})^2+({e_z}-{s_z})^2}) ⋅ ((e-s)÷\sqrt{({e_x}-{s_x})^2+({e_y}-{s_y})^2+({e_z}-{s_z})^2})$$
$$d= {({w_x}-{s_x})({e_x}-{s_x})+({w_y}-{s_y})({e_y}-{s_y})+({w_z}-{s_z})({e_z}-{s_z})\over{({e_x}-{s_x})^2+({e_y}-{s_y})^2+({e_z}-{s_z})^2}}$$
Do the same with *p1* and *p<sub>3</sub>*, so this time $\ e = {p_3}\$
$$t = .(do the same)..$$
if d and t are between the range of 0 and 1, then the point land on the triangle
