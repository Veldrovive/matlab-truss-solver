# Matlab Warren Truss Solver
For ESC103.

By default, this will construct and solve for the internal forces of a Warren truss.
There is no reason the truss has to be a Warren truss, however. The only restriction is that each joint is connected to no more than four members so that each joint is solvable. Every force is assumed to be in the -y direction for simplicity of calculating moments.

This works by constructing a matrix that represents the linear equations for each joint. For each joint, the sum of forces in the x and y direction must both be 0 so we have 2*(number of joints) equations to solve. The number of members is 2*(number of joints) - 3 for a warren truss.

The reaction forces on each pinned joint are calculated such that the moment around that point must be zero. We assume that the two outermost joints are pinned while the rest float.
