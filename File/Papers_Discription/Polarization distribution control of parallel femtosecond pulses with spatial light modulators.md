$$
\begin{aligned}
\boldsymbol{E} _ {out} &=
J _ {QWP(\frac{\pi}{4})} J _ {SLM2(\beta)} J_{HWP(\frac{\pi}{8})} J _ {SLM1(\alpha)} \boldsymbol{E}_{in} \newline
&\propto
\begin{bmatrix}
1+i & 1-i \newline
1-i & 1+i
\end{bmatrix}
\begin{bmatrix}
e^{-i\beta} & 0 \newline
0 & 1
\end{bmatrix}
\begin{bmatrix}
1 & 1 \newline
1 & -1
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
e^{-i\beta} & 0 \newline
0 & 1
\end{bmatrix}
\begin{bmatrix}
1 \newline
1 
\end{bmatrix} \newline
&=
\begin{bmatrix}
1+i & 1-i \newline
1-i & 1+i
\end{bmatrix}
\begin{bmatrix}
e^{-i\beta} \newline
1 
\end{bmatrix} \newline
&=
\begin{bmatrix}
e^{-i\beta}(1+i) + 1-i \newline
e^{-i\beta}(1-i) + 1+i
\end{bmatrix} \newline
&=
\begin{bmatrix}
\cos{\beta} + \sin{\beta} + 1 \newline
\cos{\beta} - \sin{\beta} + 1
\end{bmatrix}
+i
\begin{bmatrix}
\cos{\beta} - \sin{\beta} - 1 \newline
-(\cos{\beta} + \sin{\beta} - 1)
\end{bmatrix} \newline
\therefore \boldsymbol{E}_{out}
&=
\begin{bmatrix}
\cos{\frac{\beta}{2}} + \sin{\frac{\beta}{2}} \newline
\cos{\frac{\beta}{2}} - \sin{\frac{\beta}{2}}
\end{bmatrix}
+i
\begin{bmatrix}
\cos{\frac{\beta}{2}} - \sin{\frac{\beta}{2}} - 2 \newline
-(\cos{\frac{\beta}{2}} + \sin{\frac{\beta}{2}} - 2)
\end{bmatrix} \newline
\therefore Re(\boldsymbol{E} _ {out})
&=
\begin{bmatrix}
\cos{\frac{\beta}{2}} + \sin{\frac{\beta}{2}} \newline
\cos{\frac{\beta}{2}} - \sin{\frac{\beta}{2}}
\end{bmatrix}
\end{aligned}
$$

$$
\beta = 2\varphi + \theta
$$

とすると

$$
\begin{aligned}
\boldsymbol{E} _ {out} &\propto
\begin{bmatrix}
\cos{(\frac{2\varphi + \theta}{2})} + \sin{(\frac{2\varphi + \theta}{2})} \newline
\cos{(\frac{2\varphi + \theta}{2})} - \sin{(\frac{2\varphi + \theta}{2})}
\end{bmatrix} \newline
&=
\begin{bmatrix}
\cos{(\varphi + \frac{\theta}{2})} + \sin{(\varphi + \frac{\theta}{2})} \newline
\cos{(\varphi + \frac{\theta}{2})} - \sin{(\varphi + \frac{\theta}{2})}
\end{bmatrix} \newline
\therefore \boldsymbol{E} _ {out} &\propto
\begin{bmatrix}
\cos{\varphi}(\cos{\frac{\theta}{2}} + \sin{\frac{\theta}{2}}) + \sin{\varphi}(\cos{\frac{\theta}{2}} - \sin{\frac{\theta}{2}}) \newline
\cos{\varphi}(\cos{\frac{\theta}{2}} - \sin{\frac{\theta}{2}}) - \sin{\varphi}(\cos{\frac{\theta}{2}} + \sin{\frac{\theta}{2}})
\end{bmatrix}
\end{aligned}
$$

もし$\theta = -\frac{\pi}{2}$なら

$$
\begin{aligned}
\boldsymbol{E} _ {out} &\propto
\begin{bmatrix}
\cos{\varphi}(\cos{\frac{\pi}{4}} - \sin{\frac{\pi}{4}}) + \sin{\varphi}(\cos{\frac{\pi}{4}} + \sin{\frac{\pi}{4}}) \\
\cos{\varphi}(\cos{\frac{\pi}{4}} + \sin{\frac{\pi}{4}}) - \sin{\varphi}(\cos{\frac{\pi}{4}} - \sin{\frac{\pi}{4}})
\end{bmatrix} \newline
&\propto
\begin{bmatrix}
\sin{\varphi} \newline
\cos{\varphi}
\end{bmatrix}
\end{aligned}
$$
