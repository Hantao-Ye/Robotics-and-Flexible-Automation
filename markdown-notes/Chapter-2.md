# Chapter-2

[TOC]

## 1 - Descriptions: Positions, Orientations, and Frames

### Position

Any point could be located in the universe with a $3\times1$ **position vector** once a coordinate system is established. And the notation for the position of $A$ is $^AP$, which is defined by

$$
\begin{aligned}
    ^AP=\begin{bmatrix}
        p_x\\[1ex]
        p_y\\[1ex]
        p_z
    \end{bmatrix}
\end{aligned}
$$

### Orientations

In order to describe the orientation of body, we will *attach a coordinate system to the body* and then give a description of this coordinate system **relative to** the reference system.

One way to describe the body-attached coordinate system $\{B\}$, is to write the unit vectors of its three principal axes in terms of the coordinate system $\{A\}$

The principal directions of $\{B\}$ is defined as $\hat{X}_B$, $\hat{Y}_B$ and $\hat{Z}_B$. If the terms of coordinate system $\{A\}$, they are called $^A\hat{X}_B$, $^A\hat{Y}_B$ and $^A\hat{Z}_B$, whose combination will be called as a **rotation matrix**, where $\{B\}$ is relative to $\{A\}$

$$
^A_BR = 
\begin{bmatrix}
    ^A\hat{X}_B&^A\hat{Y}_B&^A\hat{Z}
\end{bmatrix} = 
\begin{bmatrix}
    \hat{X}_B\cdot \hat{X}_A&\hat{Y}_B\cdot \hat{X}_A&\hat{Z}_B\cdot \hat{X}_A\\[2ex]
    \hat{X}_B\cdot \hat{Y}_A&\hat{Y}_B\cdot \hat{Y}_A&\hat{Z}_B\cdot \hat{Y}_A\\[2ex]
    \hat{X}_B\cdot \hat{Z}_A&\hat{Y}_B\cdot \hat{X}_A&\hat{Z}_B\cdot \hat{Z}_A
\end{bmatrix}
$$

since $^A_BR =\ ^B_AR^T$ and $^A_BR\cdot ^B_AR^T = I$, we can know that the rotation matrix is **a orthogonal matrix**

### Frames

A frame is defined as the set of four vectors giving position position and orientation information

## 2 - Mappings

### Translation

according to the spacial relationship, translation could be simply calculated by addition

$$
^AP =\ ^BP+\ ^AP_{BORG}
$$

### Rotation

according to the definition of the rotation matrix, rotation could be simply calculated by multiply

$$
^AP =\ ^A_BR\ ^BP
$$

#### Axis

- X axis
$$
R_x(\theta)=\begin{bmatrix}
    1&0&0\\[2ex]
    0&\cos\theta&-\sin\theta\\[2ex]
    0&\sin\theta&\cos\theta
\end{bmatrix}
$$

- Y axis
$$
R_y(\theta)=\begin{bmatrix}
    \cos\theta&0&\sin\theta\\[2ex]
    0&1&0\\[2ex]
    -\sin\theta&0&\cos\theta
\end{bmatrix}
$$

- Z axis
$$
R_z(\theta)=\begin{bmatrix}
    \cos\theta&-\sin\theta&0\\[2ex]
    \sin\theta&\cos\theta&0\\[2ex]
    0&0&1
\end{bmatrix}
$$

### General Frames

according to the translation and rotation, the general transform could be written into

$$
\begin{bmatrix}
    ^AP\\[1ex]
    1
\end{bmatrix}=
\begin{bmatrix}
   \begin{array}{ccc | c}
        &^A_BR&&  ^AP_{BORG} \\[1ex]\hline
        0&0&0  & 1
   \end{array}
\end{bmatrix}
\begin{bmatrix}
    ^BP\\[1ex]
    1
\end{bmatrix}
$$

### Algorithm

- if the tool frame is to be rotated or translated about the $k_{th}$ unit vector of the **reference frame**, then **pre-multiply** it by the general frames
- if the tool frame is to be rotated or translated about **its own $k_{th}$ unit vector**, then **post-multiply** it by the general frame