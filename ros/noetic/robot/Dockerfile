FROM jwhitleywork/ros:noetic-ros-base-focal

RUN apt-get update && apt-get install -y --no-install-recommends \
    ros-noetic-control-msgs \
    ros-noetic-diagnostics \
    ros-noetic-executive-smach \
    ros-noetic-filters \
    ros-noetic-geometry \
    ros-noetic-joint-state-publisher \
    ros-noetic-kdl-parser \
    ros-noetic-kdl-parser-py \
    ros-noetic-robot-state-publisher \
    ros-noetic-urdf \
    ros-noetic-urdf-parser-plugin \
    ros-noetic-xacro \
    && rm -rf /var/lib/apt/lists/*
