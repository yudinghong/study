# <center>线性规划</center>

## 一般形式

$$max z = \sum\limits_{j=1}^{n}{c_j}{x_j}$$
$$
\begin{cases}
\sum\limits_{j=1}^{n}{a_{ij}}{x_j} = b_i,\ \ \ i=1,2,\cdots,m\\\\
{x_j}\geqslant0,\ \ \ \ \ \ j=1,2,\cdots,n
\end{cases}
$$
无约束取值变量拆分成 ${x_k}=x_k^{'}-x_k^{''}$
约束为 $\geqslant$, 左端减去$x_m$
约束为 $\leqslant$, 左端加上$x_m$