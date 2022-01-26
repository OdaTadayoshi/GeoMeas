![](https://gitee.com/huangzhexiaohao/geo-meas/raw/master/README/image-20220110185635682.png)

This project is dedicated to the in depth development of  geometric measurement algorithms. The inspiration is derived from the vision software HALCON.

In the fields of navigation, industrial measurement, surveying and mapping .etc, we need to develop a large number of geometric measurement algorithms, and most of them is reusable. However, few of people tried to classify and arrange them. So we are trying to do something to make it easier for developers based on python.

# Tools
- Solidworks 3D sketch functions
- [Mermaid ](https://mermaid-js.github.io/mermaid/#/flowchart?id=graph)based on markdown



# Framework

 Any geometric algorithm can be regarded as realized by the fusion of **physical quantities** and **geometric elements**.  Geometric elements include **point**, **line** and **plane** and physical quantities include **angle**, **distance**, **coordinate**, **vector** and **pose**.  Any function can be named as the form of cal[...]From[...]()() and any conversion can be made between them. For example as [calCoordinateFrome2Lines](https://gitee.com/huangzhexiaohao/geo-meas/blob/master/doc/Coordinate.calCoordinateFrom2Lines.md).

![整体结构图](README/整体结构图.png)

 [The drawing tools can refer to here](https://excalidraw.com/).

# Data format

- **Coordinate:**
  $$
  P=\begin{bmatrix}
  x\\
  y\\
  z\\
  \end{bmatrix}
  $$
  →numpy.array

- **Vector:**
  $$
  \vec{l}=\begin{bmatrix}
  a\\
  b\\
  c\\
  \end{bmatrix}
  $$
  →numpy.array

- **Pose:** 
  $$
  R=\begin{bmatrix}
    r11&r12&r13\\
    r21&r22&r23\\
    r31&r32&r33\\
    \end{bmatrix}_{3×3}
    ,T=\begin{bmatrix}
    t_x\\
    t_y\\
    t_z\\
    \end{bmatrix}_{3×1}
  $$

  →numpy.array

- **Distance:**
  $$
  d
  $$
  →float

- **Angle：**
  $$
  θ
  $$
  →float

- **Plane：**
  $$
  Ax+By+Cz+D=0,[A,B,C,D]
  $$
  →numpy.array

- **Line:** 
  $$
  \frac{x-x_0}{m}=\frac{y-y_0}{n}=\frac{z-z_0}{p},[m,n,n,x_0,y_0,z_0]
  $$

  →numpy.array

# Tutorial
 Take the project of shield tail clearance measurement system as an example, the calculation flow chart could be shown as below:![盾尾间隙流程](README/盾尾间隙流程.png)



# Reference

1. http://immersivemath.com/

2. [1]丘维声. 解析几何(第2版)[M]. 北京大学出版社, 1996.
