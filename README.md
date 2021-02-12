# 2020 ロボットシステム学 課題２

提出版になります．宜しくお願い致します．

# 事前準備

 * ubuntuのセットアップは以下を参考にした．
 * https://ryuichiueda.github.io/robosys2020/lesson1_introduction.html
 
 * [ros_setup_scripts_Ubuntu20.04](http://github.com/ryuichiueda/ros_setup_scripts_Ubuntu20.04_server)
# 動作環境  
・Raspberry Pi 2 Model B    
・Ubuntu 20.04.1 LTS  
・ROS Noetic
_ _ _
# インストール方法
**・ROS**    
[ros_setup_scripts_Ubuntu20.04](http://github.com/ryuichiueda/ros_setup_scripts_Ubuntu20.04_server)をもとにROSの環境構築をします。  

**・ワークスペース**     
[ロボットシステム学第１０回](https://ryuichiueda.github.io/robosys2020/lesson10_ros.html#/)をもとにワークスペースを作成します。  

**・パッケージ**  
以下のコマンドを実行して、パッケージをクローンします。   
`$ cd ~/catkin_ws/src`  
`$ cd clone https://github.com/FujitaRyo/mypkg`  
catkin_makeを使用して、本パッケージをビルドします。  
`$ cd ~/catkin_ws`  
`$ catkin_make`  
`$ source ~/.bashrc`  
_ _ _
# 実行方法  
端末１  
`$ roscore`  

端末２   
`$ chmod +x count.py` 、`$ chmod +x twice.py`  
`$ rosrun mypkg count.py` 、`rosrun mypkg twice.py`  

端末３  
`$ rosnode list`と`$ rostopic list`でノードとトピックを確認します。  
`$ rostopic echo /count_up` 、`$ rostopic echo /twice`でデータを取り出します。　
_ _ _
# デモ動画  
・count.py  
https://www.youtube.com/watch?v=di_exuS_x94  
・twice.py  
https://www.youtube.com/watch?v=CDDHCLWzFu8  
_ _ _
# 参考著者  
[Ryuichi Ueda](https://github.com/ryuichiueda)
_ _ _
# ライセンス
BSD 3-Clause License

