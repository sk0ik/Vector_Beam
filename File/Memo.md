忘れたときに見返す用です.

- [波長板](#波長板)
  - [HWP](#hwp)
  - [QWP](#qwp)
  - [LP](#lp)
  - [SLM(反射型)](#slm反射型)
  - [表→裏](#表裏)
    - [HWP](#hwp-1)
    - [QWP](#qwp-1)
- [ベクトルビームの作り方](#ベクトルビームの作り方)


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

$$
J _ {QWP(\pi-\theta)}=
\begin{bmatrix}
1 - i\cos{2\theta} & i\sin{2\theta} \newline
i\sin{2\theta} & 1 + i\cos{2\theta}
\end{bmatrix}
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

### SLM(反射型)

$$
\begin{bmatrix}
  -e^{i\delta} & 0 \newline
  0 & 1
\end{bmatrix}
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

## ベクトルビームの作り方

<p align="center">
<img src="https://github.com/sk0ik/Vector_Beam/blob/main/Pic/setup/generate_radial_azimuthal.png" alt="サンプル画像" width="500">
</p>

この光学系で得られるジョーンズベクトル

$$
J = J _ {QWP(\theta _ 2)} J _ {SLM} J _ {HWP(\theta _ 1)} J _ {PBS}
\begin{bmatrix}
\alpha \newline
\beta
\end{bmatrix}
$$

$$
\begin{aligned}
J &= 
  \begin{bmatrix}
    1 - i\cos{2\theta _ 2} & i\sin{2\theta _ 2} \newline
    i\sin{2\theta _ 2} & 1 + i\cos{2\theta _ 2}
  \end{bmatrix}
  \begin{bmatrix}
    -e^{i\delta} & 0 \newline
    0 & 1
  \end{bmatrix}
  \begin{bmatrix}
    \cos{2\theta _ 1} & \sin{2\theta _ 1} \newline
    \sin{2\theta _ 1} & -\cos{2\theta _ 1}
  \end{bmatrix}
  \begin{bmatrix}
    1 & 0 \newline
    0 & 0
  \end{bmatrix}
  \begin{bmatrix}
    \alpha \newline
    \beta
  \end{bmatrix} \newline
  &=
  \begin{bmatrix}
    1 - i\cos{2\theta _ 2} & i\sin{2\theta _ 2} \newline
    i\sin{2\theta _ 2} & 1 + i\cos{2\theta _ 2}
  \end{bmatrix}
  \begin{bmatrix}
    -e^{i\delta} & 0 \newline
    0 & 1
  \end{bmatrix}
  \begin{bmatrix}
    \cos{2\theta _ 2} & \sin{2\theta _ 2} \newline
    \sin{2\theta _ 2} & -\cos{2\theta _ 2}
  \end{bmatrix}
  \begin{bmatrix}
    \alpha \newline
    0
  \end{bmatrix} \newline
&\propto
  \begin{bmatrix}
    1 - i\cos{2\theta _ 2} & i\sin{2\theta _ 2} \newline
    i\sin{2\theta _ 2} & 1 + i\cos{2\theta _ 2}
  \end{bmatrix}
  \begin{bmatrix}
    -e^{i\delta} & 0 \newline
    0 & 1
  \end{bmatrix}
  \begin{bmatrix}
    \cos{2\theta _ 1} \newline
    \sin{2\theta _ 1}
  \end{bmatrix} \newline
&=
  \begin{bmatrix}
    1 - i\cos{2\theta _ 2} & i\sin{2\theta _ 2} \newline
    i\sin{2\theta _ 2} & 1 + i\cos{2\theta _ 2}
  \end{bmatrix}
  \begin{bmatrix}
    -e^{i\delta}\cos{2\theta _ 1} \newline
    \sin{2\theta _ 1}
  \end{bmatrix} \newline
\therefore J &\propto
  \begin{bmatrix}
    -e^{i\delta}\cos{2\theta _ 1}(1 - i\cos{2\theta _ 2})+i\sin{2\theta _ 1}\sin{2\theta _ 2} \newline
    -ie^{i\delta}\cos{2\theta _ 1}\sin{2\theta _ 2}+\sin{2\theta _ 1}(1+\cos{2\theta _ 2})
  \end{bmatrix}
\end{aligned}
$$

(ⅰ)$\theta _ 1=\frac{\pi}{8}, \theta _ 2=\frac{\pi}{4}$

$$
\begin{aligned}
  J &\propto
  \begin{bmatrix}
    -e^{i\delta}+i \newline
    -ie^{i\delta}+1
  \end{bmatrix} \newline
  &=
  \begin{bmatrix}
    -e^{i\delta}+i \newline
    -ie^{i\delta}+1
  \end{bmatrix} \newline
  &=e^{\frac{\delta}{2}}
  \begin{bmatrix}
    -e^{i\frac{\delta}{2}}+ie^{-i\frac{\delta}{2}} \newline
    -ie^{i\frac{\delta}{2}}+e^{-i\frac{\delta}{2}}
  \end{bmatrix} \newline
  &=e^{\frac{\delta}{2}}
  \begin{bmatrix}
  -\cos{\frac{\delta}{2}-i\sin{\frac{\delta}{2}}}+i\cos{\frac{\delta}{2}}+\sin{\frac{\delta}{2}} \newline
  -i\cos{\frac{\delta}{2}}+\sin{\frac{\delta}{2}}+\cos{\frac{\delta}{2}}-i\sin{\frac{\delta}{2}}
  \end{bmatrix} \newline
  &=e^{\frac{\delta}{2}}(1-i)
  \begin{bmatrix}
  \sin{\frac{\delta}{2}}-\cos{\frac{\delta}{2}} \newline
  \sin{\frac{\delta}{2}}+\cos{\frac{\delta}{2}}
  \end{bmatrix} \newline
  \therefore J &\propto
  \begin{bmatrix}
  \sin{\bigl(\frac{\delta}{2}-\frac{\pi}{4}\bigr)} \newline
  \sin{\bigl(\frac{\delta}{2}+\frac{\pi}{4}\bigr)}
  \end{bmatrix}  
\end{aligned}
$$

(ⅱ)$\theta _ 1=\frac{\pi}{8}, \theta _ 2=\frac{\pi}{4}+\frac{\alpha}{2}$

$$
\begin{aligned}
  J &\propto
  \begin{bmatrix}
    -e^{i\delta}(1 - i\cos{2\theta _ 2})+i\sin{2\theta _ 2} \newline
    -ie^{i\delta}\sin{2\theta _ 2}+(1+\cos{2\theta _ 2})
  \end{bmatrix} \newline
  \therefore J &\propto
  \begin{bmatrix}
    -e^{i\delta}(1 +i\sin{\alpha})+i\cos{\alpha} \newline
    -ie^{i\delta}\cos{\alpha}+1-\sin{\alpha}
  \end{bmatrix} \newline  
\end{aligned}
$$

$\delta = 2(\varphi+\frac{\pi}{4})$のとき

$$
J\propto e^{i\varphi}
\begin{bmatrix}
  -e^{i\varphi}(1 +i\sin{\alpha})-ie^{-i\varphi}\cos{\alpha} \newline
  -ie^{i\\varphi}\cos{\alpha}+e^{i\varphi}(\sin{\alpha}-1)
\end{bmatrix}
$$