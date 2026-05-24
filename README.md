# Unitree Robotics

Unitree Robotics is a Hangzhou, China-based high-performance robot manufacturer founded in 2016 by Wang Xingxing. It is a global pioneer in the commercial quadruped (robot dog) market and has expanded into bipedal humanoid robots. Its product line spans the Go1/Go2/Go2-W consumer and research quadrupeds, the industrial B1/B2 quadrupeds, the H1/G1/R1 humanoids, the Z1 six-DOF robotic arm, in-house L1/L2 LiDAR sensors, and the Dex1-1 dexterous hand.

## Developer Surface

Unitree does **not** publish a public REST, GraphQL, or gRPC cloud API. The developer surface is SDK-centric — applications communicate with robots locally over DDS (Data Distribution Service). The company maintains an active GitHub presence at [github.com/unitreerobotics](https://github.com/unitreerobotics) with 46+ public repositories spanning SDKs, ROS/ROS2 bindings, simulation environments, RL training stacks, teleoperation pipelines, and a vision-language-action model.

Developer documentation lives at [support.unitree.com/home/en/developer](https://support.unitree.com/home/en/developer).

## Profile Classification

- **Type**: company
- **Tier**: 2 (SDK-only developer surface — no hosted API)
- **Position**: Provider
- **Access**: 3rd-Party

## Key SDKs

| Repo | Purpose | Stars | License |
|---|---|---|---|
| [unitree_sdk2](https://github.com/unitreerobotics/unitree_sdk2) | C++ SDK for current-generation robots (DDS) | 1.1k | BSD-3-Clause |
| [unitree_sdk2_python](https://github.com/unitreerobotics/unitree_sdk2_python) | Python bindings for unitree_sdk2 | 698 | BSD-3-Clause |
| [unitree_legged_sdk](https://github.com/unitreerobotics/unitree_legged_sdk) | Legacy SDK for Go1/B1/A1/AlienGo | 418 | BSD-3-Clause |
| [unitree_ros](https://github.com/unitreerobotics/unitree_ros) | ROS1 messages and packages | 1.4k | BSD-3-Clause |
| [unitree_ros2](https://github.com/unitreerobotics/unitree_ros2) | ROS2 messages and packages | 706 | BSD-3-Clause |
| [z1_sdk](https://github.com/unitreerobotics/z1_sdk) | SDK for Z1 robotic arm | 44 | BSD-3-Clause |
| [unilidar_sdk2](https://github.com/unitreerobotics/unilidar_sdk2) | SDK for L2 LiDAR | 86 | BSD-3-Clause |
| [unitree_actuator_sdk](https://github.com/unitreerobotics/unitree_actuator_sdk) | SDK for Unitree actuators | 124 | BSD-3-Clause |
| [UnitreecameraSDK](https://github.com/unitreerobotics/UnitreecameraSDK) | Go1 camera SDK | 115 | MPL-2.0 |
| [unitree_dds_wrapper](https://github.com/unitreerobotics/unitree_dds_wrapper) | DDS communication wrapper | 32 | BSD-3-Clause |

## Simulation, RL, and Learning

- [unitree_mujoco](https://github.com/unitreerobotics/unitree_mujoco) — MuJoCo simulation environment (985 stars)
- [unitree_sim_isaaclab](https://github.com/unitreerobotics/unitree_sim_isaaclab) — Isaac Lab simulation environment
- [unitree_pybullet](https://github.com/unitreerobotics/unitree_pybullet) — PyBullet environment
- [unitree_rl_gym](https://github.com/unitreerobotics/unitree_rl_gym) — RL training environment (3.3k stars)
- [unitree_rl_lab](https://github.com/unitreerobotics/unitree_rl_lab) — Isaac Lab-based RL
- [unitree_rl_mjlab](https://github.com/unitreerobotics/unitree_rl_mjlab) — MuJoCo-based RL
- [unitree_lerobot](https://github.com/unitreerobotics/unitree_lerobot) — LeRobot fork for G1 dual-arm imitation learning
- [unifolm-vla](https://github.com/unitreerobotics/unifolm-vla) — Vision-Language-Action model
- [unifolm-world-model-action](https://github.com/unitreerobotics/unifolm-world-model-action) — World model

## Teleoperation

- [xr_teleoperate](https://github.com/unitreerobotics/xr_teleoperate) — XR teleop for humanoids (1.5k stars)
- [kinect_teleoperate](https://github.com/unitreerobotics/kinect_teleoperate) — Azure Kinect-based teleop for H1/G1
- [televuer](https://github.com/unitreerobotics/televuer) — XR vision and hand/controller interface
- [teleimager](https://github.com/unitreerobotics/teleimager) — Multi-camera streaming server

## On-Robot Apps

- [unitree-app-templates](https://github.com/unitreerobotics/unitree-app-templates) — App templates for the Unitree App Store

## Why No Generated Artifacts

`openapi/`, `asyncapi/`, `json-schema/`, `capabilities/`, `plans/`, `rate-limits/`, and `finops/` directories are intentionally absent. Generating empty or placeholder specs would violate the pipeline contract — Unitree has no HTTP/gRPC API surface to describe. The DDS message catalog under `unitree_ros2` is the closest analogue to an interface contract; if Unitree ever ships a cloud control plane (e.g., for fleet management or the Unitree App Store), this profile can be upgraded to Tier 1 with proper artifacts.

## Source

This profile was generated from public sources:
- [unitree.com](https://www.unitree.com)
- [github.com/unitreerobotics](https://github.com/unitreerobotics)
- [support.unitree.com/home/en/developer](https://support.unitree.com/home/en/developer)

Part of the [API Evangelist](https://apievangelist.com) network.
