# ジョーンズベクトル

光というのは電場と磁場が

のように進んでいく。

振幅や波長はなじみ深いと思うがここでは光の**偏光**という特徴について見ていく。

電場だけに着目すると

のように水平に振動するものや

のように $\frac{\pi}{4}$ 傾いて振動するものなどがある。

この電場を $x$ 軸(水平方向), $y$ 軸(垂直方向)に分けて考える。

ベクトルで表すと

$$
\boldsymbol{E} = 
\begin{bmatrix}
E_{x0} e^{i\varphi_x} \newline
E_{y0} e^{i\varphi_y}
\end{bmatrix}
$$

となる。

これは1941年にアメリカの物理学者ジョーンズ(R. Clark Jones)によって考案されたもので**ジョーンズベクトル**と言う。

偏光状態を**複素ベクトル**によって表すことができる。

それぞれの振幅や位相の違いによって色々な偏光状態が表される。

**※全体にかかる振幅の大きさや位相は偏光の状態に影響しないことに注意**

これは

- 全体にかかる振幅とは、例えば水平方向に振動している電場の振動の幅が変わるだけで水平であるという形は変わらない。
- 全体にかかる位相とは、例えば水平方向に振動している電場をどの位置から観測するのか(右に一番振れているところから観測するのか、
- 原点から観測するのか)の違いであり物理的にはどちらも同じ電場を表している。

ということに対応している。

## 直線偏光

例えばそれぞれの成分の振幅と位相が共に等しいとき

つまり

$$
\varphi_y = \varphi_x
$$

$$
E_{y0} = E_{x0}
$$

のとき

$$
\boldsymbol{E} = E_{x0} e^{i \varphi_x}
\begin{bmatrix}
1 \\
1
\end{bmatrix}
$$

となり、これは反時計回りに $\frac{\pi}{4}$ だけ傾いた直線偏光を表している。


確かにベクトルの成分だけで見ると $\frac{\pi}{4}$ だけ傾いたベクトルだからそう思えるかもしれないが複素数が係数としてかかっているからなんか腑に落ちない

と思う。

そこで実部を取ってみると

$$
Re(\boldsymbol{E}) = E_{x0} \cos{\varphi_x}
\begin{bmatrix}
1 \\
1
\end{bmatrix}
$$

となりこのベクトルの先端の軌跡を考えると、晴れて実平面で $\frac{\pi}{4}$ だけ傾いた直線偏光が表された。

そもそも波を複素数で表現するのは実部だけ( $\cos$ だけ)で考えると計算が面倒になるという問題を解決するためだったので最終的には実部を取るというのは理にかなっている。
<br>

## 円偏光

次に振幅が等しく$x$ 成分が $y$ 成分より $\frac{\pi}{2}$ だけ進んでいる場合を考える。(例えば $x$ 成分が $\cos{\varphi_x}$ なら $y$ 成分は $\cos{(\varphi_x-\frac{\pi}{2})}=\sin{\varphi_x}$ のように波が $y$ 成分の方が $z$ 軸性の方向にずれている)

$$
\begin{aligned}
\varphi_y &= \varphi_x - \frac{\pi}{2} \newline
\varphi_y - \varphi_x &= -\frac{\pi}{2} \newline
\therefore \delta &= -\frac{\pi}{2}
\end{aligned}
$$

※位相差を $\delta$ とした。

を(1)に代入すると

$$
\begin{aligned}
\boldsymbol{E} &= E_{x0}
\begin{bmatrix}
e^{i \varphi_x} \newline
e^{i (\varphi_x - \frac{\pi}{2})}
\end{bmatrix} \newline
&= E_{x0} e^{i\varphi_x}
\begin{bmatrix}
1 \newline
e^{-i\pi}
\end{bmatrix} \newline
&= E_{x0} e^{i\varphi_x}
\begin{bmatrix}
1 \\
-i
\end{bmatrix} \newline
\end{aligned}
$$

これは**左回り円偏光**を表している。

なぜなら、これも実部をとると

$$
Re(\boldsymbol{E}) = \frac{1}{\sqrt{2}}
\begin{bmatrix}
\cos{\varphi_x} \newline
\sin{\varphi_x}
\end{bmatrix}
$$

となるがこれは $\varphi_x$ を変化させていくと $x-y$ 平面で左回りに回転するベクトル場になる。

【補足】
上ではこのジョーンズベクトルは左回り円偏光を表しているといったが、右回り円偏光を表していると書いてある教科書もあるこれは***座標系をどこから見るかによって起こる問題である。***

座標は右手系が基本なのでz軸が紙面裏面から紙面表面に向かうようにとると、水平方向はx軸に、垂直方向はy軸になる。つまり、 $z$ 軸正の方向から見るのか、負の方向から見るのかで回り方が逆転する。

***なんでx,yが反転するような立場から考えるの？***
と思うかもしれないがこれは工学系と理学系で光のとらえ方が異なるかららしい。

つまり**工学寄りの光学**の分野ではあくまで**主役は光であり**光を迎える視点で考えたいのだと思う。

逆に**理学寄りの光学**では**主役は光によって照らされるサンプル**であるので光を送り出す立場で現象を考える。

同様に $y$ 成分が $x$ 成分より $\frac{\pi}{2}$ だけ遅れている場合を考えると

$$
\boldsymbol{E} = E_{x0} e^{i\varphi_x}
\begin{bmatrix}
1 \newline
i
\end{bmatrix}
$$

これは右回り円偏光を表している。

なぜなら、これも実部をとると

$$
Re(\boldsymbol{E}) = E _ {x0}
\begin{bmatrix}
\cos{\varphi _ x} \newline
-\sin{\varphi _ x}
\end{bmatrix}
$$

となり、先ほどとは逆に左回り円偏光になる。

これは

のように電場が変化しているということで

$z$ 軸正の方向から見ると電場が

のように変化する。

まとめると

**電場の振動方向はジョーンズベクトルという複素ベクトルで表現することができ、偏光状態を変えるということはジョーンズベクトルを変えるということである。**

【補足】

ここで左右円偏光を表す2つのベクトルの内積をとってみると

$$
E_{x0}^2 e^{2i\varphi _ x}
\begin{aligned}
\begin{bmatrix}
1 & -i
\end{bmatrix}
^*
\begin{bmatrix}
1  \newline
i
\end{bmatrix}
\end{aligned}
= 0
$$

となり直交していることが分かる。

実は任意の偏光状態は左右円偏光の重ね合わせで表すことができる。

それだけでなく、基底の取り方は無数にある。

後の項でこれは詳しく説明する。

## 楕円偏光

直線をめちゃくちゃ楕円、円を全然楕円じゃない、とすると任意の偏光分布は楕円偏光として考えていい(直線、円偏光を楕円偏光の特殊形と考える。)

# ジョーンズ行列

偏光状態を変えるということはジョーンズベクトルを異なるジョーンズベクトルに変換することだと言った。

変換させる方法として**波長板**と呼ばれているものを使う。

$2$成分ベクトルを変換させるということはこの波長板という素子は $2 \times 2$ の行列とみなせそうだと思える。

実際に行列で表現でき、この行列を**ジョーンズ行列**という。

波長板は遅相子(retardar)と呼ばれ、2つの直交する電場の一方の位相を変化させる。

どちらの位相を遅らせるかで2通りの種類があるがここでは

$y$ 成分の位相が進むように($x$成分の位相が遅れるように)方向を選ぶ。(yを進相軸に選ぶ。)

それぞれの位相を独立に変化させるので行列の非対角成分は0になると予想できる。

確かに波長板は

$$
\begin{aligned}
J &=
\begin{bmatrix}
e^{i\varphi_x} & 0 \newline
0 & e^{i\varphi_y}
\end{bmatrix} \newline
&= e^{i\varphi_x}
\begin{bmatrix}
1 & 0 \newline
0 & e^{i(\varphi_y - \varphi_x)}
\end{bmatrix} \newline
&= e^{i\varphi_x}
\begin{bmatrix}
1 & 0 \newline
0 & e^{i\delta}
\end{bmatrix} \newline
\end{aligned}
$$

となる。(例によって位相差を $\delta$ とした。)

偏光素子では位相差をどのくらい与えるのだけが重要なのであると述べたのでこれを

$$
J =
\begin{bmatrix}
1 & 0 \newline
0 & e^{i\delta}
\end{bmatrix}
$$

とする。

ここでこの行列の転置をとって複素共役をとったものと元の行列を掛けてみると、これは単位行列になる。

つまり偏光素子を行列で表したものは**ユニタリー行列**であることが分かる。

また、偏光子は $x-y$ 平面でどのくらい傾けるかという自由度があり, $\theta$ だけ回転させるとジョーンズ行列は

$$
\begin{aligned}
J &=
\begin{bmatrix}
\cos{\theta} & -\sin{\theta} \newline
\sin{\theta} & \cos{\theta}
\end{bmatrix}
\begin{bmatrix}
1 & 0 \newline
0 & e^{i\delta}
\end{bmatrix}
\begin{bmatrix}
\cos{\theta} & \sin{\theta} \newline
-\sin{\theta} & \cos{\theta}
\end{bmatrix} \newline
&= 
\begin{bmatrix}
\cos{\theta} & -e^{i\delta} \sin{\theta} \newline
\sin{\theta} & e^{i\delta} \cos{\theta}
\end{bmatrix}
\begin{bmatrix}
\cos{\theta} & \sin{\theta} \newline
-\sin{\theta} & \cos{\theta}
\end{bmatrix} \newline
\therefore J &= 
\begin{bmatrix}
e^{i\delta} \sin^2{\theta} + \cos^2{\theta} & \sin{\theta} \cos{\theta} (1 - e^{i\delta}) \\
\sin{\theta} \cos{\theta} (1 - e^{i\delta}) & \sin^2{\theta} + e^{i\delta} \cos^2{\theta}
\end{bmatrix} \newline
\end{aligned}
$$

となる。

次の項では位相差をどのくらい与えるかを考える
## 1/2波長板

位相差を $\delta=\pi$ 与えるものを **1/2波長板(HWP:Half Wave Plate)** という。

前項で導出した式に代入してみると

$$
\begin{aligned}
J_{HWP(\theta)} &=
\begin{bmatrix}
-\sin^2{\theta} + \cos^2{\theta} & 2\sin{\theta} \cos{\theta} \newline
2\sin{\theta} \cos{\theta} & \sin^2{\theta} - \cos^2{\theta}
\end{bmatrix} \newline
&= 
\begin{bmatrix}
\cos{2\theta} & \sin{2\theta} \newline
\sin{2\theta} & -\cos{2\theta}
\end{bmatrix}
\end{aligned}
$$

を得る。

特に $\theta = 0$ のときは

$$
J_{HPW(\theta=0)} =
\begin{bmatrix}
1 & 0 \newline
0 & -1
\end{bmatrix}
$$

というジョーンズ行列を得る。

ここに $\frac{\pi}{4}$ だけ傾いた直線偏光

$$
\boldsymbol{E}_{in} = 
\begin{bmatrix}
1 \newline
1
\end{bmatrix}
$$

を入射させると

$$
\boldsymbol{E}_{out} = 
\begin{bmatrix}
1 \newline
-1
\end{bmatrix}
$$

となり, $-\frac{\pi}{4}$ だけ傾いた直線偏光を表していている。

元の状態から時計回りに $2 \times \frac{\pi}{4}$ だけ回転している。

となる。

また、 $\theta = \frac{\pi}{4}$ だけ回転させると

$$
J_{HWP(\theta=\frac{\pi}{4})} =
\begin{bmatrix}
0 & 1 \newline
1 & 0
\end{bmatrix}
$$

となり **x,y成分を交換する** という働きをする。

## 1/4波長板
位相差 $\delta=\frac{\pi}{2}$ であるので

$$
\begin{aligned}
J_{QWP(\theta)} &=
\begin{bmatrix}
e^{i \frac{\pi}{2}} \sin^2{\theta} + \cos^2{\theta} & \sin{\theta} \cos{\theta} (1 - e^{i \frac{\pi}{2}}) \newline
\sin{\theta} \cos{\theta} (1 - e^{i \frac{\pi}{2}}) & \sin^2{\theta} + e^{i \frac{\pi}{2}} \cos^2{\theta}
\end{bmatrix} \newline
&=
\begin{bmatrix}
i \sin^2{\theta} + \cos^2{\theta} & \sin{\theta} \cos{\theta} (1 - i) \\
\sin{\theta} \cos{\theta} (1 - i) & \sin^2{\theta} + i \cos^2{\theta}
\end{bmatrix} \newline
&=
\begin{bmatrix}
1 - i\cos{2\theta} & -i\sin{2\theta} \newline
-i\sin{2\theta} & 1 + i\cos{2\theta}
\end{bmatrix}
\end{aligned}
$$

を得る。

 $\theta = 0$ のときは

$$
J_{QWP(\theta=0)} =
\begin{bmatrix}
1 & 0 \newline
0 & i
\end{bmatrix}
$$

となる。

$\frac{\pi}{4}$ だけ傾いた直線偏光

$$
\boldsymbol{E}_{in} = 
\begin{bmatrix}
1 \newline
1
\end{bmatrix}
$$

を入射させると

$$
\boldsymbol{E}_{out} = 
\begin{bmatrix}
1 \newline
i
\end{bmatrix}
$$

となりこれは右回り円偏光を表している。

## 直線偏光子
波長板とは違ってもっとシンプルに考えることができて

$$
\begin{aligned}
J &=
\begin{bmatrix}
\cos{\theta} & -\sin{\theta} \newline
\sin{\theta} & \cos{\theta}
\end{bmatrix}
\begin{bmatrix}
1 & 0 \newline
0 & 0
\end{bmatrix}
\begin{bmatrix}
\cos{\theta} & \sin{\theta} \newline
-\sin{\theta} & \cos{\theta}
\end{bmatrix} \newline
&= 
\begin{bmatrix}
\cos{\theta} & 0 \newline
\sin{\theta} & 0
\end{bmatrix}
\begin{bmatrix}
\cos{\theta} & \sin{\theta} \newline
-\sin{\theta} & \cos{\theta}
\end{bmatrix} \newline
\therefore J &= 
\begin{bmatrix}
\cos^2{\theta} & \sin{\theta} \cos{\theta} \newline
\sin{\theta} \cos{\theta} & \sin^2{\theta}
\end{bmatrix} \newline
\end{aligned}
$$

となる。
$\frac{\pi}{4}$傾ければ

$$
J=
\begin{bmatrix}
1 & 1 \newline
1 & 1
\end{bmatrix}
$$

## SLM

$$
J _ {SLM} = A _ 0
\begin{bmatrix}
e^{i\delta} & 0 \newline
0 & 1
\end{bmatrix}
$$