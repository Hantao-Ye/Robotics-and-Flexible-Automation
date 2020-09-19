# Lecture-1

[TOC]

## Joint Type

- Prismatic
- Revolve

## Robot Types

### Cartesian Robot

<div align = center><img src = "../assets/L1-1.png" height = 400></div>

- Major axis: PPP
- Work envelope: rectangular box
- Gantry robot
- Easy to control

### Cylinder Robot

<div align = center><img src = "../assets/L1-2.png" height = 400></div>

- Major axis: RPP
- Work envelope: cylinder

### Spherical Robot

<div align = center><img src = "../assets/L1-3.png" height = 400></div>

- Major axis: RRP
- Work envelope: sphere

### Scara Robot

<div align = center><img src = "../assets/L1-4.png" height = 400></div>

- Major axis: RRP
- All three joints are vertical 
- Work envelope: complex
- Selective Compliance Assembly Robot Arm
- Applications: assembly

### Articulated Robot

<div align = center><img src = "../assets/L1-5.png" height = 400></div>

- Major Axis: RRR
- Most popular, largest workspace
- Work envelope: very complex
- Applications: various

## Drive System

- Electrical
  - Most popular
- Chain drive
  - Educational
- Hydraulic
  - Most powerful
- Direct drive
  - No transmission
  - Easier to control
  - Adept one
  
## Precision, Repeatability, Accuracy

### Precision

Resolution, smallest move robot can make

### Repeatability

A measure of the ability of the robot to position the tool tip in the same place repeatedly

### Accuracy

A measure of the ability of the robot to place the tool tip at an arbitrarily prescribed location

## Degree of Freedoms

position could be changed by prismatic joints and revolute joints

but the orientation could only be changed by revolute joint

**For a structure with n joints to have n DOF, these n joints must be linear independent**

**In 3D space, the maximal number of linear independent direction is 6**