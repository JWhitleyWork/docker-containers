FROM ubuntu:focal

# setup timezone
RUN echo 'Etc/UTC' > /etc/timezone && \
    ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime && \
    apt-get update && \
    apt-get install -q -y --no-install-recommends tzdata && \
    rm -rf /var/lib/apt/lists/*

# install packages
RUN apt-get update && apt-get install -q -y --no-install-recommends \
    dirmngr \
    gnupg2 \
    && rm -rf /var/lib/apt/lists/*

# setup ros2 keys
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654

# setup sources.list
RUN echo "deb http://packages.ros.org/ros2-testing/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list

# setup environment
ENV ROS_DISTRO foxy
ENV LANG C.UTF-8
ENV LC_ALL C.UTF-8

RUN apt-get update && apt-get install -q -y --no-install-recommends \
    ros-foxy-ament-cmake \
    ros-foxy-ament-cmake-auto \
    ros-foxy-ament-cmake-gmock \
    ros-foxy-ament-cmake-gtest \
    ros-foxy-ament-cmake-pytest \
    ros-foxy-ament-cmake-ros \
    ros-foxy-ament-index-cpp \
    ros-foxy-ament-index-python \
    ros-foxy-ament-lint-auto \
    ros-foxy-ament-lint-common \
    ros-foxy-class-loader \
    ros-foxy-common-interfaces \
    ros-foxy-pluginlib \
    ros-foxy-rcl-lifecycle \
    ros-foxy-rclcpp \
    ros-foxy-rclcpp-lifecycle \
    ros-foxy-rclpy \
    ros-foxy-ros-environment \
    ros-foxy-ros-workspace \
    ros-foxy-ros2action \
    ros-foxy-ros2component \
    ros-foxy-ros2interface \
    ros-foxy-ros2launch \
    ros-foxy-ros2lifecycle \
    ros-foxy-ros2multicast \
    ros-foxy-ros2node \
    ros-foxy-ros2param \
    ros-foxy-ros2pkg \
    ros-foxy-ros2run \
    ros-foxy-ros2service \
    ros-foxy-ros2topic \
    ros-foxy-rosidl-default-generators \
    ros-foxy-rosidl-default-runtime \
    ros-foxy-sros2 \
    ros-foxy-sros2-cmake \
    && rm -rf /var/lib/apt/lists/*

# setup entrypoint
COPY ./ros_entrypoint.sh /

ENTRYPOINT ["/ros_entrypoint.sh"]
CMD ["bash"]
