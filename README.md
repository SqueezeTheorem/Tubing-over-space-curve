# Tubing a Vector Space Curve using the Frenet-Serret Frame

The process of generating a tube around a space curve involves constructing a localized, moving coordinate system at every point on the curve. This is precisely the role of the Frenet-Serret Frame $\{\mathbf{T}, \mathbf{N}, \mathbf{B}\}$.

### 1. Defining the Space Curve

Let the space curve be defined by a vector function $\mathbf{r}$ that depends on a parameter $t$:

$$\mathbf{r}(t) = \left\langle x(t), y(t), z(t) \right\rangle$$

### 2. The Frenet-Serret Frame

The Frenet-Serret frame is an orthonormal basis that travels along the curve, providing the three crucial directions at any point:

The Unit Tangent Vector ($\mathbf{T}$)

This vector points in the direction of motion along the curve. It is the normalized first derivative of $\mathbf{r}(t)$.

$$\mathbf{T}(t) = \frac{\mathbf{r}'(t)}{|\mathbf{r}'(t)|}$$

The Unit Normal Vector ($\mathbf{N}$)

This vector points inward, indicating the direction in which the curve is bending. It is calculated from the normalized derivative of the tangent vector.

$$\mathbf{N}(t) = \frac{\mathbf{T}'(t)}{|\mathbf{T}'(t)|}$$

The Unit Binormal Vector ($\mathbf{B}$)

This vector completes the right-handed coordinate system. It measures the "twist" or torsion of the curve in space and is found via the cross product of $\mathbf{T}$ and $\mathbf{N}$.

$$\mathbf{B}(t) = \mathbf{T}(t) \times \mathbf{N}(t)$$

### 3. The Normal Plane

The vectors $\mathbf{N}(t)$ and $\mathbf{B}(t)$ are both mutually perpendicular, and critically, they are both perpendicular to the tangent vector $\mathbf{T}(t)$.

Together, $\mathbf{N}$ and $\mathbf{B}$ define the Normal Plane—a plane that is always perfectly perpendicular to the curve's instantaneous direction of travel. This is the plane in which the circular cross-section of the tube must lie.

### 4. Defining the Circular Cross-Section

To form the tube, we need to trace a circle of constant radius $a$ in the Normal Plane at every point $\mathbf{r}(t)$. We use a new angular parameter, $\theta$, for this circle (where $0 \le \theta < 2\pi$).

The vector function $\mathbf{c}(t, \theta)$ describes the position of a point on the cross-section circle, relative to the curve itself:

$$\mathbf{c}(t, \theta) = a \left( \mathbf{N}(t) \cos \theta + \mathbf{B}(t) \sin \theta \right)$$

Here, $a$ represents the radius of the tube.

### 5. The Final Tube Surface

Since the vectors $\mathbf{N}(t)$ and $\mathbf{B}(t)$ are calculated relative to the origin (i.e., they define directions), the vector $\mathbf{c}(t, \theta)$ is currently centered at the origin.

To properly place the cross-section circle onto the curve, we simply add the vector $\mathbf{r}(t)$ (the position on the path) to the cross-section vector $\mathbf{c}(t, \theta)$.

This two-parameter function, $\mathbf{f}(t, \theta)$, now describes the entire 3D tube surface:

$$\mathbf{f}(t, \theta) = \mathbf{r}(t) + a \left( \mathbf{N}(t) \cos \theta + \mathbf{B}(t) \sin \theta \right)$$

As the parameter $t$ sweeps along the curve and $\theta$ sweeps around the circle, this function generates the surface of the tube over the space curve $\mathbf{r}(t)$.
