# 2020 ロボットシステム学 課題２

提出版になります．宜しくお願い致します．
成果物は[上田先生](https://github.com/ryuichiueda)の作成したパッケージを自分で動かせるかどうかの確認．

# 事前準備

 * ubuntuのセットアップは以下を参考にした．
 * https://ryuichiueda.github.io/robosys2020/lesson1_introduction.html
 
 * ROSのインストール方法および環境構築は以下を参考にした．
 * [ros_setup_scripts_Ubuntu20.04](http://github.com/ryuichiueda/ros_setup_scripts_Ubuntu20.04_server)
 * [ロボットシステム学第１０回](https://ryuichiueda.github.io/robosys2020/lesson10_ros.html#/)
 
# 動作環境  
・Raspberry Pi 2 Model B    
・Ubuntu 20.04.1 LTS  
・ROS Noetic

# パッケージ

 ```
以下のコマンドを実行して、パッケージをクローンします。   

$ cd ~/catkin_ws/src
$ cd clone https://github.com/rate84/report2fin

catkin_makeを使用して、本パッケージをビルドします。  

$ cd ~/catkin_ws 
$ catkin_make
$ source ~/.bashrc
 ```

# 実行方法  

端末１  
`$ roscore`  

端末２   
`$ chmod +x count.py` 、`$ chmod +x twice.py`  
`$ rosrun report2fin count.py` 、`rosrun report2fin twice.py`  

端末３  
`$ rosnode list`と`$ rostopic list`でノードとトピックを確認。  
`$ rostopic echo /count_up` 、`$ rostopic echo /twice`でデータを取り出し。　

# 実際の動作の様子

https://youtu.be/pESZtdHxPBY

# ライセンス
[BSD 3-Clause License](https://github.com/rate84/report2fin/blob/main/LICENSE)

