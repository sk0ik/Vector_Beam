# ベクトルビーム

## 高次元ポアンカレ球

今まではジョーンズベクトルを

$$
\begin{bmatrix}
\alpha \newline
\beta
\end{bmatrix}
$$

と表してきたがこれを

$$
\ket{\psi _ l}=
\psi^l _ R \vert R _ l> + \psi^l _ L \vert L _ l >
$$

と表す。

$\psi^l _ R, \psi^l _ L$ はそれぞれの基底の係数で基底の取り方は例えば

$$
\vert R _ l > = \frac{1}{\sqrt{2}}e^{-il\phi}
\begin{bmatrix}
1 \newline
i
\end{bmatrix}
$$

$$
\vert L _ l > = \frac{1}{\sqrt{2}}e^{il\phi}
\begin{bmatrix}
1 \newline
-i
\end{bmatrix}
$$

つまり左右円偏光に $e^{\pm il\phi}$ という位相項がついている。これは光の軌道角運動量 $\frac{lh}{2\pi}$ に関係するもので $l$ をトポロジカルチャージと言う。 
実は軸対称なベクトルビームはこの式で書ける。
スカラービームの時と同様にこの基底の取り方は無数に（球の反対のものとセット）ある。

ただし係数にもトポロジカルチャージ $l$ が出てくることに注意。そうするとこの場合のストークスパラメーターはスカラービームの時のアナロジーから

$$
\begin{aligned}
S^l _ 0 &= \vert \psi^l _ R \vert ^ 2 + \vert \psi^l _ L \vert ^ 2 \newline
S^l _ 1 &= 2\vert \psi^l _ R \vert \vert \psi^l _ L \vert \cos{\phi} \newline
S^l _ 2 &= 2\vert \psi^l _ R \vert \vert \psi^l _ L \vert \sin{\phi} \newline
S^l _ 3 &= \vert \psi^l _ R \vert ^ 2 - \vert \psi^l _ L \vert ^ 2 \newline
(\phi &: arg(\psi^l _ R) - arg(\psi^l _ L))
\end{aligned}
$$

また高次元ポアンカレ球の経度と緯度がそれぞれ

$$
\begin{aligned}
2\theta &= \tan ^ {-1} {\Bigl( \frac{S^l _ 2}{S^l _ 1}\Bigr )} \newline
2\varphi &= \sin ^ {-1}{\Bigl (\frac{S^l _ 3}{S^l _ 0}\Bigr )}
\end{aligned}
$$

例としてラジアル偏光ビームを見ていく。ジョーンズベクトルは

$$
\begin{bmatrix}
\cos{\phi} \newline
\sin{\phi}
\end{bmatrix}
$$

であったのでこれを

$$
\vert \psi _ l = \cos{\phi}
\begin{bmatrix}
1 \newline
0
\end{bmatrix}
+\sin{\phi}
\begin{bmatrix}
0 \newline
1
\end{bmatrix}
$$

と書き直す。スカラービームで言うところの水平、垂直偏光は

$$
\begin{aligned}
\vert V _ l &= \cos{l\phi}
\begin{bmatrix}
1 \newline
0
\end{bmatrix}
+\sin{l\phi}
\begin{bmatrix}
0 \newline
1
\end{bmatrix} \newline
\vert H _ l &= -\sin{l\phi}
\begin{bmatrix}
1 \newline
0
\end{bmatrix}
+\cos{l\phi}
\begin{bmatrix}
0 \newline
1
\end{bmatrix}
\newline
&=
-(\sin{l\phi}
\begin{bmatrix}
1 \newline
0
\end{bmatrix}
-\cos{l\phi}
\begin{bmatrix}
0 \newline
1
\end{bmatrix})
\end{aligned}
$$

と書けるのでラジアル偏光ビームは

$$
\vert \psi _ 1 = \vert V _ 1
$$

同様ににアジマス偏光ビームはと書ける。

$$
\vert \psi _ {1'} = \vert H _ 1
$$

**つまりアジマス偏光とラジアル偏光は高次元ポアンカレ球上で基底の組になっている。**

ラジアル偏光のストークスパラメーターは $\phi = 0$ より

$$
\boldsymbol{S} =
\begin{bmatrix}
1 \newline
0 \newline
1 \newline
0
\end{bmatrix}
$$

となり $(2\phi, 2\theta) = (0, 0)$ となる。

アジマル偏光のストークスパラメーターは $\phi = \pi$ より

$$
\boldsymbol{S} =
\begin{bmatrix}
1 \newline
0 \newline
-1 \newline
0
\end{bmatrix}
$$

となり $(2\phi, 2\theta) = (\pi, 0)$ となる。

$C = 0$

$C = 1$
