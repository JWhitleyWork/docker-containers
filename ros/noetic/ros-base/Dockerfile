FROM jwhitleywork:noetic-ros-core-focal

# install bootstrap tools
RUN apt-get update && apt-get install --no-install-recommends -y \
    build-essential \
    python-rosdep \
    python-rosinstall \
    python-vcstools \
    && rm -rf /var/lib/apt/lists/*

# bootstrap rosdep
RUN rosdep init && \
  rosdep update --rosdistro $ROS_DISTRO

# install ros packages
RUN apt-get update && apt-get install -y --no-install-recommends \
    ros-noetic-actionlib \
		ros-noetic-bond-core \
		ros-noetic-dynamic-reconfigure \
		ros-noetic-nodelet-core \
    && rm -rf /var/lib/apt/lists/*
