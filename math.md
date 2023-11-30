$$Loss=-\sum(ln(b)+\lambda ||b||_2)*x_i$$

$$CurLoss=-\sum b_ix_i+\lambda||x||_2$$

$$
\text{Regret}=\sum_{\tau=1}^{T}\langle g,x_{\tau}\rangle-\min_{x \in X}\sum_{\tau=1}^{T}\langle g,x_{\tau}\rangle
$$