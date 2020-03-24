# Reformulation of Lemma 4.2



Let $S$ be a finite set with power set $\mathcal{P}(S)$. Let $F$ be a distribution on $\mathcal{P}(S)$ and let $X = \{X_i\}_{i \ge 1}$, $Y = \{Y_i\}_{i \ge 1}$ both be i.i.d $F$. Then if $M,N$ are random subsets of an index set $I$ such that $|M| \ge_{ST} |N|$, then:
$$
\left|\bigcup_{i\in M}X_i\right| \ge{ST} \left|\bigcup_{i\in N}Y_i\right|.
$$

## Proof

We want to show that 
$$
\mathbb{P}\left\{\left|\bigcup_{i\in M}X_i\right|\ge z\right\} \ge \mathbb{P}\left\{\left|\bigcup_{i\in N}Y_i\right|\ge z\right\}, \quad \forall z.
$$
We first observe that $\displaystyle \mathbb{P}\left\{\left|\bigcup_{i\in M}X_i\right|\ge z\right\} = \sum_{j=0}^{\infty} \mathbb{P}\left\{\left|\bigcup_{i= 0}^{j}X_i\right|\ge z\right\} \cdot \mathbb{P}\{|M|=j\}$, by conditioning on the size of the random set $M$.  This implies that 
$$
\mathbb{P}\left\{\left|\bigcup_{i\in M}X_i\right|\ge z\right\} = \mathbb{E}_{|M|}\left[\mathbb{P}\left\{\left|\bigcup_{i=0}^{|M|}X_i\right|\ge z\right\}\right].
$$
We therefore need to show that 
$$
\mathbb{E}_{|M|}\left[\mathbb{P}\left\{\left|\bigcup_{i=0}^{|M|}X_i\right|\ge z\right\}\right] \ge \mathbb{E}_{|N|}\left[\mathbb{P}\left\{\left|\bigcup_{i=0}^{|N|}Y_i\right|\ge z\right\}\right].
$$

#### CLAIM 1:

Let $\displaystyle f_X(K,z) = \mathbb{P}\left\{\left|\bigcup_{i=0}^{|M|}X_i\right|\ge z\right\}$. For any given fix $z$, $f_X(K,z)$ is a non-decreasing function of $K$.

#### CLAIM 2:

Let $X \ge_{ST} Y$, and let $g \colon \mathbb{R} \mapsto \mathbb{R}$ be non-decreasing, then $\mathbb{E}[g(X)] \ge \mathbb{E}[g(Y)]$.

Fix an arbitrary $z$, using **claims** **1** and **2**, we can write
$$
\mathbb{E}_{|M|}\left[\mathbb{P}\left\{\left|\bigcup_{i=0}^{|M|}X_i\right|\ge z\right\}\right] = \mathbb{E}_{|M|}\left[f_X(|M|,z)\right] \ge \mathbb{E}_{|N|}\left[f_X(|N|,z)\right] = \mathbb{E}_{|N|}\left[\mathbb{P}\left\{\left|\bigcup_{i=0}^{|N|}Y_i\right|\ge z\right\}\right].
$$
To conclude the proof, we need to establish both  **claims** **1** and **2**.