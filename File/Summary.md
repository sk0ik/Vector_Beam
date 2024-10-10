# 研究内容

## はじめに

自分は光の分野のベクトルビームというものについて研究しています.特に空間光変調素子:SLM(Spatial Light Modulator)という光学素子を用いてベクトルビームを高精度で生成する研究をしています.

光は波としての性質も持ちますが以下のように電場と磁場が直交して振動しながら伝播していきます.

</br>

<div align="center">

| ![GIF1](https://github.com/sk0ik/Vector_Beam/blob/main/GIF/crop_resize_EMwave.gif)|
|:---:|
| 光の伝播の様子 |

</div>

</br>

※以下では電場について考えていきます.上図のように電場と磁場は直交しているので磁場を考えるときは直交成分を考えれば良いです.

高校の物理でも波の運動としてばねや振り子を考えており振幅と周波数という2つの自由度がありましたが光も同様に自由度を持ち

- 振幅
- 位相
- 時間周波数(単位時間当たりの波の数)
- 空間周波数(単位長さ当たりの波の数)
- 振動方向

のような自由度があります.自分はこの中でも光の振動方向を考える **偏光** という分野について研究をしています.例えば上記で挙げた自由度は以下のような光を考えることに対応しています.

| ![GIF1](https://github.com/sk0ik/Vector_Beam/blob/main/GIF/Ewave_normal.gif) | ![GIF2](https://github.com/sk0ik/Vector_Beam/blob/main/GIF/Ewave_amp.gif) | ![GIF3](https://github.com/sk0ik/Vector_Beam/blob/main/GIF/Ewave_phase.gif) | ![GI43](https://github.com/sk0ik/Vector_Beam/blob/main/GIF/Ewave_freq.gif) |
|:---:|:---:|:---:|:---:|
| 元の電場 | 振幅が大きくなったもの | 位相が進んだもの | (時間もしくは空間)周波数が大きくなったもの |

</br>

高校の物理ではばねや振り子の運動を1次元上で考えており振動方向は考えていませんでした.振動方向を考えることによって

- レーザー加工
- 光トラッピング
- スピントロニクス

などの分野に応用されています.

## スカラービーム

一般的に用いられるビーム(ここではスカラービームと呼びます.)は断面内で偏光状態が一様です.例えば直線偏光や円偏光はスカラービームです.直線偏光はなんとなく想像しやすいですが円偏光はどうでしょうか？円偏光は光の振動方向が時間的に(もしくは伝播距離的に)変化しているものを指します.以下にスカラービームの例を示します.

※光は紙面裏から表に向かって進んでおりその断面での電場の振動の様子を描画しています.

</br>

<div align="center">

| ![GIF1](https://github.com/sk0ik/Vector_Beam/blob/main/GIF/x_polarization.gif) | ![GIF2](https://github.com/sk0ik/Vector_Beam/blob/main/GIF/y_polarization.gif) |
|:---:|:---:|
| +0度偏光 | +90度偏光 |

</br>

| ![GIF1](https://github.com/sk0ik/Vector_Beam/blob/main/GIF/+45_polarization.gif) | ![GIF2](https://github.com/sk0ik/Vector_Beam/blob/main/GIF/-45_polarization.gif) |
|:---:|:---:|
| +45度偏光 | -45度偏光 |

</br>

| ![GIF1](https://github.com/sk0ik/Vector_Beam/blob/main/GIF/rcp.gif) | ![GIF2](https://github.com/sk0ik/Vector_Beam/blob/main/GIF/lcp.gif) |
|:---:|:---:|
| 右回り円偏光 | 左回り円度偏光 |

</div>

</br>

振動の様子はすべて異なりますが断面内ではすべて一様に振動していることが分かります.

## ベクトルビーム

次にベクトルビームの例を示します.同様に光は紙面裏から表に向かって進んでいます.

</br>

<div align="center">

| ![GIF1](https://github.com/sk0ik/Vector_Beam/blob/main/GIF/radial_polarization.gif) | ![GIF2](https://github.com/sk0ik/Vector_Beam/blob/main/GIF/azimuthal_polarization.gif) |
|:---:|:---:|
| ラジアル偏光ビーム | アジマス偏光ビーム |

</br>

| ![GIF1](https://github.com/sk0ik/Vector_Beam/blob/main/GIF/hatena1_polarization.gif) | ![GIF2](https://github.com/sk0ik/Vector_Beam/blob/main/GIF/hatena2_polarization.gif) |
|:---:|:---:|
| ? | ?? |

</div>

</br>

上図のようにベクトルビームは電場の振動方向が位置によって異なります.また,上図に示したラジアル偏光やアジマス偏光と呼ばれるベクトルビームは断面内で軸対称になっています.これを軸対称ベクトルビームと言います."?","??"のビームも軸対称ベクトルビームで,名前がついているかもしれませんが自分は知りません.もちろん,軸対称でなくても不一様な偏光分布であればベクトルビームに分類されます.

ここまでの説明ではベクトルビームの偏光状態だけを考えていましたがスカラービームの時のように位相という自由度も考えることができます.もし,ビーム断面の位置で位相が違ってもベクトルビームであることに変わりはありませんが物理的に違った特性を持ちます.

<div align="center">

| ![GIF1](https://github.com/sk0ik/Vector_Beam/blob/main/GIF/radial_polarization_phase1.gif) | ![GIF2](https://github.com/sk0ik/Vector_Beam/blob/main/GIF/radial_polarization_phase2.gif) |
|:---:|:---:|
| ラジアル偏光:らせん位相(l=1) | ラジアル偏光:らせん位相(l=-1) |

</div>

</br>

<div align="center">

| ![GIF1](https://github.com/sk0ik/Vector_Beam/blob/main/GIF/radial_polarization_phase3.gif) | ![GIF2](https://github.com/sk0ik/Vector_Beam/blob/main/GIF/radial_polarization_phase4.gif) |
|:---:|:---:|
| ラジアル偏光:らせん位相(l=2) | ラジアル偏光:らせん位相(l=-2) |

</div>

上図のように同じ偏光状態でも振動が遅れている部分があることが分かります.

## 実験光学系

<div align="center">

| ![GIF1](https://github.com/sk0ik/Vector_Beam/blob/main/Pic/setup/make_radial_azimuthal)|
|:---:|
| ラジアル,アジマス偏光を生成する光学系 |

</div>

## まとめ

上記で説明したような不一様な偏光状態,位相状態をSLMを用いて高精度に生成する研究をしています.実験がメインですが理論的な理解をしたうえで実験結果を考察し,誤差や失敗の原因を探るような研究をすることを心がけています.
