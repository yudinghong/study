```latex
\alpha \beta \gamma \delta \epsilon \zeta \eta \theta \iota \kappa \lambda \mu \nu \xi \pi \rho \sigma \tau \upsilon \phi \chi \psi \omega
\Alpha \Beta \Gamma \Delta \Epsilon \Zeta \Eta \Theta \Iota \Kappa \Lambda \Mu \Nu \Xi \Pi \Rho \Sigma \Tau \Upsilon \Phi \Chi \Psi \Omega
```
$\alpha \beta \gamma \delta \epsilon \zeta \eta \theta \iota \kappa \lambda \mu \nu \xi \pi \rho \sigma \tau \upsilon \phi \chi \psi \omega \Alpha \Beta \Gamma \Delta \Epsilon \Zeta \Eta \Theta \Iota \Kappa \Lambda \Mu \Nu \Xi \Pi \Rho \Sigma \Tau \Upsilon \Phi \Chi \Psi \Omega $
` 变量形式则加上var前缀如 \varGamma` $\varGamma$
`\displaystyle` `\textstyle`
$$a^{21}$$
$\underset{a}{\bigcup}$
$$a_2$$
$\pm$
$\vec a$ $\overrightarrow{xy}$ $\overleftarrow{xy}$
$\mathtt{A}$ $\mathbb{A}$ $\mathsf{A}$
$\langle\rangle$
$\left(\frac{x}{y}\right)$ `使符号大小与临近的公式相适应，适用所有括号`
$\sum_{i=1}^n{a_i}$
$\sum\limits_{i=1}^n{a_i}$
$\prod_{i=0}^n$
$\prod\limits_{i=0}^n$
$\lim_{x\to0}$
$\lim\limits_{x\to0}$
$\int_0^\infty{fxdx}\quad\prime\iint\oint$
$\frac{a}{b}$
$\dfrac{a}{c}\ \tfrac{a}{c}$
$\sqrt[x]{y}$
$\infty \cup \cap \subset \subseteq \supset \in \notin \varnothing \forall \exists \lnot \nabla \partial \bigvee \bigwedge$ 
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

c 居中 l 左对齐 r 右对齐 | 竖线
$$\begin{array}{c|lll}
{\downarrow}&{a}&{b}&{c}\\
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
$\because\ \times\ \div\ \mid\ \nmid\ \cdot\ \circ\ \ast\ \bigodot\ \bigotimes\ \leq\ \geq\ \neq\ \approx\ \equiv\ \coprod\ \therefore$
$\uparrow\downarrow\Uparrow\Downarrow\rightarrow\leftarrow\Rightarrow\Leftarrow\longrightarrow\longleftarrow\Longrightarrow\Longleftarrow$
$\angle\quad30^\circ$
$\overbrace{a+\underbrace{b+c}_{1.0}+d}^{2.0}$
$\underbrace{a\cdot a\cdots a}_{b\text{ times}}$
`如果你需要在不同的行显示对应括号，可以在每一行对应处使用 \left. 或 \right. 来放一个"影子"括号`
$
\begin{aligned}
a=&\left(1+2+3+  \cdots \right. \\
& \cdots+ \left. \infty-2+\infty-1+\infty\right)
\end{aligned}
$
行内$\bigl( \begin{smallmatrix} a & b \\ c & d \end{smallmatrix} \bigr)$ 