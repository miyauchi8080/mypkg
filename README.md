# mypkg
## 説明
* ROS2のパッケージ

talker、listenerというノードが含まれたパッケージ。

## 機能

### talker

パブリッシャを持つノード

数字をカウントしてトピック/countupに流す。

メッセージ:16bit符号付き整数

### listener

サブスクライバを持つノード

トピック/countupからのメッセージを表示
## 使用法
### パッケージのビルド
~~~
$ cd ~/ros2_ws/
$ colcon build
$ source ~/ros2_ws/install/setup.bash
$ source ~/ros2_ws/install/local_setup.bash
$ source ~/.bashrc
~~~
### 動作

* ２つの端末にそれぞれ
~~~
$ ros2 run mypkg talker
~~~
~~~
$ ros2 run mypkg listener
~~~
と入力することでlistener側に
~~~
[INFO] [1672380949.514107954] [listener]: Listen: 0
[INFO] [1672380950.006545193] [listener]: Listen: 1
[INFO] [1672380950.506559977] [listener]: Listen: 2
[INFO] [1672380951.005573418] [listener]: Listen: 3
[INFO] [1672380951.506397551] [listener]: Listen: 4
~~~
と表示される。
ctrl+cで終了。
## 動作確認
* ros2
* ubuntu-22.04

## ライセンス
* このソフトウェアパッケージは，3条項BSDライセンスの下，再頒布および使用が許可されます．
* © 2022 Koji Miyauchi
## 謝辞
* このソフトウェアパッケージは上田隆一氏の指導を受け制作しました。
