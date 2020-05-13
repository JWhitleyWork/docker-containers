FROM jwhitleywork/ros:noetic-robot-focal

# install ros packages
RUN apt-get update && apt-get install -y --no-install-recommends \
    ros-melodic-angles \
    ros-melodic-common-tutorials \
    ros-melodic-geometry-tutorials \
    ros-melodic-ros-tutorials \
    ros-melodic-roslint \
    ros-melodic-urdf-tutorial \
    ros-melodic-visualization-tutorials \
    ros-melodic-viz \
    && rm -rf /var/lib/apt/lists/*
