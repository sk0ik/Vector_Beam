# 実験案
## その１(未完成)

⓵,BSに入射するビーム(HWP, PBS)
レーザーから出た光のジョーンズベクトルは

$$
\boldsymbol{E} = 
\begin{bmatrix}
E _ {x0} e^{i\varphi_x} \newline
E _ {y0} e^{i\varphi_y}
\end{bmatrix}
$$

となる。

$\alpha$ だけ傾けたHWPのジョーンズ行列は

$$
J _ {HWP(\alpha)} = 
\begin{bmatrix}
\cos{2\alpha} & \sin{2\alpha} \newline
\sin{2\alpha} & -\cos{2\alpha}
\end{bmatrix}
$$

となる。

今はPBSをP偏光を取り出すものとして使っているのでジョーンズ行列は

$$
J _ {PBS} = 
\begin{bmatrix}
1 & 0 \newline
0 & 0
\end{bmatrix}
$$

となる。これらをかければよいので

$$\begin{aligned}
\boldsymbol{E} _ {out1} &=
J_{PBS} J _ {HWP(\alpha)} \boldsymbol{E} _ {in} \newline
&= 
\begin{bmatrix}
1 & 0 \newline
0 & 0 
\end{bmatrix}
\begin{bmatrix}
\cos{2\alpha} & \sin{2\alpha} \newline
\sin{2\alpha} & -\cos{2\alpha}
\end{bmatrix}
\begin{bmatrix}
E _ {x0} e^{i\varphi_x} \newline
E _ {y0} e^{i\varphi_y}
\end{bmatrix} \newline
&=
\begin{bmatrix}
\cos{2\alpha} & \sin{2\alpha} \newline
0 & 0
\end{bmatrix}
\begin{bmatrix}
E _ {x0} e^{i\varphi_x} \newline
E _ {y0} e^{i\varphi_y}
\end{bmatrix} \newline
\therefore \boldsymbol{E} _ {out1}&=
\begin{bmatrix}
E _ {x0} e^{i\varphi_x} \cos{2\alpha} + E _ {y0} e^{i\varphi_y} \sin{2\alpha} \newline
0
\end{bmatrix}
\end{aligned}$$

つまりここではP偏光成分の大きさを決めていている。
今は偏光を考えているのでここでは便宜上

$$
\boldsymbol{E} _ {out1} =
\begin{bmatrix}
1 \newline
0
\end{bmatrix}
$$

とする。

⓶,SLM1で反射してBSに戻ってくるビーム

$$
J _ {SLM} = A_0
\begin{bmatrix}
-e^{i\delta} & 0 \newline
0 & 1
\end{bmatrix}
$$

であったが先ほどと同様に強度の情報はいらないので今は

$$
J _ {SLM1} = 
\begin{bmatrix}
-e^{i\delta _ 1} & 0 \newline
0 & 1
\end{bmatrix}
$$

$\delta _ 1 = p\varphi + \delta_{10} \quad (p \in \mathbb{Z})$

$$
J _ {SLM2} = 
\begin{bmatrix}
-e^{i\delta _ 2} & 0 \newline
0 & 1
\end{bmatrix}
$$

$\delta _ 2 = q\varphi + \delta _ {20} \quad (q \in \mathbb{Z})$

- $\varphi:$ 方位角(azimuthal angle)
- $\delta _ {10}, \delta _ {20}:$ constant phase

とする。(軸対称なベクトルビームを作りたいので変数は $\varphi$ (方位角のみ))
よってSLM1で反射してBSに戻ってくるビームは

$$
\begin{aligned}
\boldsymbol{E} _ {out2}
&=
\begin{bmatrix}
-e^{i\delta _ 1} & 0 \newline
0 & 1
\end{bmatrix}
\boldsymbol{E} _ {out1} \newline 
\boldsymbol{E} _ {out2}
&=
\begin{bmatrix}
-e^{i\delta _ 1} & 0 \newline
0 & 1
\end{bmatrix}
\begin{bmatrix}
1 \newline
0
\end{bmatrix} \newline
\therefore \boldsymbol{E} _ {out2}
&=
\begin{bmatrix}
 -e^{i\delta _ 1} \newline
0
\end{bmatrix}
\end{aligned}
$$

これも偏光だけを考えているので

$$
\boldsymbol{E} _ {out2} = 
\begin{bmatrix}
1 \newline
0
\end{bmatrix}
$$

SLM1の役割は波面変調

⓷, $\beta$ 傾けたHWPを通過してSLM2で反射して先ほどと同じHWPを通過してBSに戻ってくるビーム

$$
\begin{aligned}
\boldsymbol{E} _ {out3} &=
J_{HWP(-\beta)} J_{SLM2} J_ {HWP(\beta)} \boldsymbol{E} _ {out1}\\
&=
\begin{bmatrix}
\cos{2\beta} & -\sin{2\beta} \newline
-\sin{2\beta} & -\cos{2\beta}
\end{bmatrix}
\begin{bmatrix}
-e^{i\delta _ 2} & 0 \newline
0 & 1
\end{bmatrix}
\begin{bmatrix}
\cos{2\beta} & \sin{2\beta} \newline
\sin{2\beta} & -\cos{2\beta}
\end{bmatrix}
\begin{bmatrix}
1 \newline
0 
\end{bmatrix} \newline
&=
\begin{bmatrix}
\cos{2\beta} & -\sin{2\beta} \newline
-\sin{2\beta} & -\cos{2\beta}
\end{bmatrix}
\begin{bmatrix}
-e^{i\delta _ 2} & 0 \newline
0 & 1
\end{bmatrix}
\begin{bmatrix}
\cos{2\beta} \newline
\sin{2\beta}
\end{bmatrix} \newline
&=
\begin{bmatrix}
\cos{2\beta} & \sin{2\beta} \newline
\sin{2\beta} & -\cos{2\beta}
\end{bmatrix}
\begin{bmatrix}
-e^{i\delta _ 2}\cos{2\beta} \newline
\sin{2\beta}
\end{bmatrix} \newline
\therefore \boldsymbol{E} _ {out3}
&=
\begin{bmatrix} 
-e^{i\delta _ 2} \cos^2{2\beta} + \sin^2{2\beta} \newline
-\frac{e^{i\delta _ 2}}{2} \sin{4\beta} - \frac{\sin{4\beta}}{2}
\end{bmatrix}
\end{aligned}
$$

⓸各SLMで反射して戻ってきたビームがBSで合わさったビーム

$$
\begin{aligned}
\boldsymbol{E} _ {out4} &= \boldsymbol{E} _ {out2} + \boldsymbol{E} _ {out3} \newline
&=
\begin{bmatrix}
1 \newline
0
\end{bmatrix} + 
\begin{bmatrix}
-e^{-i\delta _ 2} \cos^2{2\beta} - \sin^2{2\beta} \newline
-\frac{e^{-i\delta _ 2}}{2} \sin{4\beta} - \frac{\sin{4\beta}}{2}
\end{bmatrix} \newline
\therefore \boldsymbol{E} _ {out4} &= 
\begin{bmatrix}
1 -e^{-i\delta _ 2} \cos^2{2\beta} + \sin^2{2\beta} \newline
-\frac{e^{-i\delta _ 2}}{2} \sin{4\beta} - \frac{\sin{4\beta}}{2}
\end{bmatrix}
\end{aligned}
$$

⓹,⓸のビームが $\gamma$ 傾けたQWPで変換されたビーム

$$
\begin{aligned}
\boldsymbol{E} _ {out} &=
J_{QWP(\gamma)} \boldsymbol{E} _ {out4} \newline
&=
\begin{bmatrix}
i \sin^2{\gamma} + \cos^2{\gamma} & \sin{\gamma} \cos{\gamma} (1 - i) \newline
\sin{\gamma} \cos{\gamma} (1 - i) & \sin^2{\gamma} + i \cos^2{\gamma}
\end{bmatrix}
\begin{bmatrix}
1 -e^{-i\delta _ 2} \cos^2{2\beta} + \sin^2{2\beta} \newline
-\frac{e^{-i\delta _ 2}}{2} \sin{4\beta} - \frac{\sin{4\beta}}{2}
\end{bmatrix} \newline
&=
\begin{bmatrix}
(1 -e^{-i\delta _ 2} \cos^2{2\beta} + \sin^2{2\beta}) (i \sin^2{\gamma} + \cos^2{\gamma}) + (-\frac{e^{-i\delta _ 2}}{2} \sin{4\beta} - \frac{\sin{4\beta}}{2}) (\sin{\gamma} \cos{\gamma} (1 - i)) \newline
(1 -e^{-i\delta _ 2} \cos^2{2\beta} + \sin^2{2\beta}) (\sin{\gamma} \cos{\gamma} (1 - i)) + (-\frac{e^{-i\delta _ 2}}{2} \sin{4\beta} - \frac{\sin{4\beta}}{2}) (\sin^2{\gamma} + i \cos^2{\gamma})
\end{bmatrix}
\end{aligned}
$$

天下り的に軸対称ビームを作るとき $\beta, \gamma$ をどうすればいいか考える。
例えば

$$
\boldsymbol{a} = e^{i\theta}
\begin{bmatrix}
\cos{\varphi} \newline
\sin{\varphi}
\end{bmatrix}
$$

というジョーンズベクトルを考えるとこれは各 $\varphi$ で半径方向を向く直線偏光を表している。今は半径:r=1とすると
偏光分布は以下のようになる。

また

$$
\boldsymbol{b} = e^{i\theta}
\begin{bmatrix}
-\sin{\varphi} \newline
\cos{\varphi}
\end{bmatrix}
$$

というジョーンズベクトルは各 $\varphi$ で円の接線方向を向く直線偏光を表している。また、半径方向には依存性はないので偏光分布は以下のようになる。

今は一つ目の偏光分布を作ることを考える。

解くのは

$$
\begin{aligned}
Re[(1 -e^{i\delta _ 2} \cos^2{2\beta} - \sin^2{2\beta}) (i \sin^2{\gamma} + \cos^2{\gamma}) + \frac{\sin4\beta}{2}(-e^{i\delta _ 2} + 1) (\sin{\gamma} \cos{\gamma} (1 - i))] &= \cos{\varphi} \\
Re[(1 -e^{i\delta _ 2} \cos^2{2\beta} - \sin^2{2\beta}) (\sin{\gamma} \cos{\gamma} (1 - i)) + \frac{\sin{4\beta}}{2}(-e^{i\delta _ 2} + 1) (\sin^2{\gamma} + i \cos^2{\gamma})] &= \sin{\varphi}
\end{aligned}
$$

まず

$$
\delta _ 2 = 2\varphi - \frac{\pi}{2}
$$

と仮定する。第一式は

$$
Re[(1 - \sin{2\varphi} \cos^2{2\beta} - \sin^2{2\beta} -i\cos{2\varphi} \cos^2{2\beta}) (i\sin^2{\gamma} + \cos^2{\gamma}) + \frac{\sin{4\beta}}{2} (1 - \sin{2\varphi} - i\cos{2\varphi})]
$$

**[補足]**
もしSLM2に入射するビームのところのHWPが1回だけしか通らないとしたら

$$
\boldsymbol{E} _ {out} = J _ {QWP(\gamma)} [J_{SLM1} + J _ {SLM2} J _ {HWP(\beta)}] J _ {PBS} J _ {HWP(\alpha)} \boldsymbol{E} _ {in}
$$

となるので

$$
\begin{aligned}
\boldsymbol{E} _ {out3}
&=
J _ {SLM2} J _ {HWP(\beta)} \boldsymbol{E} _ {out1} \newline
&=
\begin{bmatrix}
-e^{i\delta _ 2} & 0 \newline
0 & 1
\end{bmatrix}
\begin{bmatrix}
\cos{2\beta} & \sin{2\beta} \newline
\sin{2\beta} & -\cos{2\beta}
\end{bmatrix}
\begin{bmatrix}
1 \newline
0 
\end{bmatrix} \newline
&=
\begin{bmatrix}
-e^{i\delta _ 2} & 0 \newline
0 & 1
\end{bmatrix}
\begin{bmatrix}
\cos{2\beta} \newline
\sin{2\beta}
\end{bmatrix} \newline
\therefore \boldsymbol{E }_ {out3} &=
\begin{bmatrix} 
-e^{i\delta _ 2} \cos{2\beta} \newline
\sin{2\beta}
\end{bmatrix}
\end{aligned}
$$

となり

$$
\begin{aligned}
\boldsymbol{E} _ {out4} &= \boldsymbol{E} _ {out2} + \boldsymbol{E} _ {out3} \newline
&=
\begin{bmatrix}
1 \newline
0
\end{bmatrix} + 
\begin{bmatrix} 
-e^{-i\delta_2} \cos{2\beta} \newline
\sin{2\beta}
\end{bmatrix} \newline
\therefore \boldsymbol{E} _ {out4} &=
\begin{bmatrix}
1 -e^{-i\delta _ 2} \cos{2\beta} \newline
\sin{2\beta}
\end{bmatrix}
\end{aligned}
$$

$$
\begin{aligned}
\boldsymbol{E} _ {out} &=
J _ {QWP(\gamma)} \boldsymbol{E} _ {out4} \newline
&=
\begin{bmatrix}
i \sin^2{\gamma} + \cos^2{\gamma} & \sin{\gamma} \cos{\gamma} (1 - i) \newline
\sin{\gamma} \cos{\gamma} (1 - i) & \sin^2{\gamma} + i \cos^2{\gamma}
\end{bmatrix}
\begin{bmatrix}
1 -e^{-i\delta_2} \cos{2\beta} \newline
\sin{2\beta}
\end{bmatrix} \newline
\therefore \boldsymbol{E} _ {out}
&=
\begin{bmatrix}
(1 -e^{-i\delta_2} \cos{2\beta}) (i \sin^2{\gamma} + \cos^2{\gamma}) + \sin{2\beta} (\sin{\gamma} \cos{\gamma} (1 - i)) \newline
(1 -e^{-i\delta_2} \cos{2\beta}) (\sin{\gamma} \cos{\gamma} (1 - i)) +\sin{2\beta} (\sin^2{\gamma} + i \cos^2{\gamma})
\end{bmatrix}
\end{aligned}
$$

ここで

$$
\delta _ 2 = 2\varphi + \theta
$$

とすると

$$
\begin{aligned}
\therefore \boldsymbol{E} _ {out} &=
\begin{bmatrix}
(1 -\cos{(2\varphi + \theta)} -i\sin{(2\varphi + \theta)} \cos{2\beta}) (i \sin^2{\gamma} + \cos^2{\gamma}) + \sin{2\beta} (\sin{\gamma} \cos{\gamma} (1 - i)) \newline
(1 -\cos{(2\varphi + \theta)} -i\sin{(2\varphi + \theta)} \cos{2\beta}) (\sin{\gamma} \cos{\gamma} (1 - i)) +\sin{2\beta} (\sin^2{\gamma} + i \cos^2{\gamma})
\end{bmatrix} \newline
&=
\begin{bmatrix}
(1 - \cos{2\varphi} \cos{\theta} + \sin{2\varphi} \sin{\theta} -i \cos{2\beta} (\sin{2\varphi} \cos{\theta} + \cos{2\varphi} \sin{\theta})) (i \sin^2{\gamma} + \cos^2{\gamma}) + \sin{2\beta} (\sin{\gamma} \cos{\gamma} (1 - i)) \newline
(1 - \cos{2\varphi} \cos{\theta} + \sin{2\varphi} \sin{\theta} -i \cos{2\beta} (\sin{2\varphi} \cos{\theta} + \cos{2\varphi} \sin{\theta})) (\sin{\gamma} \cos{\gamma} (1 - i)) +\sin{2\beta} (\sin^2{\gamma} + i \cos^2{\gamma})
\end{bmatrix} \newline
\end{aligned}
$$

## その２(未完成)

これは

$$
\boldsymbol{E} _ {out} = J _ {QWP(\gamma)} J _ {HWP(-\beta)} J _ {SLM2(\delta _ 2)} J _ {HWP(\beta)} J _ {SLM1(\delta _ 1)}J _ {PBS} J _ {HWP(\alpha)} \boldsymbol{E} _ {in}
$$

HWPが $\frac{\pi}{8}$, QWPが$\frac{\pi}{4}$ 傾いているとき

$$
\begin{bmatrix}
1 & -i \newline
-i & 1
\end{bmatrix}
\begin{bmatrix}
1 & -1 \newline
-1 & -1
\end{bmatrix}
\begin{bmatrix}
e^{i\beta} & 0 \newline
0 & 1
\end{bmatrix}
\begin{bmatrix}
1 & 1 \newline
1 & -1
\end{bmatrix}
\begin{bmatrix}
1 \newline
0
\end{bmatrix}
$$

$$
\begin{bmatrix}
i\sin{(\beta + \frac{\pi}{4})} \newline
-\cos{(\beta + \frac{\pi}{4})}
\end{bmatrix}
$$

## その３(未完成)

$$
\boldsymbol{E} _ {out} = J _ {QWP(\frac{\pi}{4})} (J _ {SLM1} \boldsymbol{E} _ {1} + J _ {HWP(-\frac{\pi}{4})} J _ {SLM2} J _ {HWP(\frac{\pi}{4})} \boldsymbol{E} _ {2}) \newline
(\boldsymbol{E} _ {in} = \boldsymbol{E} _ {1} + \boldsymbol{E} _ {2})
$$

今はPBSによって

$$
\boldsymbol {E} _ {in} = \boldsymbol {E} _ {1} + \boldsymbol {E} _ {2} = 
\begin{bmatrix}
1 \newline
0
\end{bmatrix}
+
\begin{bmatrix}
0 \newline
1
\end{bmatrix}
$$

と分けられる。よって

$$
\begin{aligned}
\boldsymbol {E} _ {out}
&=
J _ {QWP(\frac{\pi}{4})} (J _ {SLM1} 
\begin{bmatrix}
1 \newline
0
\end{bmatrix} 
+J_{HWP(-\frac{\pi}{4})} J _ {SLM2} J _ {HWP(\frac{\pi}{4})} 
\begin{bmatrix}
0 \newline
1
\end{bmatrix}
) \newline
&=
\begin{bmatrix}
1 & -i \newline
-i & 1
\end{bmatrix} \biggl(
\begin{bmatrix}
e^{i\delta _ 1} & 0 \newline
0 & 1
\end{bmatrix}
\begin{bmatrix}
1 \newline
0 
\end{bmatrix}
+\begin{bmatrix}
0 & -1 \newline
-1 & 0
\end{bmatrix}
\begin{bmatrix}
e^{i\delta _ 2} & 0 \newline
0 & 1
\end{bmatrix}
\begin{bmatrix}
0 & 1 \newline
1 & 0
\end{bmatrix}
\begin{bmatrix}
0 \newline
1
\end{bmatrix} \biggr) \newline
&=
\begin{bmatrix}
1 & -i \newline
-i & 1
\end{bmatrix} \biggl(
\begin{bmatrix}
e^{i\delta _ 1} \newline
0 
\end{bmatrix}
+\begin{bmatrix}
0 & -1 \newline
-1 & 0
\end{bmatrix}
\begin{bmatrix}
e^{i\delta _ 2} & 0 \newline
0 & 1
\end{bmatrix}
\begin{bmatrix}
1 \newline
0
\end{bmatrix} \biggr) \newline
&=
\begin{bmatrix}
1 & -i \newline
-i & 1
\end{bmatrix} \biggl(
\begin{bmatrix}
e^{i\delta _ 1} \newline
0 
\end{bmatrix}
+\begin{bmatrix}
0 & -1 \newline
-1 & -0
\end{bmatrix}
\begin{bmatrix}
e^{i\delta _ 2} \newline
0
\end{bmatrix}
\biggr)
\newline
&=
\begin{bmatrix}
1 & -i \newline
-i & 1
\end{bmatrix} \biggl(
e^{i\delta _ 1}
\begin{bmatrix}
1 \newline
0 
\end{bmatrix}
+e^{i\delta _ 2}
\begin{bmatrix}
0 \newline
1
\end{bmatrix}
\biggr)
\newline
&=
e^{i\delta _ 1}
\begin{bmatrix}
1 \newline
-i 
\end{bmatrix}
+e^{i\delta _ 2}
\begin{bmatrix}
-i \newline
1
\end{bmatrix} \newline
\therefore \boldsymbol{E} _ {out} &=
e^{i\delta _ 1}
\begin{bmatrix}
1 \newline
-i 
\end{bmatrix}
+e^{i\delta _ 2}
\begin{bmatrix}
1 \newline
i
\end{bmatrix}
\end{aligned}
$$

$$
\begin{aligned}
J _ {SLM1} 
\begin{bmatrix}
1 \newline
0
\end{bmatrix}
&=
\begin{bmatrix}
\cos{\phi} + i \sin{\phi} \newline
0
\end{bmatrix} \newline
&=
\frac{1}{\sqrt{2}}
\begin{bmatrix}
1 + i \newline
0
\end{bmatrix} \newline
&=
\begin{bmatrix}
i \newline
0
\end{bmatrix}
\end{aligned}
$$

$$
\begin{aligned}
J _ {SLM2} 
\begin{bmatrix}
1 \newline
0
\end{bmatrix}
&=
\begin{bmatrix}
\cos{\phi} -i \sin{\phi} \newline
0
\end{bmatrix}
\end{aligned}
$$

の $x, y$ 成分を入れ替えたもの

$$
\begin{bmatrix}
0 \newline
\cos{\phi} - i \sin{\phi}
\end{bmatrix}
$$

足し合わせて

$$
\begin{bmatrix}
\cos{\phi} + i \sin{\phi} \newline
\cos{\phi} - i \sin{\phi}
\end{bmatrix}
$$

これがQWPで変換されると

$$
\begin{aligned}
\begin{bmatrix}
1 & -i \newline
-i & 1
\end{bmatrix}
\begin{bmatrix}
\cos{\phi} + i \sin{\phi} \newline
\cos{\phi} - i \sin{\phi}
\end{bmatrix}
&=
\begin{bmatrix}
\cos{\phi} - \sin{\phi} + i(\sin{\phi} - \cos{\phi}) \newline
\cos{\phi} + \sin{\phi} - i(\cos{\phi} + \sin{\phi})
\end{bmatrix}
\begin{bmatrix}
\cos{\phi} - \sin{\phi} \newline 
\cos{\phi} + \sin{\phi}
\end{bmatrix} \newline
&=
\begin{bmatrix}
\cos{\bigl (\phi + \frac{\pi}{4} \bigr )} \newline
\cos{\bigl ( \phi - \frac{\pi}{4} \bigr )}
\end{bmatrix} \newline
&=
\begin{bmatrix}
\cos{\phi} \newline
\sin{\phi}
\end{bmatrix}
\end{aligned}
$$

このように位相変調された左右円偏光の重ね合わせで表現される。

ここで

$$
\begin{aligned}
\delta_{1}
&=
\phi + \phi_{0} \newline
\delta_{2}
&=
-(\phi + \phi_{0})
\end{aligned}
$$

という位相をSLMに表示させることを考える。
例えば

$$
\begin{aligned}
\delta _ 1
&=
\phi \newline
\delta _ 2
&=
-\phi
\end{aligned}
$$

とすると

$$
\begin{bmatrix}
e^{i \phi} & 0 \newline
0 & 1
\end{bmatrix}
\begin{bmatrix}
1 \newline
0 
\end{bmatrix}
$$

$$
\begin{aligned}
\boldsymbol{E} _ {out} &= e^{i\phi}
\begin{bmatrix}
1 \newline
-i
\end{bmatrix}
+e^{-i\phi}
\begin{bmatrix}
1 \newline
i
\end{bmatrix} \newline
&= (\cos{\phi} + i\sin{\phi})
\begin{bmatrix}
1 \newline
-i
\end{bmatrix}
+(\cos{\phi} - i\sin{\phi})
\begin{bmatrix}
1 \newline
i
\end{bmatrix} \newline
&=
\begin{bmatrix}
\cos{\phi} + i\sin{\phi} \newline
\sin{\phi} - i\cos{\phi}
\end{bmatrix}+
\begin{bmatrix}
\cos{\phi} - i\sin{\phi} \newline
\sin{\phi} + i\cos{\phi}
\end{bmatrix} \newline
&=
\begin{bmatrix}
2\cos{\phi} \newline
2\sin{\phi}
\end{bmatrix} \newline
\therefore \boldsymbol{E} _ {out} & \propto
\begin{bmatrix}
\cos{\phi} \newline
\sin{\phi}
\end{bmatrix}
\end{aligned}
$$

これは各 $\phi$ でその点と原点を結ぶ方向の直線偏光を表している。
つまり中心から外側に向かうような偏光分布になる。

SLM1

$$
\begin{bmatrix}
\cos{\phi} \cos{t} - \sin{\phi} \sin{t} \newline
\sin{\phi} \cos{t} + \cos{\phi} \sin{t}
\end{bmatrix}
$$

$(\cos{\phi}, \sin{\phi})$ の点でのベクトル $\boldsymbol{E} _ {out}$ をプロットしたもの

次に

$$
\begin{aligned}
\delta _ 1
&=
\phi + \frac{\pi}{2} \newline
\delta _ 2
&=
-(\phi + \frac{\pi}{2})
\end{aligned}
$$

とすると

$$
\begin{aligned}
\boldsymbol{E} _ {out} &= e^{i(\phi + \frac{\pi}{2})}
\begin{bmatrix}
1 \newline
-i
\end{bmatrix}
+e^{-i(\phi + \frac{\pi}{2})}
\begin{bmatrix}
1 \newline
i
\end{bmatrix} \newline
&= \Bigl( \cos{(\phi + \frac{\pi}{2})} + i\sin{(\phi + \frac{\pi}{2})} \Bigr)
\begin{bmatrix}
1 \newline
-i
\end{bmatrix}
+\Bigl(\cos{(\phi + \frac{\pi}{2})} - i\sin{(\phi + \frac{\pi}{2})} \Bigr)
\begin{bmatrix}
1 \newline
i
\end{bmatrix} \newline
&= \Bigl( -\sin{\phi} + i\cos{\phi} \Bigr)
\begin{bmatrix}
1 \newline
-i
\end{bmatrix}
+\Bigl(-\sin{\phi} - i\cos{\phi} \Bigr)
\begin{bmatrix}
1 \newline
i
\end{bmatrix} \newline
&=
\begin{bmatrix}
-\sin{\phi} + i\cos{\phi} \newline
\cos{\phi} + i\sin{\phi}
\end{bmatrix}+
\begin{bmatrix}
-\sin{\phi} - i\cos{\phi} \newline
\cos{\phi} - i\sin{\phi}
\end{bmatrix} \newline
&=
\begin{bmatrix}
-2\sin{\phi} \newline
2\cos{\phi}
\end{bmatrix} \newline
\therefore \boldsymbol{E} _ {out} & \propto
\begin{bmatrix}
\sin{\phi} \newline
-\cos{\phi}
\end{bmatrix}
\end{aligned}
$$

これは各 $\phi$ で円の接線方向を向いた直線偏光を表している。確かに

$$
\begin{bmatrix}
\cos{\phi} \newline
\sin{\phi}
\end{bmatrix} \cdot
\begin{bmatrix}
\sin{\phi} \newline
-\cos{\phi}
\end{bmatrix}
= 0
$$

直交している。

$(\cos{\phi}, \sin{\phi})$ の点でのベクトル $\boldsymbol{E} _ {out}$ をプロットしたもの

最後に

$$
\begin{aligned}
\delta _ 1 &= 2 \phi \newline
\delta _ 2 &= -2 \phi
\end{aligned}
$$

を考える。

$$
\begin{aligned}
\boldsymbol{E} _ {out} &= e^{i2\phi}
\begin{bmatrix}
1 \newline
-i
\end{bmatrix}
+e^{-i2\phi}
\begin{bmatrix}
1 \newline
i
\end{bmatrix} \newline
&= (\cos{2\phi}+i\sin{2\phi})
\begin{bmatrix}
1 \newline
-i
\end{bmatrix}
+(\cos{2\phi}-i\sin{2\phi})
\begin{bmatrix}
1 \newline
i
\end{bmatrix} \newline
&=
\begin{bmatrix}
\cos{2\phi} + i\sin{2\phi} \newline
\sin{2\phi} - i\cos{2\phi}
\end{bmatrix}+
\begin{bmatrix}
\cos{2\phi} - i\sin{2\phi} \newline
\sin{2\phi} + i\cos{2\phi}
\end{bmatrix} \newline
&=
\begin{bmatrix}
2\cos{2\phi} \newline
2\sin{2\phi}
\end{bmatrix} \newline
\therefore \boldsymbol{E} _ {out} &\propto
\begin{bmatrix}
\cos{2\phi} \newline
\sin{2\phi}
\end{bmatrix}
\end{aligned}
$$

$(\cos{\phi}, \sin{\phi})$ の点でのベクトル $\boldsymbol{E}_{out}$ をプロットしたもの

## その4

$$
\begin{aligned}
\boldsymbol{E} _ {out}
&=
\begin{bmatrix}
1+i & 1-i \newline
1-i & 1+i
\end{bmatrix}
\begin{bmatrix}
e^{i\beta} & 0 \newline
0 & 1
\end{bmatrix}
\begin{bmatrix}
1 & 1 \newline
1 & -1
\end{bmatrix}
\begin{bmatrix}
e^{i\alpha} & 0 \newline
0 & 1
\end{bmatrix}
\begin{bmatrix}
1 \newline
0
\end{bmatrix} \newline
&=
\begin{bmatrix}
1+i & 1-i \newline
1-i & 1+i
\end{bmatrix}
\begin{bmatrix}
e^{i\beta} & 0 \newline
0 & 1
\end{bmatrix}
\begin{bmatrix}
1 & 1 \newline
1 & -1
\end{bmatrix}
\begin{bmatrix}
e^{i\alpha} \newline
0
\end{bmatrix} \newline
&=
\begin{bmatrix}
1+i & 1-i \newline
1-i & 1+i
\end{bmatrix}
\begin{bmatrix}
e^{i\beta} & 0 \newline
0 & 1
\end{bmatrix}
e^{i\alpha}
\begin{bmatrix}
1 \newline
1
\end{bmatrix} \newline
&=
e^{i\alpha}
\begin{bmatrix}
1+i & 1-i \newline
1-i & 1+i
\end{bmatrix}
\begin{bmatrix}
e^{i\beta} \newline
1
\end{bmatrix} \newline
&=
e^{i\alpha}
\begin{bmatrix}
e^{i\frac{\pi}{4}}e^{i\beta}+e^{-i\frac{\pi}{4}} \newline
e^{-i\frac{\pi}{4}}e^{i\beta}+e^{i\frac{\pi}{4}}
\end{bmatrix} \newline
\therefore \boldsymbol{E}
&=
\begin{bmatrix}
i \cos{\beta} - \sin{\beta} + 1 \newline
\cos{\beta} + i\sin{\beta} + i
\end{bmatrix}
\end{aligned}
$$

## その５

上の光学系で得られるジョーンズベクトルは

$$
\begin{aligned}
\boldsymbol{E}
&=
\begin{bmatrix}
1 - i \cos{2\theta _ Q} & - i \sin{2\theta _ Q} \newline
-i \sin{2\theta _ Q} & 1 + i \cos{2\theta _ Q}
\end{bmatrix}
\begin{bmatrix}
e^{i\beta} & 0 \newline
0 & 1
\end{bmatrix}
\begin{bmatrix}
\cos{2\theta _ H} & \sin{2\theta _ H} \newline
\sin{2\theta _ H} & - \cos{2\theta _ H}
\end{bmatrix}
\begin{bmatrix}
e^{i\alpha} & 0 \newline
0 & 1
\end{bmatrix}
\begin{bmatrix}
1 \newline
0
\end{bmatrix} \newline
&=
\begin{bmatrix}
1 - i \cos{2\theta _ Q} & - i \sin{2\theta _ Q} \newline
-i \sin{2\theta _ Q} & 1 + i \cos{2\theta _ Q}
\end{bmatrix}
\begin{bmatrix}
e^{i\beta} & 0 \newline
0 & 1
\end{bmatrix}
\begin{bmatrix}
\cos{2\theta _ H} & \sin{2\theta _ H} \newline
\sin{2\theta _ H} & - \cos{2\theta _ H}
\end{bmatrix}
e^{i\alpha}
\begin{bmatrix}
1 \newline
0
\end{bmatrix} \newline
&=
e^{i\alpha}
\begin{bmatrix}
1 - i \cos{2\theta _ Q} & - i \sin{2\theta _ Q} \newline
-i \sin{2\theta _ Q} & 1 + i \cos{2\theta _ Q}
\end{bmatrix}
\begin{bmatrix}
e^{i\beta} & 0 \newline
0 & 1
\end{bmatrix}
\begin{bmatrix}
\cos{2\theta _ H} \newline
\sin{2\theta _ H}
\end{bmatrix} \newline
&=
e^{i\alpha}
\begin{bmatrix}
1 - i \cos{2\theta _ Q} & - i \sin{2\theta _ Q} \newline
-i \sin{2\theta _ Q} & 1 + i \cos{2\theta _ Q}
\end{bmatrix}
\begin{bmatrix}
e^{i\beta}\cos{2\theta _ H} \newline
\sin{2\theta _ H}
\end{bmatrix} \newline
\therefore \boldsymbol{E}
&=
e^{i\alpha}
\begin{bmatrix}
e^{i\beta}(1 - i \cos{2\theta _ Q})\cos{2\theta _ H} - i \sin{2\theta _ Q}\sin{2\theta _ H} \newline
-i e^{i\beta}\sin{2\theta _ Q}\cos{2\theta _ H} + (1 + i \cos{2\theta _ Q})\sin{2\theta _ H}
\end{bmatrix}
\end{aligned}
$$

$$
\vec{E} =
\begin{bmatrix}
e^{i\beta}(1 - i \cos{2\theta _ Q}) - i \sin{2\theta _ Q} \newline
-i e^{i\beta}\sin{2\theta _ Q} + 1 + i \cos{2\theta _ Q}
\end{bmatrix}
$$

となる。

例えば

$$
\theta _ H = \frac{\pi}{8}, \theta _ Q = \frac{\pi}{4}
$$

のとき、ジョーンズベクトルは

$$
\boldsymbol{E} = e^{i\alpha}
\begin{bmatrix}
e^{i\beta}-i \newline
-ie^{i\beta}+1
\end{bmatrix}
$$

となる。少し変形すると

$$
\begin{aligned}
\boldsymbol{E}
&=
e^{i\alpha}e^{i\frac{\beta}{2}}
\begin{bmatrix}
e^{i\frac{\beta}{2}}+e^{-i\frac{\beta+\pi}{2}} \newline
e^{i\frac{\beta-\pi}{2}}+e^{-i\frac{\beta}{2}}
\end{bmatrix} \newline
&=
e^{i\alpha}e^{i\frac{\beta}{2}}
\begin{bmatrix}
\cos{\frac{\beta}{2}}+i\sin{\frac{\beta}{2}}+\cos{\frac{\beta+\pi}{2}}-i\sin{\frac{\beta+\pi}{2}} \newline
\cos{\frac{\beta-\pi}{2}}+i\sin\frac{\beta-\pi}{2}+\cos{\frac{\beta}{2}}-i\sin{\frac{\beta}{2}}
\end{bmatrix} \newline
&=
e^{i\alpha}e^{i\frac{\beta}{2}}
\begin{bmatrix}
\cos{\frac{\beta}{2}}+i\sin{\frac{\beta}{2}}-\sin{\frac{\beta}{2}}-i\cos{\frac{\beta}{2}} \newline
\sin{\frac{\beta}{2}}-i\cos\frac{\beta}{2}+\cos{\frac{\beta}{2}}-i\sin{\frac{\beta}{2}}
\end{bmatrix} \newline
&=
e^{i\alpha}e^{i\frac{\beta}{2}}
\begin{bmatrix}
(1-i)\cos{\frac{\beta}{2}}-(1-i)\sin{\frac{\beta}{2}} \newline
(1-i)\cos{\frac{\beta}{2}}+(1-i)\sin{\frac{\beta}{2}}
\end{bmatrix} \newline
&=
e^{i\alpha}e^{i\frac{\beta}{2}}(1-i)
\begin{bmatrix}
\cos{\frac{\beta}{2}}-\sin{\frac{\beta}{2}} \newline
\cos{\frac{\beta}{2}}+\sin{\frac{\beta}{2}}
\end{bmatrix} \newline
\therefore \boldsymbol{E} &=
e^{i\alpha}e^{i\frac{\beta}{2}}(1-i)
\begin{bmatrix}
\cos({\frac{\beta}{2}+\frac{\pi}{4}}) \newline
\sin({\frac{\beta}{2}+\frac{\pi}{4}})
\end{bmatrix}
\end{aligned}
$$

$$
\vec{E} =
\begin{bmatrix}
\cos({\frac{\beta}{2}+\frac{\pi}{4}}) \newline
\sin({\frac{\beta}{2}+\frac{\pi}{4}})
\end{bmatrix}
$$

を得る。

もし

$$
\beta=2\phi-\frac{\pi}{2}
$$

なら

$$
\boldsymbol{E} = 
\begin{bmatrix}
\cos{\phi} \newline
\sin{\phi}
\end{bmatrix}
$$

となりこれは径方向偏光ビームを表している。

### 歪の原因

aaaaa

### 測定について

それぞれの偏光成分を取りたい

１，垂直、水平、斜め　それぞれの偏光成分は直線偏光子をかませればいい

２，円偏光をどうやって取り出すか

QWPに入る前のビームは

$$
\begin{aligned}
\begin{bmatrix}
e^{i(2\phi-\frac{\pi}{2})} \newline
1
\end{bmatrix}
& \propto
\begin{bmatrix}
e^{i(\phi-\frac{\pi}{4})} \newline
e^{-i(\phi-\frac{\pi}{4})}
\end{bmatrix} \newline
&=
\begin{bmatrix}
e^{i\phi} \newline
ie^{-i\phi}
\end{bmatrix} \newline
&=
\begin{bmatrix}
\cos{\phi}+i\sin{\phi} \newline
i(\cos{\phi}-i\sin{\phi})
\end{bmatrix}
\end{aligned}
$$

となるがこれを水平、垂直偏光の重ね合わせでかくと

$$
(\cos{\phi}+i\sin{\phi})
\begin{bmatrix}
1 \newline
0
\end{bmatrix}
+
i(\cos{\phi}-i\sin{\phi})
\begin{bmatrix}
0 \newline
1
\end{bmatrix}
$$

これが$\frac{\pi}{4}$傾けたQWPに入ると

$$
\begin{aligned}
E_{out}
&=
(\cos{\phi}+i\sin{\phi})
\begin{bmatrix}
1 & -i \newline
-i & 1
\end{bmatrix}
\begin{bmatrix}
1 \newline
0
\end{bmatrix}
+
\begin{bmatrix}
1 & -i \newline
-i & 1
\end{bmatrix}
i(\cos{\phi}-i\sin{\phi})
\begin{bmatrix}
0 \newline
1
\end{bmatrix} \newline
&=
(\cos{\phi}+i\sin{\phi})
\begin{bmatrix}
1 \newline
-i
\end{bmatrix}
+
i(\cos{\phi}-i\sin{\phi})
\begin{bmatrix}
-i \newline
1
\end{bmatrix} \newline
&=
(\cos{\phi}-i\sin{\phi})
\begin{bmatrix}
1 \newline
i
\end{bmatrix}
+
(\cos{\phi}+i\sin{\phi})
\begin{bmatrix}
1 \newline
-i
\end{bmatrix} \newline
& \propto
\begin{bmatrix}
\cos{\phi} \newline
\sin{\phi}
\end{bmatrix}
\end{aligned}
$$

つまりQWPで変換される前のビームの水平偏光成分が最終的に得られるベクトルビームの左回り円偏光成分に、垂直成分が右回り円偏光成分に対応している

また

$$
\beta=2\phi+\frac{\pi}{2}
$$

なら

$$
\boldsymbol{E} = 
\begin{bmatrix}
-\sin{\phi} \newline
\cos{\phi}
\end{bmatrix}
$$

となり、これは方位角方向偏光ビームを表している。

またこれらのビームを作るためにSLMに表示させたホログラムの位相分布は渦が2回繰り返して45°傾いているものになる。

角度を代入する前のジョーンズ行列を詳しく見ていく。

任意のジョーンズベクトルは直交する2つのジョーンズベクトルで展開できる。その2つのジョーンズベクトルの選び方は無数にあり、ポアンカレ球上で真反対に位置する偏光を表すジョーンズベクトル(北極と南極、日本とブラジル、みたいな)がそのペアになる。

# その６

SLMの左半分水平偏光を当てるとして

$$
HWP(-\theta) \rightarrow WHP(\theta) \rightarrow SLM(\beta) \rightarrow HWP(-\theta)
$$

ベクトルは

$$
\begin{bmatrix}
\cos{2\theta _ H} & -\sin{2\theta _ H} \newline
-\sin{2\theta _ H} & -\cos{2\theta _ H}
\end{bmatrix}
\begin{bmatrix}
e^{i\beta} & 0 \newline
0 & 1
\end{bmatrix}
\begin{bmatrix}
\cos{2\theta _ H} & \sin{2\theta _ H} \newline
\sin{2\theta _ H} & -\cos{2\theta _ H}
\end{bmatrix}
\begin{bmatrix}
\cos{2\theta _ H} & -\sin{2\theta _ H} \newline
-\sin{2\theta _ H} & -\cos{2\theta _ H}
\end{bmatrix}
\begin{bmatrix}
1 \newline
0
\end{bmatrix} \newline
-------- \newline
\begin{bmatrix}
e^{i\beta} \cos^3{2\theta _ H} - e^{i\beta} \sin^2{2\theta _ H} \cos{2\theta _ H} -2\sin^2{2\theta _ H} \cos{2\theta _ H} \newline
-e^{i\beta} \sin{2\theta _ H} \cos^2{2\theta _ H} + e^{i\beta} \sin^3{2\theta _ H} - 2\sin{2\theta _ H} \cos^2{2\theta _ H}
\end{bmatrix}
$$

QWPをかければ

$$
\begin{bmatrix}
1 - i\cos{2\theta _ Q} & -i\sin{2\theta _ Q} \newline
-i\sin{2\theta _ Q} & 1 + i\cos{2\theta _ Q}
\end{bmatrix}
\begin{bmatrix}
e^{i\beta} \cos^3{2\theta _ H} - e^{i\beta} \sin^2{2\theta _ H} \cos{2\theta _ H} -2\sin^2{2\theta _ H} \cos{2\theta _ H} \newline
-e^{i\beta} \sin{2\theta _ H} \cos^2{2\theta _ H} + e^{i\beta} \sin^3{2\theta _ H} - 2\sin{2\theta _ H} \cos^2{2\theta _ H}
\end{bmatrix}
$$