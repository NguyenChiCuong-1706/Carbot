Build worksapce steps:
1. **Create workspace**:
   - mkdir carbot_ws && cd carbot_ws
   - mkdir src && cd src
   - git clone https://github.com/NguyenChiCuong-1706/Carbot
2. **Build workspace**:
   - colcon build --symlink -install (file code moi phai build lai de chay)
   - source install/setup.bash
     
3. **Run workspace**: 
   - cd carbot_ws
   - source install/setup.bash
  
4. **Launch/Node commands**: (ros2 launch <package name> <launch file>)
   
**Launch robot**: (Robot_state_publisher + ros2_control)
  - ros2 launch carbot launch_realrobot.launch.py

**Run teleop node**: 
  - ros2 run teleop_twist_keyboard teleop_twist_keyboard --ros-args -r /cmd_vel:=/diff_cont/cmd_vel_unstamped
