## Warm-up
Consider the system of equations:
$$
\begin{cases}
x+y-z &=& 4 \\
2x+y+z &=& 1 \\
5x-y-3z &=& 10
\end{cases}
$$
### Answer
$$
\begin{cases}
x = 1 \\
y = 1 \\
z = -2
\end{cases}
$$


## Linear equations

```slide-note 
file: LA - Chap1.pdf
page: 4
dpi: 4
```

### Example

```slide-note 
file: LA - Chap1.pdf
dpi: 4
page: 6
```

## Linear system

```slide-note 
file: LA - Chap1.pdf
dpi: 4
page: 8
```

### Example

```slide-note 
file: LA - Chap1.pdf
dpi: 4
page: 9
```

## General system of two

```slide-note 
file: LA - Chap1.pdf
dpi: 4
page: 10-11
```

## Augmented matrices

```slide-note 
file: LA - Chap1.pdf
dpi: 4
page: 13
```

### Example

```slide-note 
file: LA - Chap1.pdf
dpi: 4
page: 14
```

## Elementary row operations

```slide-note 
file: LA - Chap1.pdf
dpi: 4
page: 16
```

### Example

```slide-note 
file: LA - Chap1.pdf
dpi: 4
page: 17-19
```

## Gaussian elimination

### Echelon forms

#### Zero / nonzero row
```slide-note 
file: LA - Chap1.pdf
dpi: 4
page: 22
```

#### Reduced / NOT reduced row-echelon form
```slide-note 
file: LA - Chap1.pdf
dpi: 4
page: 23-24
```

#### Solve system of equation from reduced row-echelon form augmented matrix

```slide-note 
file: LA - Chap1.pdf
dpi: 4
page: 26-27
```

#### Exercise

$$
\begin{cases}
x+y-2z &=& 1 \\
4x-y+z &=& 6 \\
3x+y-3z &=& 2
\end{cases}
$$
##### Solution
The augmented matrix:
$$
\begin{flalign*}
&
\begin{bmatrix}
1 & 1 & -2 & 1 \\ 
4 & -1 & 1 & 6 \\ 
3 & 1 & -3 & 2
\end{bmatrix}\\\\
\begin{cases}
R_{2}=R_{2}-4R_{1}\\
R_{3}=R_{3}-3R_{1}\\
\end{cases}\Rightarrow\ & 
\begin{bmatrix}
1 & 1 & -2 & 1 \\ 
0 & -5 & 9 & 2 \\
0 & -2 & 3 & -1
\end{bmatrix}\\\\
\begin{cases}
R_{2}=\frac{1}{5}R_{2}\\
\end{cases}\Rightarrow\ & 
\begin{bmatrix}
1 & 1 & -2 & 1 \\ 
0 & 1 & -\frac{9}{5} & -\frac{2}{5} \\
0 & -2 & 3 & -1
\end{bmatrix}\\\\
\begin{cases}
R_{1}=R_{1}-R_{2}\\
R_{3}=R_{3}+2R_{2}
\end{cases}\Rightarrow\ & 
\begin{bmatrix}
1 & 0 & - \frac{1}{5} & \frac{7}{5} \\ 
0 & 1 & -\frac{9}{5} & -\frac{2}{5} \\
0 & 0 & - \frac{3}{5} & - \frac{9}{5}
\end{bmatrix}\\\\
\begin{cases}
R_{3}=-\frac{5}{3}R_{3}
\end{cases}\Rightarrow\ & 
\begin{bmatrix}
1 & 0 & - \frac{1}{5} & \frac{7}{5} \\
0 & 1 & -\frac{9}{5} & -\frac{2}{5} \\
0 & 0 & 1 & 3
\end{bmatrix}\\\\
\begin{cases}
R_{1}=R_{1} + \frac{1}{5}R_{3}\\
R_{2}=R_{2} + \frac{9}{5}R_{3}
\end{cases}\Rightarrow\ & 
\begin{bmatrix}
1 & 0 & 0 & 2 \\ 
0 & 1 & 0 & 5 \\
0 & 0 & 1 & 3
\end{bmatrix}\\\\
\end{flalign*}
$$
So the solution is:
$$
\begin{cases}
x=2 \\
y=5 \\
z=3
\end{cases}
$$

### Eliminating Method

The **Gaussian Elimination** procedure (also called **row-reduction**) allows us to put a matrix in a **row-echelon** form. It consists of **five** steps.

##### Step 1.
***Locate*** the **leftmost nonzero column**.

##### Step 2. 
***Swap* the $1^{st}$ row** with another row (if necessary) **so** that **the top of the column found in Step 1 is nonzero**.

##### Step 3.
***Multiply*** the $1^{st}$ row with **a scalar** to **make the leading $= 1$.**

##### Step 4. 
***Add*** some **multiple of $1^{st}$ row** to make the **column becomes all zeros** (except the $1^{st}$ row).

##### Step 5.
***Cover* the $1^{st}$ row**, **restart the procedure** with the remaining matrix **until** the whole matrix is in  **row-echelon form**.

The **Gauss-Jordan Elimination** procedure allows to find the reduced row-echelon form. It includes another Step.

##### Step 6
***Working upward*** from the last nonzero row. **Add suitable multiples** of each row to the rows above it so that **all entries above the pivot becomes zeros**.

#### Example

```slide-note 
file: LA - Chap1.pdf
page: 38
```
$$
\begin{flalign*}
& 
\begin{bmatrix}
1 & 3 & -2 & 0 & 2 & 0 & 0\\
2 & 6 & -5 & -2 & 4 & -3 & -1\\
0 & 0 & 5 & 10 & 0 & 15 & 5\\
2 & 6 & 0 & 8 & 4 & 18 & 6
\end{bmatrix}\\\\
\Rightarrow\ &
\begin{bmatrix}
1 & 3 & -2 & 0 & 2 & 0 & 0\\
0 & 0 & -1 & -2 & 0 & -3 & -1\\
0 & 0 & 5 & 10 & 0 & 15 & 5\\
0 & 0 & -4 & 8 & 0 & 18 & 6
\end{bmatrix}\\\\
\Rightarrow\ &
\begin{bmatrix}
1 & 3 & -2 & 0 & 2 & 0 & 0\\
0 & 0 & 1 & 2 & 0 & 3 & 1\\
0 & 0 & 0 & 0 & 0 & 0 & 0\\
0 & 0 & 0 & 0 & 0 & 6 & 2
\end{bmatrix}\\\\
\Rightarrow\ &
\begin{bmatrix}
1 & 3 & -2 & 0 & 2 & 0 & 0\\
0 & 0 & 1 & 2 & 0 & 3 & 1\\
0 & 0 & 0 & 0 & 0 & 1 & \frac{1}{3}\\
0 & 0 & 0 & 0 & 0 & 0 & 0
\end{bmatrix}\\\\
\end{flalign*}
$$
```slide-note 
file: LA - Chap1.pdf
page: 41
```

### Homogeneous linear systems

```slide-note 
file: LA - Chap1.pdf
page: 45
```

#### Example

```slide-note 
file: LA - Chap1.pdf
page: 47
```

> **Theorem.** A homogeneous linear system with more unknowns than equations has infinitely many solutions.

