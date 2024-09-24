#### 研究背景
非近軸近似のもとでの光の伝播を考えることは重要.
#### 研究目的
NAが上がるにつれてスカラー回折ではなくベクトル回折で光の伝播を考える必要がある.
解決法としてリチャードウルフ回折が有用だがこれは近軸近似のもとで考えている.
この論文では非近軸近似のもとでリチャードウルフ回折のような方法を発案している.
#### 原理

### "PyFocus – A Python package for vectorial calculations of focused optical fields under realistic conditions. Application to toroidal foci"
#### 原理
位置にのみ依存する電場ベクトルは

$$
\vec{E} _ f = -\frac{kfe^{-ikf}}{2\pi} \int_{0}^{2\pi} \int_{0}^{\alpha} \vec{E} _ 0 e^{i\vec{k} \cdot \vec{r}} \sqrt{\cos{\theta}} \sin{\theta} d\theta d\phi
$$

のように書ける.以下に図を示す.

<div align="center">
<img src="pic\PyFocus – A Python package for vectorial calculations of focused optical fields under realistic conditions. Application to toroidal foci\cordinate.png" alt="alt text" width="700">
</div>

位置ベクトル$\vec{r}$を

$$
\vec{r} = (\rho \cos{\phi}, \rho \sin{\phi}, z)
$$

のような3個のパラメーターで表す.上図の波数ベクトル$\vec{k}$は

$$
\vec{k} = (\rho ' \cos{\phi '}, \rho ' \sin{\phi '}, k\cos{\theta}) = (k\sin{\theta}\cos{\phi '}, k\sin{\theta}\sin{\phi '}, k\cos{\theta})
$$

と書ける.これらの内積をとってみると

$$
\begin{aligned}
\vec{k} \cdot \vec{r}
&=
k \rho \sin{\theta} \cos{\phi '} \cos{\phi} + k \rho \sin{\theta} \sin{\phi '} \sin{\phi} + kz\cos{\theta} \newline
\therefore \vec{k} \cdot \vec{r} &=
k\bigl(z\cos{\theta} + \rho\sin{\theta} \cos{(\phi ' - \phi)}\bigr)
\end{aligned}
$$

となる.

収差のないレンズでは

$$
\rho ' = f\sin{\theta}
$$

で与えられる.

先ほどの

$$
\vec{E} _ f = -\frac{kfe^{-ikf}}{2\pi} \int_{0}^{2\pi} \int_{0}^{\alpha} \vec{E} _ 0 e^{i\vec{k} \cdot \vec{r}} \sqrt{\cos{\theta}} \sin{\theta} d\theta d\phi
$$

の$\vec{E} _ 0$について考える.

レンズに入射するビームを$\vec{E} _ i$としたときレンズと焦点位置の間の電場は

$$
\begin{aligned}
E _ {i _ s} &= \vec{E} _ i \cdot \hat{\phi '} \newline
E _ {i _ p} &= \vec{E} _ i \cdot \hat{\rho '} 
\end{aligned}
$$

と$s,p$偏光に分解したとき

$$
\vec{E} _ 0 = E _ {i _ s} \hat{\phi '} + E _ {i _ p} \hat{\theta '}
$$

のような重ね合わせで書ける.$s$偏光はレンズに入射する前と後で方向を変えないが$p$偏光は$\hat{\theta} '$の方向を向く.

2次元極座標から2次元デカルト座標へは

$$
\begin{aligned}
\vec{\rho '} &= \cos{\phi '} \hat{x} + \sin{\phi '} \hat{y} \newline
\vec{\phi '} &= -\sin{\phi '} \hat{x} + \cos{\phi '} \hat{y}
\end{aligned} 
$$

と変換でき

$$
\hat{\theta} = \cos{\theta} \cos{\phi '} \hat{x} + \cos{\theta} \sin{\phi '} \hat{y} -\sin{\theta} \hat{z}
$$

って書いてあるけど

$$
\hat{\theta} = \cos{\theta} \cos{\phi '} \hat{x} + \cos{\theta} \sin{\phi '} \hat{y} +\sin{\theta} \hat{z}
$$

じゃね？

楕円偏光を

$$
\vec{E} _ i = E _ i(c _ x \hat{x} + c _ y \hat{y}) \newline
(c _ x ^2 + c _ y ^2 = 1, c _ x, c _ y \in \cnums)
$$

のように$x,y$偏光の重ね合わせで表す.このビームがレンズによって変換され最終的に

$$
\vec{E} _ f = c _ x \vec{E}^{(x)} _ f + c _ y\vec{E}^{(y)} _ f
$$
