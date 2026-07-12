# GitHub math render test

Temporary diagnostic file. Please report which of A–F render as math vs. show as raw source.

**A. Inline, bare dollars:** here is $a_{\mu\nu}$ and $\gamma = 1/\sqrt{1-\beta^2}$ inline.

**B. Inline, backtick form:** here is $`a_{\mu\nu}`$ and $`\gamma = 1/\sqrt{1-\beta^2}`$ inline.

**C. Block, simple single line:**

$$
\gamma = \frac{1}{\sqrt{1-\beta^2}}
$$

**D. Block, split wrapper, single line:**

$$
\begin{split}
\gamma = \frac{1}{\sqrt{1-\beta^2}}
\end{split}
\tag{T.1}
$$

**E. Block, split + pmatrix + `\\` row breaks (like Eq. 4.10):**

$$
\begin{split}
\begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} & = \gamma^2 \begin{pmatrix} 1 & -\beta \\ -\beta & 1 \end{pmatrix} \\
& = \gamma^2 \begin{pmatrix} 1 - \beta^2 & 0 \\ 0 & 1 - \beta^2 \end{pmatrix}
\end{split}
\tag{T.2}
$$

**F. Fenced math block:**

```math
\begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = \gamma^2 \begin{pmatrix} 1 - \beta^2 & 0 \\ 0 & 1 - \beta^2 \end{pmatrix}
```
