# <center>线性规划</center>

## 一般形式

$$max z = \sum\limits_{j=1}^{n}{c_j}{x_j}$$
$$
\begin{cases}
\sum\limits_{j=1}^{n}{a_{ij}}{x_j} = b_i,\ \ \ i=1,2,\cdots,m\\\\
{x_j}\geqslant0,\ \ \ \ \ \ j=1,2,\cdots,n
\end{cases}
$$
> 在标准型式中规定个约束条件的右端项 $b_i<0$，否则等式两端乘以-1

用向量和矩阵符号表述时为：
$$max z = C X$$
$$
\begin{cases}
\sum\limits_{j=1}^nP_jx_j = b \\\\
x_j \geqslant 0,\ \ \ j = 1,2,\cdots,n
\end{cases} 
$$
其中： $C = (c_1, c_2, \cdots, c_n)$
$$
X= \begin{bmatrix}x_1\\x_2\\\vdots\\x_n \end{bmatrix}; P_j= \begin{bmatrix}a_{1j}\\a_{2j}\\\vdots\\a_{mj} \end{bmatrix};b= \begin{bmatrix}b_1\\b_2\\\vdots\\b_m \end{bmatrix}
$$

$$
\begin{aligned}
max z &= CX \\
AX&=b \\
X&\geqslant0
\end{aligned}
$$
其中
$$
A=\begin{pmatrix}
a_{11}&a_{12}&\cdots&a_{1n} \\
\vdots&\vdots&&\vdots \\
a_{11}&a_{12}&\cdots&a_{1n} \\
\end{pmatrix}=(P_1,P_2,\cdots,P_n);0=\begin{bmatrix}0\\0\\\vdots\\0\end{bmatrix}
$$
A————约束条件的$m\times n$维系数矩阵，一般$m\lt n$
b————资源向量
C————价值向量
X————决策变量向量

无约束取值变量拆分成 ${x_k}=x_k^{'}-x_k^{''}$
约束为 $\geqslant$, 左端减去$x_m$
约束为 $\leqslant$, 左端加上$x_m$  