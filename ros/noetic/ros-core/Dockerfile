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
    git \
    && rm -rf /var/lib/apt/lists/*

# setup keys
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654

# setup sources.list
RUN echo "deb http://repositories.ros.org/ubuntu/testing focal main" > /etc/apt/sources.list.d/ros1-latest.list

# setup environment
ENV LANG C.UTF-8
ENV LC_ALL C.UTF-8

ENV ROS_DISTRO noetic

RUN apt-get update && apt-get install -q -y --no-install-recommends \
    ros-noetic-catkin \
    ros-noetic-class-loader \
    ros-noetic-cmake-modules \
    ros-noetic-common-msgs \
    ros-noetic-gencpp \
    ros-noetic-geneus \
    ros-noetic-genlisp \
    ros-noetic-genmsg \
    ros-noetic-gennodejs \
    ros-noetic-genpy \
    ros-noetic-message-generation \
    ros-noetic-message-runtime \
    ros-noetic-pluginlib \
    ros-noetic-ros \
    ros-noetic-ros-comm \
    ros-noetic-rosbag-migration-rule \
    ros-noetic-rosconsole \
    ros-noetic-rosconsole-bridge \
    ros-noetic-roscpp-core \
    ros-noetic-rosgraph-msgs \
    ros-noetic-roslisp \
    ros-noetic-rospack \
    ros-noetic-std-msgs \
    ros-noetic-std-srvs \
    && rm -rf /var/lib/apt/lists/*

# setup entrypoint
COPY ./ros_entrypoint.sh /

ENTRYPOINT ["/ros_entrypoint.sh"]
CMD ["bash"]
