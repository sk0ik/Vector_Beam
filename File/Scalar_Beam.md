- [スカラービーム](#スカラービーム)
- [楕円率](#楕円率)
- [射影演算子](#射影演算子)
- [スカラービームの表現](#スカラービームの表現)
- [パウリ行列展開](#パウリ行列展開)
- [ストークスパラメーター](#ストークスパラメーター)
- [ポアンカレ球](#ポアンカレ球)
- [1/2波長板](#12波長板)
- [1/4波長板](#14波長板)
  - [直線偏光子](#直線偏光子)
- [波長板,直線偏光子の使い道](#波長板直線偏光子の使い道)
  - [任意量のx偏光成分を取り出す](#任意量のx偏光成分を取り出す)
  - [円偏光成分を取り出す](#円偏光成分を取り出す)
- [パウリ行列と物理量](#パウリ行列と物理量)

## スカラービーム

ベクトルビームについて考える前に直線偏光,楕円偏光,円偏光などのスカラービームについて考えます.楕円偏光は直線偏光と円偏光の中間に位置するような偏光状態でその名の通り振動の軌跡が楕円になっています.以下ではこれらの分類,もしくは各偏光状態がどのようなパラメーターを持っているのかを考えます.

## 楕円率

上に挙げた3つの偏光状態はまとめて楕円偏光と呼ぶことができます.つまり直線偏光と円偏光を楕円偏光の特殊な形と考えるということです.

その偏光状態がどれだけ"楕円らしいか"を表す指標に **楕円率** というものがあります.これは単に数学でやるような幾何学的なものです.これについて説明します.

電場のx,y成分を

$$
\begin{aligned}
E _ {x} &= E _ {x0} \cos{(kz-\omega t)} \newline
E _ {y} &= E _ {y0} \cos{(kz-\omega t+\epsilon)}
\end{aligned}
$$

と表します.繰り返しますが偏光を考えるうえで重要なのは振幅 $E _ {x0},E _ {y0}$ の比と位相差 $\varepsilon$ のみです.よってこれらだけのパラメーターでこの偏光状態を表したいです.(zやtの変数を消したい.)まずy成分は

$$
\frac{E _ {y}}{E _ {y0}} = \cos{(kz-\omega t)}\cos{\varepsilon}-\sin{(kz-\omega t)}\sin{\varepsilon}
$$

のように書けます.ここにx成分を代入すると

$$
\frac{E _ {y}}{E _ {y0}} = \frac{E _ {x}}{E _ {x0}} \cos{\varepsilon}-\sin{(kz-\omega t)}\sin{\varepsilon}
$$

となります.またx成分をsinで表すと

$$
\begin{aligned}
E _ {x}&=E _ {x0} \sqrt{1-\sin^2{(kz-\omega t)}} \newline
\sin{(kz-\omega t)}&=\sqrt{1-\frac{E _ x}{E _ {x0}}^2}
\end{aligned}
$$

となるので結局

$$
\frac{E _ {y}}{E _ {y0}} = \frac{E _ {x}}{E _ {x0}} \cos{\varepsilon}-\sqrt{1-\frac{E _ x}{E _ {x0}}^2}\sin{\varepsilon}
$$

となりz,tを失くすことができました.移項して両辺を二乗すると

$$
\Bigl(\frac{E _ {y}}{E _ {y0}}-\frac{E _ {x}}{E _ {x0}} \cos{\varepsilon}\Bigr)^2=(1-\frac{E _ x}{E _ {x0}})\sin^2{\varepsilon}
$$

$$
\Bigl(\frac{E _ {x}}{E _ {x0}}\Bigr)^2+\Bigl(\frac{E _ {y}}{E _ {y0}}\Bigr)^2-2\frac{E _ {x}E _ y}{E _ {x0}E _ {y0}} \cos{\varepsilon}=\sin^2{\varepsilon}
$$

## 射影演算子

今までの説明では偏光を表すときにジョーンズベクトルの各成分の振幅比と位相差のみが重要と言ってきました.つまりジョーンズベクトルが

$$
\begin{bmatrix}
\alpha \newline
\beta
\end{bmatrix}
$$

と書けるとき,

$$
\vert \alpha \vert ^2 + \vert \beta \vert ^2 = 1
$$

としても任意の振幅比も表現できる。

ここで天下り的だが以下のようにジョーンズベクトルから行列を作る。

$$
P = \begin{bmatrix}
\alpha \newline
\beta 
\end{bmatrix}
\begin{bmatrix}
\alpha
\beta 
\end{bmatrix} ^*
$$

これは**射影演算子**と呼ばれる。

ただしどんな行列も射影演算子となるわけではなく以下の2つを満たす必要がある。(線形写像となる条件？)

$$
\begin{aligned}
-P^2 &= 1 \newline
P^ \dagger &= P
\end{aligned}
$$

計算してみると、確かに

$$
\begin{aligned}
P^2 &= (
\begin{bmatrix}
\alpha \newline
\beta 
\end{bmatrix} 
\begin{bmatrix}
\alpha
\beta 
\end{bmatrix} ^* ) (
\begin{bmatrix}
\alpha \newline
\beta 
\end{bmatrix}
\begin{bmatrix}
\alpha
\beta 
\end{bmatrix} ^* ) \newline
&= 
\begin{bmatrix}
\alpha \newline
\beta 
\end{bmatrix} (
\begin{bmatrix}
\alpha
\beta 
\end{bmatrix} ^*  
\begin{bmatrix}
\alpha \newline
\beta 
\end{bmatrix} )
\begin{bmatrix}
\alpha
\beta 
\end{bmatrix} ^* \newline
&= 
\begin{bmatrix}
\alpha \newline
\beta 
\end{bmatrix} (
| \alpha | ^2 + | \beta | ^2 )
\begin{bmatrix}
\alpha
\beta 
\end{bmatrix} ^* \newline
\therefore P^2 &= P
\end{aligned}
$$

次に

$$
\begin{aligned}
P ^{\dagger}
&=
(
\begin{bmatrix}
\alpha \newline
\beta 
\end{bmatrix}
\begin{bmatrix}
\alpha
\beta 
\end{bmatrix}
^* ) ^{\dagger} \newline
&=
(
\begin{bmatrix}
\alpha \newline
\beta 
\end{bmatrix}
\begin{bmatrix}
\alpha
\beta 
\end{bmatrix}
^* ) ^{\dagger} \newline
&=
(
\begin{bmatrix}
\alpha \newline
\beta 
\end{bmatrix}
^* )^*
\begin{bmatrix}
\alpha
\beta 
\end{bmatrix}
^* \newline
\therefore P^{\dagger} 
&=
P
\end{aligned}
$$

## スカラービームの表現

任意のスカラービームは２つの直交基底ベクトルの重ね合わせで表現できる

ジョーンズベクトルを

$$
\begin{bmatrix}
\alpha \newline
\beta 
\end{bmatrix}
(\alpha, \beta \in C)
$$

と表したときストークスパラメーターという実数値は

$$
\begin{bmatrix}
S _ 1 \newline
S _ 2 \newline
S _ 3
\end{bmatrix} =
\begin{bmatrix}
\vert \alpha \vert ^2 - \vert \beta \vert ^2 \newline
2 Re(\alpha \beta ^\ast) \newline
-2 Im(\alpha \beta ^\ast)
\end{bmatrix}
$$

例えばジョーンズベクトルが

$$
\frac{1}{\sqrt{2}}
\begin{bmatrix}
\alpha \newline
\beta
\end{bmatrix}
=\frac{1}{\sqrt{2}}(\alpha
\begin{bmatrix}
1 \newline
0
\end{bmatrix}
+\beta
\begin{bmatrix}
0 \newline
1
\end{bmatrix}
)
$$

のように垂直、水平偏光の重ね合わせでと書けるとする。

これを左右円偏光の重ね合わせで書くと

$$
\frac{1}{2\sqrt{2}} \Bigl ( (\alpha-i\beta)
\begin{bmatrix}
1 \newline
i
\end{bmatrix}
\Bigr ) +
\frac{1}{2\sqrt{2}} \Bigl ( (\alpha+i\beta)
\begin{bmatrix}
1 \newline
-i
\end{bmatrix}
\Bigr )
$$

逆に

$$
\alpha _ 2
\begin{bmatrix}
1 \newline
i
\end{bmatrix}
+
\beta _ 2
\begin{bmatrix}
1 \newline
-i
\end{bmatrix}
$$

と書けるとき

$$
(\alpha _ 2 + \beta _ 2)
\begin{bmatrix}
1 \newline
0
\end{bmatrix}
+i(\alpha _ 2 - \beta _ 2)
\begin{bmatrix}
0 \newline
1
\end{bmatrix}
$$

$$
\begin{aligned}
\vec{\psi}
&=
\alpha
\begin{bmatrix}
1 \newline
i
\end{bmatrix}
+\beta
\begin{bmatrix}
1 \newline
-i
\end{bmatrix} \newline
&=
(\alpha+\beta)
\begin{bmatrix}
1 \newline
0
\end{bmatrix}
+i(\alpha+\beta)
\begin{bmatrix}
0 \newline
1
\end{bmatrix} \newline
&=
\frac{1}{2}(1+i)(\alpha+\beta)
\begin{bmatrix}
1 \newline
1
\end{bmatrix}
+\frac{1}{2}(1-i)(\alpha+\beta)
\begin{bmatrix}
1 \newline
-1
\end{bmatrix}
\end{aligned}
$$

$$
\vec{\psi} = e^{-i\varphi}\cos{\Bigl (\theta+\frac{\pi}{4}\Bigr )}
\begin{bmatrix}
1 \newline
i
\end{bmatrix}
+
e^{i\varphi}\sin{\Bigl (\theta+\frac{\pi}{4}\Bigr )}
\begin{bmatrix}
1 \newline
-i
\end{bmatrix}
$$

## パウリ行列展開

パウリ行列は

$$
\sigma_0 =
\begin{bmatrix}
1 & 0 \newline
0 & 1
\end{bmatrix}, \quad
\sigma_1 =
\begin{bmatrix}
1 & 0 \newline
0 & -1
\end{bmatrix}, \quad
\sigma_2 =
\begin{bmatrix}
0 & 1 \newline
1 & 0
\end{bmatrix}, \quad
\sigma_3 =
\begin{bmatrix}
0 & -i \newline
i & 0
\end{bmatrix}
$$

で表される。

さきほどのジョーンズベクトルから作った行列をパウリ行列の和で表すことを考える。

ここでパウリ行列の性質として、例えば

$$
\begin{aligned}
\sigma _ 2 ^2 &=
\begin{bmatrix}
0 & 1 \newline
1 & 0
\end{bmatrix}
\begin{bmatrix}
0 & 1 \newline
1 & 0
\end{bmatrix} \newline
&= 
\begin{bmatrix}
1 & 0 \newline
0 & 1
\end{bmatrix}
\end{aligned}
$$

となり2乗すると単位行列であり、

異なる行列同士の積のTrを考えると、例えば

$$
\begin{aligned}
Tr( \sigma _ 3 \sigma _ 2 ) &= Tr \Bigl (
\begin{bmatrix}
0 & -i \newline
i & 0
\end{bmatrix}
\begin{bmatrix}
0 & 1 \newline
1 & 0
\end{bmatrix} \Bigr ) \newline
&= Tr \Bigl (
\begin{bmatrix}
-i & 0 \newline
0 & i
\end{bmatrix} \Bigr ) \newline
&= 
-i + i \newline
\therefore Tr( \sigma _ 3 \sigma _ 2 ) 
&=
0
\end{aligned}
$$

となり0となる。

これら2つの性質を使うと、以下のようにパウリ行列の和で表したとき、

$$
\begin{aligned}
P &= \frac{1}{2} (
h _ 0 \sigma _ 0 + h _ 1
\sigma _ 1 + h _ 2 \sigma _ 2 + h _ 3 \sigma _ 3 ) \newline
&= \frac {1} {2} \Bigl (
h_0 
\begin{bmatrix}
1 & 0 \newline
0 & 1
\end{bmatrix}
+h _ 1
\begin{bmatrix}
1 & 0 \newline
0 & -1
\end{bmatrix}
+h _ 2
\begin{bmatrix}
0 & 1 \newline
1 & 0
\end{bmatrix}
+h _ 3
\begin{bmatrix}
0 & -i \newline
i & 0 
\end{bmatrix} 
\Bigr )
\end{aligned}
$$

と仮定すると

先ほどの積の性質を使えば、例えば

$$
\begin{aligned}
\mathrm{Tr}(P \sigma _ 3) &= \frac{1}{2} \Bigl(h_0 \mathrm{Tr}(\sigma _ 0 \sigma _ 3) + h _ 1 \mathrm{Tr}(\sigma _ 1 \sigma _ 3) + h _ 2 \mathrm{Tr}(\sigma _ 2 \sigma _ 3) + h _ 3 \mathrm{Tr}(\sigma _ 3 \sigma _ 3) \Bigr) \newline
&=
h_3 \newline
&=
2 \mathrm{Tr} \Bigl(
\begin{bmatrix}
\mid \alpha \mid ^2 & \alpha \beta ^ \ast \newline
\alpha  \ast* \beta & \mid \beta \mid ^2
\end{bmatrix}
\begin{bmatrix}
0 & -i \newline
 i & 0
\end{bmatrix}
\Bigr) \newline
&=
\mathrm{Tr} \Bigl( 
\begin{bmatrix}
i \alpha \beta^* & -i \mid \alpha \mid ^2 \newline
i \mid \beta \mid ^2 & -i \alpha ^\ast \beta
\end{bmatrix}
\Bigr) \newline
&=
i (\alpha \beta ^ \ast - \alpha ^ \ast \beta) \newline
&=
-2 \mathrm{Im}(\alpha \beta ^ \ast) \newline
\therefore h_3
&=
-2 \mathrm{Im}(\alpha \beta ^ \ast)
\end{aligned}
$$


のように係数が求められる。

他も同じように計算すると結局

$$
\begin{aligned}
P
&=
\frac{1}{2} (
h _ 0 \sigma _ 0 + h _ 1 \sigma _ 1 + h _ 2 \sigma _ 2 + h _ 3 \sigma _ 3 ) \newline
&=
\frac{1}{2} \Bigl (
h_0 
\begin{bmatrix}
1 & 0 \newline
0 & 1
\end{bmatrix}
+h_1
\begin{bmatrix}
1 & 0 \newline
0 & -1
\end{bmatrix}
+h_2
\begin{bmatrix}
0 & 1 \newline
1 & 0
\end{bmatrix}
+h_3
\begin{bmatrix}
0 & -i \newline
i & 0 
\end{bmatrix}
\Bigr ) \newline
&=
\frac{1}{2} \Bigl (
\bigl (\mid \alpha \mid ^2 + \mid \beta \mid ^2 \bigr )
\begin{bmatrix}
1 & 0 \newline
0 & 1
\end{bmatrix}
+\bigl (\mid \alpha \mid ^2 - \mid \beta \mid ^2 \bigr )
\begin{bmatrix}
1 & 0 \newline
0 & -1
\end{bmatrix}
+2 Re( \alpha \beta ^ \ast)
\begin{bmatrix}
0 & 1 \newline
1 & 0
\end{bmatrix}
-2 Im( \alpha \beta ^ \ast)
\begin{bmatrix}
0 & -i \newline
i & 0 
\end{bmatrix}
\Bigr )
\end{aligned}
$$

今は $|\alpha| ^2 + |\beta| ^2 = 1$ を考えているので第一項目の係数は1になるため、以下では $h_1, h_2, h_3$ のみを考える。

この係数をベクトルとしたもの

$$
\begin{aligned}
\boldsymbol{ S }
&= 
\begin{bmatrix}
S _ 1 \newline
S _ 2 \newline
S _ 3
\end{bmatrix}
\newline
&=
\begin{bmatrix}
h _ 1 \newline
h _ 2 \newline
h _ 3
\end{bmatrix}
\newline
\therefore \boldsymbol{S}
&= 
\begin{bmatrix}
\mid \alpha \mid ^2 - \mid \beta \mid ^2 \newline
2 Re( \alpha \beta ^ \ast) \newline
-2 Im( \alpha \beta ^ \ast)
\end{bmatrix}
\end{aligned}
$$

となりストークスベクトルを導出できた。

## ストークスパラメーター

次にストークスパラメーターを計算します.

$$
\begin{aligned}
S' _ 1&=(Re(\alpha)\cos{\delta}-Im(\alpha)\sin{\delta})^2+(Re(\alpha)\sin{\delta}+Im(\alpha)\cos{\delta})^2+Re^2(\beta)+Im^2(\beta) \newline
&=Re^2(\alpha)\cos^2{\delta}-2Re(\alpha)Im(\alpha)\sin{\delta}\cos{\delta}+Im^2(\alpha)\sin^2{\delta}+Re^2(\alpha)\sin^2{\delta}+2Re(\alpha)Im(\alpha)\sin{\delta}\cos{\delta}+Im^2(\alpha)\cos^2{\delta}+\vert \beta \vert^2 \newline
&=Re^2(\alpha)+Im^2(\alpha)+\vert \beta \vert^2 \newline
\therefore S' _ 1&=\vert \alpha \vert^2+\vert \beta \vert^2=S _ 1
\end{aligned}
$$

$$
\begin{aligned}
\alpha' \beta'^\ast&=-\bigl(Re(\alpha)\cos{\delta}-Im(\alpha)\sin{\delta}+i(Re(\alpha)\sin{\delta}+Im(\alpha)\cos{\delta})\bigr)(Re(\beta)-iIm(\beta)) \newline
&=Re(\beta)Im(\alpha)\sin{\delta}-Re(\alpha)Re(\beta)\cos{\delta}-Re(\alpha)Im(\beta)\sin{\delta}-Im(\alpha)Im(\beta)\cos{\delta}+i(Re(\alpha)Im(\beta)\cos{\delta}-Re(\alpha)Re(\beta)\sin{\delta}-Im(\alpha)Im(\beta)\sin{\delta}-Re(\beta)Im(\alpha)\cos{\delta})
\end{aligned}
$$

となるが

$$
\alpha \beta^\ast=Re(\alpha)Re(\beta)+Im(\alpha)Im(\beta)+i(Re(\beta)Im(\alpha)-Re(\alpha)Im(\beta))
$$

であるので

$$
\alpha'\beta'^\ast=-Re(\alpha \beta^\ast)\cos{\delta}+Im(\alpha \beta^\ast)\sin{\delta}+i(-Re(\alpha \beta^\ast)\sin{\delta}-Im(\alpha \beta^\ast)\cos{\delta})
$$

となります.よって

$$
\begin{aligned}
S' _ 2&=2Re(\alpha' \beta'^\ast) \newline
&=-2Re(\alpha \beta^\ast)\cos{\delta}+2Im(\alpha \beta^\ast)\sin{\delta} \newline
\therefore S' _ 2 &= -S _ 2\cos{\delta}-S _ 3\sin{\delta}
\end{aligned}
$$

$$
\begin{aligned}
S' _ 3&=-2Im(\alpha' \beta'^\ast) \newline
&=-2Re(\alpha \beta^\ast)\sin{\delta}-2Im(\alpha \beta^\ast)\cos{\delta} \newline
\therefore S' _ 2 &= -S _ 2\sin{\delta}+S _ 3\cos{\delta}
\end{aligned}
$$

$$
\begin{aligned}
\vec{S'} &=
\begin{bmatrix}
S _ 1 \newline
-S _ 2\cos{\delta}-S _ 3\sin{\delta} \newline
-S _ 2\sin{\delta}+S _ 3\cos{\delta}
\end{bmatrix} \newline
\therefore \vec{S'}&=\begin{bmatrix}
1 & 0 & 0 \newline
0 & -\cos{\delta} & -\sin{\delta} \newline
0 & -\sin{\delta} & \cos{\delta}
\end{bmatrix}
\begin{bmatrix}
S _ 1 \newline
S _ 2 \newline
S _ 3
\end{bmatrix}
\end{aligned}
$$

## ポアンカレ球

実は計算すると分かるが先ほど導出したストークスパラメーターは

$$
S^2 _ 1 + S^2 _ 2 + S^2 _ 3 = 1
$$


の関係がある。

これはストークスベクトルが

 $S_1, S_2, S_3$ **を軸とした単位球面上の1点を指している。**

ということを表している。

また、これまで波長板について話してきたが、

**波長板によって光の偏光分布が変わるということはジョーンズベクトルが変わる、つまりストークスベクトルが変わる、つまりポアンカレ球面上で別の座標に移る。**

ということを意味している。

**波長板によってポアンカレ球上の座標がくるくると移動するということ。**

※このように長さを変えない(今は球の表面上で移動する)写像を等長写像という。

水平偏光が $(S_1, S_2, S_3) = (1, 0, 0)$

右回り円偏光が $(S_1, S_2, S_3) = (0, 0, 1)$

など。

## 1/2波長板

ポアンカレ球表面上で1/2波長板の影響によって点がどのように移るかを考えます.
例によってジョーンズベクトルが

$$
\begin{bmatrix}
\alpha \newline
\beta
\end{bmatrix}
$$

と書けるとき,このジョーンズベクトルに$\theta$回転させた1/2波長板を作用させると $\alpha=\alpha _ 1+i\alpha _ 2,\beta=\beta _ 1+i\beta _ 2$

$$
\begin{aligned}
\begin{bmatrix}
\alpha' \newline
\beta'
\end{bmatrix} &=
\begin{bmatrix}
\cos{2\theta} & \sin{2\theta} \newline
\sin{2\theta} & -\cos{2\theta}
\end{bmatrix}
\begin{bmatrix}
\alpha \newline
\beta
\end{bmatrix} \newline
&= \begin{bmatrix}
\alpha \cos{2\theta} + \beta \sin{2\theta} \newline
\alpha \sin{2\theta} - \beta \cos{2\theta}
\end{bmatrix} \newline
\therefore 
\begin{bmatrix}
\alpha' \newline
\beta'
\end{bmatrix}
&=\begin{bmatrix}
\alpha _ 1 \cos{2\theta}+\beta _ 1 \sin{2\theta}+i(\alpha _ 2 \cos{2\theta}+\beta _ 2 \sin{2\theta}) \newline
\alpha _ 1 \sin{2\theta}-\beta _ 1 \cos{2\theta}+i(\alpha _ 2 \sin{2\theta}-\beta _ 2 \cos{2\theta})
\end{bmatrix}
\end{aligned}
$$

と変化します.ここで

$$
\begin{aligned}
\vert \alpha' \vert ^2 &= \alpha _ 1^2\cos^2{2\theta}+2\alpha _ 1\beta _ 1\sin{2\theta}\cos{2\theta}+\beta _ 1^2\sin^2{2\theta}+\alpha^2 _ 2 \cos^2{2\theta}+2\alpha _ 2\beta _ 2\sin{2\theta}\cos{2\theta}+\beta^2 _ 2\sin^2{2\theta} \newline
&= \vert \alpha \vert ^2 \cos^2{2\theta} + \vert \beta \vert ^2 \sin^2{2\theta} + 2(\alpha _ 1\beta _ 1+\alpha _ 2\beta _ 2)\sin{2\theta}\cos{2\theta} \newline
\vert \beta' \vert ^2 &= \alpha _ 1^2\sin^2{2\theta}-2\alpha _ 1\beta _ 1\sin{2\theta}\cos{2\theta}+\beta _ 1^2\cos^2{2\theta}+\alpha^2 _ 2 \sin^2{2\theta}-2\alpha _ 2\beta _ 2\sin{2\theta}\cos{2\theta}+\beta^2 _ 2\cos^2{2\theta} \newline
&= \vert \alpha \vert ^2 \sin^2{2\theta} + \vert \beta \vert ^2 \cos^2{2\theta}-2(\alpha _ 1\beta _ 1+\alpha _ 2\beta _ 2)\sin{2\theta}\cos{2\theta}\newline
\alpha' \beta'^\ast &= \alpha^2 _ 1\sin{2\theta}\cos{2\theta}-\alpha _ 1\beta _ 1\cos^2{2\theta}+\alpha _ 1\beta _ 1\sin^2{2\theta}-\beta^2 _ 1\sin{2\theta}\cos{2\theta}+\alpha^2 _ 2\sin{2\theta}\cos{2\theta}-\alpha _ 2\beta _ 2\cos^2{2\theta}+\alpha _ 2\sin^2{2\theta}-\beta^2 _ 2\sin{2\theta}\cos{2\theta} \newline
&+i(-\alpha _ 1\alpha _ 2\sin{2\theta}\cos{2\theta}+\alpha _ 1\beta _ 2\cos^2{2\theta}-\alpha _ 2\beta _ 1\sin^2{2\theta}+\beta _ 1\beta _ 2\sin{2\theta}\cos{2\theta}+\alpha _ 1\alpha _ 2\sin{2\theta}\cos{2\theta}-\alpha _ 2\beta _ 1\cos^2{2\theta}+\alpha _ 1\beta _ 2\sin^2{2\theta}-\beta _ 1\beta _ 2\sin{2\theta}\cos{2\theta}) \newline
\end{aligned}
$$

となりますが

$$
\alpha \beta^\ast = \alpha _ 1\beta _ 1+\alpha _ 2\beta _ 2+i(\alpha _ 2\beta _ 1-\alpha _ 1\beta _ 2)
$$

であるのでこれを使うと

$$
\begin{aligned}
\vert \alpha' \vert ^2 &= \vert \alpha \vert ^2 \cos^2{2\theta} + \vert \beta \vert ^2 \sin^2{2\theta} + 2Re(\alpha \beta^\ast)\sin{2\theta}\cos{2\theta} \newline
\vert \beta' \vert ^2 &= \vert \alpha \vert ^2 \sin^2{2\theta} + \vert \beta \vert ^2 \cos^2{2\theta}-2Re(\alpha \beta^\ast)\sin{2\theta}\cos{2\theta} \newline
\alpha' \beta'^\ast &= \alpha^2 _ 1\sin{2\theta}\cos{2\theta}-\alpha _ 1\beta _ 1\cos^2{2\theta}+\alpha _ 1\beta _ 1\sin^2{2\theta}-\beta^2 _ 1\sin{2\theta}\cos{2\theta}+\alpha^2 _ 2\sin{2\theta}\cos{2\theta}-\alpha _ 2\beta _ 2\cos^2{2\theta}+\alpha _ 2\sin^2{2\theta}-\beta^2 _ 2\cos^2{2\theta} \newline
&+i(-\alpha _ 1\alpha _ 2\sin{2\theta}\cos{2\theta}+\alpha _ 1\beta _ 2\cos^2{2\theta}-\alpha _ 2\beta _ 1\sin^2{2\theta}+\beta _ 1\beta _ 2\sin{2\theta}\cos{2\theta}+\alpha _ 1\alpha _ 2\sin{2\theta}\cos{2\theta}-\alpha _ 2\beta _ 1\cos^2{2\theta}+\alpha _ 1\beta _ 2\sin^2{2\theta}-\beta _ 1\beta _ 2\sin{2\theta}\cos{2\theta})
\end{aligned}
$$

$$
\alpha' \beta'^\ast=(\vert \alpha \vert^2-\vert \beta \vert^2)\sin{2\theta}\cos{2\theta}-\alpha _ 1\beta _ 1\cos{4\theta}-\alpha _ 2\beta _ 2\cos{4\theta}+i(\alpha _ 1\beta _ 2-\alpha _ 2\beta _ 1)
$$

$$
\begin{aligned}
\vec{S'} &= 
\begin{bmatrix}
\vert \alpha' \vert ^2 - \vert \beta' \vert ^2 \newline
2 Re( \alpha' \beta'^ \ast) \newline
-2 Im( \alpha' \beta'^ \ast)
\end{bmatrix} \newline
&=
\begin{bmatrix}
(\vert \alpha' \vert ^2 - \vert \beta' \vert ^2)(\cos^2{2\theta}-\sin^2{2\theta})+4Re(\alpha \beta ^\ast) \sin{2\theta}\cos{2\theta} \newline
2(\alpha^2 _ 1+\alpha^2 _ 2)\sin{2\theta}\cos{2\theta}-2(\beta^2 _ 1+\beta^2 _ 2)\sin{2\theta}\cos{2\theta}-2\alpha _ 1\beta _ 1(\cos^2{2\theta}-\sin^2{2\theta})-2\alpha _ 2\beta _2(\cos^2{2\theta}-\sin^2{2\theta}) \newline
-2(\alpha _ 1\beta _ 2-\alpha _ 2\beta _ 1)
\end{bmatrix} \newline
&=
\begin{bmatrix}
S _ 1\cos{4\theta}+S _ 2 \sin{4\theta} \newline
S _ 1 \sin{4\theta}-S _ 2 \cos{4\theta} \newline
-S _ 3
\end{bmatrix} \newline
\therefore \vec{S'} &=
\begin{bmatrix}
\cos{4\theta} & \sin{4\theta} & 0 \newline
\sin{4\theta} & -\cos{4\theta} & 0 \newline
0 & 0 & -1
\end{bmatrix}
\begin{bmatrix}
S _ 1\newline
S _ 2\newline
S _ 3
\end{bmatrix}
\end{aligned}
$$

と計算できます. -->

光を $\theta$ 傾けた1/2波長板によって変調するとストークスパラメーターを上式のように変換することを意味しています.つまりポアンカレ球上の $S _ 1-S _ 2$ 平面で $2\theta$ だけ方位角が反時計回りに回転し $z$ 成分の符号が反転します.

例えば $x$ 偏光ビームを $\frac{\pi}{8}$ 傾けた1/2波長板に入射させると

$$
\begin{aligned}
\begin{bmatrix}
\alpha' \newline
\beta'
\end{bmatrix}
&=\frac{1}{\sqrt{2}}
\begin{bmatrix}
1 & 1\newline
1 & -1
\end{bmatrix}
\begin{bmatrix}
1 \newline
0
\end{bmatrix} \newline
\therefore 
\begin{bmatrix}
\alpha' \newline
\beta'
\end{bmatrix}
&=\frac{1}{\sqrt{2}}
\begin{bmatrix}
1 \newline
1
\end{bmatrix}
\end{aligned}
$$

と $\frac{\pi}{4}$ 傾いた直線偏光になります.

## 1/4波長板

同様に1/4波長板について考えます.

$$
\begin{aligned}
\begin{bmatrix}
\alpha' \newline
\beta'
\end{bmatrix} &=
\begin{bmatrix}
1 - i\cos{2\theta} & -i\sin{2\theta} \newline
-i\sin{2\theta} & 1 + i\cos{2\theta}
\end{bmatrix}
\begin{bmatrix}
\alpha \newline
\beta
\end{bmatrix} \newline
&=
\begin{bmatrix}
\alpha (1 - i\cos{2\theta}) - i\beta \sin{2\theta} \newline
-i\alpha \sin{2\theta} + \beta (1 + i\cos{2\theta})
\end{bmatrix} \newline
&=
\begin{bmatrix}
\alpha -i(\alpha \cos{2\theta} + \beta \sin{2\theta}) \newline
\beta - i(\alpha \sin{2\theta} - \beta \cos2\theta{})
\end{bmatrix} \newline
\therefore 
\begin{bmatrix}
\alpha' \newline
\beta'
\end{bmatrix}
&=\begin{bmatrix}
\alpha _ 1+\alpha _ 2\cos{2\theta}+\beta _ 2\sin{2\theta}+i(\alpha _ 2-\alpha _ 1\cos{2\theta}-\beta _ 1\sin{2\theta}) \newline
\beta _ 1+\alpha _ 2\sin{2\theta}-\beta _ 2\cos{2\theta}+i(\beta _ 2-\alpha _ 1\sin{2\theta}+\beta _ 1\cos{2\theta})
\end{bmatrix} \newline
\end{aligned}
$$

となります.よって

$$
\begin{aligned}
\vert \alpha'\vert^2
&=
\vert \alpha \vert^2+\vert \beta \vert^2 \sin^2{2\theta}+\vert \alpha \vert^2 \cos^2{2\theta}+2(\alpha _ 1\beta _ 1+\alpha _ 2\beta _ 2)\sin{2\theta}\cos{2\theta}+2(\alpha _ 1\beta _ 2-\alpha _ 2\beta _ 1)\sin{2\theta} \newline
\vert \beta'\vert ^2
&= \vert \beta \vert^2+\vert \alpha \vert^2 \sin^2{2\theta}+\vert \beta \vert^2 \cos^2{2\theta} -2(\alpha _ 1\beta _ 2-\alpha _ 2\beta _ 1)\sin{2\theta}-2(\alpha _ 1\beta _ 1+\alpha _ 2\beta _ 2)\sin{2\theta}\cos{2\theta}\newline
\alpha'\beta'^\ast
&=
\alpha _ 1 \beta _ 1+\alpha _ 2\beta _ 2+(\vert \alpha \vert^2-\vert \beta \vert^2)\sin{2\theta}\cos{2\theta}-2(\alpha _ 1\beta _ 2-\alpha _ 2\beta _ 1)\cos{2\theta}-(\alpha _ 1\beta _ 1+\alpha _ 2\beta _ 2)\cos{4\theta} \newline
&+i((\vert \alpha \vert^2-\vert \beta \vert^2)\sin{2\theta}-2(\alpha _ 1\beta _ 1+\alpha _ 2\beta _ 2)\cos{2\theta})
\end{aligned}
$$

となります.

$$
\begin{aligned}
\vec{S'} &= 
\begin{bmatrix}
\vert \alpha' \vert ^2 - \vert \beta' \vert ^2 \newline
2 Re( \alpha' \beta'^ \ast) \newline
-2 Im( \alpha' \beta'^ \ast)
\end{bmatrix} \newline
&=
\begin{bmatrix}
(1+\cos{4\theta})(\vert \alpha \vert ^2 - \vert \beta \vert ^2)-4(\alpha _ 2\beta _ 1-\alpha _ 1\beta _ 2)\sin{2\theta}+4(\alpha _ 1\beta _ 1+\alpha _ 2\beta _ 2)\sin{2\theta}\cos{2\theta}\newline
2(\alpha _ 1 \beta _ 1+\alpha _ 2\beta _ 2+(\vert \alpha \vert^2-\vert \beta \vert^2)\sin{2\theta}\cos{2\theta}-2(\alpha _ 1\beta _ 2-\alpha _ 2\beta _ 1)\cos{2\theta}-(\alpha _ 1\beta _ 1+\alpha _ 2\beta _ 2)\cos{4\theta}) \newline
-2((\vert \alpha \vert^2-\vert \beta \vert^2)\sin{2\theta}-2(\alpha _ 1\beta _ 1+\alpha _ 2\beta _ 2)\cos{2\theta})
\end{bmatrix} \newline
&=
\begin{bmatrix}
(1+\cos{4\theta})S _ 1+2S _ 2\sin{2\theta}\cos{2\theta}+2S _ 3\sin{2\theta} \newline
S _ 1\sin{4\theta}+S _ 2(1-\cos{4\theta})-2S _ 3\cos{2\theta} \newline
-2S _ 1\sin{2\theta}+2S _ 2\cos{2\theta}
\end{bmatrix} \newline
\therefore \vec{S'} &=
\begin{bmatrix}
1+\cos{4\theta} & \sin{4\theta} & 2\sin{2\theta} \newline
\sin{4\theta} & 1-\cos{4\theta} & -2\cos{2\theta} \newline
-2\sin{2\theta} & 2\cos{2\theta} & 0
\end{bmatrix}
\begin{bmatrix}
S _ 1 \newline
S _ 2 \newline
S _ 3
\end{bmatrix}
=2\begin{bmatrix}
\cos^2{2\theta} & \sin{2\theta}\cos{2\theta} & \sin{2\theta} \newline
\sin{2\theta}\cos{2\theta} & \sin^2{2\theta} & -\cos{2\theta} \newline
-\sin{2\theta} & \cos{2\theta} & 0
\end{bmatrix}
\begin{bmatrix}
S _ 1 \newline
S _ 2 \newline
S _ 3
\end{bmatrix}
\end{aligned}
$$

と計算できます.先ほどの1/2波長板と違って自分はどのようなパターンで変化させているか(自分は)イメージがつかめません.

### 直線偏光子

同様に考えます.

$$
\begin{aligned}
\begin{bmatrix}
\alpha' \newline
\beta'
\end{bmatrix}
&=
\begin{bmatrix}
\cos^2{\theta} & \sin{\theta}\cos{\theta} \newline
\sin{\theta} & \sin^2{\theta}
\end{bmatrix}
\begin{bmatrix}
\alpha \newline
\beta
\end{bmatrix} \newline
&=
\begin{bmatrix}
\alpha \cos^2{\theta}+\beta \sin{\theta} \cos{\theta} \newline
\alpha \sin{\theta} \cos{\theta} & \beta \sin^2{\theta}
\end{bmatrix} \newline
\therefore
\begin{bmatrix}
\alpha' \newline
\beta'
\end{bmatrix}
&=
\begin{bmatrix}
\alpha _ 1 \cos^2{\theta}+\beta _ 1 \sin{\theta} \cos{\theta}+i(\alpha _ 2 \cos^2{\theta}+\beta _ 2\sin{\theta} \cos{\theta}) \newline
\alpha _ 1 \sin{\theta} \cos{\theta}+\beta _ 1 \sin^2{\theta}+i(\alpha _ 2 \sin{\theta} \cos{\theta}+\beta _ 2\sin^2{\theta})
\end{bmatrix}
\end{aligned}
$$

であるので

$$
\begin{aligned}
\vert \alpha' \vert^2
&=
\alpha^2 _ 1\cos^4{\theta}+2\alpha _ 1 \beta _ 1\sin{\theta} \cos^3{\theta}+\beta^2 _ 1\sin^2{\theta} \cos^2{\theta}+\alpha _ 2 \cos^4{\theta}+2\alpha^2 _ 2 \beta _ 2 \sin{\theta} \cos^3{\theta}+\beta^2 _ 2\sin^2{\theta} \cos^2{\theta} \newline
\therefore
\vert \alpha' \vert^2
&=
\vert \alpha \vert^2 \cos^4{\theta}+\vert \beta \vert^2 \sin^2{\theta} \cos^2{\theta}+2(\alpha _ 1 \beta _ 1+\alpha _ 2\beta _ 2)\sin{\theta}\cos^3{\theta}
\end{aligned}
$$

$$
\begin{aligned}
\vert \beta' \vert^2
&=
\alpha^2 _ 1\sin^2{\theta} \cos^2{\theta}+2\alpha _ 1 \beta _ 1\sin^3{\theta} \cos{\theta}+\beta^2 _ 1\sin^4{\theta}+\alpha^2 _ 2 \sin^2{\theta} \cos^2{\theta}+2\alpha _ 2 \beta _ 2 \sin^3{\theta} \cos{\theta}+\beta^2 _ 2\sin^4{\theta} \newline
\therefore
\vert \beta' \vert^2
&=
\vert \alpha \vert^2 \sin^2{\theta} \cos^2{\theta}+\vert \beta \vert^2 \sin^4{\theta}+2(\alpha _ 1 \beta _ 1+\alpha _ 2\beta _ 2)\sin^3{\theta}\cos{\theta}
\end{aligned}
$$

$$
\begin{aligned}
\alpha \beta^\ast
&=
\alpha _ 1 \cos^2{\theta}+\beta _ 1 \sin{\theta} \cos{\theta}+i(\alpha _ 2 \cos^2{\theta}+\beta _ 2\sin{\theta} \cos{\theta}) \times \bigl(\alpha _ 1 \sin{\theta} \cos{\theta}+\beta _ 1 \sin^2{\theta}-i(\alpha _ 2 \sin{\theta} \cos{\theta}+\beta _ 2\sin^2{\theta})\bigr)
\end{aligned}
$$

<!-- 
$$
\begin{aligned}
S _ 0 &=
\begin{bmatrix}

\end{bmatrix}
\end{aligned}
$$ -->

## 波長板,直線偏光子の使い道

### 任意量のx偏光成分を取り出す

一般的なレーザーは $x,y$ 偏光が組み合わさってできています.そこでこのレーザーの $x$ 偏光成分を任意の量取り出すことを考えます.具体的には下図のような光学系を組みます.

~PBS+HWP~

まずHWPでレーザーのジョーンズベクトルを回転させます.言い換えると $x,y$ 偏光の比率を変えるということです.次にPBS(Polarization Beam  Spliter) で $x$ 偏光のみを取り出します.HWPを回すことで得られる $x$ 偏光ビームの光強度が変わります.もちろん同じ要領で $y$ 偏光も任意の光強度を取り出すことができます.

### 円偏光成分を取り出す

<!-- ## n波長板

$\frac{\delta}{2\pi}$ 波長板のジョーンズ行列は

$$
J = 
\begin{bmatrix}
e^{i\delta}\sin^2{\theta}+\cos^2{\theta} & \sin{\theta}\cos{\theta}(1-e^{i\delta}) \newline
\sin{\theta}\cos{\theta}(1-e^{i\delta}) & \sin^2{\theta}+e^{i\delta}\cos^2{\theta}
\end{bmatrix}
$$

となります.この行列によってジョーンズベクトルが

$$
\begin{bmatrix}
\alpha \newline
\beta
\end{bmatrix}
\stackrel{J}{\rightarrow}
\begin{bmatrix}
\alpha' \newline
\beta'
\end{bmatrix}
$$

のように変化したときポアンカレ球上で点がどのように移動するかを考えます.ストークスベクトルも

$$
\begin{bmatrix}
S _ 1 \newline
S _ 2 \newline
S _ 3
\end{bmatrix}
\stackrel{J}{\rightarrow}
\begin{bmatrix}
S' _ 1 \newline
S' _ 2 \newline
S' _ 3
\end{bmatrix}
$$

のように変化します.

$$
\begin{bmatrix}
\alpha' \newline
\beta'
\end{bmatrix} =
\begin{bmatrix}
\alpha(e^{i\delta}\sin^2{\theta}+\cos^2{\theta})+\beta(\sin{\theta}\cos{\theta}(1-e^{i\delta})) \newline
\alpha\sin{\theta}\cos{\theta}(1-e^{i\delta})+\beta(\sin^2{\theta}+e^{i\delta}\cos^2{\theta})
\end{bmatrix} 
$$

ここで

$$
\alpha = \alpha _ 1+i\alpha _ 2 \newline
\beta = \beta _ 1+i\beta _ 2
$$

として実部と虚部に分けると

$$
\alpha' = \bigl[\alpha _ 1(\cos{\delta}\sin^2{\theta}+\cos^2{\theta})-\alpha _ 2\sin{\delta}\sin^2{\theta}+\sin{\theta}\cos{\theta}(\beta _ 1+\beta _ 2\sin{\delta})\bigr] \newline
+i\bigl[\alpha _ 2(\cos{\delta}\sin^2{\theta}+\cos^2{\theta}+\alpha _ 1\sin{\delta}\sin^2{\theta}+\sin{\theta}\cos{\theta}(\beta _ 2-\beta _ 1\cos{\delta}))\bigr]
$$

$$
\beta' = \bigl[\sin{\theta}\cos{\theta}(\alpha _ 1+\alpha _ 2\sin{\delta})+\beta _ 1(\sin^2{\theta}+\cos{\delta}\cos^2{\theta})-\beta _ 2\sin{\delta}\cos^2{\theta}\bigr] \newline
+i\bigl[\sin{\theta}\cos{\theta}(\alpha _ 2-\alpha _ 1\cos{\delta})+\beta _ 2(\sin^2{\theta}+\cos{\delta}\cos^2{\theta})+\beta _ 1\sin{\delta}\cos^2{\theta}\bigr]
$$

となります. -->

<!-- ## SLM

SLMのジョーンズ行列は

$$
J=
\begin{bmatrix}
-e^{i\delta(x, y)} & 0 \newline
0 & 1
\end{bmatrix}
$$

となります. $(1,1)$ 成分にマイナスがついているのは反射したことで水平方向の軸が反転するためです.ジョーンズベクトルは

$$
\begin{bmatrix}
\alpha' \newline
\beta'
\end{bmatrix}=
\begin{bmatrix}
-\alpha e^{i\delta} \newline
\beta
\end{bmatrix}
$$

となります.まず

$$
\begin{aligned}
S' _1 &= \vert -\alpha e^{i\delta} \vert^2-\vert \beta \vert^2 \newline
\therefore S' _ 1 &= \vert \alpha \vert^2-\vert \beta \vert^2 = S _ 1
\end{aligned}
$$

です.次に

$$
\begin{aligned}
S' _ 2 &= 2Re(-\alpha \beta^\ast e^{i\delta}) \newline
&= -2(\alpha _ 1\beta _ 1\cos{\delta}-\alpha _ 2\beta _ 1\sin{\delta}+\alpha _ 1\beta _ 2\sin{\delta}+\alpha _ 2\beta _ 2\cos{\delta}) \newline
\therefore S' _ 2 &= -2\bigl[(\alpha _ 1\beta _ 1+\alpha _ 2\beta _ 2)\cos{\delta}+(\alpha _ 1\beta _ 2-\alpha _ 2\beta _ 1)\sin{\delta}\bigr]
\end{aligned}
$$

最後に

$$
\begin{aligned}
S' _ 3 &= -2Im(-\alpha \beta^\ast e^{i\delta}) \newline
&= 2(\alpha _ 1\beta _ 1\sin{\delta}-\alpha _ 1\beta _ 2\cos{\delta}+\alpha _ 2\beta _ 1\cos{\delta}+\alpha _ 2\beta _ 2\sin{\delta}) \newline
\therefore S' _ 3 &= 2\bigl[(\alpha _ 2\beta _ 1-\alpha _ 1\beta _ 2)\cos{\delta}+(\alpha _ 1\beta _ 1+\alpha _ 2\beta _ 2)\sin{\delta}\bigr]
\end{aligned}
$$

となります.ここで

$$
\alpha \beta^\ast = \alpha _ 1\beta _ 1+\alpha _ 2\beta _ 2+i(\alpha _ 2\beta _ 1-\alpha _ 1\beta _ 2)
$$

より

$$
\begin{aligned}
Re(\alpha \beta^\ast)&=\alpha _ 1\beta _ 1+\alpha _ 2\beta _ 2 \newline
Im(\alpha \beta^\ast)&=\alpha _ 2\beta _ 1-\alpha _ 1\beta _ 2
\end{aligned}
$$

であるので

$$
\begin{aligned}
S' _ 2 &= -2Re(\alpha \beta^\ast)\cos{\delta}+2Im(\alpha \beta^\ast)\sin{\delta} = -S _ 2\cos{\delta}-S _ 3\sin{\delta} \newline
S' _ 3 &= 2Re(\alpha \beta^\ast)\sin{\delta}+2Im(\alpha \beta^\ast)\cos{\delta} = S _ 2\sin{\delta}-S _ 3\cos{\delta}
\end{aligned}
$$

となります.よってまとめると

$$
\begin{aligned}
\vec{S'} &=
\begin{bmatrix}
\vert \alpha \vert^2-\vert \beta \vert^2 \newline
-2Re(\alpha \beta^\ast)\cos{\delta}+2Im(\alpha \beta^\ast)\sin{\delta} \newline
2Re(\alpha \beta^\ast)\sin{\delta}+2Im(\alpha \beta^\ast)\cos{\delta}
\end{bmatrix} \newline
&= \begin{bmatrix}
S _ 1 \newline
-S _ 2\cos{\delta}+S _ 3\sin{\delta} \newline
S _ 2\sin{\delta}-S _ 3\cos{\delta}
\end{bmatrix}
\newline
\therefore \vec{S'}&= \begin{bmatrix}
1 & 0 & 0 \newline
0 & -\cos{\delta} & -\sin{\delta} \newline
0 & \sin{\delta} & -\cos{\delta}
\end{bmatrix}
\begin{bmatrix}
S _ 1 \newline
S _ 2 \newline
S _ 3
\end{bmatrix}
\end{aligned}
$$ -->

<!-- が得られます.つまりSLMは $S _ 2-S _ 3$ 平面で時計回りに $\delta$ 回転させる働きをすることが分かります.

## パウリ行列と物理量

パウリ行列はそれぞれどの軸のスピンをもっているかをあらわす物理量を観測できる。

例えば

$$
\begin{aligned}
S_1 &=
\begin{bmatrix}
\alpha ^* \: \beta ^*
\end{bmatrix}
\begin{bmatrix}
1 & 0 \\
0 & -1
\end{bmatrix}
\begin{bmatrix}
\alpha \\
\beta
\end{bmatrix} \\ 
&=
\begin{bmatrix}
\alpha ^* \: \beta
\end{bmatrix}
\begin{bmatrix}
\alpha \\
-\beta
\end{bmatrix} \\
\therefore S_1
&=  
| \alpha | ^2 - | \beta | ^2
\end{aligned}
$$

$$
\begin{aligned}
S_2 &=
\begin{bmatrix}
\alpha ^* \: \beta ^*
\end{bmatrix}
\begin{bmatrix}
0 & 1 \\
1 & 0
\end{bmatrix}
\begin{bmatrix}
\alpha \\
\beta
\end{bmatrix} \\ 
&=
\begin{bmatrix}
\alpha ^* \: \beta
\end{bmatrix}
\begin{bmatrix}
\beta \\
\alpha
\end{bmatrix} \\
&= \alpha ^* \beta + \alpha \beta ^* \\
\therefore S_2
&=  
2Re(\alpha \beta ^*)
\end{aligned}
$$

$$
\begin{aligned}
S_3 &=
\begin{bmatrix}
\alpha ^* \: \beta ^*
\end{bmatrix}
\begin{bmatrix}
0 & -i \\
i & 0
\end{bmatrix}
\begin{bmatrix}
\alpha \\
\beta
\end{bmatrix} \\ 
&=
\begin{bmatrix}
\alpha ^* \: \beta
\end{bmatrix}
\begin{bmatrix}
-i \beta \\
i \alpha
\end{bmatrix} \\
&= 
-i \alpha ^* \beta + i \alpha \beta ^* \\
&=
i (\alpha \beta ^* - \alpha ^* \beta) \\
\therefore S_3 &= -2Im(\alpha \beta ^*)
\end{aligned}
$$

右回り円偏光のストークスパラメーターを計算してみる。
規格化されたジョーンズベクトルは

$$
\frac{1}{\sqrt{2}}
\begin{bmatrix}
1 \\
i
\end{bmatrix}
$$

であったので

$\alpha = \frac{1}{\sqrt{2}}, \beta = \frac{i}{\sqrt{2}}$

を代入すると

$$
\begin{aligned}
S_1 &=
\Bigl |\frac {1}{\sqrt{2}} \Bigr | ^2 - \Bigl |\frac {i}{\sqrt{2}} \Bigr | ^2 \\
&=
\frac {1}{2} - \frac {1}{2} \\
&=
0 
\end{aligned}
$$

$$
\begin{aligned}
S_2 &= 2Re\Bigl (\frac {1}{\sqrt{2}} \times \frac {i^*}{\sqrt{2}} \Bigr ) \\
&=
2Re(-i) \\
&=
0
\end{aligned}
$$

$$
\begin{aligned}
S_3
&=
-2Im\Bigl (\frac {1}{\sqrt{2}} \times \frac {i ^*}{\sqrt{2}}\Bigr ) \\ 
&=
-2Im \Bigl (- \frac {i}{2} \Bigr ) \\ 
&=
1
\end{aligned}
$$

よって

$$
S = 
(S_1, S_2, S_3) = (0, 0, 1)
$$

となる。

実は偏光と電子のスピンは密接な関係があり、電子のポアンカレ球に相当するものをブロッホ球という。

具体的には

のように対応している。

実際に論文として出されていて

これは半導体に右回り円偏光を当てた時、上向きのスピン(赤いやつ)が励起されている様子を表している。