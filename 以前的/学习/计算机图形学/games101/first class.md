games101主要讲四个部分
·光栅化
·几何
·光线追踪
·模拟动画

计算机图形学和计算机视觉的区别
![[Pasted image 20240620194513.png]]
## transform
### 2D transformations
scale:
![[Pasted image 20240627154634.png]]
以原点为中心等比例缩放
$$\left[\begin{array}{c}x'\\y'\end{array}\right]=\left[\begin{array}{cc}s&0\\0&s\end{array}\right]\left[\begin{array}{c}x\\y\end{array}\right]$$
shear:
![[Pasted image 20240627154833.png]]
$$\left[\begin{array}{c}x'\\y'\end{array}\right]=\left[\begin{array}{cc}1&a\\0&1\end{array}\right]\left[\begin{array}{c}x\\y\end{array}\right]$$
 图形的切变，$y=\frac{1}{a}x$
 rotation:
 ![[Pasted image 20240627161220.png]]
 $$x^{\prime}=a x+b$$$$y\\y^{\prime}=c x+d y$$
 绕原点旋转
 $$\left[\begin{array}{c}x'\\y'\end{array}\right]=\left[\begin{array}{cc}a&b\\c&d\end{array}\right]\left[\begin{array}{c}x\\y\end{array}\right]$$
 ### 平移变换
 ![[Pasted image 20240627164719.png]]
$$\begin{bmatrix}x'\\y'\end{bmatrix}=\begin{bmatrix}a&b\\c&d\end{bmatrix}\begin{bmatrix}x\\y\end{bmatrix}+\begin{bmatrix}t_x\\t_y\end{bmatrix}$$
![[Pasted image 20240627164913.png]]
### 3D Transformations
![[Pasted image 20240627170026.png]]
Scale和Translate
Rotation![[Pasted image 20240627170355.png]]
3DRotation![[Pasted image 20240627171013.png]]
任意维度在某轴上旋转的公式
![[Pasted image 20240627171059.png]]
将3D物体映射到2D

Orthographic projection and Perspective projection
正交投影和透视投影
 ## Transform Count
 
 
 