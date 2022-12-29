## MYPKG
このリポジトリは未来ロボティクス学科のロボットシステム学の授業の課題で作ったものをあげるためのものです
* ![test](https://github.com/Joffan/mypkg/actions/workflows/test.yml/badge.svg)
* ![test](https://img.shields.io/badge/ros2-humble-blue)
* ![test](https://img.shields.io/badge/python-v3.10-blue)

##　概要
* countupという名のトピックを介して16bitの符号つき整数型のメッセージをtalker.py,listener.pyという名の２つのノードでパブリッシュ並びにサブスクライブするros2用のパッケージ

## ビルド
```
colcon build
```
```
source ~/.bashrc
```
## 必要ソフトウエア
  * Ubuntu 22.04
  * ROS2 humble 
  * Python 3.10

## 実行方法　(listener とtalker)
```
$ ros2 run mypkg listener
```
```
$ ros2 run mypkg talker 
```
* 別の方法として、このやり方は一つのターミナルで同時に実行ことができます。
```
ros2 launch mypkg talk_listen.launch.py
```

## Result (Listener and Talker )/ 結果
* listener
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
* Ubuntu 22.04

## LICENSE
 * このソフトウェアパッケージは、３条項BSDライセンスの下、再配布および許可が許可されています。
 * LICENSE
 * このパッケージのコードは千葉工業大学の上田　隆一先生スライドの許可を得て自身の著作としています。
 * 2022 Joffan Matthews Tanubrata

