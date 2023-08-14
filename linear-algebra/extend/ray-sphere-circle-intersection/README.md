***Ray*** is a normalized vector that represents a direction <br>
***Origin*** is a vector that represents a position <br>
***Sphere/Circle*** is a shape that has a position, and *radius*

# Sphere / Circle-ray (from an origin intersection)
We know that a point inside a circle or sphere must have a distance from the center of the sphere to be equal to the radius of the sphere/radius. So we have this equation 
$\ \sqrt{ {d_x}^2 + {d_y}^2 + {d_z}^2} \le r\$ , $\ \sqrt{ {d_x}^2 + {d_y}^2 + {d_z}^2}\$ is to calculate the of distance vector from the *scaled ray from origin (O+R)* to *Sphere/Cirlce* by an *n* number.
Where (*S* is the sphere/circle location)
+ *d<sub>x</sub>* = $\{S_x}-{O_x}-{R_x}n\$
+ *d<sub>y</sub>* = $\{S_y}-{O_y}-{R_y}n\$
+ *d<sub>z</sub>* = $\{S_z}-{O_z}-{R_z}n\$
By substituting to the equation, we have
$$\sqrt{({S_x}-{O_x}-{R_x}n)^2+({S_y}-{O_y}-{R_y}n)^2+({S_z}-{O_z}-{R_z}n)^2} \le r$$
After expanding
$$\sqrt{{S_x}^2 + {O_x}^2 + {R_x}^2{n}^2 -2{S_x}{O_x} -2{S_x}{R_x}n + 2{O_x}{R_x}n + {S_y}^2 + {O_y}^2 + {R_y}^2{n}^2 -2{S_y}{O_y} -2{S_y}{R_y}n + 2{O_y}{R_y}n + {S_z}^2 + {O_z}^2 + {R_z}^2{n}^2 -2{S_z}{O_z} -2{S_z}{R_z}n + 2{O_z}{R_z}n}  \le  r$$
$${S_x}^2 + {O_x}^2 + {R_x}^2{n}^2 -2{S_x}{O_x} -2{S_x}{R_x}n + 2{O_x}{R_x}n + {S_y}^2 + {O_y}^2 + {R_y}^2{n}^2 -2{S_y}{O_y} -2{S_y}{R_y}n + 2{O_y}{R_y}n + {S_z}^2 + {O_z}^2 + {R_z}^2{n}^2 -2{S_z}{O_z} -2{S_z}{R_z}n + 2{O_z}{R_z}n  \le  r^2$$
Isolation n
$${R_x}^2{n}^2 + {R_y}^2{n}^2 + {R_z}^2{n}^2 -2{S_x}{R_x}n -2{S_y}{R_y}n -2{S_z}{R_z}n + 2{O_x}{R_x}n + 2{O_y}{R_y}n + 2{O_z}{R_z}n \le r^2 - {S_x}^2 - {S_y}^2 - {S_z}^2 - {O_x}^2 - {O_y}^2 - {O_z}^2 + 2{S_x}{O_x} + 2{S_y}{O_y} + 2{S_z}{O_z}$$
Make the equation become a quadratic equation ($\ ax^2 + bx = c\$):
$$n^2({R_x}^2 + {R_y}^2+{R_z}^2) + 2n({O_x}{R_x} + {O_y}{R_y} + {O_z}{R_z} - {S_x}{R_x}-{S_y}{R_y}-{S_z}{R_z}) \le r^2 - {S_x}^2 - {S_y}^2 - {S_z}^2 - {O_x}^2 - {O_y}^2 - {O_z}^2 + 2{S_x}{O_x} + 2{S_y}{O_y} + 2{S_z}{O_z}$$
where
- $\ x=n\$
- $\ a={R_x}^2 + {R_y}^2+{R_z}^2\$
- $\ b=2({O_x}{R_x} + {O_y}{R_y} + {O_z}{R_z} - {S_x}{R_x}-{S_y}{R_y}-{S_z}{R_z})\$
- $\ c=r^2 - {S_x}^2 - {S_y}^2 - {S_z}^2 - {O_x}^2 - {O_y}^2 - {O_z}^2 + 2{S_x}{O_x} + 2{S_y}{O_y} + 2{S_z}{O_z}\$
