$$Loss=-\sum(ln(b)+\lambda ||b||_2)*x_i$$

$$CurLoss=-\sum b_ix_i+\lambda||x||_2$$

$$
\text{Regret}=\sum_{\tau=1}^{T}\langle g,x_{\tau}\rangle-\min_{x \in X}\sum_{\tau=1}^{T}\langle g,x\rangle
$$
### RM algorithm
$$
r_{ts}=\sum_{\tau=1}^{t}  \langle g_{\tau},x_{\tau} \rangle-g_{\tau}[s]
$$
$$
x_{t+1}[s]=\frac{[r_{ts}^+]}{\sum_{s'}[r_{ts'}]^+}
$$

### RM+ algorithms

$$Q_{ts}=[Q_{t-1s}+\langle g_{\tau},x_{\tau} \rangle-g_{\tau}[s]]$$

$$
x_{t+1}[s]=\frac{Q_{ts}}{\sum_{s'} Q_{ts'}}
$$

### EG algorithm
$$
x_{t+1}=\frac{x_t \circ \exp{(-\eta g)}}{x_t \cdot \exp((-\eta g)) }
$$

### OMD

$$
x_{t+1}=\arg \min_{x \in X} g^Tx+\frac{1}{2}(x-x_{t})^TA(x-x_{t})
$$
$A$ is a diagonal matrix with strictly positive diagonal entrie. i.e. $A_{ii}>0$ for all $i \in {[n]}$,and $A_{ij}=0$ for $i\neq j$.

### OGD


$$x_{t+1}=\arg \min_{x \in X}||x_t-\eta g_t-x||=\arg \min_{x \in X}\langle \eta g_t,x \rangle+\frac{1}{2}||x_t-x||_2^2$$

### end