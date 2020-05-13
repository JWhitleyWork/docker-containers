FROM jwhitleywork/ros:noetic-ros-base-focal

RUN apt-get update && apt-get install -y --no-install-recommends \
    ros-noetic-image-common \
    ros-noetic-image-pipeline \
    ros-noetic-image-transport-plugins \
    ros-noetic-laser-pipeline \
    ros-noetic-pcl-conversions \
    ros-noetic-pcl-msgs \
    ros-noetic-pcl-ros \
    ros-noetic-vision-opencv \
    && rm -rf /var/lib/apt/lists/*
