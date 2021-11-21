## GAMES103
notes and ref. for GAMES103

仓库将会存放课程学习过程中的相关资料、个人笔记等内容

### After-class reading list _of the first 6 lessons_

*Read on [After-class reading list](https://github.com/indevn/GAMES103/tree/main/After-class reading list)*

1. [Witkin and Baraff.2001.Physically Based Modeling - Rigid Body Dynamics.SIGS GRAPH Courses.](https://graphics.stanford.edu/courses/cs448b-00-winter/papers/phys_model.pdf)

2. [Muller et al.2005.Meshless Deformations Based on Shape Matching.TOG(SIGS GRAPH)](http://www.beosil.com/download/MeshlessDeformations_SIG05.pdf)

3. [Baraff and Witkin.1998. Large Step in Cloth Simulation.SIGGRAPH](https://www.ri.cmu.edu/pub_files/pub1/baraff_david_1998_1/baraff_david_1998_1.pdf)

4. [Bridson et al.2003.Simulation of Clothing with Folds and Wrinkles.SCA.](http://physbam.stanford.edu/~fedkiw/papers/stanford2003-06.pdf)
5. [Bergou et al.2006.A Quadratic Bending Model for lnextensible Surfaces.SCA.](https://cims.nyu.edu/gcl/papers/bergou2006qbm.pdf)
6. [Muller.2008.Hierarchical Position Based Dynamics.VRIPHYS.](https://matthias-research.github.io/pages/publications/hpbd.pdf)
7. [Bouaziz et al.2014.Projective Dynamics: Fusing Constraint Projections for Fast Simulation.TOG(SIGGRAPH)](https://www.cs.utah.edu/~ladislav/bouaziz14projective/bouaziz14projective.pdf)
8. [Le Grand.2007.GPU Gems 3-Chapter 32.Broad-Phase Collision Detection with CUDA.](https://developer.nvidia.com/gpugems/gpugems3/part-v-physics-simulation/chapter-32-broad-phase-collision-detection-cuda)
9. [Bridson et al.2002.Robust Treatment of Collisions, Contact and Friction for Cloth Animation.TOG (SIGGRAPH)](https://www.cs.ubc.ca/~rbridson/docs/cloth2002.pdf)
10. [Volino et al.2006.Resolving Surface Collisions through Intersection Contour Mir imization. TOG (SIGGRAPH)](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.92.863&rep=rep1&type=pdf)

(Optional)
1. Provot.1995.Deformation Constraints in a Mass-Spring Model to Describe Rigid Cloth Behavior. Graphics Interface.
2. Tournier et al.2015.Stable Constrained Dynamics.TOG(SIGGRAPH).
### Relevant Courses
- http://www.cs.cornell.edu/courses/cs5643/2014sp/



### Outline of Course

#### 1. Introduction

#### 2. Math Background

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

#### 3. Rigid Body Dynamics

- Rigid Body Motion 描述刚体运动(旋转和平移)
- Translation Motion
  - Integration Methods Explained
