$
\documentclass{article}
\usepackage{amsmath}

\begin{document}

\section*{How to Find the Inverse of a Matrix (Mod 26)}

We'll go through the steps using our example matrix:

\[
K =
\begin{bmatrix} 3 & 2 \\ 5 & 7 \end{bmatrix}
\]

We want to find \( K^{-1} \mod 26 \).

\hrule
\vspace{0.3cm}

\section*{Step 1: Find the Determinant}
The determinant of a \( 2 \times 2 \) matrix is given by:

\[
\det(K) = (a \times d - b \times c)
\]

For our matrix:

\[
\det(K) = (3 \times 7) - (2 \times 5) = 21 - 10 = 11
\]

\hrule
\vspace{0.3cm}

\section*{Step 2: Find the Modular Inverse of the Determinant (mod 26)}
We need the multiplicative inverse of \( 11 \mod 26 \). This means finding a number \( x \) such that:

\[
11 \times x \equiv 1 \pmod{26}
\]

Using the Extended Euclidean Algorithm, we find:

\[
11^{-1} \equiv 19 \pmod{26}
\]

(You can check: \( 11 \times 19 = 209 \), and \( 209 \mod 26 = 1 \), so \( 19 \) is correct.)

\hrule
\vspace{0.3cm}

\section*{Step 3: Swap and Negate Terms to Form the Adjugate Matrix}
For a \( 2 \times 2 \) matrix, we swap \( a \) and \( d \), and negate \( b \) and \( c \):

\[
\text{Adjugate of } K =
\begin{bmatrix} 7 & -2 \\ -5 & 3 \end{bmatrix}
\]

Since we're in mod 26, convert negatives:
- \( -2 \mod 26 = 24 \)
- \( -5 \mod 26 = 21 \)

So the adjugate matrix is:

\[
\begin{bmatrix} 7 & 24 \\ 21 & 3 \end{bmatrix}
\]

\hrule
\vspace{0.3cm}

\section*{Step 4: Multiply by the Modular Inverse of the Determinant}
Now, multiply each term in the adjugate matrix by \( 19 \mod 26 \):

\[
K^{-1} =
(19) \times
\begin{bmatrix} 7 & 24 \\ 21 & 3 \end{bmatrix} \mod 26
\]

Calculate each element mod 26:

\begin{itemize}
    \item \( 19 \times 7 = 133 \Rightarrow 133 \mod 26 = 3 \)
    \item \( 19 \times 24 = 456 \Rightarrow 456 \mod 26 = 14 \)
    \item \( 19 \times 21 = 399 \Rightarrow 399 \mod 26 = 9 \)
    \item \( 19 \times 3 = 57 \Rightarrow 57 \mod 26 = 5 \)
\end{itemize}

So, the inverse matrix mod 26 is:

\[
K^{-1} =
\begin{bmatrix} 3 & 14 \\ 9 & 5 \end{bmatrix}
\]

\hrule
\vspace{0.3cm}

\section*{Final Answer}
The inverse of 

\[
K =
\begin{bmatrix} 3 & 2 \\ 5 & 7 \end{bmatrix}
\]

mod 26 is:

\[
K^{-1} =
\begin{bmatrix} 3 & 14 \\ 9 & 5 \end{bmatrix} \mod 26
\]

\end{document}
$
