## MYPKG
このリポジトリは未来ロボティクス学科のロボットシステム学の授業の課題で作ったものをあげるためのものです
* ![test](https://github.com/Joffan/mypkg/actions/workflows/test.yml/badge.svg)
* ![test](https://img.shields.io/badge/ros2-humble-blue)
* ![test](https://img.shields.io/badge/python-v3.10-blue)

## 概要
* Countup is a package for ROS2 to publish and subscribe with a 16bit signed integer messages on two nodes
* Countupは、ROS2が2つのノードで16ビットの署名付き整数メッセージをパブリッシュおよびサブスクライブするためのパッケージです

## インストール方法
* ros2をダウンロードした環境で以下のコマンドを実行

``
$ git clone https://github.com/Joffan/mypkg.git
``
 
## Talker とListener 説明
* Talker sends messages with type Int16 through Countup.
 * 和訳
    * Talkerは、タイプInt16の完全カウントアップでメッセージを送信します。
　　
* Listener receives messages of type Int16 from Countup and outputs them.
 * 和訳
    * リスナーは、CountupからタイプInt16のメッセージを受信し、出力します。

## トピック
* talker and listner graph to understand the relation.
<img width="373" alt="画像1" src="https://user-images.githubusercontent.com/115678367/211147023-e18966d8-9739-447a-9a6b-f9b1413182dc.png">
## ビルドやり方
1)
```
colcon build
```
2)
```
source ~/.bashrc
```
## 必要ソフトウエア
  * Ubuntu 22.04
  * ROS2 humble 
  * Python 3.10

## 実行方法　(listener とtalker)
* 端末1(Send messages every 0.5 seconds.Messages increase by 1 in natural numbers)
```
$ ros2 run mypkg listener
```
* 端末2.1 (Receive and display messages from talker . If talker is not running, nothing is displayed)
```
$ ros2 run mypkg talker 
``` 
* Launch(Talker and listener can run simultaneously.)
```
ros2 launch mypkg talk_listen.launch.py
```

## Result (Listener and Talker )/ 結果
* Listener
```
$ ros2 run mypkg listener
[INFO] [1671701267.171804400] [listener]: Listen: 0
[INFO] [1671701267.672352000] [listener]: Listen: 1
[INFO] [1671701268.172334200] [listener]: Listen: 2
[INFO] [1671701268.672022600] [listener]: Listen: 3
[INFO] [1671701269.172308500] [listener]: Listen: 4
[INFO] [1671701269.672704900] [listener]: Listen: 5
[INFO] [1671701270.172425900] [listener]: Listen: 6
[INFO] [1671701270.672327900] [listener]: Listen: 7
....
```
* Talker  
```
$ ros2 launch mypkg talk_listen.launch.py
[listener-2] [INFO] [1671768364.680333300] [listener]: Listen: 0
[listener-2] [INFO] [1671768365.140367600] [listener]: Listen: 1
[listener-2] [INFO] [1671768365.640273900] [listener]: Listen: 2
[listener-2] [INFO] [1671768366.140561700] [listener]: Listen: 3
[listener-2] [INFO] [1671768366.640282900] [listener]: Listen: 4
[listener-2] [INFO] [1671768367.140304000] [listener]: Listen: 5
[listener-2] [INFO] [1671768367.640747100] [listener]: Listen: 6
....
```

##  テスト 環境
* Ubuntu 22.04 LTS
* ROS2 foxy
## LICENSE/権利表示
 * このソフトウェアパッケージは、3条項BSDライセンスの下、再配布および許可が許可されています。
 * このパッケージのコードは，下記のスライド（CC-BY-SA 4.0 by Ryuichi Ueda）のものを，本人の許可を得て自身の著作としたも    のです.
 * [ryuichiueda/my_slides robosys_2022](https://github.com/ryuichiueda/my_slides/tree/master/robosys_2022)
 * ©2022 Joffan Matthews Tanubrata 

