# RocketAscent
Some rocket ascent guidance code using primer vector theory

Read the Readme.pdf for a full description including the theory, algorithm and "documentation"

So far the most important contribution is the high-level code I wrote to get me started
Here's a description of the idea:

Here is a detailed explanation of the code:

    1. The Spacecraft struct represents the state of the spacecraft, including its position (x, y, z) and velocity (vx, vy, vz). These variables are defined as double data types.

    2. The objectiveFunction function calculates the objective function based on the current state of the spacecraft. The objective function represents the mission requirements and the desired spacecraft trajectory. It returns a double value.

    3. The computePrimerVectors function computes the primer vectors based on the current state of the spacecraft. The primer vectors represent small changes in the spacecraft's position and velocity that can be used to correct its trajectory. The function returns a std::vector of Spacecraft objects.

    4. The computeTrajectoryCorrections function computes the trajectory corrections iteratively using an optimization algorithm. The function takes the current state of the spacecraft as an input and updates the spacecraft state with each correction.

    5. The main function initializes the spacecraft state and calls the computeTrajectoryCorrections function to compute the trajectory corrections.

Here are some additional details on the implementation:

    1. The optimization algorithm used to compute the trajectory corrections is not shown in the code. It could be a simple gradient descent algorithm or a more advanced algorithm, such as a nonlinear programming algorithm.

    2. The while loop in the computeTrajectoryCorrections function continues until the optimal trajectory is achieved. In practice, the loop would terminate after a certain number of iterations or when the objective function reaches a minimum value.

    3. The correction variable represents the optimal trajectory correction computed by the optimization algorithm. It is added to the spacecraft state to correct its trajectory.

    4. The primer vectors are not computed in the code, but the computePrimerVectors function would calculate them based on the current state of the spacecraft and the objective function.

Again, this is a high-level example of how a C++ code for primer vector guidance could be structured, and the actual implementation details will depend on the specific mission requirements and spacecraft dynamics.
