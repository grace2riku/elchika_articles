# Spresenseモーラーについて
Spresenseがモーターを駆動し、モーラーをランダムに動かします。

猫を楽しませるためのロボットです。次の図がSpresenseモーラーの全体写真です。


# 部品
Spresenseモーラーの使用部材です。
SpresenseモーラーはつぎのGitHubのローバー**SprTurtleBot**をベースに製作しました。

バガスどんぶり + モーラーを取り付ける駆動部はSprTurtleBotのハードウェアをそのまま流用しています。

https://github.com/TE-YoshinoriOota/Spresense-microROS-Seminar/blob/main/Documents/Spresense%20%E3%81%A8micro-ROS%20%E3%81%A7%E3%81%AF%E3%81%98%E3%82%81%E3%82%8B%E3%83%AD%E3%83%9C%E3%83%83%E3%83%88%E3%83%97%E3%83%AD%E3%82%B0%E3%83%A9%E3%83%9F%E3%83%B3%E3%82%B0.pdf


| No | 部品 | 個数 | 役割 | 備考 |
| :--- | :--- | :--- | :--- | :--- |
| 1 | Spresense メインボード | 1 | モーラーのコントローラ | SPRESENSEメインボード[CXD5602PWBMAIN1](https://www.switch-science.com/products/3900) |
| 2 | Spresense 拡張ボード | 1 | IOボード | SPRESENSE拡張ボード[CXD5602PWBEXT1](https://www.switch-science.com/products/3901) |
| 3 | 台座+モーター+タイヤキット | 1 | 基本シャーシ | [2WDロボットスマートカーシャーシ 2輪駆動 DIY教材](https://www.amazon.co.jp/gp/product/B01IWHE9VI/ref=ppx_yo_dt_b_asin_title_o02_s00?ie=UTF8&psc=1) |
| 4 | エンコーダー | 2 | タイヤの回転数をカウント | [IR赤外線スロット付きオプトカプラーモーター速度検出](https://www.amazon.co.jp/gp/product/B084VP1GXS/ref=ppx_yo_dt_b_asin_title_o03_s00?ie=UTF8&psc=1) |
| 5 | モータードライバ | 1 | モーター駆動用回路 | [DRV8835使用ステッピング&DCモータドライバモジュール](https://akizukidenshi.com/catalog/g/g109848/) |
| 6 | ブレッドボード | 1 | 配線の中継 |  |
| 7 | ワイヤー | 多数 |  |  |
| 8 | モバイルバッテリー | 1 |  |  |
| 9 | Micro USB(USB A-MicroB)ケーブル | 1 | モバイルバッテリーからSpresenseに給電するために必要 |  |
| 10 | モーラー | 1 | 猫の興味を引く | [オリジナル　モーラー　パープル](https://item.rakuten.co.jp/auc-ookawaya/4979092016953/?s-id=pc_shop_recommend&rtg=c1e67285c7003768080607e3d6635f69) |
| 11 | バガスどんぶり | 1 | モーラーの取り付けと配線を隠す | [電子レンジに使えるバガスどんぶり](https://jp.daisonet.com/products/4550480309866) |
| 12 | つまようじ | 1 | モーラーのテグスを巻き、どんぶりに固定する |  |
| 13 | ネジ | 2 | ネジ・ワッシャー・ナットで台座とエンコーダーを固定する |  |
| 14 | ワッシャー | 2 |  |  |
| 15 | ナット | 2 |  |  |


# 設計図
Spresenseモーラーは前述したとおり**SprTurtleBot**をベースにしています。
必要な設計図はつぎのGitHub資料に記載されていたので流用します。

[Spresense とmicro-ROS ではじめるロボットプログラミング.pdf](https://github.com/TE-YoshinoriOota/Spresense-microROS-Seminar/blob/main/Documents/Spresense%20%E3%81%A8micro-ROS%20%E3%81%A7%E3%81%AF%E3%81%98%E3%82%81%E3%82%8B%E3%83%AD%E3%83%9C%E3%83%83%E3%83%88%E3%83%97%E3%83%AD%E3%82%B0%E3%83%A9%E3%83%9F%E3%83%B3%E3%82%B0.pdf)

# 組み立て
## エンコーダーの取り付け
エンコーダーの取り付けはNo. 13, 14, 15のネジ、ワッシャー、ナットで行います。

このネジ・ワッシャー・ナットは部品表No.3の台座+モーター+タイヤキット、No.4のエンコーダーに付属していません。個別に購入または調達する必要があります。

下図は台座表面の写真です。エンコーダーの片側だけネジを挿入しています。もう一方はモーターとぶつかり固定できません。そのためエンコーダーの固定は2箇所のうち1つとします。

下図は台座裏面の写真です。ワッシャー、ナットで固定しています。

## どんぶりとモーラーの取り付け
モーラーはどんぶりに取り付けます。モーラーを取り付けたどんぶりは配線を隠すように被せます。
モーラーとどんぶりを取り付けは下図になります。

モーラーとどんぶりの取り付け手順はつぎのとおりです。

どんぶりにはキリなどで穴を開けます。
モーラーは透明なテグスがついています。
どんぶりに開けた穴にテグスをとおします。
テグスを適度な長さにしたら、半分におった爪楊枝にテグスを巻き付けます。
テグスを巻き付けた爪楊枝とどんぶりをテープなどで固定します。
モーラーを取り付けたどんぶりで配線を隠して組み立て完成です。

# 配線
## 配線図
下図は[Spresense とmicro-ROS ではじめるロボットプログラミング.pdf](https://github.com/TE-YoshinoriOota/Spresense-microROS-Seminar/blob/main/Documents/Spresense%20%E3%81%A8micro-ROS%20%E3%81%A7%E3%81%AF%E3%81%98%E3%82%81%E3%82%8B%E3%83%AD%E3%83%9C%E3%83%83%E3%83%88%E3%83%97%E3%83%AD%E3%82%B0%E3%83%A9%E3%83%9F%E3%83%B3%E3%82%B0.pdf)のp56からの引用した配線図です。このとおりに配線していきます。

### 配線図とモーラー実体との対応
モーラーはSpresenseメインボードと拡張ボードの**SONY**のシルクの向きを配線図と合わせます。向きを合わせたら配線図のとおりに配線してきます。

### モーター（AOUT2, BOUT2）の配線について
モーター（AOUT2, BOUT2）の配線は下図のようにモータ上側の端子（ケースに近い方）と接続します（赤の配線がAOUT2, BOUT2）。

### 電源の配線について
配線図では電源は基板で分配されています。今回は電源分配用基板を使わず、ブレッドボードで電源ラインを分配します。


# ソースコード
ソースコードはつぎのGitHubリポジトリに格納しています。

* https://github.com/grace2riku/cat_moeller_spresense


## ライセンス
### LGPL-2.1 license
つぎのファイルは **【LGPL-2.1 license】** です。

* CatMoeller/Main_Rover_PID_Adjustment/Main_Rover_PID_Adjustment.ino
* CatMoeller/Main_Rover_PID_Adjustment/pwm_control.ino

ベースにしたつぎのリポジトリのライセンスと同様です。

* https://github.com/TE-YoshinoriOota/Spresense-microROS-Seminar/tree/main/Sketches/SprTurtleBot_PID_Adjustment/Main_Rover_PID_Adjustment

### MIT license
上記以外のソースコードは **【MIT license】** です。

## ソースコードの配置
Spresenseモーラーのメインの責務はつぎの2つです。

* モーター駆動をおこなうソースコード
* モーター駆動パラメータを生成するソースコード

モーター駆動パラメータはつぎになります。
* 移動スピード（0〜1.0(m/s) ）
* 移動方向（前進・後進・右回り・左回り）


開発環境はArduino IDEです。

ソースコードはつぎの配置になっています。


### モーター駆動
モータ駆動のソースコードはつぎになります。

* CatMoeller/Main_Rover_PID_Adjustment
  * Main_Rover_PID_Adjustment.ino
  * pwm_control.ino

モータ駆動のコードはメインコアに配置します。


### モーター駆動のパラメータ生成
モーター駆動のパラメータ生成のソースコードはつぎになります。

* RandomParameterCreater/cat_moeller_spresense
  * src/ntshell
  * RandomParameterCreater.cpp
  * RandomParameterCreater.h
  * cat_moeller_spresense.ino
  * usrcmd_cat_moeller_spresense.cpp

モーター駆動のパラメータ生成はサブコア1に配置します。


## モーター駆動（メインコアに配置）のソースコードの説明


## モーター駆動のパラメータ生成（サブコア1に配置）のソースコードの説明
