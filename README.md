# robomas_driver

ros2 run robomas_driver robomaster_ros2_ctrl

0 : 電流制御モード　1 : 速度制御モード　2: 位置制御モード

ros2 topic pub -1 /rm_cmd_array robomas_driver/MotorCmdArray "
cmds:
- {id: 1, type: 'M3508', mode: 1, value: 2400.0}     # 位置 2.0 rev
- {id: 2, type: 'M3508', mode: 1, value: 1200.0}  # 速度 1200 rpm
- {id: 3, type: 'M3508', mode: 1, value: 500.0}     # 電流 1.5 A
- {id: 6, type: 'M2006', mode: 1, value: 100.0}
- {id: 8, type: 'M2006', mode: 1, value: 200.0}
"


ros2 topic pub -1 /rm_cmd_array robomas_driver/MotorCmdArray "
cmds:
- {id: 1, type: 'M3508', mode: 1, value: 100.0}     # 位置 2.0 rev
"