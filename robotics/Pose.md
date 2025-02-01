- A combination of [Position](Position) and [Orientation](Orientation) that fully describes how an object is situated in three-dimensional space
$$
T = SE(3) = \begin{pmatrix} 
R & p \\
0_{1\times3} & 1
\end{pmatrix} = \begin{pmatrix}
r_{11} & r_{12} & r_{13} & x \\
r_{21} & r_{22} & r_{23} & y \\
r_{31} & r_{32} & r_{33} & z \\
0 & 0 & 0 & 1
\end{pmatrix}
$$

Where:
- $R \in SO(3)$ is the 3×3 rotation matrix representing orientation
- $p \in \mathbb{R}^3$ is the position vector
- $SE(3)$ is the Special Euclidean group in 3D, representing all possible poses
