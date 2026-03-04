### **I. Distance & Proximity Metrics**

For two points $X = (x_1, \dots, x_n)$ and $Y = (y_1, \dots, y_n)$:


| **Euclidean Distance ($L_2$):**      | $$d(\mathbf{x}, \mathbf{y}) = \sqrt{\sum^{n}_{k = 1} (x_k - y_k)^2}$$                            |
| ------------------------------------ | ------------------------------------------------------------------------------------------------ |
| **Manhattan Distance ($L_1$):**      | $$d(\mathbf{x}, \mathbf{y}) = \sum^{n}_{k = 1}  \vert x_k - y_k \vert $$                         |
| **Minkowski Distance ($L_p$):**      | $$d(\mathbf{x}, \mathbf{y}) = \left( \sum^{n}_{k = 1} {\vert x_k - y_k \vert} ^r \right)^{1/r}$$ |
| **Chebyshev Distance ($L_\infty$):** | $$d_{\infty}(\mathbf{x}, \mathbf{y}) = \max_i \vert x_i - y_i \vert$$                            |
| **Mahalanobis Distance:**            | $$d(X,Y) = \sqrt{(X-Y)^T \Sigma^{-1} (X-Y)}$$<br>_Where $\Sigma$ is the covariance matrix._      |

### **II. Similarity Measures**

| $$A \cdot B = \sum^{n}_{i = 1} A_i B_i$$<br><br>*Where $A$ and $B$ are valid matrices.* | $$\vert \vert A \vert \vert = \sqrt{\sum^{n}_{i = 1} A^2_i}$$<br><br>*Where $A$ is a valid matrix.* |
| --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |

| **Cosine Similarity:**           | $$\cos({\theta}) = \frac{A \cdot B}{\vert \vert A \vert \vert \space \vert \vert B \vert \vert}$$ |
| -------------------------------- | ------------------------------------------------------------------------------------------------- |
| **Extended Jaccard (Tanimoto):** | $$T(A,B) = \frac{A \cdot B}{\vert\vert A \vert\vert^2 + \vert\vert B \vert\vert^2 - A \cdot B}$$  |
### **III. Information Theory**
| **Entropy ($H$):**           | $$H(S) = -\sum_{i=1}^{c} p_i \log_2(p_i)$$                                                       |
| ---------------------------- | ------------------------------------------------------------------------------------------------ |
| **Information Gain ($IG$):** | $$IG(S, A) = H(S) - \sum_{v \in \text{Values}(A)} \frac{\vert S_v \vert}{\vert S \vert} H(S_v)$$ |
### **General Problem-Solving Logic**
#### **1. Constructing the Covariance Matrix ($\Sigma$)**
For a 2D dataset with variables $X$ and $Y$:
1. **Find Means:** Calculate $\bar{x}$ and $\bar{y}$.
2. **Calculate Variances:** Use $s^2 = \frac{\sum (x_i - \bar{x})^2}{n - 1}$ for both $X$ and $Y$.
3. **Calculate Covariance:** Use $Cov(X,Y) = \frac{\sum (x_i - \bar{x})(y_i - \bar{y})}{n - 1}$.
4. **Assemble Matrix:** $\Sigma = \begin{bmatrix} Var(X) & Cov(X,Y) \\ Cov(X,Y) & Var(Y) \end{bmatrix}$.
#### **2. Matrix Inversion ($2 \times 2$)**

If $\Sigma = \begin{bmatrix} a & b \\ c & d \end{bmatrix}$, then $\Sigma^{-1} = \frac{1}{ad - bc} \begin{bmatrix} d & -b \\ -c & a \end{bmatrix}$.
#### **3. Calculating Entropy/Gain**
1. **Base Entropy:** Calculate $H(S)$ for the target class (the "Total" entropy).
2. **Weighted Average:** For a specific attribute, calculate the entropy of each subset ($H(S_{sunny})$, $H(S_{rainy})$, etc.).
3. **Weighting:** Multiply each subset's entropy by its proportion relative to the total dataset ($\frac{n_{subset}}{n_{total}}$).
4. **Subtract:** Subtract the sum of the weighted entropies from the Base Entropy.