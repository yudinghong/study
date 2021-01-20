```latex
\alpha \beta \gamma \delta \epsilon \zeta \eta \theta \iota \kappa \lambda \mu \nu \xi \pi \rho \sigma \tau \upsilon \phi \chi \psi \omega
\Alpha \Beta \Gamma \Delta \Epsilon \Zeta \Eta \Theta \Iota \Kappa \Lambda \Mu \Nu \Xi \Pi \Rho \Sigma \Tau \Upsilon \Phi \Chi \Psi \Omega
```
$\alpha \beta \gamma \delta \epsilon \zeta \eta \theta \iota \kappa \lambda \mu \nu \xi \pi \rho \sigma \tau \upsilon \phi \chi \psi \omega \Alpha \Beta \Gamma \Delta \Epsilon \Zeta \Eta \Theta \Iota \Kappa \Lambda \Mu \Nu \Xi \Pi \Rho \Sigma \Tau \Upsilon \Phi \Chi \Psi \Omega $
`如果需要斜体则加上var前缀如 \varGamma` $\varGamma$

$$a^{21}$$
$$a_2$$
$\vec a$ $\overrightarrow{xy}$ $\overleftarrow{xy}$
$\mathtt{A}$ $\mathbb{A}$ $\mathsf{A}$
$\langle\rangle$
$\left(\frac{x}{y}\right)$ `使符号大小与临近的公式相适应，适用所有括号`
$\sum_{i=1}^n{a_i}$
$\lim_{x\to0}$
$\int_0^\infty{fxdx}$
$\frac{a}{b}$
$\sqrt[x]{y}$
$\infty \cup \cap \subset \subseteq \supset \in \notin \varnothing \forall \exists \lnot \nabla \partial$ 
$a\ b$
$a\quad b$
$$\begin{matrix}
1&0&0\\
1&0&0\\
1&0&0\\
\end{matrix}
$$
* pmatrix ：小括号边框
* bmatrix ：中括号边框
* Bmatrix ：大括号边框
* vmatrix ：单竖线边框
* Vmatrix ：双竖线边框
* 横省略号：\cdots
* 竖省略号：\vdots
* 斜省略号：\ddots
$$\begin{bmatrix}
{a_{11}}&{a_{12}}&{\cdots}&{a_{1n}}\\
{a_{21}}&{a_{22}}&{\cdots}&{a_{2n}}\\
{\vdots}&{\vdots}&{\ddots}&{\vdots}\\
{a_{m1}}&{a_{m2}}&{\cdots}&{a_{mn}}\\
\end{bmatrix}$$
### 阵列
c 居中 l 左对齐 r 右对齐 | 竖线
$$\begin{array}{c|lll}
{↓}&{a}&{b}&{c}\\
\hline
{R_1}&{c}&{b}&{a}\\
{R_2}&{b}&{c}&{c}\\
\end{array}$$
$$\begin{cases}
a_1x+b_1y+c_1z=d_1\\
a_2x+b_2y+c_2z=d_2\\
a_3x+b_3y+c_3z=d_3\\
\end{cases}
$$
