<div style="text-align: center; font-size: 25px; font-weight: bold;">
Adaptive optical microscopy the ongoing quest for a perfect image(2014)
</div>

- [研究背景](#研究背景)
- [研究目的](#研究目的)
- [原理](#原理)
  - [収差について](#収差について)
  - [収差の計測方法](#収差の計測方法)
    - [直接測る](#直接測る)
  - [間接的に測る](#間接的に測る)
- [多光子顕微鏡(multiphoton microscope)](#多光子顕微鏡multiphoton-microscope)
- [共焦点顕微鏡(confocal microscope)](#共焦点顕微鏡confocal-microscope)
- [広視野顕微鏡(widefield microscopy)](#広視野顕微鏡widefield-microscopy)
- [構造化照明顕微鏡法（Structured Illumination Microscopy）](#構造化照明顕微鏡法structured-illumination-microscopy)
- [ライトシート顕微(light sheet microscopy)](#ライトシート顕微light-sheet-microscopy)
- [Microendoscopy](#microendoscopy)
- [Stimulated emission depletion(STED)microscopes](#stimulated-emission-depletionstedmicroscopes)
- [結果](#結果)
- [結論](#結論)


</br>

## 研究背景

</br>

AO(Adaptive Optics:補償光学)は高解像度顕微鏡で使われてきたが標本により発生する収差の補正は行われてこなかった.生物,医学の分野で高精度な計測(観察)とそれを補正する方法(AO)が必要になる.

</br>

## 研究目的

</br>

標本で反射することにより発生する収差は光学系が完璧でも起こってしまう収差.これにより

- 解像度
- コントラスト

が低下する.

</br>

## 原理

</br>

### 収差について

</br>

今までは収差は空間で一様なものとして扱ってきた.実際は場所によって収差の量が異なるのでこれは空間の収差の平均値で扱ってきたことを意味する.

</br>

### 収差の計測方法

</br>

収差の計測方法には直接的,間接的なものがある.

#### 直接測る

</br>

シャックハルトマンセンサーなどを使って３次元のサンプルから反射してきた光を集光して計測する.しかし焦点位置だけでの光が欲しいのにその周辺の光も計測してしまう.

ピンホールの穴が大きすぎると焦点位置以外の光が入ってしまうし小さすぎると収差の情報を持った光が入ってこない

</br>

### 間接的に測る

</br>

複数枚の画像を取得し解析することで収差の情報を測る.直接的な方法と違いハードウェア(光学素子など)は簡単になるがソフトウェアは複雑になる.

収差は異なるモードの重ね合わせであるとして複数枚の画像からそれらがどのくらいの割合で重ね合わせられているかを調べる.この複数の画像から収差の情報の勾配がわかる.

## 多光子顕微鏡(multiphoton microscope)

</br>

この顕微鏡では入射ビームの収差だけを補正すればいい.

## 共焦点顕微鏡(confocal microscope)

</br>

先ほどとは違いサンプルで反射したビームの収差も補正する必要がある.

</br>

## 広視野顕微鏡(widefield microscopy)

</br>

これだと逆に入射ビームの収差は考えずにサンプルから反射してきたビームの収差を考える必要がある.

</br>

## 構造化照明顕微鏡法（Structured Illumination Microscopy）

</br>

これもどちらのパスの収差を補正する.厚いサンプルに有効.

</br>

## ライトシート顕微(light sheet microscopy)

</br>

複数の光を当てるのでそれぞれに収差が発生.

</br>

## Microendoscopy

</br>

軸外幾何収差

</br>

## Stimulated emission depletion(STED)microscopes

</br>

回折限界を超えた結像.原子レベルのものも観察可能.

## 結果


## 結論