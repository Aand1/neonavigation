----
# planner_cspace package

## planner_3d

planner_3d node provides 2-D/3-DOF seamless global-local path and motion planner.

### Sources

* src/planner_3d.cpp
* src/grid_astar.hpp

### Subscribed topics

* ~/costmap (costmap_cspace::CSpace3D)
* ~/costmap_update (costmap_cspace::CSpace3DUpdate)
* ~/goal (geometry_msgs::PoseStamped)
* /tf

### Published topics

* ~/path (nav_msgs::Path)
* ~/debug (sensor_msgs::PointCloud)
* ~/path_start (geometry_msgs::PoseStamped)
* ~/path_end (geometry_msgs::PoseStamped)
* ~/status (planner_cspace::PlannerStatus)

### Services


### Called services


### Parameters

* "goal_tolerance_lin" (double, default: 0.05)
* "goal_tolerance_ang" (double, default: 0.1)
* "goal_tolerance_ang_finish" (double, default: 0.05)
* "unknown_cost" (int, default: 100)
* "hist_cnt_max" (int, default: 20)
* "hist_cnt_thres" (int, default: 19)
* "hist_cost" (int, default: 90)
* "hist_ignore_range" (double, default: 1.0)
* "remember_updates" (bool, default: false)
* "local_range" (double, default: 2.5)
* "longcut_range" (double, default: 0.0)
* "esc_range" (double, default: 0.25)
* "find_best" (bool, default: true)
* "pos_jump" (double, default: 1.0)
* "yaw_jump" (double, default: 1.5)
* "force_goal_orientation" (bool, default: true)
* "temporary_escape" (bool, default: true)
* "fast_map_update" (bool, default: false)
* "debug_mode" (string, default: std::string("cost_estim"))
* "queue_size_limit" (int, default: 0)

----

## planner_2dof_serial_joints

planner_2dof_serial_joints provides collision avoidance for 2-DOF serial joint (e.g. controlling interfering pairs of sub-tracks for tracked vehicle.)

### Sources

* src/planner_2dof_serial_joints.cpp
* src/grid_astar.hpp

### Subscribed topics

* ~/trajectory_in (trajectory_msgs::JointTrajectory)
* ~/joint (sensor_msgs::JointState)
* /tf

### Published topics

* ~/trajectory_out (trajectory_msgs::JointTrajectory)
* ~/status (planner_cspace::PlannerStatus)

### Services


### Called services


### Parameters

* "resolution" (int, default: 128)
* "debug_aa" (bool, default: false)
* "replan_interval" (double, default: 0.2)
* "queue_size_limit" (int, default: 0)
* "link0_name" (string, default: std::string("link0"))
* "link1_name" (string, default: std::string("link1"))
* "point_vel_mode" (string, default: std::string("prev"))
* "range" (int, default: 8)
* "num_groups" (int, default: 1)

----

