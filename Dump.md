$$
\begin{flalign*}
\begin{bmatrix}
1 & 1 & 1 & 1 & 7\\
27 & 9 & 3 & 1 & -11\\
64 & 16 & 4 & 1 & -14\\
0 & 0 & 0 & 1 & 10
\end{bmatrix}
\end{flalign*}
$$
$$
\begin{flalign*}
\begin{cases}
x_1&-&6x_2&&&&&+&3x_5&=&-2\\
&&&&x_3&&&+&4x_5&=&7\\
&&&&&&x_4&+&5x_5&=&8\\
&&&&&&&&0&=&0\\
\end{cases}
\end{flalign*}
\Leftrightarrow\ 
$$
$$
\begin{bmatrix}
0 & -2 & 3 & 1 \\ 3 & 6 & -3 & -2 \\ 6 & 6 & 3 & 5
\end{bmatrix}
$$
$$
\begin{flalign*}
&
\begin{bmatrix}
0 & -2 & 3 & 1 \\ 
3 & 6 & -3 & -2 \\ 
6 & 6 & 3 & 5
\end{bmatrix}\\[1em]
\begin{array}{l}
R_1\Leftrightarrow R_2
\end{array}
\Longrightarrow\ &
\begin{bmatrix} 
3 & 6 & -3 & -2 \\ 
0 & -2 & 3 & 1 \\
6 & 6 & 3 & 5
\end{bmatrix}\\[1em]
\begin{array}{l}
R_{1}= \frac{1}{3}R_{1}\\
R_3=R_3-6R_1
\end{array}
\Longrightarrow\ &
\begin{bmatrix} 
1 & 2 & -1 & - \frac{2}{3} \\ 
0 & -2 & 3 & 1 \\
0 & -6 & 9 & 9
\end{bmatrix}\\[1em]
\begin{array}{l}
R_{2}= -\frac{1}{2}R_{2}\\
R_3=R_3+6R_2
\end{array}
\Longrightarrow\ &
\begin{bmatrix} 
1 & 2 & -1 & - \frac{2}{3} \\ 
0 & 1 & - \frac{3}{2} & - \frac{1}{2} \\
0 & 0 & 0 & 6
\end{bmatrix}\\
\end{flalign*}
$$