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

~~~
$ cd ~/ros2_ws/
$ colcon build
$ source ~/ros2_ws/install/setup.bash
$ source ~/ros2_ws/install/local_setup.bash
$ source ~/.bashrc
$ ros2 run mypkg talker
~~~
もう一つの端末で
~~~
$ ros2 run mypkg listener
~~~
と入力して下記のように表示される。

~~~
[listener-2] [INFO] [1672379361.260214520] [listener]: Listen: 0
[listener-2] [INFO] [1672379361.744006958] [listener]: Listen: 1
[listener-2] [INFO] [1672379362.244047634] [listener]: Listen: 2
[listener-2] [INFO] [1672379362.743929742] [listener]: Listen: 3
[listener-2] [INFO] [1672379363.242907580] [listener]: Listen: 4
[listener-2] [INFO] [1672379363.743900063] [listener]: Listen: 5
~~~


## 動作確認
* ros2
* ubuntu-22.04

## ライセンス
* このソフトウェアパッケージは，3条項BSDライセンスの下，再頒布および使用が許可されます．
* © 2022 Koji Miyauchi
## 謝辞
* このソフトウェアパッケージは上田隆一氏の指導を受け制作しました。
