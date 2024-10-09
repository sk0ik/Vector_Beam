忘れたときに見返す用です.

- [波長板](#波長板)
  - [HWP](#hwp)
  - [QWP](#qwp)
  - [LP](#lp)
  - [表→裏](#表裏)
    - [HWP](#hwp-1)
    - [QWP](#qwp-1)


## 波長板

### HWP

$$
\begin{aligned}
J_{HWP(\theta)} &=
\begin{bmatrix}
-\sin^2{\theta} + \cos^2{\theta} & 2\sin{\theta} \cos{\theta} \newline
2\sin{\theta} \cos{\theta} & \sin^2{\theta} - \cos^2{\theta}
\end{bmatrix} \newline
\therefore J_{HWP(\theta)} &= 
\begin{bmatrix}
\cos{2\theta} & \sin{2\theta} \newline
\sin{2\theta} & -\cos{2\theta}
\end{bmatrix}
\end{aligned}
$$

### QWP

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
\therefore J_{QWP(\theta)}
&=
\begin{bmatrix}
1 - i\cos{2\theta} & -i\sin{2\theta} \newline
-i\sin{2\theta} & 1 + i\cos{2\theta}
\end{bmatrix}
\end{aligned}
$$

### LP

$$
\begin{aligned}
J _ {LP(\theta)} &=
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
\therefore J _ {LP(\theta)} &= 
\begin{bmatrix}
\cos^2{\theta} & \sin{\theta} \cos{\theta} \newline
\sin{\theta} \cos{\theta} & \sin^2{\theta}
\end{bmatrix} \newline
\end{aligned}
$$

### 表→裏

#### HWP

$$
\begin{aligned}
J _ {HWP} &=
\begin{bmatrix}
\cos{2(\pi-\theta)} & \sin{2(\pi-\theta)} \newline
\sin{2(\pi-\theta)} & -\cos{2(\pi-\theta)}
\end{bmatrix}
\begin{bmatrix}
-1 & 0 \newline
0 & 1
\end{bmatrix}
\begin{bmatrix}
\cos{2\theta} & \sin{2\theta} \newline
\sin{2\theta} & -\cos{2\theta}
\end{bmatrix} \newline
&=
\begin{bmatrix}
-\cos{2\theta} & -\sin{2\theta} \newline
\sin{2\theta} & -\cos{2\theta}
\end{bmatrix}
\begin{bmatrix}
\cos{2\theta} & \sin{2\theta} \newline
\sin{2\theta} & -\cos{2\theta}
\end{bmatrix} \newline
&=
\begin{bmatrix}
-\cos^2{2\theta}-\sin^2{2\theta} & 0 \newline
0 & \sin^2{2\theta}+\cos^2{2\theta}
\end{bmatrix} \newline
\therefore J _ {HWP} &=
\begin{bmatrix}
-1 & 0 \newline
0 & 1
\end{bmatrix}
\end{aligned}
$$

#### QWP

$$
\begin{aligned}
J _ {QWP(\theta)}&=
\begin{bmatrix}
1 - i\cos{2(\pi-\theta)} & -i\sin{2(\pi-\theta)} \newline
-i\sin{2(\pi-\theta)} & 1 + i\cos{2(\pi-\theta)}
\end{bmatrix}
\begin{bmatrix}
-1 & 0 \newline
0 & 1
\end{bmatrix}
\begin{bmatrix}
1 - i\cos{2\theta} & -i\sin{2\theta} \newline
-i\sin{2\theta} & 1 + i\cos{2\theta}
\end{bmatrix} \newline
&=
\begin{bmatrix}
-1+i\cos{2\theta} & i\sin{2\theta} \newline
-i\sin{2\theta} & 1 + i\cos{2\theta}
\end{bmatrix}
\begin{bmatrix}
1 - i\cos{2\theta} & -i\sin{2\theta} \newline
-i\sin{2\theta} & 1 + i\cos{2\theta}
\end{bmatrix} \newline
&=
\begin{bmatrix}
\cos^2{2\theta}-1+2i\cos{2\theta}+\sin^2{2\theta} & i\sin{2\theta}+\sin{2\theta}\cos{2\theta}-\sin{2\theta}\cos{2\theta} \newline
-i\sin{2\theta}-\sin{2\theta}\cos{2\theta}-i\sin{2\theta}+\sin{2\theta}\cos{2\theta} & -\sin^2{2\theta}+1+2i\cos{2\theta}\cos^2{2\theta}
\end{bmatrix} \newline
\therefore J _ {QWP(\theta)} &= 2i
\begin{bmatrix}
\cos{2\theta} & \sin{2\theta} \newline
-\sin{2\theta} & \cos{2\theta}
\end{bmatrix}
\end{aligned}
$$