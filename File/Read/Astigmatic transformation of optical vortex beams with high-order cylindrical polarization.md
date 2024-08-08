#### 研究背景
astigmation(収差)は良い側面もある.
- 光トラッピング(ボリュームディスプレイ)
- 光通信(軌道角運動量が1光子あたり1000$\hbar$)

2019年に光渦ガウシアンビームと非点収差非光渦ガウスビームを合わせてた非点収差楕円ガウスビーム(astigmatic elliptical Gaussian optical vortices(AEGOVs))が発案された.

#### 研究目的
光渦や非点収差ビームはこれまでたくさん研究されてきたがそれらはスカラービームだった.この論文ではベクトルビームの場合のAEGOVsについて研究している.

#### 原理

<div align="center">
<img src="pic/Astigmatic transformation of optical vortex beams with high-order cylindrical polarization/Fig1.png" alt="alt text" width="400">
</div>

$(\rho, \varphi, z)$は焦点面での座標,$(\theta, \phi)$はレンズ上での座標,$B(\theta, \phi)$はレンズの透過関数,$T(\theta)$は瞳関数,$\vec{P}(\theta, \phi)$は偏光行列としたとき

$$
\vec{E}(\rho, \varphi, z) = 
-\frac{if}{\lambda} \int_{0}^{\alpha} \int_{0}^{2\pi} B(\theta, \phi) T(\theta) \vec{P}(\theta, \phi) e^{ik(\rho\sin{\theta} \cos{(\phi - \varphi)} + z\cos{\theta})} \sin{\theta} d\theta d\phi
$$

と書ける.
$\vec{P}(\theta, \phi)$を数式で表すと

<div align="center">
<img src="pic/Astigmatic transformation of optical vortex beams with high-order cylindrical polarization/polarization matrix.png" alt="alt text" width="700">
</div>

$\vec{C}$は入力ビームの$x,y,z$偏光成分の複素振幅.
もし軸対称かつ$z$偏光成分が$0$であると焦点面での電場の分布は

<div align="center">
<img src="pic/Astigmatic transformation of optical vortex beams with high-order cylindrical polarization/Richards-Wolf equation.png" alt="alt text" width="700">
</div>

のようになる.透過関数は

<div align="center">
<img src="pic/Astigmatic transformation of optical vortex beams with high-order cylindrical polarization/transmission function.png" alt="alt text" width="700">
</div>

となる.最後の指数の項がシリンドリカルレンズと関係している.
