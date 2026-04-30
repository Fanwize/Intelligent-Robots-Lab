# LAB6：实验报告

---

## 1. 实验

在 Gazebo 中加载自定义差速小车模型，为其配置**相机**与**二维激光雷达**仿真插件，在 RViz 中同时显示机器人模型、激光扫描与相机图像

---

## 2. 工程结构

| 包名 | 作用 |
|------|------|
| `my_robot_description` | 存放 `urdf/my_robot.xacro`：底盘、轮系、`base_footprint`、相机与激光 link 及 Gazebo 插件 |
| `my_robot_gazebo` | 存放 `launch/gazebo_sim.launch`：空世界、加载 xacro、`spawn_model`、`robot_state_publisher` 等 |

（launch 通过 `$(find my_robot_description)` 引用模型）

---


## 3. 运行结果

- Gazebo 中机器人成功生成
- RViz 中可同时显示 **RobotModel**、**LaserScan**（红色扫描点/线）与 **Image**（相机画面）
