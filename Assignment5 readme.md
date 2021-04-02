# Assignment-5
## AIM
In this assignment we'll try to plot the potentials and the current vectors on a square electrode which is grounded on one side and is connected to a 1V potential by a wire of radius r,which is connected to the center of the electrode.
### Introduction 
We will use various equations such as relation between electric field and potential,continuity of the charge etc.
We also solve a differential equation
#### Assigining Potential

Assigining 1V to potential in contact with the wire

We first initialize the phi vector to all zeroes.Then we find out the points which are in contact with the wire using the condition,X*X+Y*Y is less than or equal to 8*8(Radius of the wire=8) We assign a value of 1V to the points obtained from the above condition. We plot this along with contour of potential matrix.

![Figure_5 1](https://user-images.githubusercontent.com/81006760/113404927-9bb3ed80-93c6-11eb-9a9d-d3dd5f6f5753.png)
Figure1 Points at 1V and contour(Phi)

Using the difference equation and boundary conditions to find Phi

We first store the present values of phi in a new matrix called oldphi.Then we start iterating phi using the difference equation mentioned above.We also keep track of the error after every iteration.We apply boundary conditions by making sure that at the edges the gradient of potentialis tangential.The points on the edge which is grounded are assigned 0V.
Then we plot the values of error vs noof iterations in semilogy,loglog and normal error vs no of iterations.We also plot every 50th point on the semilogy plot.

![Figure_5 2](https://user-images.githubusercontent.com/81006760/113404944-a2426500-93c6-11eb-879d-b1d074a42666.png)
Figure2 semilogy plot of error

![Figure_5 3](https://user-images.githubusercontent.com/81006760/113404953-a53d5580-93c6-11eb-9a12-b42c82ef5832.png)
Figure3 loglog plot of error

![Figure_5 4](https://user-images.githubusercontent.com/81006760/113404973-ac646380-93c6-11eb-8460-c3848e6e781b.png)
Figure4 error vs Niter

Fitting exp functions to the error plots

We try to fit exponential functions to the error plots.We do that for 2 cases.First we try to fit the whole error function and we try to fit only after 500 iterations.This is done using the lstsq function.

![Figure_5 5](https://user-images.githubusercontent.com/81006760/113405024-c2722400-93c6-11eb-8a7b-66f1d8305a95.png)
Figure5 Error fit plots

Plotting 3D surface potential 

WE plot the 3D surface potential of the electrode using a special library called the mpltoolkits.mplot3d.axes3d.
##### Computing and plotting the current vectors 
Calculating the current vectors

We then define two arrays jx and jy to store the values of current vectors along x-axis and y-axis.

![Figure_5 6](https://user-images.githubusercontent.com/81006760/113405043-c9993200-93c6-11eb-83d1-de7c1266d58e.png)
Figure6 3D surface potential

Plotting the current vectors 

For plotting the current vectors we use a special function called quiver which helps us in plotting vectors along with their direction.
We also plot the contour plot of potential which gives us the following plot.It can be noted that there is hardly any current in the upper part because there isn't any major change in potential in thet region.

###### Conclusion
This way we have assigned potential values to all the points on the electrode and plotted them.We also studied the error along with no of iterations.We finally calculated the current vectors and plotted them

![Figure_5 7](https://user-images.githubusercontent.com/81006760/113405067-d28a0380-93c6-11eb-97ab-1110f80cdff9.png)
Figure7 Current vector plot 

![Figure_5 8](https://user-images.githubusercontent.com/81006760/113405087-da49a800-93c6-11eb-97d3-2a0ab1807ec7.png)
Figure8 Contour plot of potential
