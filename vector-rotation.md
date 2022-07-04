Coordinate system: $x$ points to right, $y$ points to up.

A vector $\overrightarrow{OA}$ : $(x_A, y_A)$, length is $r$, rotates $\theta$ 
on counterclockwise direction to vector $\overrightarrow{OB}$ : $(x_B, y_B)$.  
Angles between $\overrightarrow{OA}$, $\overrightarrow{OB}$ and axis $x$ are 
$\alpha$ and $\beta$.  
  
Polar coordinate format:  
$\overrightarrow{OA}$ : $(r\cos\alpha, r\sin\alpha)$  
$\overrightarrow{OB}$ : $(r\cos\beta, r\sin\beta)$  
  
$\beta=\alpha+\theta$  
  
$
\begin{cases}
x_A &= &r\cos\alpha \\
y_A &= &r\sin\alpha \\
x_B &= &r\cos\beta \\
y_B &= &r\sin\beta \\
\end{cases}
$
  
$
\begin{cases}
r\cos\beta &= &r\cos(\alpha+\theta) &= 
&r(\cos\alpha\cos\theta-\sin\alpha\sin\theta) &=
&r\cos\alpha\cos\theta-r\sin\alpha\sin\theta \\
r\sin\beta &= &r\sin(\alpha+\theta) &=
&r(\sin\alpha\cos\theta+\cos\alpha\sin\theta) &=
&r\sin\alpha\cos\theta+r\cos\alpha\sin\theta \\
\end{cases}
$
  
$\Longrightarrow$
  
$
\begin{cases}
x_B &= &x_A\cos\theta-y_A\sin\theta \\
y_B &= &x_A\sin\theta+y_A\cos\theta \\
\end{cases}
$
  
Example: Define direction as forward of current path, slope is perpendicular to 
direction and points to right. That is to say direction rotates -90 degrees to 
slope.  
$direction=Eigen::Vector2f(x, y)$  
$slope=Eigen::Vector2f(y, -x)$  
or  
$slope=Eigen::Vector2f(x, y)$
$direction=Eigen::Vector2f(-y, x)$
  
Represented by matrix multiplication format:  
$
[x_B, y_B] = [x_A, y_A] \times
\begin{bmatrix}
\cos\theta & \sin\theta \\
-\sin\theta & \cos\theta \\
\end{bmatrix}
$
  
$
R_{counter_clockwise}=
\begin{bmatrix}
\cos\theta & \sin\theta \\
-\sin\theta & \cos\theta \\
\end{bmatrix}
$
  
$
R_{clockwise} =
\begin{bmatrix}
\cos(-\theta) & \sin(-\theta) \\
-\sin(-\theta) & \cos(-\theta) \\
\end{bmatrix}
= \begin{bmatrix}
\cos\theta & -\sin\theta \\
\sin\theta & \cos\theta \\
\end{bmatrix}
$