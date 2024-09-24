得られるビームのジョーンズベクトルは以下

$$
\boldsymbol{E} = 
e^{iA\varphi}[
\cos{2\alpha}
e^{-i(B\varphi+C)}
\boldsymbol{S_1}(2\gamma, 2(2\beta-\gamma))
+\sin{2\alpha}
e^{i(B\varphi+C)}
\boldsymbol{S_2}(2\gamma+\pi, -2(2\beta-\gamma))]
$$

ただし2つのベクトル$\boldsymbol{S}$は

$$\boldsymbol{S}(2\psi, 2\chi) = 
\begin{bmatrix}
\frac{1}{\sqrt{2}}[\sin{(\chi + \frac{\pi}{4})} e^{-i\psi} + \cos{(\chi + \frac{\pi}{4}) e^{i\psi}}] \newline
\frac{i}{\sqrt{2}}[\sin{(\chi + \frac{\pi}{4})} e^{-i\psi} - \cos{(\chi + \frac{\pi}{4}) e^{i\psi}}]
\end{bmatrix}
$$

SLMに表示させるホログラムは
- SLM1: $\delta_1 = p\varphi + \delta_{10}$
- SLM2: $\delta_2 = q\varphi + \delta_{20}$

パラメーターは
- $\alpha$ :1つ目の半波長板を傾ける角度
- $\beta$ :2つ目の半波長板を傾ける角度
- $\gamma$ :4分の1波長板を傾ける角度
- $\boldsymbol{S_i}(i \in 1, 2)$ は互いに直交するベクトル、**波長板を傾けるということは直交基底を選ぶことに対応する。**
- $A = p + \frac{q}{2}$
- $B = -\frac{q}{2}$
- $C = -\frac{2\delta_{20} + \pi}{4}$

ここで $\alpha = \frac{\pi}{8}, \beta = 0, \gamma = -\frac{\pi}{4}$ とすると

$$
\boldsymbol{S_1}(-\frac{\pi}{2}, \frac{\pi}{2}) \propto 
\begin{bmatrix}
1 \newline
-i
\end{bmatrix}(右回り円偏光)
$$

$$
\boldsymbol{S_2}(\frac{\pi}{2}, -\frac{\pi}{2}) \propto 
\begin{bmatrix}
1 \newline
i
\end{bmatrix}(左回り円偏光)
$$

となる。
さらに $p = 1, q = 2, \delta_{20} = -\frac{\pi}{2}$
とすると
$A = 2, B = -1, C = 0$
となるので代入すると

$$
\boldsymbol{E} = 
\sqrt{2} e^{i2\varphi}
\begin{bmatrix}
\cos{\varphi} \newline
\sin{\varphi}
\end{bmatrix}
$$

$$
Re(\boldsymbol{E}) = \sqrt{2} \cos{2\varphi}
\begin{bmatrix}
\cos{\varphi} \newline
\sin{\varphi}
\end{bmatrix}
\propto
\begin{bmatrix}
\cos{\varphi} \newline
\sin{\varphi}
\end{bmatrix}
$$

この偏光分布が時々刻々と変化していくつまりこれに位相項 $e^{iX}$ をかけて実部を取ったものの形が偏光分布

たしかに種々の $\varphi$ に値を代入してみると

$$
\begin{aligned}
Re(\boldsymbol{E_{\varphi=0}}) &= 
\begin{bmatrix}
1 \newline
0
\end{bmatrix} (水平偏光) \newline
Re(\boldsymbol{E_{\varphi=\frac{\pi}{4}}})
&\propto 
\begin{bmatrix}
1 \newline
1 
\end{bmatrix} (\frac{\pi}{4}傾いた直線偏光) \newline
Re(\boldsymbol{E_{\varphi=\frac{\pi}{2}}})
&= 
\begin{bmatrix}
0 \newline
1 
\end{bmatrix} (垂直偏光) \newline
\end{aligned}
$$

今は偏光分布が中心からの距離に依存しないので結局

のような偏光分布が得られる。

次にパラメーターを変えて同じように考えてみる。
今度は $\alpha = \frac{\pi}{8}, \beta = -\frac{\pi}{4}, \gamma = -\frac{3\pi}{16}$


$$
\begin{aligned}
\boldsymbol{S _ 1}(-\frac{\pi}{2}, -\frac{\pi}{4}) &\propto 
\begin{bmatrix}
\sin{\frac{\pi}{8} e^{i\frac{\pi}{4}}} + \cos{\frac{\pi}{8}} e^{-i\frac{\pi}{4}} \newline
i[\sin{\frac{\pi}{8} e^{i\frac{\pi}{4}}} - \cos{\frac{\pi}{8}} e^{-i\frac{\pi}{4}}]
\end{bmatrix}
\newline
\boldsymbol{S_2}(\frac{\pi}{2}, \frac{\pi}{4})
&\propto 
\begin{bmatrix}
\sin{\frac{3\pi}{8} e^{-i\frac{\pi}{4}}} + \cos{\frac{3\pi}{8}} e^{i\frac{\pi}{4}} \newline
i[\sin{\frac{3\pi}{8} e^{-i\frac{\pi}{4}}} - \cos{\frac{3\pi}{8}} e^{i\frac{\pi}{4}}]
\end{bmatrix}
\end{aligned}
$$


こっちは先ほどと同じで $p = 1, q = 2, \delta_{20} = -\frac{\pi}{2}$
ゆえ
$A = 2, B = -1, C = 0$ を代入

$$
\boldsymbol{E}
\propto 
\begin{bmatrix}
e^{i\varphi} [\sin{\frac{\pi}{8} e^{i\frac{\pi}{4}}} + \cos{\frac{\pi}{8}} e^{-i\frac{\pi}{4}}] + e^{-i\varphi} [\sin{\frac{3\pi}{8} e^{-i\frac{\pi}{4}}} + \cos{\frac{3\pi}{8}} e^{i\frac{\pi}{4}}] \\
i (e^{i\varphi} [\sin{\frac{\pi}{8} e^{i\frac{\pi}{4}}} - \cos{\frac{\pi}{8}} e^{-i\frac{\pi}{4}}] + e^{-i\varphi} [\sin{\frac{3\pi}{8} e^{-i\frac{\pi}{4}}} - \cos{\frac{3\pi}{8}} e^{i\frac{\pi}{4}}])
\end{bmatrix}
$$

$$
\begin{aligned}
\boldsymbol{E} _ {\varphi = \frac{\pi}{4}}
&\propto
\begin{bmatrix}
e^{i\frac{\pi}{2}} \sin{\frac{\pi}{8}} + e^{-\frac{i\pi}{2}} \sin{\frac{3\pi}{8}} + \cos{\frac{\pi}{8}} + \cos{\frac{3\pi}{8}}\\
i[e^{i\frac{\pi}{2}} \sin{\frac{\pi}{8}} + e^{-\frac{i\pi}{2}} \sin{\frac{3\pi}{8}} - \cos{\frac{\pi}{8}} - \cos{\frac{3\pi}{8}}] 
\end{bmatrix} \newline
&\propto
\begin{bmatrix}
\cos{\frac{\pi}{8}} + \cos{\frac{3\pi}{8}} + i[\sin{\frac{\pi}{8}} - \sin{\frac{3\pi}{8}}] \newline
\sin{\frac{3\pi}{8}} - \sin{\frac{\pi}{8}} - i[\cos{\frac{\pi}{8}} + \cos{\frac{3\pi}{8}}] 
\end{bmatrix} \newline
&\propto
\begin{bmatrix}
1.3 - i0.54 \newline
0.54 - i1.3
\end{bmatrix}
\end{aligned}
$$

ここで位相項 $e^{i\theta}$ をかけて実部を取って $\theta$を $0\rightarrow 2\pi$ と変化させたときの軌跡をプロットすると

となりこのように傾いた左回りの楕円偏光が得られる。
論文中では

であり確かに $\varphi = \frac{\pi}{4}$ の位置ではこのような楕円になっている。
