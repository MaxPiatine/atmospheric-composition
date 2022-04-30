# Atmospheric Composition

We will simulate the collisions of nitrogen gas ($N_2$) and oxygen gas ($O_2$), the main gas molecules that make up air. We will assume they are ideal gases so there are only elastic collisions. Air is about $80\%$ nitrogen gas and about $20\%$ oxygen gas, so this will be reflected in the amount of each molecule in the simulation.

We are animating multiple objects to be able to collide between each other with different velocities. The question we are trying to solve is “What happens when you place multiple objects inside a box and give them different masses and velocities”. In theory, we know that momentum depends on the mass and velocity $p=mv$; therefore, we can assume if objects with higher mass and/or velocity would “somewhat” conserve their momentum compared to the smaller in mass and velocity objects. 

Since we are trying to animate the different objects in a friction-less box, we would set up a $n\times n$ grid and have a function that would take $N$ amounts of circular shaped objects in it.

We set the initial positions of the molecules in the box, and give them random initial velocities. We set the mass and size for nitrogen gas molecules, and the mass and size for oxygen gas molecules. As well as, colour coding the objects depending on the heavier masses, going from blue to red. Red being the heavier mass and blue being the lighter. 

Set the total animation time to somewhere between  30-60 seconds and time-step to $0.02s$ for $50$ frames per second animation. Allocate numpy zeros arrays for velocity and position of objects.

For each frame, determine which molecules are colliding and compute the resulting velocities of the collisions with conservation of momentum. This will be done with a double for loop to iterate over all possible pairs of objects. The objects collide if the distance between their positions is less than the sum of their radii. We would need to check if objects are colliding with the walls/borders of the box and determine the resulting velocities. Also, the position for each molecule will be determined for each frame/time-step.

Say we take two objects to collide in our animation, we would need to find out if the collision was elastic. We will use the following equations to compute the elastic collisions of the molecules.

\[m_1v_{1i}+m_2v_{2i}=m_1v_{1f}+m_2v_{2f}   \textbf{ }(\textbf{Elastic Collisions})\]

Repeat for $N$ frames to get 30-60 seconds. Depending on the run time complexity of the program the time of animation might vary. 

Create the animation using the matplotlib animation function.


‪Collision Lab‬ - PhET Interactive Simulations, \url{https://phet.colorado.edu/sims/html/collision-lab/latest/collision-lab_en.html}

Mantina, Manjeera et al. “Consistent van der Waals radii for the whole main group.” The journal of physical chemistry. A vol. 113,19 (2009): 5806-12. doi:10.1021/jp8111556

"Air - Molecular Weight and Composition", \url{https://www.engineeringtoolbox.com/molecular-mass-air-d_679.html}, Engineering ToolBox

![alt text](https://github.com/maxpiatine/atmospheric-composition/blob/main/frame0.png?raw=true)
