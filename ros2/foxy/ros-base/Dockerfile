FROM jwhitleywork/ros:foxy-ros-core-focal

# install bootstrap tools
RUN apt-get update && apt-get install --no-install-recommends -y \
    build-essential \
    git \
    python3-colcon-common-extensions \
    python3-colcon-mixin \
    python3-rosdep \
    python3-vcstool \
    && rm -rf /var/lib/apt/lists/*

# bootstrap rosdep
RUN rosdep init && \
  rosdep update --rosdistro $ROS_DISTRO

# setup colcon mixin and metadata
RUN colcon mixin add default \
      https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml && \
    colcon mixin update && \
    colcon metadata add default \
      https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml && \
    colcon metadata update

# install ros packages
RUN apt-get update && apt-get install -y --no-install-recommends \
    ros-foxy-geometry2 \
    ros-foxy-kdl-parser \
    ros-foxy-robot-state-publisher \
    ros-foxy-urdf \
    ros-foxy-ros-workspace \
    && rm -rf /var/lib/apt/lists/*
