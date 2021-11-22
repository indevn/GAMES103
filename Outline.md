# Outline

## 1. Introduction

## 2. Math Background

**Vector**

- Definition
- Arithematic: Addition and Subtraction
  - Example: Linear Representation
- Vector Norm
  - Distance between **q** and **p**
- Arithematic: Dot Product
  - Example: Particle-Line Projection 点到线的投影
  - Example: Plane Representation 判断点和平面的位置关系
  - Example: Particle-Sphere Collision 点和球体的碰撞检测
- Arithematic: Cross Product
  - Triangle Normal and Area
  - Triangle Inside/Outside Test(假设四点同面)
  - Barycentric Coordinates 重心坐标
    - Baryoncentric weights → Barycentric Interpolation 重心插值
      - Gouraud shading

Tetrahedral Volume 四面体（体积的点积叉积形式，行列式形式）

- Example: Barycentric Weights
- Example: Particle-triangle Intersection 点和三角形的碰撞检测

**Matrix**

- Definition (Transpose, Diagonal, Identity, Symmetric)

- Multiplication

  - inverse

- Orthogonality 正交矩阵

  - $A=[a_0\,a_1\,a_2]\;\;,a_i^Ta_j=(i==j)?1:0$
  - Matrix Transformation （参考MVP变换）
    - Rotation
    - Scaling

- Singular Value Decomposition 奇异值分解

  A matrix can be decomposed into $A=UDV^T$,such that **D** is diagonal, and **U** and **V** are orthogonal

- Eigenvalue Decomposition 特征值分解

  A matrix can be decomposed into $A=UDU^{-1}$,such that **D**(eigenvalue) is diagonal, and **U** is are orthogonal

- Symetric Positive Definiteness(正定矩阵, s.p.d.)

- Linear Solver

  - Direct Linear Solver
  - Iterative Solver

- Tensor Calculus

  - 1st-order derivatives
  - 2nd-order derivatives
  - Example: A Spring
    - with two ends

## 3. Rigid Body Dynamics

- Rigid Body Motion 描述刚体运动(旋转和平移)
- Translation Motion
  - Integration Methods Explained